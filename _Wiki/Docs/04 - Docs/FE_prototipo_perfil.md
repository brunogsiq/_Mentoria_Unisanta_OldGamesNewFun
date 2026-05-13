# prototipo_profile.md

# Tela: Meu Perfil

## Objetivo
Exibir informações principais e atalhos de forma simples.

## Componentes
- Sidebar de perfil
- Avatar grande
- Dados principais (nome, e-mail)
- Cards de estatísticas
- Atalhos: editar dados, avatar, pagamento

## Estrutura visual
Sidebar (17.5rem) | Conteúdo principal (cards + ações)

## CSS recomendado
```css
.profile-page {
	display: grid;
	grid-template-columns: 17.5rem 1fr; /* 280px */
	min-height: 100vh;
}

.profile-avatar {
	width: 8.75rem; /* 140px */
	height: 8.75rem; /* 140px */
	border-radius: 50%;
}
```

## Notas
- Permitir edição inline com confirmação.
- Incluir dicas e acessibilidade em campos editáveis.