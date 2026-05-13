# Backend: Jogo da Velha (Tic-Tac-Toe)

## Objetivo
Gerenciar sessões de jogo da velha, movimentos, vitória/empate e placar.

## Endpoints / Sockets
- `POST /api/games/tictactoe/sessions` — cria nova sessão e retorna `sessionId`.
- WebSocket `wss://.../games/tictactoe/{sessionId}` — mensagens: `join`, `move`, `state`, `end`.
- `POST /api/games/tictactoe/{sessionId}/move` — alternativa HTTP para jogar (com validação).

## Validação
- Validar vez do jogador, posição válida e célula livre.

## Persistência
- Salvar movimentos e resultado final; atualizar leaderboard.

## Notas
- Usar locks otimistas ou servidor autoritativo para evitar condições de corrida.