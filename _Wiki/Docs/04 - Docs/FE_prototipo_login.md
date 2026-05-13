# prototipo_login.md

# Tela: Login

## Objetivo
Arquivo renomeado a partir de `prototipo_tokens.md` — contém tokens e regras base usados pela tela de Login. Os tokens estão incluídos aqui para referência rápida; recomenda-se mover os tokens para um arquivo central `prototipo_tokens.md` (já presente) quando o time consolidar o design system.

## Tokens e referência rápida (temporário)
```css
:root {
  --color-primary: #062B55;
  --color-primary-dark: #031B36;
  --color-secondary: #FFD21F;
  --color-secondary-hover: #F2C300;

  --color-background: #F5F7FA;
  --color-surface: #FFFFFF;
  --color-border: #D8DEE8;

  --color-text-primary: #071B3A;
  --color-text-secondary: #4B5563;
  --color-text-light: #FFFFFF;

  --space-1: 0.5rem; /* 8px */
  --space-2: 1rem;   /* 16px */
  --space-3: 1.5rem; /* 24px */
  --space-4: 2rem;   /* 32px */

  --radius-sm: 0.5rem;  /* 8px */
  --radius-md: 0.75rem; /* 12px */
  --radius-lg: 1.25rem; /* 20px */

  --container-max: 75rem; /* 1200px */

  --shadow-card: 0 0.25rem 0.75rem rgba(0,0,0,0.12);
}
```

## Observações
- Este arquivo agora atende à tela de `Login` mas contém tokens para referência. Se preferir, posso: 1) extrair os tokens para um arquivo `prototipo_tokens.md` limpo e 2) manter `prototipo_login.md` apenas com a especificação da tela (Objetivo/Componentes/Exemplo CSS). Diga qual opção prefere.