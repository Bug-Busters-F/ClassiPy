# API - 4º Semestre ADS

# ClassiPy

# Documentação - Sprint 1

<p align="center">
     <h2 align="center"> Bug Busters</h2>
</p>

<p align="center">
 | <a href ="#desafio"> Desafio da Sprint</a>  |
 <a href ="#user-stories"> User Stories</a>  |
 <a href ="#burndown-sprint"> Burndown</a> |
 <a href ="#backlog"> Backlog</a> |
 <a href ="#dor">DoR</a>  |
 <a href ="#dod">DoD</a>  |
 <a href ="#equipe"> Equipe</a> |
</p>

> Status da Sprint: Concluída ✅

## Desafio <a id="desafio"></a>

O desafio da Sprint 1 foi estabelecer a fundação completa do ClassiPy. O objetivo era construir a arquitetura inicial do sistema, incluindo a configuração do servidor backend com FastAPI e a estruturação do frontend com React. As metas principais foram implementar a modelagem do banco de dados, desenvolver a funcionalidade core de upload e leitura de PDFs para extrair Part Numbers, e criar a interface inicial para que o usuário pudesse visualizar os dados extraídos, validando assim o fluxo principal da aplicação.

## 📋 User Stories <a id="user-stories"></a>

| Rank | Prioridade | User Story                                                                                                                            | Status |
| :--: | :--------: | ------------------------------------------------------------------------------------------------------------------------------------- | :----: |
|  1   |    Alta    | Como operador de cadastro, eu gostaria de carregar um PDF de documentos de importação para que o sistema identifique os Part Numbers. |   ✅   |
|  2   |    Alta    | Como operador de cadastro, eu gostaria de visualizar a lista de Part Numbers extraídos para confirmar que a leitura foi correta.      |   ✅   |
|  3   |   Média    | Como operador de cadastro, eu gostaria de acessar uma interface clara e organizada para acompanhar o processo de classificação.       |   ✅   |

---

## 📉 Burndown Sprint <a id="burndown-sprint"></a>

<img src="./Burndown-Sprint1.png">

## 🎯 Backlog Sprint <a id="backlog">

<img src="./Backlog-Sprint1.png">

## 🏅 DoR - Definition of Ready <a id="dor"></a>

| Critério                          | Descrição                                                                                              |
| :-------------------------------- | ------------------------------------------------------------------------------------------------------ |
| **Clareza na Descrição**          | A User Story está escrita no formato “Como [persona], quero [ação] para que [objetivo]”.               |
| **Critérios de Aceite Definidos** | A história possui critérios objetivos que indicam o que é necessário para considerá-la concluída.      |
| **Protótipo/Design Disponível**   | Se a tarefa envolve UI, mockups ou fluxos de tela estão anexados ou referenciados.                     |
| **Contrato de API Acordado**      | As necessidades de comunicação entre Frontend e Backend foram claramente definidas (quando aplicável). |
| **Modelo de Dados Validado**      | O modelo de dados relacionado à tarefa foi validado pela equipe.                                       |
| **Compreensão Compartilhada**     | Toda a equipe (incluindo PO e devs) compreende o propósito e o escopo da história.                     |
| **Estimável**                     | A história foi pontuada ou tem uma estimativa clara.                                                   |

## 🏅 DoD - Definition of Done <a id="dod"></a>

| Critério                            | Descrição                                                                                      |
| :---------------------------------- | ---------------------------------------------------------------------------------------------- |
| **Critérios de Aceite Atendidos**   | Todos os critérios de aceite da história foram implementados e validados.                      |
| **Código Implementado e Funcional** | A funcionalidade foi desenvolvida em uma branch `feature/` e não quebra a aplicação.           |
| **Testes Manuais Realizados**       | O fluxo da funcionalidade foi testado manualmente pelo desenvolvedor, incluindo casos de erro. |
| **Código Revisado (Code Review)**   | O Pull Request foi revisado e aprovado por pelo menos um outro membro da equipe.               |
| **Integração à `main`**             | O código foi integrado à branch `main` após a aprovação.                                       |
| **Documentação Atualizada**         | O `README.md` ou outra documentação relevante foi atualizada para refletir as novas mudanças.  |
| **Validação do PO**                 | O Product Owner validou a entrega com base nos critérios definidos.                            |

---

## Colaboradores <a id="equipe"></a>

| Função        | Nome           |
| :------------ | :------------- |
| Product Owner | Humberto Ishii |
| Scrum Master  | Diego Castilho |
| Team Member   | Gabriel Viell  |
| Team Member   | Vinicius Elias |
| Team Member   | Davi Miyake    |
