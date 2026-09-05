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

