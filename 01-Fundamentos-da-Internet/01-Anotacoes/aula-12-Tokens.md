Aula 12 — Tokens 

- Token é uma credencial usada para autenticar um cliente/usuário perante uma API.
- Normalmente é obtido após um login/autenticação.
- O token não é necessariamente a senha.
- Depois do login, o token pode ser utilizado nas requisições.
- Normalmente é enviado no Header Authorization.

Exemplo:

Authorization: Bearer TOKEN

Fluxo:

Login
  ↓
Email + senha
  ↓
Servidor autentica
  ↓
Token
  ↓
Cliente utiliza o token
  ↓
API valida o token
  ↓
Requisição é processada

Token inválido/ausente pode resultar em:
401 Unauthorized

-----------------------------------------------------------------------------------
