# Backend: Infraestrutura base para jogos

## Objetivo
Definir serviços comuns a jogos (sessões, matchmaking, persistência e auditoria).

## Componentes
- Matchmaking / criação de sessão
- Gerenciamento de sessão em memória + persistência eventual
- Pontuação e leaderboard
- WebSocket / realtime events para jogabilidade

## Endpoints / Sockets
- `POST /api/games/{gameId}/sessions` — cria sessão (singleplayer/multiplayer).
- WebSocket `wss://.../games/{sessionId}` — eventos: `move`, `state`, `end`.
- `GET /api/games/{gameId}/sessions/{id}` — obter status da sessão (persistido).

## Notas de arquitetura
- Persistir checkpoints periódicos para evitar perda de progresso.
- Projetar limites de escalabilidade: usar Redis para pub/sub e armazenamento de sessão em cache.
- Autorização por token emitido na criação da sessão.