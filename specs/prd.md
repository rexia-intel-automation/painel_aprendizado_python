
PRD: PySchool
Versão: 1.0.0Ambiente: Localhost (Local)

1. Visão Geral
O PySchool é uma plataforma de aprendizado de Python projetada para rodar localmente (localhost). Seu objetivo é fornecer um ambiente interativo, gamificado e estruturado onde usuários podem aprender desde os conceitos básicos até tópicos avançados de Python, acompanhando seu progresso através de trilhas de conhecimento, exercícios práticos e testes de unidade (unit tests) simulados.

2. Objetivos
Para o usuário: Aprender Python de forma estruturada, prática e no seu próprio ritmo, com feedback imediato.
Para o produto: Servir como um ambiente de estudo isolado e seguro no localhost, sem necessidade de nuvem ou contas externas.
3. Personas
Iniciante: Aluno sem experiência em programação que precisa de teoria combinada com prática guiada.
Intermediário: Desenvolvedor que já conhece o básico e quer aprofundar em tópicos específicos (ex: POO, Data Science, Web Scraping) através de desafios.
4. Requisitos Funcionais (MVP)
4.1. Autenticação e Perfil
Como a aplicação roda em localhost, o sistema deve ter um cadastro simples (usuário/senha armazenados no MySQL local).
Perfil do usuário contendo nome, nível (XP) e foto de avatar (padrão).
4.2. Trilhas de Aprendizado (Módulos)
O sistema deve ter Módulos estruturados (ex: "Básico", "Estruturas de Dados", "Orientação a Objetos").
Cada Módulo contém Lições ordenadas.
As Lições possuem conteúdo teórico (Markdown/HTML) e exemplos de código.
4.3. Exercícios e Ambiente Prático
Cada lição ou módulo deve conter Exercícios.
O exercício possui um enunciado, um código inicial (starter code) e testes ocultos (doctest ou unittest format).
Interface de editor de código integrada (Syntax highlighting).
Botão "Rodar Código" que envia o código para o backend local, executa em um ambiente seguro (sandbox subprocess) e retorna o stdout/stderr.
Botão "Validar Resposta" que roda os testes de unidade contra o código do usuário.
4.4. Gamificação e Progresso
O usuário ganha XP ao concluir lições e exercícios.
Sistema de Conquistas (Badges) por marcos atingidos (ex: "Primeiro Hello World", "Mestre das Listas").
Barra de progresso global e por módulo.
5. Requisitos Não Funcionais
Performance: O tempo de resposta para executar scripts Python locais não deve exceder 3 segundos.
Segurança: Execução de código do usuário deve ser isolada (uso de subprocess com timeout e restrições de módulos permitidos).
Stack: Backend Python (FastAPI/Flask), Frontend Web (HTML/CSS/JS ou React), Banco de dados MySQL local.
Portabilidade: Fácil de rodar via docker-compose up ou script de inicialização local.
6. Fluxo de Experiência do Usuário (UX)
Usuário acessa http://localhost:8000.
Faz login ou cria conta.
Visualiza o Dashboard com trilhas disponíveis e seu progresso.
Entra em um Módulo -> Seleciona uma Lição.
Lê a teoria, copia/modifica o código no editor embutido.
Clica em "Rodar" para testar outputs.
Clica em "Validar" para passar nos testes. Recebe XP e conclui a lição.
7. Métricas de Sucesso (Local)
Taxa de conclusão dos módulos iniciados.
Tempo médio gasto por lição.
Taxa de sucesso na primeira tentativa dos exercícios.
