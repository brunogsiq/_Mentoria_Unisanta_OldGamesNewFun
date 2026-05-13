# Backend: Forca

## Objetivo
Gerenciar sessões do jogo da forca: palavra, tentativas, histórico de letras e resultado.

## Endpoints / Sockets
- `POST /api/games/hangman/sessions` — cria sessão com palavra (pode ser servidor-side ou seleção aleatória).
- `POST /api/games/hangman/{sessionId}/guess` — body: `{ letter }` → retorna estado atualizado.
- `GET /api/games/hangman/{sessionId}` — retorna estado atual da sessão.

## Segurança / Notas
- Evitar exposição da palavra em APIs públicas; enviar somente estados cifrados ou por WebSocket autenticado.
- Validar input de letra, normalizar maiúsculas/minúsculas.