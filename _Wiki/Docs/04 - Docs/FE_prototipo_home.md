# Tela: Home — Seleção de Jogos

## Objetivo
Permitir escolha rápida de jogos com cartões grandes e acionáveis.

## Componentes
- Header
- Título
- Grid de cards de jogos
- Botões: Perfil, Sair

## Estrutura visual
Header → Título → Games grid (cards grandes)

## CSS recomendado
```css
.games-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(13.75rem, 1fr)); /* 220px */
  gap: 1.5rem; /* 24px */
}

.game-card {
  min-height: 11.25rem; /* 180px */
  border-radius: var(--radius-lg);
  padding: 1.5rem; /* 24px */
}
```

## Notas
- Grid responsivo para encaixar em diferentes larguras.
- Cartões com área de clique expandida.