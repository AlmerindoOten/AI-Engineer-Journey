Webhooks: Webhook é um mecanismo que permite que um sistema envie automaticamente uma requisição para outro sistema quando determinado evento acontece.

- Na API tradicional, o cliente faz a requisição para obter uma informação.
- No Webhook, o sistema envia uma requisição quando determinado evento acontece.
- Webhooks normalmente utilizam o método POST.
- O sistema que possui o evento envia o Webhook.
- O sistema receptor possui um endpoint para receber o Webhook.

Exemplo:

Sistema de pagamento
        ↓
POST /webhook
        ↓
Meu sistema

Exemplos de eventos:
- pagamento_aprovado
- pagamento_cancelado
- pedido_criado
- mensagem_recebida
-----------------------------------------------------------------------------------------------
- Um Webhook normalmente possui um endpoint específico para receber eventos.
- Exemplo:
  POST /webhook/pagamento

- O evento é enviado no Body da requisição, geralmente em JSON.

Exemplo:

{
  "evento": "pagamento_aprovado",
  "pedido_id": 42,
  "valor": 150.00
}

- O sistema receptor interpreta o evento e executa uma ação.
- Um mesmo endpoint pode receber diferentes eventos.
- Webhook não é uma API inteira; é um mecanismo de comunicação baseado em eventos.

