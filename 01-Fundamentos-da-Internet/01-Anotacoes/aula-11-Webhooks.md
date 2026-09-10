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

Pedido é enviado
      ↓
Sistema identifica o evento
      ↓
Sistema envia POST para o Webhook
      ↓
Sua aplicação recebe o JSON
      ↓
Identifica "pedido_enviado"
      ↓
Lê pedido_id = 42
      ↓
Atualiza/processa o pedido 42. 
-----------------------------------------------------------------------------------------------
- Webhooks precisam ser protegidos contra requisições falsas.
- A aplicação pode verificar uma assinatura ou credencial.
- Se a autenticação for válida, o evento pode ser processado.
- Se for inválida, a requisição deve ser rejeitada.

Fluxo:

Webhook recebido
      ↓
Validar assinatura/credencial
      ↓
Ler evento
      ↓
Identificar recurso
      ↓
Executar ação
      ↓
Responder com status HTTP

Exemplo:

POST /webhook/pagamento

{
  "evento": "pagamento_aprovado",
  "pedido_id": 42
}

→ Validar
→ Identificar evento
→ Identificar pedido
→ Atualizar pedido
→ Responder 200 OK

WEBHOOKS FILE








