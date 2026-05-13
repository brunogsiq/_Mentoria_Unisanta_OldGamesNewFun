# Prototipo: Base para Jogos

## Objetivo
Definir estrutura base usada por telas de jogos (grid, painéis laterais, responsive).

## Estrutura
- Conteúdo principal (board) + painel lateral (placar/ações)

## CSS recomendado
```css
.game-layout { display: grid; grid-template-columns: 1fr 20rem; gap: 2rem; }
.game-panel { padding: 1.5rem; /* 24px */ }
```

## Notas
- Manter painel lateral fixo em dispositivos maiores; empilhar em mobile.