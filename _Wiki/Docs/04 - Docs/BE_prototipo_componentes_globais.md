# Backend: Componentes e Serviços Globais

## Objetivo
Descrever serviços compartilhados usados pelo backend: autenticação, storage, notificações, logs e métricas.

## Serviços
- **Auth Service** — emissão/validação de JWT, refresh tokens, políticas de sessão.
- **Storage Service** — integração com S3/Blob para arquivos (avatars, assets); gerar URLs assinadas.
- **Payments Adapter** — encapsula provider (Stripe) e webhooks.
- **Realtime / PubSub** — Redis / Socket server para eventos de jogo.
- **Email Service** — templates e envio (verificação, recuperação de senha).

## Observações
- Isolar integrações externas em adaptadores para facilitar testes.
- Centralizar logging estruturado (JSON) e rotacionamento.