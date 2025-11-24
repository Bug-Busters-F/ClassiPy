# API - 4º Semestre ADS

<p align="center">
  <h2 style="font-size: 2em; margin-bottom: 0;">
    <img src="./docs/img/ClassiPyLogo.png" alt="ClassiPy Logo" width="40" height="40" style="vertical-align: middle;"> 
    ClassiPy
  </h2>
</p>

Projeto API do 4° semestre de Análise e Desenvolvimento de Sistemas da equipe Bug Busters, FATEC Jessen Vidal, São José dos Campos

| Cliente | Periodo/Curso                                  | Professor M2     | Professor P2     | Contato Cliente              |
| ------- | ---------------------------------------------- | ---------------- | ---------------- | ---------------------------- |
| TecSys  | 4º ADS (Análise e Desenvolvimento de Sistemas) | Giuliano Bertoti | Juliana Pasquini | creonice@tecsysbrasil.com.br |

## 📃 Índice

<p align="center">
 | <a href ="#desafio"> Desafio </a>  |
 <a href ="#solução"> Solução </a>  |   
 <a href ="/docs"> Documentação </a>  |   
 <a href ="#backlog-do-produto"> Backlog do Produto </a>  |
 <a href ="#️demonstracao"> Demonstração </a>  |
 <a href ="#️cronogramaSprints"> Cronograma de Sprints </a>  |
 <a href ="#road-map">RoadMap </a> |
 <a href ="#tecnologias-utilizadas">Tecnologias </a> |
 <a href ="#manual-de-instalação">Manual de Instalação </a>  | 
 <a href ="#guia-usuario">Guia do Usuário </a>  | 
 <a href ="#autores"> Autores </a> |
</p>

# 🎯 Desafio <a id="desafio"></a>

O desafio consiste no desenvolvimento de um Agente de Inteligência Artificial para instrução de Processo para Registro de Importação. O processo manual de elaboração de registros aduaneiros para materiais produtivos, especialmente na indústria eletroeletrônica, é complexo e suscetível a erros. É necessário relacionar informações como Part-Number, classificação fiscal (NCM), fabricante e origem com endereço completo, gerando uma descrição detalhada do material. Qualquer ambiguidade ou erro nessas informações pode gerar dúvidas para a Receita Federal, acarretando penalidades e multas sobre a declaração do material importado.

# 🧠 Solução <a id="solução"></a>

ClassiPy - Classificação Inteligente de Produtos, é uma aplicação web projetada para resolver este desafio, automatizando e otimizando o processo de instrução de registro aduaneiro. A solução permite que o usuário faça o upload de um pedido de compras em formato PDF. A partir do documento, nosso agente de IA extrai todos os Part-Numbers e, para cada um, realiza uma busca inteligente para sugerir a classificação fiscal completa, incluindo descrição detalhada do produto, NCM, fabricante e mais.

---

## 📋 Backlog do Produto <a id="backlog-do-produto"></a>

| Rank | Prioridade | User Story                                                                                                                                                                                      | Sprint | Status |
| :--: | :--------: | :---- | :----: | :----: |
|  1   |    Alta    | Como operador de cadastro, eu gostaria de carregar um PDF de documentos de importação para que o sistema identifique automaticamente os Part Numbers.                                           |   1    |   ✅   |
|  2   |    Alta    | Como operador de cadastro, eu gostaria de visualizar a lista de Part Numbers extraídos para confirmar que a leitura foi correta.                                                                |   1    |   ✅   |
|  3   |   Média    | Como operador de cadastro, eu gostaria de acessar uma interface clara e organizada para acompanhar o processo de classificação.                                                                 |   1    |   ✅   |
|  4   |    Alta    | Como operador de cadastro, eu gostaria de visualizar de forma clara as informações classificadas de cada peça (descrição, NCM, alíquota, fabricante e origem) para validar antes da exportação. |   2    |   ✅   |
|  5   |   Média    | Como operador de cadastro, eu gostaria de editar manualmente informações classificadas caso o sistema apresente dados incorretos ou incompletos.                                                |   2    |   ✅   |
|  6   |   Média    | Como analista de importação, eu gostaria de exportar as informações classificadas em planilha Excel no formato padrão da empresa, para facilitar a entrega do processo de registro.             |   2    |   ✅   |
|  7   |   Média    | Como operador de cadastro, eu gostaria de receber uma prévia dos resultados processados antes de salvar ou exportar, para evitar erros.                                                         |   2    |   ✅   |
|  8   |    Alta    | Como operador de cadastro, eu gostaria que o sistema apresente resultados cada vez mais precisos para reduzir retrabalho.                                                                       |   3    |   ✅   |
|  9   |    Alta    | Como operador de cadastro, eu gostaria de utilizar um sistema estável e sem erros críticos, para não comprometer os prazos de importação.                                                       |   3    |   ✅   |
|  10  |   Média    | Como analista de importação, eu gostaria de ter acesso a um guia de uso do sistema para operar corretamente e sem dúvidas.                                                                      |   3    |   ✅   |

---

## 📽️ Demonstração do Projeto - Sprint 1 <a id="demonstracao"></a>

![GIF Sprint 1](docs/gifs/gifSprint1.gif)

---

## 📽️ Demonstração do Projeto - Sprint 2 <a id="demonstracao"></a>

![GIF Sprint 2](docs/gifs/gifSprint2.gif)

---

## 📽️ Demonstração do Projeto - Sprint 3 <a id="demonstracao"></a>

![GIF Sprint 3](docs/gifs/gifSprint3.gif)

---


## 🗓️ Cronograma das Sprints <a id="cronogramaSprints"></a>

| Sprint            | Previsão   | Status    | Documentação                                               |
| :-----------------: | ---------- | :---------: | ---------------------------------------------------------- |
| 01                | 29/09/2025 | ✅ | [Docs Sprint-1](./docs/processo/sprints/sprint1/README.md) |
| 02                | 26/10/2025 | ✅ | [Docs Sprint-2](./docs/processo/sprints/sprint2/README.md) |
| 03                | 23/11/2025 | ✅ | [Docs Sprint-3](./docs/processo/sprints/sprint3/README.md) |
| Feira de Soluções | 04/12/2025 | A fazer   |                                                            |

---

## 🛣️ Roadmap das Sprints <a id="road-map"></a>

<div style="display: flex; justify-content: center;">
  <img src="./docs/img/RoadMap-ClassiPy.png" style="width: 70%">
</div>

---

## 🧑‍💻 Tecnologias Utilizadas <a id="tecnologias-utilizadas"></a>

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

## 📖 Manual de Instalação <a id="manual-de-instalação"></a>
Acesse o manual de instalação seguindo os passos pelo arquivo [CONTRIBUTING.md](./CONTRIBUTING.md)

## 📖 Guia do Usuário <a id="guia-usuario"></a>
Acesse o guia do usuário aqui [GUIA DO USUÁRIO](./docs/tecnica/guia-usuario.pdf)

---

## 👥 Autores <a id="autores"></a>

|    Função     | Nome           |                                                                                                                                               GitHub |                                                                                                                               Linkedin                                                                                                                               |
| :-----------: | :------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| Product Owner | Humberto Ishii |        [![GitHub Badge](https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white)](https://github.com/HumbertoIshii) |                                            [![Linkedin Badge](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://br.linkedin.com/in/humberto-ishii-silva-754489161)                                            |
| Scrum Master  | Diego Castilho |             [![GitHub Badge](https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white)](https://github.com/DigoCast) |                                              [![Linkedin Badge](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/diego-castilho-8b87a8301/)                                              |
|  Team Member  | Gabriel Viell  | [![GitHub Badge](https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white)](https://github.com/GabrielViellCastilho) | [![Linkedin Badge](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gabriel-viell-castilho-220438317?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app) |
|  Team Member  | Vinicius Elias |            [![GitHub Badge](https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white)](https://github.com/ViniElias) |                                              [![Linkedin Badge](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/vinicius-elias-895332235/)                                              |
|  Team Member  | Davi Miyake    |            [![GitHub Badge](https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white)](https://github.com/DaviMBDev) |                                                    [![Linkedin Badge](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/davimiyakeb/)                                                     |

<img src="./docs/img/bug-busters-logo-black.jpg">
