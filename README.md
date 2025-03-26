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




Testando a API


![image](https://github.com/user-attachments/assets/9de4421b-a1df-4392-8aa1-94236f416369)
![image](https://github.com/user-attachments/assets/1fde9a67-572b-492f-8f3c-bd780b907351)



Postando um produto novo

![image](https://github.com/user-attachments/assets/3697de6e-db5e-415d-92ec-3d56f322a37d)

Buscando todos os pedidos.

![image](https://github.com/user-attachments/assets/b1f32083-31ed-41f1-9287-1be569469ffd)


Buscar um pedido pelo ID

![image](https://github.com/user-attachments/assets/2451f381-ba51-43c5-a6b6-975aee2959fa)


Atualizar um pedido.

![image](https://github.com/user-attachments/assets/9c3f7bde-293e-4a98-a236-0f967f5d321a)


Deletar um pedido

![image](https://github.com/user-attachments/assets/4da35d11-dc56-40c8-b101-51839655cec2)

*peguei todos os pedidos para mostra que só ficou 1 e o outro foi excluído

![image](https://github.com/user-attachments/assets/a39bca3d-78b9-4dd6-b619-0468ea399483)

