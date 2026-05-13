# Backend: Login

## Objetivo
Endpoints para autenticação de usuários (login, refresh token, logout) e proteção de sessão.

## Endpoints
- `POST /api/auth/login` — body: `{ email, password }` → retorna `accessToken`, `refreshToken`, `user`.
- `POST /api/auth/refresh` — body: `{ refreshToken }` → novo `accessToken`.
- `POST /api/auth/logout` — invalida `refreshToken`.

## Validação
- Email: formato válido
- Senha: não vazia
- Rate limit, bloqueio após N tentativas (ex.: 5 em 15m)

## Segurança
- Armazenar `refreshToken` hashed no DB ou usar JWT com short TTL para `accessToken`.
- Senhas com `bcrypt` (`cost >= 12`).
- Usar HTTPS obrigatório; cookies `httpOnly`, `secure`, `SameSite=Strict` para sessões se aplicável.

## Modelos / DB
- `User { id, name, email, password_hash, created_at, verified_at }`
- `RefreshToken { id, user_id, token_hash, revoked, expires_at }`

## Exemplo de request/response
```json
POST /api/auth/login
{ "email":"user@ex.com", "password":"senha" }

200 OK
{ "accessToken":"<jwt>", "refreshToken":"<token>", "user": { "id":1, "name":"Bruno" } }
```

## Notas de implementação
- Bloquear conta temporariamente após falhas repetidas.
- Registrar tentativas para análise de segurança.