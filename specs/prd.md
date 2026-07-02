PRD: PySchool - Plataforma de Aprendizado de Python
1. Visão Geral
O PySchool é uma plataforma educacional focada no ensino e acompanhamento do aprendizado da linguagem Python. Projetada para rodar em localhost, a plataforma oferece uma experiência guiada, interativa e rastreável, permitindo que estudantes progridam do básico ao avançado através de trilhas estruturadas, exercícios práticos e acompanhamento de métricas de desempenho.

2. Objetivos
Primário: Fornecer um ambiente local completo para estudo de Python, sem dependência de nuvem.
Secundário: Motivar o usuário através de gamificação (XP, níveis e selos).
Técnico: Facilitar a execução de código local de forma segura e registrar o progresso em um banco de dados relacional (MySQL).
3. Público-Alvo
Iniciantes e programadores intermediários que desejam aprender Python de forma estruturada, em seu próprio ambiente de desenvolvimento.

4. Escopo da Versão 1.0 (MVP)
4.1. Funcionalidades Incluídas
Dashboard (Painel Principal): Visão geral do progresso, trilha atual, XP total e sequência de dias de estudo (streak).
Trilhas de Aprendizado: Módulos estruturados (Básico, Intermediário, Avançado, Estruturas de Dados, POO, etc.).
Lições Teóricas: Conteúdo em formato Markdown renderizado, com exemplos de código.
Ambiente de Prática (Playground): Editor de código integrado para executar scripts Python locais e visualizar a saída.
Desafios e Exercícios: Problemas com testes unitários automatizados para validar a resposta do usuário.
Sistema de Gamificação: Ganho de XP por lições concluídas e exercícios resolvidos, desbloqueio de Selos (Achievements).
Perfil e Estatísticas: Histórico de tempo de estudo, lições completadas e taxa de acerto.
4.2. Fora do Escopo (V1)
Modo multiusuário com autenticação remota (focado em usuário local/único por enquanto).
Fórum da comunidade.
Integração com IA para revisão de código (planejado para V2).
5. Fluxos de Usuário Principais
Fluxo 1: Concluir uma Lição Teórica
Usuário acessa o Dashboard e clica em "Continuar Trilha".
O sistema abre a próxima lição não concluída.
Usuário lê o material e clica em "Marcar como concluída" (ou "Próximo").
Sistema atualiza o banco de dados, concede XP e redireciona para o próximo módulo/exercício.
Fluxo 2: Resolver um Desafio de Código
Usuário acessa um exercício a partir da Trilha.
Sistema exibe o enunciado, testes esperados e o editor de código (Playground).
Usuário escreve o código e clica em "Executar & Validar".
Backend recebe o código, salva em arquivo temporário, roda os testes via CLI do Python local.
Backend captura a saída (stdout/stderr), compara com os testes e retorna o resultado (Sucesso/Falha).
Em caso de sucesso, concede XP, atualiza o progresso e emite selos se aplicável.
6. Requisitos Técnicos
Frontend: HTML, CSS (com Design System estruturado) e JavaScript (ou framework leve como Alpine.js/Vue, dependendo da preferência).
Backend: Python (FastAPI ou Flask) - Recomendado para fácil integração com o ambiente Python do usuário.
Banco de Dados: MySQL (local).
Ambiente de Execução: O backend Python do PySchool executará o código do usuário em subprocessos isolados com timeout para evitar loops infinitos (ex: subprocess.run).
7. Métricas de Sucesso (Local)
Taxa de conclusão dos módulos pelo usuário.
Tempo médio gasto na plataforma.
Número de exercícios resolvidos sem dicas.
