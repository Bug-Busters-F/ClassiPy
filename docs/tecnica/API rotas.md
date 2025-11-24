 📘 API ClassiPy – Documentação de Rotas

## ⚙️ Rotas Principais do Sistema

### `GET /`
**Descrição:** Verifica o status da API (health check).  
**Resposta `200`:**

```json
{
  "ClassiPy API is running"
}
```

### `GET /template/`
**Descrição:** Retorna uma mensagem de template utilizada para testes de comunicação.  
**Resposta `200`:**
```json
{
  "Template Message"
}
```

## 📄 Processamento de Arquivos

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

## 🧩 Produtos
### `POST /produto/`
**Descrição:** Cria novos registros de produtos processados a partir do arquivo enviado.  
**Resposta `200`:**                    
**Corpo da requisição (`application/json`):**
```json
[
  {
    "partNumber": "string",
    "fileHash": "string"
  }
]
```

**Resposta `201`:**      
```json
[
  {
    "pro_id": 0,
    "partNumber": "string",
    "fileHash": "string",
    "status": "string"
  }
]
```

### `GET /produto/`
**Descrição:** Retorna o histórico de produtos processados, com paginação.        
**Parâmetros de Query:**
- `skip`: número de registros a ignorar (default: 0)
- `limit`: número máximo de registros a retornar (default: 100)

**Resposta `200`:**   
```json
[
  {
    "pro_id": 0,
    "historyId": 0,
    "fileHash": "string",
    "processedDate": "2025-10-26T21:04:34.266Z",
    "partNumber": "string",
    "status": "string",
    "classification": {
      "description": "string",
      "ncmCode": "string",
      "taxRate": 0,
      "manufacturer": {
        "name": "string",
        "country": "string",
        "address": "string"
      }
    }
  }
]
```
### `DELETE /produto/{id}`
**Descrição:** Exclui um produto do banco de dados    
**Parâmetros de Caminho:**
- `id`: ID do produto.    
  
**Resposta `200`:**   
```json
"Produto excluído com sucesso"
```

### `PUT /produto/{id}`
**Descrição:** Atualiza os dados de um produto específico.        
**Corpo da requisição (application/json):**
```json
{
  "partNumber": "string",
  "description": "string",
  "status": "string",
  "classification": {
    "description": "string",
    "ncmCode": "string",
    "taxRate": 0
  },
  "manufacturer": {
    "name": "string",
    "country": "string",
    "address": "string"
  }
}
```

**Resposta `200`:**   
```json
{
  "pro_id": 0,
  "historyId": 0,
  "fileHash": "string",
  "processedDate": "2025-10-26T21:04:34.271Z",
  "partNumber": "string",
  "status": "string",
  "classification": {
    "description": "string",
    "ncmCode": "string",
    "taxRate": 0,
    "manufacturer": {
      "name": "string",
      "country": "string",
      "address": "string"
    }
  }
}
```

### `GET /produto/{pro_id}/classification`
**Descrição:** Retorna as informações de classificação de um produto específico.        
**Parâmetros de Caminho:**
 `id`: ID do produto.

**Resposta `200`:**  
```json
{
  "ncmCode": "string",
  "description": "string",
  "taxRate": 0,
  "manufacturerName": "string",
  "countryOfOrigin": "string",
  "fullAddress": "string"
}
```
### `GET /produto/recent`
**Descrição:** Retorna as informações de classificação dos 5 produtos recentes.
**Resposta `200`:**  
```json
[
  {
    "pro_id": 0,
    "historyId": 0,
    "fileHash": "string",
    "processedDate": "2025-10-26T21:04:34.280Z",
    "partNumber": "string",
    "status": "string",
    "classification": {
      "description": "string",
      "ncmCode": "string",
      "taxRate": 0,
      "manufacturer": {
        "name": "string",
        "country": "string",
        "address": "string"
      }
    }
  }, 
  ...
]
```
## 🕓 Histórico
### `GET /historico/`
**Descrição:** Retorna uma lista paginada do histórico de produtos processados.

**Parâmetros de Query:**

| Nome | Tipo | Descrição | Padrão |
| :--- | :--- | :--- | :--- |
| "page" | "integer" | Número da página a ser retornada. | 1 |
| "limit" | "integer" | Número máximo de registros por página. | 10 |
| "search" | "string" | Termo para buscar nos registros. | - |
| "filter_date" | "string" | Filtra registros por data. | - |

**Resposta 200 (Successful Response):**

```json
{
  "pns": [
    {
      "pro_id": 0,
      "historyId": 0,
      "fileHash": "string",
      "processedDate": "2025-11-23T21:09:02.700Z",
      "partNumber": "string",
      "status": "string",
      "classification": {
        "description": "string",
        "ncmCode": "string",
        "taxRate": 0,
        "manufacturer": {
          "name": "string",
          "country": "string",
          "address": "string"
        }
      }
    }
  ],
  "page": 0,
  "limit": 0,
  "pages": 0
}
```

**Resposta 422 (Validation Error):**

```json
{
  "detail": [
    {
      "loc": [
        "string",
        0
      ],
      "msg": "string",
      "type": "string"
    }
  ]
}
```

### `DELETE /historico/{history_id}`
**Descrição:** Remove um registro específico do histórico de produtos processados usando o ID do histórico.

**Parâmetros de Path:**

| Nome | Tipo | Descrição |
| :--- | :--- | :--- |
| "history_id" | "integer" | O ID do registro histórico a ser deletado. |

**Resposta 200 (Successful Response):**

```json
"string"
```

**Resposta 422 (Validation Error):**

```json
{
  "detail": [
    {
      "loc": [
        "string",
        0
      ],
      "msg": "string",
      "type": "string"
    }
  ]
}
```

## 🤖 Classificação por IA
### `GET /classify/{part_number}`
**Descrição:** Recebe um Part Number e retorna os dados de classificação obtidos pelo serviço de IA.        
**Parâmetros de Caminho:**
- `part_number`: código do produto a ser classificado.

**Resposta `200`:** 
```json
{
  "ncm": "string",
  "descricao": "string",
  "fabricante": "string",
  "aliquota": 0,
  "descricao_ncm": "string"
}
```