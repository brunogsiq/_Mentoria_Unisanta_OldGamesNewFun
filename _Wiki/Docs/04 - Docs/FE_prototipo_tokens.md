# prototipo_tokens.md

# Tokens e Design System

## Objetivo
Fornecer um arquivo central de tokens (cores, espaçamentos, raios, sombras) que pode ser importado ou consultado pelas telas.

## Tokens (CSS custom properties)
```css
:root {
  /* Cores */
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

  /* Espaçamentos escalares */
  --space-1: 0.5rem; /* 8px */
  --space-2: 1rem;   /* 16px */
  --space-3: 1.5rem; /* 24px */
  --space-4: 2rem;   /* 32px */

  /* Raios */
  --radius-sm: 0.5rem;  /* 8px */
  --radius-md: 0.75rem; /* 12px */
  --radius-lg: 1.25rem; /* 20px */

  /* Layout */
  --container-max: 75rem; /* 1200px */

  /* Sombras */
  --shadow-card: 0 0.25rem 0.75rem rgba(0,0,0,0.12);
}
```

## Tipografia (recomendação)
Use `html { font-size: 100%; }` e defina escalas relativas em `rem`.

```css
html { font-size: 1rem; }
body { font-family: Arial, Helvetica, sans-serif; font-size: 1.125rem; }
```

## Notas
- Mantenha apenas tokens reutilizáveis aqui; valores específicos de tela (ex.: largura do card de login) devem ficar nos arquivos de tela.