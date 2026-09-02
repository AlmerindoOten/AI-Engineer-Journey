REST é um conjunto de princípios para projetar APIs de maneira organizada e previsível.

EX: PATCH /usuarios/25
seria lido como: 
usuarios/25
↓
recurso: usuário 25

PATCH
↓
ação: atualização parcial

Endpoint = endereço + método que você usa para acessar determinada operação da API.

- Endpoint = ponto de acesso específico de uma API.
- /produtos → coleção de produtos.
- /produtos/10 → produto específico.
- Recursos podem ser aninhados:
  /usuarios/15/pedidos
  → pedidos do usuário 15.

- /usuarios/15/pedidos/8
  → pedido 8 do usuário 15.

- REST permite uma estrutura previsível para que clientes e agentes entendam a API.
- REST é um estilo arquitetural/conjunto de princípios para organizar APIs.
- URL identifica o recurso.
- Método HTTP define a ação.
- Exemplo:
  GET /produtos → listar produtos
  GET /produtos/10 → consultar produto 10
  POST /produtos → criar produto
  PATCH /produtos/10 → alterar produto 10
  DELETE /produtos/10 → excluir produto 10
