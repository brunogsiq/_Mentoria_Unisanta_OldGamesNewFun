# Componentes Globais

## Objetivo
Definir componentes reutilizáveis (botões, inputs, cards).

## Componentes
- `Button` primário e secundário
- `Input` com estados (focus, error)
- `Card` com sombra e padding

## CSS recomendado
```css
.btn-primary { padding: 0.75rem 1rem; /* 12px 16px */ border-radius: var(--radius-md); }
.input { padding: 0.75rem; /* 12px */ border: 0.0625rem solid var(--color-border); /* 1px */ }
.card { padding: 1.5rem; /* 24px */ box-shadow: var(--shadow-card); }
```

## Notas
- Documentar variações responsivas e tokens usados.