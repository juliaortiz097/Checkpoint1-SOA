# API de Pedidos

Este projeto contém uma API para gerenciar pedidos. Abaixo estão os detalhes dos endpoints disponíveis, incluindo exemplos de requisições e respostas, com base no fluxo de pedidos que você demonstrou.

## Endpoints

### 1. Criar um Pedido

**Método:** `POST`  
**URL:** `http://localhost:8080/pedidos`  

**Descrição:**  
Cria um novo pedido. O ID do pedido será gerado automaticamente pelo banco de dados.

**Requisição (Body):**
```json
{
  "clienteNome": "Juliazinha Ortizinha",
  "valorTotal": 180.00
}
Resposta (200 - OK):

json
Copiar
Editar
{
  "id": 3,
  "clienteNome": "Juliazinha Ortizinha",
  "dataPedido": "2025-03-26",
  "valorTotal": 180.00
}
2. Criar outro Pedido
Método: POST
URL: /pedidos

Descrição:
Cria outro novo pedido. O ID será gerado automaticamente.

Requisição (Body):

json
Copiar
Editar
{
  "clienteNome": "Julião Ortizão",
  "valorTotal": 320.00
}
Resposta (200 - OK):

json
Copiar
Editar
{
  "id": 4,
  "clienteNome": "Julião Ortizão",
  "dataPedido": "2025-03-26",
  "valorTotal": 320.00
}
3. Buscar Todos os Pedidos
Método: GET
URL: /pedidos

Descrição:
Retorna uma lista de todos os pedidos cadastrados.

Resposta (200 - OK):

json
Copiar
Editar
[
  {
    "id": 3,
    "clienteNome": "Juliazinha Ortizinha",
    "dataPedido": "2025-03-26",
    "valorTotal": 180.00
  },
  {
    "id": 4,
    "clienteNome": "Julião Ortizão",
    "dataPedido": "2025-03-26",
    "valorTotal": 320.00
  }
]
4. Buscar Pedido por ID
Método: GET
URL: /pedidos/{id}

Descrição:
Retorna um pedido específico baseado no ID fornecido.

Exemplo de URL: /pedidos/4

Resposta (200 - OK):

json
Copiar
Editar
{
  "id": 4,
  "clienteNome": "Julião Ortizão",
  "dataPedido": "2025-03-26",
  "valorTotal": 320.00
}
5. Atualizar um Pedido
Método: PUT
URL: /pedidos/{id}

Descrição:
Atualiza os dados de um pedido existente.

Exemplo de URL: /pedidos/4

Requisição (Body):

json
Copiar
Editar
{
  "clienteNome": "Julia Ortiz",
  "valorTotal": 320.00
}
Resposta (200 - OK):

json
Copiar
Editar
{
  "id": 4,
  "clienteNome": "Julia Ortiz",
  "dataPedido": "2025-03-26",
  "valorTotal": 320.00
}
6. Deletar um Pedido
Método: DELETE
URL: /pedidos/{id}

Descrição:
Deleta um pedido específico baseado no ID fornecido.

Exemplo de URL: /pedidos/3

Resposta (200 - OK):

json
Copiar
Editar
{
  "message": "Pedido deletado com sucesso"
}
7. Buscar Todos os Pedidos após Deletar
Método: GET
URL: /pedidos

Descrição:
Retorna uma lista de todos os pedidos após deletar o pedido com ID 3.

Resposta (200 - OK):

json
Copiar
Editar
[
  {
    "id": 4,
    "clienteNome": "Julia Ortiz",
    "dataPedido": "2025-03-26",
    "valorTotal": 320.00
  }
]
