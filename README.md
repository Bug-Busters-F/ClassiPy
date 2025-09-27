# API - 4º Semestre ADS

# ClassiPy

Projeto API do 4° semestre de Análise e Desenvolvimento de Sistemas da equipe Bug Busters, FATEC Jessen Vidal, São José dos Campos

| Cliente | Periodo/Curso                                  | Professor M2     | Professor P2     | Contato Cliente              |
| ------- | ---------------------------------------------- | ---------------- | ---------------- | ---------------------------- |
| TecSys  | 4º ADS (Análise e Desenvolvimento de Sistemas) | Giuliano Bertoti | Juliana Pasquini | creonice@tecsysbrasil.com.br |

## 📃 Índice

<p align="center">
 | <a href ="#-desafio"> Desafio</a>  |
 <a href ="#-solução"> Solução</a>  |   
 <a href ="#-backlog-do-produto"> Backlog do Produto</a>  |
 <a href ="#️-cronograma-das-sprints"> Cronograma de Sprints</a>  |
 <a href ="#-tecnologias-utilizadas">Tecnologias</a> |
 <a href ="#-manual-de-instalação">Manual de Instalação</a>  | 
 <a href ="#-autores"> Autores</a> |
</p>

# 🎯 Desafio

O desafio consiste no desenvolvimento de um Agente de Inteligência Artificial para instrução de Processo para Registro de Importação. O processo manual de elaboração de registros aduaneiros para materiais produtivos, especialmente na indústria eletroeletrônica, é complexo e suscetível a erros. É necessário relacionar informações como Part-Number, classificação fiscal (NCM), fabricante e origem com endereço completo, gerando uma descrição detalhada do material. Qualquer ambiguidade ou erro nessas informações pode gerar dúvidas para a Receita Federal, acarretando penalidades e multas sobre a declaração do material importado.

# 🧠 Solução

ClassiPy - Classificação Inteligente de Produtos, é uma aplicação web projetada para resolver este desafio, automatizando e otimizando o processo de instrução de registro aduaneiro. A solução permite que o usuário faça o upload de um pedido de compras em formato PDF. A partir do documento, nosso agente de IA extrai todos os Part-Numbers e, para cada um, realiza uma busca inteligente para sugerir a classificação fiscal completa, incluindo descrição detalhada do produto, NCM, fabricante e mais.

---

## 📋 Backlog do Produto

| Rank | Prioridade | User Story                                                                                                                                                                                      | Sprint | Status |
| :--: | :--------: | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :----: | :----: |
|  1   |    Alta    | Como operador de cadastro, eu gostaria de carregar um PDF de documentos de importação para que o sistema identifique automaticamente os Part Numbers.                                           |   1    |   ✅   |
|  2   |    Alta    | Como operador de cadastro, eu gostaria de visualizar a lista de Part Numbers extraídos para confirmar que a leitura foi correta.                                                                |   1    |   ✅   |
|  3   |   Média    | Como operador de cadastro, eu gostaria de acessar uma interface clara e organizada para acompanhar o processo de classificação.                                                                 |   1    |   ✅   |
|  4   |    Alta    | Como operador de cadastro, eu gostaria de visualizar de forma clara as informações classificadas de cada peça (descrição, NCM, alíquota, fabricante e origem) para validar antes da exportação. |   2    |   ❌   |
|  5   |   Média    | Como operador de cadastro, eu gostaria de editar manualmente informações classificadas caso o sistema apresente dados incorretos ou incompletos.                                                |   2    |   ❌   |
|  6   |   Média    | Como analista de importação, eu gostaria de exportar as informações classificadas em planilha Excel no formato padrão da empresa, para facilitar a entrega do processo de registro.             |   2    |   ❌   |
|  7   |   Média    | Como operador de cadastro, eu gostaria de receber uma prévia dos resultados processados antes de salvar ou exportar, para evitar erros.                                                         |   2    |   ❌   |
|  8   |    Alta    | Como operador de cadastro, eu gostaria que o sistema apresente resultados cada vez mais precisos para reduzir retrabalho.                                                                       |   3    |   ❌   |
|  9   |    Alta    | Como operador de cadastro, eu gostaria de utilizar um sistema estável e sem erros críticos, para não comprometer os prazos de importação.                                                       |   3    |   ❌   |
|  10  |   Média    | Como analista de importação, eu gostaria de ter acesso a um guia de uso do sistema para operar corretamente e sem dúvidas.                                                                      |   3    |   ❌   |

---

## 📽️ Demonstração do Projeto - Sprint 1

<!-- colocar video aqui -->

---

## 🗓️ Cronograma das Sprints

| Sprint            | Previsão   | Status  | Documentação                                               |
| ----------------- | ---------- | ------- | ---------------------------------------------------------- |
| 01                | 29/09/2025 | A fazer | [Docs Sprint-1](./docs/processo/sprints/sprint1/README.md) |
| 02                | 27/10/2025 | A fazer | [Docs Sprint-2](./docs/processo/sprints/sprint2/README.md) |
| 03                | 24/11/2025 | A fazer | [Docs Sprint-3](./docs/processo/sprints/sprint3/README.md) |
| Feira de Soluções | 04/12/2025 | A fazer |                                                            |

---

## 🛣️ Roadmap das Sprints

<div style="display: flex; justify-content: center;">
  <img src="./docs/img/RoadMap-ClassiPy.png" style="width: 70%">
</div>

---

## 🧑‍💻 Tecnologias Utilizadas

<h4 align="center">
  <a href="https://react.dev/"><img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB"></a>
  <a href="https://www.typescriptlang.org/"><img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white"></a>
  <a href="https://tailwindcss.com/"><img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white"></a>
  <a href="https://vitejs.dev/"><img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white"></a>
  <a href="https://nodejs.org/"><img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white"></a>
  <a href="https://www.python.org/"><img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"></a>
  <a href="https://fastapi.tiangolo.com/"><img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white"/></a>
  <a href="https://www.postgresql.org/"><img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white"></a>
  <a href="https://www.docker.com/"><img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white"></a>
  <a href="https://ollama.com/"><img src="https://img.shields.io/badge/Ollama-000000?style=for-the-badge&logo=ollama&logoColor=white"></a>
  <a href="https://www.atlassian.com/software/jira"><img src="https://img.shields.io/badge/Jira-0052CC?style=for-the-badge&logo=jira&logoColor=white"/></a>
</h4>

---

## 📖 Manual de Instalação

### ☑️ Pré-requisitos

- Uma conta no [GitHub](https://github.com/)
- O _version control system_ [Git](https://git-scm.com/) instalado.
- Um IDE para o desenvolvimento. Recomendamos o [Visual Studio Code](https://code.visualstudio.com).
- Node.js 22+ ([Download](https://nodejs.org/en/download))
- Python v3.12+ [Python v3.12](https://www.python.org/downloads/release/python-3120/).
- O runtime [Ollama](https://ollama.com/download) para LLMs locais.
- [Postgres](https://www.postgresql.org/download/) para armazenamento.
  > **Observação:** Caso não queira instalar o Ollama e o Postgres manualmente, você pode rodá-los via **Docker**. Também é possível rodar o **backend** no Docker junto com eles, o que simplifica a configuração.  
  > **Importante para usuários Windows:** Se você optar por rodar o Postgres no Docker, o backend também precisará rodar dentro de um container Docker, para evitar problemas de conexão.

## ✅ Instalação

### 1. Clonar o Repositório Back-end

O primeiro passo é clonar o repositório do projeto para o seu ambiente local.

1. Abra um terminal.

2. Execute o seguinte comando para clonar o repositório:

   ```bash
   git clone https://github.com/Bug-Busters-F/ClassiPy-backend
   ```

3. Navegue até o diretório do projeto:

   ```bash
   cd ClassiPy-backend
   ```

4. Configure as variáveis de ambiente

   ```sh
   cp .env.template .env
   ```

5. Abra o arquivo `.env` e edite as credenciais de conexão com o ollama e o banco de dados.

   ```sh
   OLLAMA_MODEL= # Modelo baixado no ollama
   OLLAMA_API_PORT=11434 # Porta padrão do ollama

   DATABASE_URL=postgresql+psycopg2://root:root123@localhost:5432/classipy_database
   ```

### 2. Rodando Backend, Postgres e Ollama via Docker

Você pode rodar o **backend**, o **Postgres** e o **Ollama** usando **Docker Compose**, sem precisar instalar nada manualmente.

1. Certifique-se de ter [Docker](https://www.docker.com/) e [Docker Compose](https://docs.docker.com/compose/install/) instalados.

2. No diretório do projeto, suba os containers:

   ```bash
   docker compose up -d
   ```

   Isso vai iniciar:

   - Backend (porta 8000)
   - Postgres (porta 5432)
   - Ollama (porta 11434)

3. Baixe o modelo LLM desejado no Ollama:
   ```bash
   docker compose exec ollama ollama pull nomeDoModelo
   ```
   Substitua **nomeDoModelo** pelo modelo que você deseja usar.

### 3. Instalação utilizando um ambiente virtual `venv`

1. Crie o ambiente virtual

   ```sh
   python -m venv venv

   # Windows - ative o ambiente
   source venv/Scripts/activate

   # Linux - ative o ambiente
   . venv/bin/activate

   # Mac - ative o ambiente
   source venv/bin/activate
   ```

2. Instale as dependências

   ```sh
   pip install -r requirements.txt
   ```

3. Execute a aplicação

   ```sh
   uvicorn src.main:app --reload
   ```

   Ou execute o camando

   ```sh
   python run.py
   ```

4. Acesse a Aplicação

- O FastAPI está disponível em: [http://localhost:8000](http://localhost:8000)
- Para testar rotas utilize: [http://localhost:8000/docs](http://localhost:8000/docs)

### 4. Clonar o Repositório Front-end

O primeiro passo é clonar o repositório do projeto para o seu ambiente local.

1.  Abra um terminal.

2.  Execute o seguinte comando para clonar o repositório:

    ```bash
    git clone [https://github.com/Bug-Busters-F/ClassiPy-frontend](https://github.com/Bug-Busters-F/ClassiPy-frontend)
    ```

3.  Navegue até o diretório do projeto:
    ```bash
    cd ClassiPy-frontend
    ```

### 5. Instalar Dependências e Rodar o Projeto

Com o ambiente configurado, basta instalar as dependências do Node.js e iniciar o servidor de desenvolvimento.

1.  Instale as dependências do projeto:

    ```sh
    npm install
    ```

2.  Execute a aplicação em modo de desenvolvimento:
    ```sh
    npm run dev
    ```

### 6. Acesse a Aplicação

- A aplicação frontend estará disponível em: [http://localhost:5173](http://localhost:5173) .

---

## 👥 Autores

|    Função     | Nome           |                                                                                                                                               GitHub |                                                                                                                               Linkedin                                                                                                                               |
| :-----------: | :------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| Product Owner | Humberto Ishii |        [![GitHub Badge](https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white)](https://github.com/HumbertoIshii) |                                            [![Linkedin Badge](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://br.linkedin.com/in/humberto-ishii-silva-754489161)                                            |
| Scrum Master  | Diego Castilho |             [![GitHub Badge](https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white)](https://github.com/DigoCast) |                                              [![Linkedin Badge](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/diego-castilho-8b87a8301/)                                              |
|  Team Member  | Gabriel Viell  | [![GitHub Badge](https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white)](https://github.com/GabrielViellCastilho) | [![Linkedin Badge](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gabriel-viell-castilho-220438317?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app) |
|  Team Member  | Vinicius Elias |            [![GitHub Badge](https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white)](https://github.com/ViniElias) |                                              [![Linkedin Badge](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/vinicius-elias-895332235/)                                              |
|  Team Member  | Davi Miyake    |            [![GitHub Badge](https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white)](https://github.com/DaviMBDev) |                                                    [![Linkedin Badge](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/davimiyakeb/)                                                     |
