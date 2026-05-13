# Jogo: Jogo da Velha

## Objetivo
Placar simples e interação clara em tabuleiro 3x3.

## Componentes
- Tabuleiro 3x3
- Células grandes
- Indicador de vez
- Placar
- Botão Reiniciar

## Estrutura visual
Board 3x3 centralizado + painel lateral com placar e ações.

## CSS recomendado
```css
.tic-tac-toe-board {
    width: 26.25rem; /* 420px */
    max-width: 100%;
    aspect-ratio: 1/1;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    border: 0.1875rem solid var(--color-primary); /* 3px */
}

.tic-tac-toe-cell {
    font-size: 4.5rem; /* 72px */
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
}
```

## Notas
- Garantir tamanho mínimo de célula para toque.
- Fornecer feedback tátil/visual ao clicar.