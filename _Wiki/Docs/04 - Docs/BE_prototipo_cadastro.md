# Backend: Cadastro (Registro)

## Objetivo
Criar novo usuário, validar dados e iniciar fluxo de verificação (e-mail).

## Endpoints
- `POST /api/users` — body: `{ name, email, password }` → cria usuário (status: unverified) e envia e-mail de verificação.
- `GET /api/users/verify?token=...` — verifica conta.

## Validação
- Email único; senha mínima (ex.: 8 caracteres com complexidade opcional).
- Sanitização dos inputs.

## Segurança
- Hash de senha com `bcrypt`/`argon2`.
- Não retornar `password_hash` em respostas.
- Proteção contra criação em massa (CAPTCHA / rate limit).

## Modelos / DB
- `User { id, name, email, password_hash, verified, created_at }`
- `EmailVerificationToken { token_hash, user_id, expires_at }`

## Notas
- Enviar e-mail com link que contém token de uso único e expiração curta.
- Registrar origem (IP) e timestamp do registro.