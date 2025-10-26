# 🧭 Guia de Contribuição - ClassiPy

Estamos felizes em saber que você quer contribuir para o **ClassiPy**!  
Cada contribuição é essencial para o crescimento e aprimoramento do projeto.  
Este guia reúne **todas as instruções** necessárias para configurar e rodar **tanto o backend (FastAPI)** quanto o **frontend (React)**.  

---

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


---

## ⚙️ Backend (FastAPI)

### 1. Clonar o Repositório


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

### 2. Executando localmente

1. Abra um terminal.

2. Acesse o terminal do Postgres com usuário padrão
   ```bash
   psql -U postgres
   ```

3. Crie o banco de dados
   ```sql
   CREATE DATABASE classipy_database WITH OWNER = postgres;
   ```

4. Saia do terminal do Postgres
   ```bash
   \q
   ```

5. Acesse a pasta do projeto
   ```bash
   cd Classipy-backend
   ```

6. Crie as tabelas do banco
   ```bash
   psql -U postgres -d classipy_database -f postgres-init/init.sql
   ```

### 3. Executando Backend, Postgres e Ollama via Docker

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

   E também baixe **bge-m3**
   ```bash
   docker compose exec ollama ollama pull bge-m3
   ```

### 4. Instalação utilizando um ambiente virtual `venv`

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
   - Instale o navegador necessário para o Playwright
   ```sh
   playwright install chromium
   ```

3. Execute a aplicação

   ```sh
   uvicorn src.main:app --reload
   ```
   Ou execute o comando

   ```sh
   python run.py
   ```

4. Opcional: testar a conexão com o banco
   ```sh
   python -m src.database.test_db_connection
   ```

5. Opcional: preencher as tabelas com dados fictícios
   ```sh
   python seed_local.py
   ```

### 5. Acesse a Aplicação

- O FastAPI está disponível em: [http://localhost:8000](http://localhost:8000)
- Para testar rotas utilize: [http://localhost:8000/docs](http://localhost:8000/docs)

--- 

## 💻 Frontend (React)

### 1. Clonar o Repositório

O primeiro passo é clonar o repositório do projeto para o seu ambiente local.

1.  Abra um terminal.

2.  Execute o seguinte comando para clonar o repositório:
    ```bash
    git clone https://github.com/Bug-Busters-F/ClassiPy-frontend
    ```

3.  Navegue até o diretório do projeto:
    ```bash
    cd ClassiPy-frontend
    ```

### 2. Instalar Dependências e Rodar o Projeto

Com o ambiente configurado, basta instalar as dependências do Node.js e iniciar o servidor de desenvolvimento.

1.  Instale as dependências do projeto:
    ```sh
    npm install
    ```

2.  Execute a aplicação em modo de desenvolvimento:
    ```sh
    npm run dev
    ```

### 3. Acesse a Aplicação

-   A aplicação frontend estará disponível em: [http://localhost:5173](http://localhost:5173) 
-   Certifique-se de que o backend também esteja rodando em `http://localhost:8000` para que a comunicação funcione.