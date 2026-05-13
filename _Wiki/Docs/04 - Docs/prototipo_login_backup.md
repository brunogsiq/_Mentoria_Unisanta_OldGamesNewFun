# backup_prototipo_login.md

Este arquivo é um backup automático do `prototipo_login.md` antes de ser substituído.

-- Conteúdo original --

# prototipo_login.md

# Tela: Login

## Objetivo
Permitir acesso rápido e claro à plataforma.

## Componentes
- Área de branding
- Card de login
- Campo E-mail
- Campo Senha
- Botão Entrar
- Botão Criar conta
- Link Esqueci minha senha
- Card de dica

## Estrutura visual
Página Login
├── Logo / Texto de apoio
├── Card Login
│   ├── Título
│   ├── Campo E-mail
│   ├── Campo Senha
│   ├── Botão Entrar
│   └── Link/CTA
└── Card Dica

## CSS recomendado (pedaço)
```css
.login-card {
    width: 100%;
    max-width: 45rem; /* 720px */
    padding: 3rem; /* 48px */
    border-radius: var(--radius-lg);
    background: var(--color-surface);
}

.login-brand__title {
    font-size: 2.75rem;
    font-weight: 800;
}

.login-tip {
    max-width: 45rem; /* 720px */
    padding: 1.5rem 2rem; /* 24px 32px */
    background: #EAF2FF;
    border-radius: var(--radius-lg);
}
```

## Notas de acessibilidade
- Inputs com aria-label e aria-invalid.
- Foco visível usando :focus-visible.
