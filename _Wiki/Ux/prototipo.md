Abaixo está a **documentação de componentização UI/UX** para você repassar à equipe de desenvolvimento. Não é implementação funcional ainda; é uma especificação visual para orientar o frontend.

---

# Old Games New FUN — Documentação de Componentes Visuais

## 1. Objetivo da interface

A plataforma será web, acessada principalmente por desktop, com foco em pessoas idosas. Portanto, todo componente deve priorizar:

Fonte grande, leitura fácil, botões amplos, alto contraste, poucos elementos por tela, navegação simples e feedback visual claro.

---

# 2. Design System Base

## 2.1 Cores principais

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

  --color-success: #22A447;
  --color-error: #D93025;
  --color-warning: #F59E0B;

  --shadow-card: 0 4px 12px rgba(0, 0, 0, 0.12);
  --radius-sm: 8px;
  --radius-md: 12px;
  --radius-lg: 20px;
}
```

---

## 2.2 Tipografia

```css
body {
  font-family: Arial, Helvetica, sans-serif;
  font-size: 18px;
  color: var(--color-text-primary);
  background: var(--color-background);
}

h1 {
  font-size: 40px;
  font-weight: 800;
}

h2 {
  font-size: 32px;
  font-weight: 700;
}

h3 {
  font-size: 24px;
  font-weight: 700;
}

p,
label,
button,
input {
  font-size: 18px;
}
```

Regra importante: nenhum texto principal deve ter menos de `18px`.

---

# 3. Componentes Globais

## 3.1 Header / Topbar

Usado em telas internas como Home, Jogos e Perfil.

### Função

Exibir identidade da plataforma, saudação do usuário e atalhos básicos.

### Deve conter

* Logo da plataforma
* Nome “Old Games New FUN”
* Saudação: “Olá, jogador!”
* Ícone de perfil
* Botão ou link de sair, quando aplicável

### CSS sugerido

```css
.app-header {
  width: 100%;
  height: 88px;
  background: var(--color-primary);
  color: var(--color-text-light);
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 40px;
  box-sizing: border-box;
}

.app-header__brand {
  display: flex;
  align-items: center;
  gap: 16px;
}

.app-header__logo {
  width: 56px;
  height: 56px;
}

.app-header__title {
  font-size: 28px;
  font-weight: 800;
}

.app-header__user {
  display: flex;
  align-items: center;
  gap: 16px;
  font-size: 20px;
}
```

---

## 3.2 Card Base

Usado para jogos, perfil, formulários e modais.

### Função

Criar blocos visuais com boa separação e leitura.

### CSS sugerido

```css
.card {
  background: var(--color-surface);
  border: 1px solid var(--color-border);
  border-radius: var(--radius-lg);
  box-shadow: var(--shadow-card);
  padding: 32px;
  box-sizing: border-box;
}
```

---

## 3.3 Botão Primário

Usado para ações principais: Entrar, Cadastrar, Salvar, Novo Jogo.

### CSS sugerido

```css
.btn-primary {
  min-height: 56px;
  padding: 0 32px;
  border: none;
  border-radius: var(--radius-md);
  background: var(--color-secondary);
  color: #000000;
  font-size: 20px;
  font-weight: 700;
  cursor: pointer;
}

.btn-primary:hover {
  background: var(--color-secondary-hover);
}

.btn-primary:focus {
  outline: 4px solid rgba(255, 210, 31, 0.45);
}
```

---

## 3.4 Botão Secundário

Usado para ações como Voltar, Criar conta, Cancelar.

```css
.btn-secondary {
  min-height: 56px;
  padding: 0 32px;
  border: 2px solid var(--color-primary);
  border-radius: var(--radius-md);
  background: var(--color-surface);
  color: var(--color-primary);
  font-size: 20px;
  font-weight: 700;
  cursor: pointer;
}
```

---

## 3.5 Botão de Perigo

Usado para sair da conta ou confirmar logout.

```css
.btn-danger {
  min-height: 56px;
  padding: 0 32px;
  border: none;
  border-radius: var(--radius-md);
  background: var(--color-error);
  color: var(--color-text-light);
  font-size: 20px;
  font-weight: 700;
  cursor: pointer;
}
```

---

## 3.6 Campo de Formulário

Usado em login, cadastro, dados pessoais e pagamento.

### Deve conter

* Label visível
* Ícone opcional
* Placeholder simples
* Estado de erro
* Mensagem de ajuda, quando necessário

```css
.form-field {
  display: flex;
  flex-direction: column;
  gap: 8px;
  margin-bottom: 20px;
}

.form-field label {
  font-size: 18px;
  font-weight: 700;
  color: var(--color-text-primary);
}

.form-input {
  height: 56px;
  border: 2px solid var(--color-border);
  border-radius: var(--radius-md);
  padding: 0 16px;
  font-size: 18px;
  color: var(--color-text-primary);
}

.form-input:focus {
  border-color: var(--color-primary);
  outline: 4px solid rgba(6, 43, 85, 0.18);
}

.form-error {
  color: var(--color-error);
  font-size: 16px;
  font-weight: 600;
}
```

---

# 4. Componentização por Tela

# 4.1 Tela de Login

## Objetivo

Permitir que o usuário acesse a plataforma de forma simples.

## Componentes da tela

1. Área de branding
2. Card de login
3. Campo de e-mail
4. Campo de senha
5. Botão Entrar
6. Separador “ou”
7. Botão Criar conta
8. Link Esqueci minha senha
9. Card de dica inferior

## Estrutura visual

```txt
Página Login
├── Logo Old Games New FUN
├── Texto de apoio
├── Card Login
│   ├── Título: Bem-vindo de volta!
│   ├── Campo E-mail
│   ├── Campo Senha
│   ├── Botão Entrar
│   ├── Separador "ou"
│   ├── Botão Criar conta
│   └── Link Esqueci minha senha
└── Card Dica
```

## CSS específico

```css
.login-page {
  min-height: 100vh;
  background: linear-gradient(180deg, var(--color-primary), var(--color-primary-dark));
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 32px;
  padding: 40px;
  box-sizing: border-box;
}

.login-brand {
  text-align: center;
  color: var(--color-text-light);
}

.login-brand__logo {
  width: 120px;
  margin-bottom: 16px;
}

.login-brand__title {
  font-size: 44px;
  font-weight: 800;
}

.login-brand__subtitle {
  font-size: 22px;
  margin-top: 8px;
}

.login-card {
  width: 100%;
  max-width: 720px;
  background: var(--color-surface);
  border-radius: var(--radius-lg);
  padding: 48px;
  box-shadow: var(--shadow-card);
}

.login-card__title {
  text-align: center;
  font-size: 36px;
  margin-bottom: 8px;
}

.login-card__subtitle {
  text-align: center;
  font-size: 22px;
  color: var(--color-text-secondary);
  margin-bottom: 32px;
}

.login-actions {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.login-divider {
  display: flex;
  align-items: center;
  gap: 16px;
  color: var(--color-text-secondary);
  font-weight: 700;
}

.login-divider::before,
.login-divider::after {
  content: "";
  flex: 1;
  height: 1px;
  background: var(--color-border);
}

.login-forgot-password {
  text-align: center;
  font-size: 20px;
  font-weight: 700;
  color: var(--color-primary);
  text-decoration: underline;
}

.login-tip {
  width: 100%;
  max-width: 720px;
  background: #EAF2FF;
  border-radius: var(--radius-lg);
  padding: 24px 32px;
  font-size: 20px;
  color: var(--color-primary);
  display: flex;
  align-items: center;
  gap: 16px;
}
```

---

# 4.2 Tela de Cadastro

## Objetivo

Permitir criação de conta com poucos campos e linguagem simples.

## Componentes

1. Logo lateral ou superior
2. Card de cadastro
3. Campo Nome completo
4. Campo E-mail
5. Campo Senha
6. Campo Confirmar senha
7. Botão Cadastrar
8. Link “Já tenho uma conta”

## CSS específico

```css
.signup-page {
  min-height: 100vh;
  background: var(--color-background);
  display: grid;
  grid-template-columns: 40% 60%;
}

.signup-brand-panel {
  background: var(--color-primary);
  color: var(--color-text-light);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 24px;
  padding: 48px;
}

.signup-content {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 48px;
}

.signup-card {
  width: 100%;
  max-width: 640px;
  background: var(--color-surface);
  border-radius: var(--radius-lg);
  padding: 48px;
  box-shadow: var(--shadow-card);
}
```

---

# 4.3 Tela Esqueci Senha

## Objetivo

Permitir recuperação de senha por e-mail.

## Componentes

1. Logo
2. Título “Esqueci minha senha”
3. Texto explicativo simples
4. Campo E-mail
5. Botão Enviar instruções
6. Link Voltar para login

## CSS específico

```css
.forgot-page {
  min-height: 100vh;
  background: var(--color-background);
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 40px;
}

.forgot-card {
  width: 100%;
  max-width: 560px;
  background: var(--color-surface);
  border-radius: var(--radius-lg);
  padding: 48px;
  box-shadow: var(--shadow-card);
  text-align: center;
}

.forgot-card__description {
  font-size: 20px;
  color: var(--color-text-secondary);
  margin-bottom: 32px;
}
```

---

# 4.4 Tela Home — Seleção de Jogos

## Objetivo

Permitir que o usuário escolha rapidamente um jogo.

## Componentes

1. Header
2. Título “Escolha um jogo para jogar”
3. Grid de cards de jogos
4. Botão Meu Perfil
5. Botão Sair

## Card de jogo

Cada card deve conter:

* Ícone grande
* Nome do jogo
* Área clicável ampla

## CSS específico

```css
.home-page {
  min-height: 100vh;
  background: var(--color-background);
}

.home-content {
  padding: 40px;
}

.home-title {
  font-size: 36px;
  margin-bottom: 32px;
}

.games-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 24px;
}

.game-card {
  min-height: 180px;
  background: var(--color-surface);
  border: 2px solid var(--color-border);
  border-radius: var(--radius-lg);
  box-shadow: var(--shadow-card);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 16px;
  cursor: pointer;
}

.game-card:hover {
  border-color: var(--color-secondary);
  transform: translateY(-2px);
}

.game-card__icon {
  font-size: 64px;
}

.game-card__title {
  font-size: 22px;
  font-weight: 800;
}
```

---

# 4.5 Tela Base de Jogo

Essa estrutura deve ser reaproveitada para todos os jogos.

## Componentes

1. Header do jogo
2. Botão Voltar
3. Título do jogo
4. Área principal do jogo
5. Painel lateral de status
6. Botões de ação
7. Área de dica/instrução

## CSS específico

```css
.game-page {
  min-height: 100vh;
  background: var(--color-background);
}

.game-header {
  height: 72px;
  background: var(--color-primary);
  color: var(--color-text-light);
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 32px;
}

.game-layout {
  display: grid;
  grid-template-columns: 1fr 320px;
  gap: 32px;
  padding: 40px;
}

.game-board-area {
  background: var(--color-surface);
  border-radius: var(--radius-lg);
  padding: 32px;
  box-shadow: var(--shadow-card);
  min-height: 520px;
}

.game-side-panel {
  background: var(--color-surface);
  border-radius: var(--radius-lg);
  padding: 24px;
  box-shadow: var(--shadow-card);
}

.game-tip {
  margin-top: 24px;
  background: #EAF2FF;
  border-radius: var(--radius-md);
  padding: 20px;
  font-size: 20px;
  color: var(--color-primary);
}
```

---

# 4.6 Jogo da Velha

## Componentes específicos

1. Tabuleiro 3x3
2. Indicador “Sua vez”
3. Placar
4. Botão Reiniciar
5. Botão Voltar

## CSS

```css
.tic-tac-toe-board {
  width: 420px;
  height: 420px;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  border: 3px solid var(--color-primary);
}

.tic-tac-toe-cell {
  border: 2px solid var(--color-border);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 72px;
  font-weight: 800;
  cursor: pointer;
}

.tic-tac-toe-status {
  font-size: 28px;
  font-weight: 800;
  color: var(--color-success);
}
```

---

# 4.7 Forca

## Componentes

1. Desenho da forca
2. Palavra oculta
3. Letras disponíveis
4. Letras erradas
5. Vidas restantes
6. Botão Dica
7. Botão Voltar

## CSS

```css
.hangman-layout {
  display: grid;
  grid-template-columns: 360px 1fr;
  gap: 32px;
}

.hangman-drawing {
  min-height: 360px;
  border: 2px solid var(--color-border);
  border-radius: var(--radius-lg);
}

.hangman-word {
  font-size: 40px;
  letter-spacing: 12px;
  font-weight: 800;
  text-align: center;
}

.hangman-keyboard {
  display: grid;
  grid-template-columns: repeat(9, 1fr);
  gap: 10px;
}

.hangman-letter {
  height: 48px;
  font-size: 20px;
  font-weight: 700;
  border-radius: var(--radius-sm);
}
```

---

# 4.8 Damas / Xadrez

## Componentes

1. Tabuleiro 8x8
2. Peças
3. Botão Novo jogo
4. Botão Voltar
5. Área de status

## CSS

```css
.board-8x8 {
  width: 560px;
  height: 560px;
  display: grid;
  grid-template-columns: repeat(8, 1fr);
  border: 4px solid var(--color-primary);
}

.board-cell {
  display: flex;
  align-items: center;
  justify-content: center;
}

.board-cell--light {
  background: #F3D9A4;
}

.board-cell--dark {
  background: #9A6A3A;
}

.board-piece {
  width: 52px;
  height: 52px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 34px;
}
```

---

# 4.9 Cobrinha

## Componentes

1. Área de jogo
2. Pontuação
3. Nível
4. Botão Pausar
5. Botão Voltar

## CSS

```css
.snake-board {
  width: 520px;
  height: 520px;
  background: #EDF7EC;
  border: 3px solid var(--color-primary);
  border-radius: var(--radius-md);
  position: relative;
}

.snake-score-card {
  background: var(--color-surface);
  border-radius: var(--radius-md);
  padding: 24px;
  text-align: center;
  border: 1px solid var(--color-border);
}

.snake-score-card strong {
  font-size: 36px;
}
```

---

# 4.10 Candy Crush Simplificado

## Componentes

1. Grid de doces
2. Pontos
3. Nível
4. Movimentos restantes
5. Botão Reiniciar
6. Botão Voltar

## CSS

```css
.candy-board {
  width: 520px;
  height: 520px;
  display: grid;
  grid-template-columns: repeat(8, 1fr);
  gap: 8px;
  background: #EAF2FF;
  padding: 16px;
  border-radius: var(--radius-lg);
}

.candy-item {
  border-radius: 50%;
  font-size: 34px;
  display: flex;
  align-items: center;
  justify-content: center;
}
```

---

# 4.11 Paciência / Spider Solitaire

## Componentes

1. Área de cartas
2. Pilhas de cartas
3. Botão Novo jogo
4. Botão Voltar

## CSS

```css
.card-game-table {
  min-height: 560px;
  background: #0E6B3A;
  border-radius: var(--radius-lg);
  padding: 24px;
}

.playing-card {
  width: 88px;
  height: 128px;
  background: white;
  border: 1px solid var(--color-border);
  border-radius: var(--radius-sm);
  box-shadow: 0 2px 6px rgba(0,0,0,0.18);
}
```

---

# 4.12 Meu Perfil — Visão Geral

## Objetivo

Exibir informações principais e atalhos do perfil.

## Componentes

1. Sidebar de perfil
2. Avatar
3. Nome do usuário
4. E-mail
5. Cards de estatísticas
6. Atalhos: Dados pessoais, Avatar, Pagamento
7. Botão Voltar para Home

## CSS

```css
.profile-page {
  min-height: 100vh;
  display: grid;
  grid-template-columns: 280px 1fr;
  background: var(--color-background);
}

.profile-sidebar {
  background: var(--color-primary);
  color: var(--color-text-light);
  padding: 32px 24px;
}

.profile-content {
  padding: 40px;
}

.profile-avatar {
  width: 140px;
  height: 140px;
  border-radius: 50%;
  background: #DDEBFF;
  object-fit: cover;
}

.profile-stats {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
  margin-top: 32px;
}

.profile-stat-card {
  background: var(--color-surface);
  border-radius: var(--radius-md);
  padding: 24px;
  text-align: center;
  box-shadow: var(--shadow-card);
}
```

---

# 4.13 Editar Dados Pessoais

## Componentes

1. Sidebar
2. Formulário de dados pessoais
3. Campos: Nome, E-mail, Data de nascimento, Telefone
4. Botão Salvar alterações
5. Botão Voltar

## CSS

```css
.profile-form {
  max-width: 720px;
  background: var(--color-surface);
  border-radius: var(--radius-lg);
  padding: 40px;
  box-shadow: var(--shadow-card);
}

.profile-form__actions {
  display: flex;
  gap: 20px;
  margin-top: 32px;
}
```

---

# 4.14 Alterar Avatar

## Componentes

1. Avatar atual
2. Lista de avatares
3. Botão Salvar
4. Botão Voltar

## CSS

```css
.avatar-selector {
  display: flex;
  align-items: center;
  gap: 24px;
  margin: 32px 0;
}

.avatar-option {
  width: 96px;
  height: 96px;
  border-radius: 50%;
  border: 3px solid transparent;
  cursor: pointer;
}

.avatar-option--selected {
  border-color: var(--color-secondary);
}
```

---

# 4.15 Dados de Pagamento

## Componentes

1. Sidebar
2. Formulário de cartão
3. Nome do titular
4. Número do cartão mascarado
5. Validade
6. CVC
7. Botão Salvar alterações

## CSS

```css
.payment-form {
  max-width: 720px;
  background: var(--color-surface);
  border-radius: var(--radius-lg);
  padding: 40px;
  box-shadow: var(--shadow-card);
}

.payment-row {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 20px;
}
```

---

# 4.16 Modal de Logout

## Objetivo

Confirmar se o usuário deseja sair.

## Componentes

1. Fundo escurecido
2. Caixa modal
3. Ícone de saída
4. Título “Sair da conta?”
5. Texto “Tem certeza que deseja sair?”
6. Botão Cancelar
7. Botão Sair

## CSS

```css
.modal-overlay {
  position: fixed;
  inset: 0;
  background: rgba(0, 0, 0, 0.55);
  display: flex;
  align-items: center;
  justify-content: center;
}

.logout-modal {
  width: 100%;
  max-width: 480px;
  background: var(--color-surface);
  border-radius: var(--radius-lg);
  padding: 40px;
  text-align: center;
  box-shadow: var(--shadow-card);
}

.logout-modal__title {
  font-size: 32px;
  margin-bottom: 12px;
}

.logout-modal__actions {
  display: flex;
  gap: 20px;
  margin-top: 32px;
}
```

---

# 5. Regras Gerais para a Equipe

A equipe deve seguir estas decisões:

1. A plataforma é web desktop-first.
2. Todo botão deve ter altura mínima de `56px`.
3. Nenhum texto importante deve ter menos de `18px`.
4. As telas devem usar alto contraste.
5. Não usar menus escondidos como única forma de navegação.
6. Sempre existir botão “Voltar” em telas internas.
7. Jogos devem ter área visual grande.
8. Cada tela deve ser componentizada para reaproveitamento.
9. CSS deve ser organizado por responsabilidade:

   * `base.css`
   * `tokens.css`
   * `buttons.css`
   * `forms.css`
   * `cards.css`
   * `layout.css`
   * `games.css`
   * `profile.css`
   * `modal.css`

---