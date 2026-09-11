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

- Tokens podem possuir tempo de validade.
- Token expirado normalmente não pode mais ser utilizado.
- Token expirado pode resultar em 401 Unauthorized.

Access Token:
- Usado para acessar recursos protegidos.
- Normalmente possui duração menor.

Refresh Token:
- Utilizado para obter um novo Access Token.
- Pode possuir duração maior.

Fluxo:

Login
  ↓
Access Token + Refresh Token
  ↓
Access Token utilizado
  ↓
Access Token expira
  ↓
Refresh Token
  ↓
Novo Access Token

-----------------------------------------------------------------------------------

- O Access Token normalmente é enviado no Header Authorization.
- Exemplo:
  Authorization: Bearer ACCESS_TOKEN

- Token inválido/ausente pode resultar em 401 Unauthorized.
- Token válido, mas sem permissão suficiente, pode resultar em 403 Forbidden.

Segurança:
- Não publicar tokens no código ou GitHub.
- Informações sensíveis podem ser armazenadas em variáveis de ambiente.

Autenticação:
→ Quem é você?

Autorização:
→ O que você pode fazer?

Tokens podem possuir diferentes permissões/scopes.

