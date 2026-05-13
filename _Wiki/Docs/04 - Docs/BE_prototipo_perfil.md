# Backend: Meu Perfil

## Objetivo
Fornecer endpoints para leitura/atualização do perfil do usuário, upload de avatar e preferências.

## Endpoints
- `GET /api/users/{id}` — retorna perfil público ou próprio com dados completos.
- `PATCH /api/users/{id}` — atualiza campos permitidos (`name`, `displayName`, `bio`, etc.).
- `POST /api/users/{id}/avatar` — upload `multipart/form-data` (avatar). Armazenar em storage e salvar URL.

## Segurança e Autorização
- Somente o próprio usuário (ou admin) pode atualizar seu perfil.
- Validar imagens (tipo, tamanho máximo) e gerar versões (thumb, webp).

## Modelos / DB
- `UserProfile { user_id, display_name, avatar_url, bio, preferences }`

## Notas
- Recomenda-se uso de CDN e assinaturas temporárias para acesso a imagens privadas.