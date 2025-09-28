## Padrão para Mensagens de Commit

Para manter nosso histórico de commits organizado e legível, adotamos o padrão **Conventional Commits**. Esta abordagem simplificada nos ajuda a comunicar as mudanças de forma clara e padronizada.

---

### Estrutura do Commit

Cada mensagem de commit deve seguir o seguinte formato:

`<tipo>: <descrição da entrega>`

---

### Tipos de Commit

| Tipo           | Descrição                                          | Exemplo                                                       |
| :------------- | :------------------------------------------------- | :------------------------------------------------------------ |
| **`feat`**     | Adição de uma nova funcionalidade ("feature").     | `feat: Implementação dos repositórios...`                     |
| **`fix`**      | Correção de um bug.                                | `fix: Correção do componente de seleção de município`         |
| **`docs`**     | Atualização ou criação de documentação.            | `docs: Inclusão de diagrama de modelo de BD para a aplicação` |
| **`style`**    | Mudança de formatação, sem afetar o código.        | `style: Ajuste de nomes de variáveis para camelCase`          |
| **`refactor`** | Refatoração do código, sem alterar funcionalidade. | `refactor: Refatora serviço de autenticação para usar classe` |
| **`test`**     | Adiciona ou modifica testes.                       | `test: Adiciona testes unitários para a função de cálculo`    |
| **`chore`**    | Atualizações menores que não impactam o código.    | `chore: Atualiza versão do React para 19.1.1`                 |

---

### Legenda

- **`<descrição da entrega>`**: É uma descrição clara e concisa do que foi feito no commit.
