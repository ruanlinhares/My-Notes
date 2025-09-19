**(Notas atualizadas em 17/08/2025)**
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

Toda vez que o cliente (aplicação) envia uma requisição para o servidor (API) ela devolve uma resposta, chamamos esta de **código de status**. O status pode é um número que responde o que ocorreu com nossa requisição após envio, ele pode ser dividido em 5 categorias:

**1xx (Códigos de informação)** : essa categoria informa que a requisição está em andamento. São respostas temporárias que indicam que o servidor recebeu a requisição e está em processo de tratamento. Exemplos:
* Código **100 Continue**: Significa que o cliente deve continuar com a requisição. O servidor recebeu as informações iniciais e o cliente pode enviar o corpo da requisição.

**2xx (Códigos de sucesso)**: essa categoria indica que a requisição foi enviada e recebida com sucesso. Exemplos:
* Código **200 OK**: significa que a requisição foi bem-sucedida e a resposta foi retornada com sucesso.
* Código **201 Created**: significa que a requisição foi bem-sucedida e um novo recurso/item foi criado no servidor. Utilizamos para enviar dados que criam algo novo (**post**), como um usuário ou um post.
* Código **201 No Content**: significa que a requisição foi bem-sucedida, mas não existe conteúdo para retornar. Utilizado em requisições de **update** ou **delete** de dados, a confirmação é o suficiente. 

**3xx (Códigos de Redirecionamento)**: essa categoria indica que a requisição precisa ser redirecionada para outro endereço. Isso pode plotar na tela caso a página foi movida permanentemente ou temporariamente. Exemplos:
* Código **301 Moved Permanently**: significa que o recurso (página) solicitado foi movido permanente para outro endereço.
* Código **307 Temporary Redirect**: significa que quele recurso foi movido temporariamente para outro endereço.

**4xx (Códigos de erro do cliente)**: esta categoria informa erros com e requisição, e a culpa é do cliente. Exemplos:
* Código **401 Unauthorized**: a requisição não contém credenciais de autenticação válidas. Acesso negado.
* Código **403 Forbidden**: significa que a requisição é válida, mas o servidor se recusa a autorizá-la. O cliente pode até ter credenciais válidas, porém o cliente não possui nível de permissão para aceso.
* Código **404 (Not Found)**: significa que o recurso solicitado não existe no servidor.
* Código **429 Too Many Requests**: significa que o cliente excedeu o número de requisições em um curto período de tempo. Geralmente é utilizado como uma prática de segurança para evitar ataques ou excesso de uso.

**5xx (Códigos de erro do servidor)**: essa categoria informa erros na requisição por parte do servidor. Quando ocorre um erro no processamento da requisição no servidor, ele retorna esses erros. Exemplos:
* Código **500 Internal Server Error**: significa que  o servidor, por algum motivo, não conseguiu atender a requisição. Um erro genérico que indica um problema interno no servidor.
* Código **503 Service Unavailable**: significa que o servidor não consegue lidar com requisições naquele momento. Podemos utilizar quando o servidor estiver em manutenção ou sobrecarregado. 

# Essencial
---
## Tipos de APIs

## Segurança da API - boas práticas
### Autenticação com JWT

O **JWT** (JSON Web Token) é um padrão **RFC 7519** que define uma jeito compacto e seguro de transmitir informações usando um objeto JSON. Usamos o JWT amplamente em processos de autenticação e autorização para aplicações web. Usamos ele, principalmente, para confirmar o usuário e fornecer acesso a recursos, sem necessidade de guardar o estado da sessão no servidor. O JWT é composto por três partes separadas por pontos:

```json
//Estrutura de um Jwt
abcdefghi.jklmnopq.rstuvwxyz
```

**Header (abcdefghi)**

O Header (cabeçalho)é composto por 2 partes:
-  O tipo do token, geralmente é ```"JWT"```
-  O algoritmo de assinatura, como ```HS256``` ou ```RS256```, são exemplos mais comuns.
  
 ```JSON
 {
	 "alg": "HS256",
	 "typ": "JWT"
 }
 ```


**Payload (jklmnopq)**

O **payload** (corpo) carrega as informações, mais conhecidas como **"claims"**, que queremos passar. Essas informações, geralmente, são coisas relevantes para a sua aplicação, podem ser a identidade do usuário, permissões, tempo de expiração do token, etc.

```JSON
{
  "sub": "1234567890",
  "name": "João Silva",
  "role": "admin",
  "iat": 1695000000,
  "exp": 1695003600
}
```

**tipos de claims**
- 


# Extra knowledge
---

