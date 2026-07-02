PRD - PySchool
Product Requirements Document

1. Visão Geral
O PySchool é uma plataforma educacional focada no ensino e acompanhamento do aprendizado da linguagem Python. Projetada para rodar em ambiente local (localhost), a plataforma oferece trilhas de conhecimento interativas, exercícios práticos e um painel de progresso detalhado, permitindo que iniciantes e desenvolvedores intermediários evoluam no seu próprio ritmo.

2. Objetivos
Facilitar o aprendizado: Fornecer conteúdo estruturado e progressivo (do básico ao avançado).
Mensurar progresso: Acompanhar métricas de uso, conclusão de aulas e acertos em exercícios.
Praticidade local: Permitir execução 100% offline (após carregamento inicial) sem dependência de serviços em nuvem.
3. Público-Alvo
Estudantes de programação iniciantes.
Desenvolvedores migrando de outras linguagens para Python.
Professores ou monitores que utilizam ambientes locais para ministrar aulas.
4. Escopo do MVP (Minimum Viable Product)
Autenticação Local: Cadastro e login de usuários no banco local.
Trilhas e Módulos: Organização do conteúdo em Trilhas (ex: Fundamentos, POO, APIs) e Módulos.
Aulas Teóricas: Visualização de conteúdo em formato Markdown renderizado.
Exercícios Práticos: Desafios com enunciado, editor de código simulado e validação de resposta (gabarito).
Dashboard de Progresso: Tela inicial mostrando XP, trilhas iniciadas e next steps.
5. Requisitos Não-Funcionais
Backend: Python (FastAPI ou Flask) + SQLAlchemy.
Banco de Dados: MySQL rodando localmente.
Frontend: HTML/CSS/JS vanilla ou framework leve (Vue/React) consumindo API REST.
Segurança: Senhas com hash (bcrypt), tokens JWT para sessões.
6. Fluxos de Usuário Principais
Onboarding: Usuário cria conta -> Recebe acesso à trilha "Python Fundamentos".
Aprendizado: Usuário seleciona módulo -> Lê aula -> Marca como concluída -> Resolve exercício -> Ganha XP.
Acompanhamento: Usuário acessa Dashboard -> Visualiza gráfico de XP e % de conclusão da trilha.
7. Métricas de Sucesso (KPIs)
Taxa de conclusão de módulos.
Tempo médio gasto por aula.
Engajamento diário (retornos à plataforma).
8. Fora do Escopo (Fase 1)
Execução de código Python em tempo real no navegador (sandbox seguro).
Integração com LLMs para correção de código.
Modo multiplayer/turma.

