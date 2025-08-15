**(Notas atualizadas em 14/08/2025)**
# Iniciando
---
**API** é uma sigla para Application Programming Interface. Geralmente integrada às aplicações, é um conjunto de regras, protocolos e ferramentas que permite a comunicação entre diferentes softwares e aplicações.

No mundo das APIs a comunicação ocorre por meio de **requisições** e **respostas**:

### Requisições 

O cliente (aplicação) envia uma requisição para a API, pedindo dados ou para realizar uma determinada ação. O corpo dessa requisição inclui:

**URL:** O endereço do recurso que deseja acessar, mais conhecido como **Endpoint**.

```jsx
https://api.exemplo/posts
htps://api.exemplo/posts/123
```

**Método HTTP**: O tipo de ação que deseja realizar. Os mais comuns são:

```jsx
GET //deseja pegar algo
POST //deseja inserir algo
PUT //deseja atualizar algo
DELETE // deseja apagar algo
```

**Header:** são informações extras, como metadados. O HTTP pode conter um header que contenham uma chave de autenticação ou tipo de dados que estão sendo enviados, etc.

**Body:** são os dados que deseja comunicar. Geralmente eles estarão em **JSON** (JavaScript Object Notation) que é um formato de dados, podemos encontrar **XML** ou **Protobuf** dependendo da situação. Estrutura básica de um **JSON**:

```json
{ 
	"nome": "Ana Silva", 
	"email": "ana.silva@exemplo.com", 
	"senha": "senha-segura123" 
}
```

Reunindo todos esses pontos podemos montar uma **requisição HTTP completa**:

```http
POST /usuarios HTTP/1.1
Content-Type: application/json 
Authorization: Bearer <seu-token-de-acesso>

{ 
	"nome": "Ana Silva", 
	"email": "ana.silva@exemplo.com", 
	"senha": "senha-segura123" 
}
```

```Post```: método HTTP.
```/usuarios```: endpoint, url.
```HTTP/1.1```: protocolo de envio de dados.

### Respostas

Toda vez que o cliente (aplicação) envia uma requisição

# Essencial
---

## Consumo de API

### JSON

## API Key

### Query String

# Extra knowledge
---

