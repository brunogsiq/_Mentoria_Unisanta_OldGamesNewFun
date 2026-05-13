# Backend: Esqueci a Senha / Reset

## Objetivo
Permitir recuperação de senha via e-mail com token de uso único e expiração.

## Endpoints
- `POST /api/auth/forgot` — body: `{ email }` → gera `passwordResetToken` e envia e-mail (não vazar existência da conta).
- `POST /api/auth/reset` — body: `{ token, newPassword }` → valida token e atualiza senha.

## Segurança
- Tokens com hashing no DB; expiração curta (ex.: 1h).
- Invalidar todos `refreshToken` ao resetar senha.

## Notas
- Não indicar se e-mail existe na resposta pública (usar mensagens genéricas).
- Log de operações sensíveis e alertas de segurança.