# 📘 API ClassiPy – Documentação de Rotas

---

## 📄 Processamento de Arquivos e IA

---

### `POST /uploadfile/`

**Descrição:** Envia um arquivo PDF para o servidor. A API processa o documento, extrai todos os Part Numbers identificados e retorna uma lista com eles, juntamente com um hash único que identifica o arquivo processado.

**Corpo da requisição (`multipart/form-data`):**

- `file`: O arquivo PDF a ser enviado.

**Resposta `200`:**

```json
{
  "Parts": [
    {
      "PartNumber": "CL10C330JB8NNNC123",
      "CountryOfOrigin": "US"
    },
    {
      "PartNumber": "CL10B472KB83213NNNC",
      "CountryOfOrigin": "UK"
    }
  ],
  "hash_code": "c370bca6d8e2b8912abf24cf0bedd1090e34be78a179de831d799f362b1b7b93"
}
```

**Resposta `422`:**

```json
{
  "detail": [
    {
      "loc": ["body", "file"],
      "msg": "Field required",
      "type": "value_error.missing"
    }
  ]
}
```

### `POST /agent/run`

**Descrição:** Executa o agente de IA para processar um prompt de texto. Esta rota é utilizada para a classificação detalhada de um Part Number, onde o prompt seria o próprio Part Number a ser classificado.

**Corpo da requisição (`json`):**

```json
{
  "prompt": "string"
}
```

---

## ⚙️ Rotas do Sistema

---

### `GET /`

**Descrição:** Endpoint raiz da API, utilizado como um "health check" para verificar se o servidor está online e respondendo.

**Resposta `200`:**

```json
{
  "message": "Classipy API is running"
}
```


### `GET /template/`

**Descrição:** Endpoint de template, pode ser utilizado para testes de conexão ou como base para novas rotas.

**Resposta `200`:**

```json
{
  "message": "Template Message"
}
```
