# Old Games New FUN — Documentação Consolidada do Chat

> Documento criado para preservar integralmente as decisões, requisitos, protótipos, backlog, diretrizes de UI/UX e especificações de componentização discutidas neste chat antes de sua exclusão.

---

# 1. Identificação do Projeto

## Nome

**Old Games New FUN**

## Tipo de Produto

Plataforma web de jogos clássicos/antigos com foco principal em pessoas da terceira idade.

## Objetivo Principal

Criar uma plataforma simples, acessível e agradável para que pessoas idosas consigam acessar jogos clássicos por meio de navegador web em computadores desktop e notebooks, com baixa barreira de uso e mínima complexidade de navegação.

## Público-Alvo

O produto é direcionado principalmente a:

- Pessoas idosas;
- Usuários com pouca familiaridade com tecnologia;
- Usuários que podem apresentar dificuldades visuais ou motoras;
- Pessoas que precisam de interfaces claras, previsíveis e com poucos elementos simultâneos;
- Usuários que desejam entretenimento simples por meio de jogos clássicos.

## Plataforma-Alvo

A decisão consolidada neste chat é:

- Produto web;
- Uso prioritário em desktop;
- Navegação por navegador;
- Protótipos e telas devem seguir padrão de portal web;
- Não desenhar as telas como aplicativo mobile;
- O desktop é a referência principal de UI/UX neste estágio;
- Código só deverá ser produzido quando for solicitado explicitamente em etapa posterior.

---

# 2. Contexto Inicial

O projeto começou com um backlog organizado em quadro Kanban, separando atividades de Frontend (FE) e Backend for Frontend (BFF).

O objetivo do backlog é estruturar as funcionalidades necessárias para a plataforma e orientar posteriormente o desenvolvimento.

O backlog apresentado incluía as seguintes tarefas.

---

# 3. Backlog Original Identificado

## 3.1 Autenticação

- FE - Tela Cadastro
- BFF - Tela Cadastro
- FE - Tela Login
- BFF - Tela Login
- FE - Tela Esqueceu a senha
- BFF - Tela Esqueceu a senha

## 3.2 Perfil

- FE - Tela Meu Perfil
- BFF - Tela Meu Perfil
- FE - Tela Meu Perfil - Seção Meu Avatar
- BFF - Tela Meu Perfil - Seção Meu Avatar
- FE - Tela Meu Perfil - Seção Dados Pessoais
- BFF - Tela Meu Perfil - Seção Dados Pessoais
- FE - Tela Meu Perfil - Seção Dados de Pagamento
- BFF - Tela Meu Perfil - Seção Dados de Pagamento

## 3.3 Jogos

- FE - Tela Jogos - Forca
- BFF - Tela Jogos - Forca
- FE - Tela Jogos - Velha
- BFF - Tela Jogos - Velha
- FE - Tela Jogos - Xadrez
- BFF - Tela Jogos - Xadrez
- FE - Tela Jogos - Dama
- BFF - Tela Jogos - Dama
- FE - Tela Jogos - Cobrinha
- BFF - Tela Jogos - Cobrinha
- FE - Tela Jogos - Clone Candy Crush
- BFF - Tela Jogos - Clone Candy Crush
- FE - Tela Jogos - Paciência
- BFF - Tela Jogos - Paciência
- FE - Tela Jogos - Spider
- BFF - Tela Jogos - Spider

## 3.4 Sistema

- FE - Tela sair
- BFF - Tela sair

---

# 4. Prompt Criado para o GitHub Copilot

Foi solicitado um prompt em inglês para explicar ao GitHub Copilot a criação dos protótipos visuais.

O prompt consolidado foi:

```text
Create visual prototypes (wireframes) for a web platform called "Old Games New FUN", focused on elderly users.

The screens must be simple, accessible, and include:
- Large buttons
- Large fonts
- High contrast
- Clean and intuitive layout

Create the following screens:

1. Login
2. Sign Up
3. Home with game selection
4. Game screen (e.g., Tic Tac Toe)
5. User Profile

Rules:
- Extremely simple UX
- Avoid excessive elements
- User-friendly interface for people with low digital familiarity
- Centered layout
- Large and clear icons

Style:
- Minimalist
- Modern
- Accessible

Return the wireframes in visual format or structured for frontend development.
```

Observação importante:

- A plataforma será utilizada em **Português do Brasil (pt-BR)**.
- Portanto, apesar de o prompt ao Copilot ter sido solicitado em inglês, os textos visíveis no produto devem estar em português brasileiro.

---

# 5. Decisão de Etapa: Primeiro UI/UX, Depois Código

Durante a conversa foi esclarecido que, nesta fase:

- Não deverá ser gerado código de frontend;
- Não deverá ser produzido HTML;
- Não deverá ser produzido CSS funcional como implementação final;
- Não deverá ser desenvolvida lógica;
- Não deverá ser criada navegação funcional;
- Não deverá ser implementado BFF;
- Não deverão ser implementados jogos.

O foco atual é:

**Criar protótipos visuais, documentação de componentes, design system e especificações de UI/UX para orientar a equipe de desenvolvimento.**

O código será solicitado posteriormente pelo usuário em momento específico.

---

# 6. Direção Visual Inicial

A identidade visual construída nas primeiras referências apresentou:

- Azul-marinho/azul escuro como cor principal;
- Amarelo/dourado como cor de destaque;
- Branco como superfície principal;
- Vermelho para ação de saída;
- Verde para feedback positivo em jogos;
- Ícones grandes;
- Botões arredondados;
- Cards com cantos arredondados;
- Interface amigável;
- Uso de ícones visuais ligados a jogos;
- Logo com controle de videogame amarelo;
- Nome “OLD GAMES NEW FUN” com destaque de “NEW FUN” em amarelo.

---

# 7. Diretrizes Fundamentais de UX

A interface foi planejada especificamente para idosos.

As seguintes regras devem ser consideradas obrigatórias como direção de UX.

## 7.1 Simplicidade

A interface deve ser entendida rapidamente.

Evitar:

- Excesso de informação;
- Menus complexos;
- Elementos escondidos;
- Ícones sem identificação;
- Fluxos com muitas etapas;
- Termos técnicos.

## 7.2 Legibilidade

- Fontes grandes;
- Textos de leitura fácil;
- Alto contraste;
- Hierarquia visual clara;
- Espaçamento adequado entre informações.

## 7.3 Interação

- Botões grandes;
- Áreas clicáveis amplas;
- Espaçamento entre controles;
- Feedback visual claro;
- Evitar elementos pequenos;
- Evitar ações dependentes de precisão do mouse.

## 7.4 Navegação

- Sempre fornecer caminho de retorno;
- Botão “Voltar” deve ser facilmente encontrado;
- Fluxo de navegação deve ser previsível;
- A Home deve funcionar como principal ponto de acesso aos jogos.

## 7.5 Carga Cognitiva

Evitar apresentar várias decisões simultaneamente.

Cada tela deve possuir:

- Um objetivo principal;
- Uma ação principal claramente destacada;
- Poucas ações secundárias.

## 7.6 Feedback

O usuário deve receber respostas visuais claras para:

- Sucesso;
- Erro;
- Seleção;
- Vitória;
- Derrota;
- Empate;
- Pausa;
- Reinício;
- Saída.

---

# 8. Mapa Consolidado de Telas

A lista consolidada discutida no chat contém **17 telas/experiências visuais**.

## 8.1 Autenticação

### 01. Tela de Login

Objetivo: permitir que o usuário acesse a plataforma.

### 02. Tela de Cadastro

Objetivo: permitir criação de uma nova conta.

### 03. Tela Esqueci Minha Senha

Objetivo: permitir recuperação de acesso por e-mail.

## 8.2 Home

### 04. Tela Home — Seleção de Jogos

Objetivo: ser o centro principal da plataforma e permitir seleção rápida de um jogo.

## 8.3 Jogos

Cada jogo possui uma tela própria.

### 05. Jogo da Velha
### 06. Forca
### 07. Damas
### 08. Xadrez
### 09. Cobrinha
### 10. Candy Crush Simplificado
### 11. Paciência
### 12. Spider Solitaire

## 8.4 Perfil

### 13. Meu Perfil — Visão Geral
### 14. Editar Dados Pessoais
### 15. Alterar Avatar
### 16. Dados de Pagamento

## 8.5 Sistema

### 17. Logout — Ação/Modal de Confirmação

---

# 9. Protótipo Inicial de Login

O primeiro protótipo individual criado foi a tela de Login.

A proposta visual apresentou:

- Fundo azul escuro;
- Logo no topo;
- Controle de videogame amarelo;
- Nome “OLD GAMES NEW FUN”;
- Frase de apoio: “Reviva grandes jogos. Divirta-se sempre!”;
- Card branco central;
- Título: “Bem-vindo de volta!”;
- Subtítulo: “Entre para continuar jogando.”;
- Campo E-mail;
- Campo Senha;
- Ícone para visualizar senha;
- Botão amarelo “Entrar”;
- Separador “ou”;
- Botão secundário “Criar conta”;
- Link “Esqueci minha senha”;
- Card inferior de dica: “Dica: Não se preocupe, é fácil e rápido!”

Posteriormente foi esclarecido que todos os protótipos devem refletir **layout de portal web desktop**, e não interface mobile.

---

# 10. Protótipo Geral do Portal Desktop

Foi criado um segundo protótipo geral consolidando as 17 telas em um mapa visual desktop.

Esse protótipo organizou autenticação, Home, jogos, perfil e logout e passou a representar a direção visual desktop do portal.

---

# 11. Design System Proposto

Foi criada uma primeira especificação de design system. Ela deverá orientar a equipe, mas poderá ser refinada durante a implementação sem romper a identidade visual.

---

# 12. Tokens de Cor

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

# 13. Tipografia

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

Regra consolidada: textos importantes não devem utilizar tamanho inferior a **18px**.

---

# 14. Componentes Globais

## 14.1 Header / Topbar

### Objetivo

Fornecer identidade e navegação consistente nas telas internas.

### Elementos possíveis

- Logo;
- Nome da plataforma;
- Saudação;
- Ícone ou acesso ao perfil;
- Ação de saída quando aplicável.

### CSS de referência

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

## 14.2 Card Base

### Uso

- Jogos;
- Formulários;
- Painéis;
- Perfil;
- Modais;
- Informações auxiliares.

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

## 14.3 Botão Primário

### Uso

- Entrar;
- Cadastrar;
- Salvar;
- Novo jogo;
- Reiniciar quando for a ação principal.

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

## 14.4 Botão Secundário

### Uso

- Voltar;
- Cancelar;
- Criar conta;
- Ações auxiliares.

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

## 14.5 Botão de Perigo

### Uso

- Logout;
- Ações destrutivas futuras.

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

## 14.6 Campo de Formulário

Cada campo deverá possuir label visível, campo de entrada, ícone quando útil, estado de foco, estado de erro e mensagem de ajuda quando necessário.

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

# 15. Tela 01 — Login

## Objetivo

Permitir que o usuário entre na plataforma com mínimo esforço cognitivo.

## Componentes

### Branding

- Logo;
- Nome “Old Games New FUN”;
- Texto de apoio.

### Card de Login

- Título “Bem-vindo de volta!”;
- Subtítulo “Entre para continuar jogando.”;
- Campo E-mail;
- Campo Senha;
- Ícone para visualizar senha.

### Ações

- Entrar;
- Criar conta;
- Esqueci minha senha.

### Elemento de apoio

Card de dica amigável.

## Hierarquia

```text
Página Login
├── Logo Old Games New FUN
├── Texto de apoio
├── Card Login
│   ├── Título
│   ├── Subtítulo
│   ├── Campo E-mail
│   ├── Campo Senha
│   ├── Botão Entrar
│   ├── Separador "ou"
│   ├── Botão Criar conta
│   └── Link Esqueci minha senha
└── Card Dica
```

## CSS de referência

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

# 16. Tela 02 — Cadastro

## Objetivo

Permitir criação de uma conta com poucos campos e linguagem simples.

## Componentes

- Logo;
- Painel visual de branding;
- Card de cadastro;
- Campo Nome completo;
- Campo E-mail;
- Campo Senha;
- Campo Confirmar senha;
- Botão Cadastrar;
- Ação para retornar ao Login.

## CSS de referência

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

# 17. Tela 03 — Esqueci Minha Senha

## Objetivo

Permitir que o usuário solicite instruções de recuperação de senha.

## Componentes

- Logo;
- Título “Esqueci minha senha”;
- Texto explicativo simples;
- Campo E-mail;
- Botão “Enviar instruções”;
- Link “Voltar para o login”.

## CSS de referência

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

# 18. Tela 04 — Home / Seleção de Jogos

## Objetivo

Permitir que o usuário escolha um jogo de forma extremamente simples.

## Componentes

### Header

- Logo;
- Nome da plataforma;
- Saudação;
- Perfil.

### Conteúdo principal

Título: **Escolha um jogo para jogar**

### Grid de Jogos

- Jogo da Velha;
- Forca;
- Damas;
- Xadrez;
- Cobrinha;
- Candy Crush;
- Paciência;
- Spider Solitaire.

### Ações adicionais

- Meu Perfil;
- Sair.

## Card de Jogo

Cada card deve possuir ícone grande, nome do jogo, área inteira clicável, alto contraste e feedback de hover/foco.

## CSS de referência

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

# 19. Estrutura Base das Telas de Jogos

Uma estrutura reaproveitável deverá servir como base para os jogos.

## Componentes comuns

- Header do jogo;
- Título;
- Botão Voltar;
- Área principal;
- Painel lateral quando necessário;
- Status;
- Pontuação quando aplicável;
- Botões de ação;
- Área de dica/instrução.

## CSS de referência

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

# 20. Tela 05 — Jogo da Velha

## Componentes

- Tabuleiro 3x3;
- Indicador de turno;
- Placar;
- Botão Reiniciar;
- Botão Voltar;
- Área de dica.

## Estados visuais previstos

- Sua vez;
- Vitória;
- Derrota;
- Empate.

## CSS de referência

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

# 21. Tela 06 — Forca

## Componentes

- Desenho da forca;
- Palavra oculta;
- Letras disponíveis;
- Letras erradas;
- Vidas restantes;
- Botão Dica;
- Botão Voltar.

## CSS de referência

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

# 22. Tela 07 — Damas

## Componentes

- Tabuleiro 8x8;
- Peças;
- Indicador de status;
- Botão Novo jogo;
- Botão Voltar.

## Observação

O protótipo inicial mostrou peças vermelhas e escuras, porém a definição final de estilo e cores das peças pode ser refinada pela equipe visual.

---

# 23. Tela 08 — Xadrez

## Componentes

- Tabuleiro 8x8;
- Conjunto completo de peças;
- Indicador de turno/status;
- Botão Novo jogo;
- Botão Voltar.

---

# 24. CSS Compartilhado para Damas e Xadrez

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

# 25. Tela 09 — Cobrinha

## Componentes

- Área principal do jogo;
- Cobrinha;
- Alimento;
- Pontuação;
- Nível;
- Botão Pausar;
- Botão Voltar.

## CSS de referência

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

# 26. Tela 10 — Candy Crush Simplificado

## Componentes

- Grid de doces;
- Pontos;
- Nível;
- Movimentos restantes;
- Botão Reiniciar;
- Botão Voltar.

## CSS de referência

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

# 27. Tela 11 — Paciência

## Componentes

- Mesa;
- Baralho;
- Colunas de cartas;
- Pilhas de destino;
- Botão Novo jogo;
- Botão Voltar.

---

# 28. Tela 12 — Spider Solitaire

## Componentes

- Mesa;
- Colunas de cartas;
- Área de novas cartas;
- Botão Novo jogo;
- Botão Voltar.

---

# 29. CSS Compartilhado para Jogos de Cartas

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

# 30. Tela 13 — Meu Perfil

## Objetivo

Centralizar informações e configurações do usuário.

## Componentes

### Navegação lateral

- Meu Perfil;
- Dados Pessoais;
- Alterar Avatar;
- Pagamento.

### Informações

- Avatar;
- Nome;
- E-mail.

### Estatísticas

O protótipo utilizou exemplos de cards como jogos jogados, conquistas e partidas.

**Atenção:** esses nomes são referências visuais e devem ser validados antes da implementação funcional, pois não foram definidos como regras de negócio no backlog inicial.

### Ação

- Voltar para Home.

## CSS de referência

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

# 31. Tela 14 — Editar Dados Pessoais

## Componentes utilizados no protótipo

- Nome completo;
- E-mail;
- Data de nascimento;
- Telefone;
- Botão Salvar alterações;
- Navegação lateral;
- Voltar.

## Observação anti-alucinação

Esses campos foram utilizados como proposta de UI.

O backlog inicial apenas indicava uma seção de **Dados Pessoais**, sem detalhar formalmente quais campos seriam obrigatórios.

Portanto, antes da implementação de regras funcionais, a equipe deverá validar quais dados pessoais realmente fazem parte do escopo.

## CSS de referência

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

# 32. Tela 15 — Alterar Avatar

## Componentes

- Avatar atual;
- Lista de avatares disponíveis;
- Estado visual selecionado;
- Botão Salvar;
- Voltar;
- Navegação lateral.

## CSS de referência

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

# 33. Tela 16 — Dados de Pagamento

## Componentes utilizados como proposta visual

- Titular do cartão;
- Número do cartão;
- Validade;
- CVC;
- Botão Salvar alterações;
- Navegação lateral.

## Observação importante

O backlog indica existência de uma seção de pagamento.

Entretanto, regras como forma de cobrança, gateway, bandeiras aceitas, validação do cartão, tokenização, armazenamento, assinatura, valor ou plano **não foram definidas neste chat**.

Portanto, não devem ser assumidas pela equipe.

## CSS de referência

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

# 34. Tela 17 — Logout

## Objetivo

Solicitar confirmação antes de encerrar a sessão.

## Componentes

- Overlay;
- Card/modal central;
- Ícone de saída;
- Título “Sair da conta?”;
- Mensagem “Tem certeza que deseja sair?”;
- Botão Cancelar;
- Botão Sair.

## CSS de referência

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

# 35. Estrutura CSS Recomendada

```text
css/
├── tokens.css
├── base.css
├── layout.css
├── cards.css
├── buttons.css
├── forms.css
├── games.css
├── profile.css
├── modal.css
└── responsive.css
```

## Responsabilidades

### tokens.css

Variáveis globais de cores, radius, sombras, espaçamentos e tipografia.

### base.css

Reset, body, tipografia e regras globais.

### layout.css

Containers, headers, grids e estruturas gerais.

### cards.css

Cards reutilizáveis.

### buttons.css

Todos os tipos de botão.

### forms.css

Campos, labels, mensagens e estados de formulário.

### games.css

Componentes visuais dos jogos.

### profile.css

Sidebar e elementos do perfil.

### modal.css

Modais e overlays.

### responsive.css

Adaptações de resolução, mesmo que desktop seja o foco principal.

---

# 36. Regras Gerais para a Equipe de Desenvolvimento

1. A plataforma é web.
2. A experiência principal é desktop.
3. Protótipos devem parecer portais web, não apps mobile.
4. Português do Brasil será o idioma do produto.
5. O público principal é idoso.
6. O design deve privilegiar acessibilidade.
7. Botões devem ser grandes.
8. Foi adotada altura mínima de referência de 56px para botões principais.
9. Textos importantes devem possuir pelo menos 18px.
10. O contraste deve ser elevado.
11. O azul escuro é a identidade principal.
12. O amarelo é a cor de ação/destaque.
13. Branco é usado como principal superfície.
14. Vermelho é reservado principalmente para ações críticas.
15. Verde pode ser utilizado em feedback positivo.
16. O usuário não deve depender apenas de ícones.
17. Ícones devem ser acompanhados de texto quando sua interpretação puder gerar dúvida.
18. Não esconder as principais opções de navegação.
19. Evitar menus excessivamente complexos.
20. Deve existir ação de retorno facilmente identificável em telas internas.
21. Cards de jogos devem possuir área clicável grande.
22. Os jogos devem utilizar grande parte da área útil disponível.
23. A Home será a principal tela de acesso aos jogos.
24. Componentes visuais devem ser reaproveitáveis.
25. A equipe deve manter separação entre estrutura visual e regras de negócio.
26. Informações presentes apenas nos protótipos não devem automaticamente se tornar regras funcionais.

---

# 37. Cuidados de Acessibilidade

Embora ainda não tenha sido definido um documento formal de WCAG, o projeto deve considerar:

- Contraste adequado;
- Navegação por teclado;
- Estado de foco visível;
- Texto de fácil leitura;
- Áreas clicáveis grandes;
- Feedback de erro próximo ao campo;
- Labels reais para formulários;
- Não usar somente cor para comunicar estado;
- Evitar animações excessivas;
- Evitar mudanças bruscas;
- Evitar conteúdo piscante;
- Não depender apenas de hover;
- Utilizar linguagem direta.

---

# 38. Primeira Fase de Implementação Visual Recomendada

Foi sugerido iniciar por:

1. Login;
2. Cadastro;
3. Esqueci Senha;
4. Home;
5. Tela Base de Jogos;
6. Meu Perfil;
7. Logout.

## Escopo desta fase

Apenas:

- UI;
- UX;
- Componentização;
- Layout;
- Design visual;
- CSS;
- Estados visuais necessários para apresentação.

## Fora do escopo desta primeira fase

- Backend;
- BFF;
- Banco de dados;
- Integração;
- Regras de autenticação;
- Lógica dos jogos;
- Sistema de pagamento real;
- Persistência;
- Ranking;
- Multiplayer;
- Monetização;
- API externa.

---

# 39. Pontos que Devem Ser Validados Antes da Implementação Funcional

## Autenticação

- Login será apenas com e-mail ou também usuário?
- Haverá login social?
- Existirá modo convidado?
- Como funcionará recuperação de senha?
- Haverá verificação de e-mail?

## Cadastro

- Quais campos serão obrigatórios?
- Existirá data de nascimento?
- Telefone será solicitado?
- Há termos de uso?
- Política de privacidade?

## Perfil

- Quais dados pessoais serão realmente armazenados?
- Estatísticas de jogos existirão?
- Quais estatísticas?
- Haverá conquistas?
- Haverá histórico de partidas?

## Avatar

- Avatares serão fixos?
- Upload de foto será permitido?
- Haverá personalização?

## Pagamento

- Qual é o modelo de monetização?
- Assinatura?
- Compra única?
- Gratuito?
- Qual gateway?
- Dados de cartão serão armazenados ou tokenizados?

## Jogos

- Serão contra computador?
- Multiplayer?
- Local?
- Online?
- Dificuldades?
- Salvar partida?
- Ranking?
- Pontuação?

## Cobrinha

- Controle por teclado?
- Setas?
- WASD?
- Controle visual?

## Candy Crush

- Quantidade de linhas/colunas?
- Número de movimentos?
- Sistema de nível?
- Objetivos?

## Paciência e Spider

- Regras exatas das variantes?
- Dificuldade?
- Quantidade de naipes no Spider?
- Função de dica?
- Desfazer jogada?

---

# 40. Decisões Que Não Devem Ser Interpretadas como Regras de Negócio

Alguns elementos apareceram nos protótipos apenas para tornar a representação visual compreensível.

Eles não devem ser considerados requisitos funcionais definitivos sem validação.

Exemplos:

- Nome fictício “João”;
- Nome “João da Silva”;
- E-mail fictício;
- Número de jogos jogados;
- Número de conquistas;
- Número de partidas;
- Dificuldade “Fácil” no Jogo da Velha;
- Pontuações fictícias;
- Níveis fictícios;
- Quantidade de movimentos;
- Dados fictícios de cartão;
- Data de nascimento;
- Telefone;
- Sistema de vidas na Forca;
- Botão de dica;
- Feedback específico de cada jogo.

Esses elementos são referências de UI/UX e não regras aprovadas.

---

# 41. Direção Recomendada para Continuidade

A continuidade ideal do projeto é construir cada protótipo individualmente.

Ordem sugerida:

1. Login;
2. Cadastro;
3. Esqueci Senha;
4. Home;
5. Jogo da Velha;
6. Forca;
7. Damas;
8. Xadrez;
9. Cobrinha;
10. Candy Crush Simplificado;
11. Paciência;
12. Spider Solitaire;
13. Meu Perfil;
14. Editar Dados Pessoais;
15. Alterar Avatar;
16. Dados de Pagamento;
17. Logout.

Para cada tela, idealmente produzir:

- Protótipo visual desktop;
- Lista de componentes;
- Hierarquia da tela;
- Estados visuais;
- Especificação de espaçamento;
- Tipografia;
- Cores;
- Botões;
- Inputs;
- Regras de interação;
- Regras de acessibilidade;
- CSS de referência;
- Pontos não definidos funcionalmente.

---

# 42. Estado Atual do Projeto ao Encerrar Este Chat

Ao final desta conversa:

- O backlog foi identificado;
- O escopo visual foi definido;
- O público-alvo foi consolidado;
- A plataforma foi definida como web desktop;
- O idioma visual foi definido como pt-BR;
- O mapa de telas foi consolidado em 17 telas;
- Foi criado um prompt em inglês para geração de wireframes;
- Foram gerados protótipos visuais iniciais;
- Foi criado um protótipo individual de Login;
- Foi criado um protótipo geral desktop;
- Foi proposta uma identidade visual;
- Foi proposta uma paleta;
- Foi proposta uma tipografia;
- Foi proposta uma estrutura CSS;
- Foram especificados componentes globais;
- Foram documentadas as 17 telas;
- Foram diferenciadas referências visuais de regras funcionais;
- Foram identificados pontos que ainda precisam de validação;
- Ficou explicitamente definido que código só será produzido quando solicitado futuramente.

---

# 43. Resumo Executivo

O **Old Games New FUN** será uma plataforma web desktop de jogos clássicos voltada principalmente para pessoas idosas.

A experiência deve ser:

- Simples;
- Acessível;
- Clara;
- Confortável;
- Previsível;
- Visualmente amigável.

A identidade inicial utiliza:

- Azul escuro;
- Amarelo;
- Branco;
- Elementos arredondados;
- Tipografia grande;
- Ícones grandes;
- Cards amplos.

O produto possui uma estrutura inicial de 17 telas distribuídas entre autenticação, Home, jogos, perfil e logout.

O projeto está atualmente na fase de **UI/UX e prototipação**, e não na fase de implementação funcional.

O próximo passo indicado é produzir e validar os protótipos individuais das telas, começando pelo Login e avançando de forma incremental.

---

# 44. Regra de Continuidade para Futuros Chats

Ao reutilizar esta documentação em outro chat, considerar como contexto inicial:

> Estou desenvolvendo a plataforma web desktop “Old Games New FUN”, focada em jogos clássicos para pessoas idosas. O produto deve priorizar simplicidade, acessibilidade, botões grandes, fontes grandes, alto contraste, baixa carga cognitiva e navegação previsível. A identidade visual inicial utiliza azul escuro, amarelo e branco. O mapa atual possui 17 telas: Login, Cadastro, Esqueci Senha, Home, oito jogos, quatro telas de Perfil e Logout. Neste estágio, quero trabalhar primeiro em UI/UX e protótipos visuais; não gerar código funcional até que eu solicite explicitamente. Informações criadas apenas para ilustrar protótipos não devem ser tratadas como regras de negócio sem minha validação.

---

# 45. Conclusão

Este documento consolida o conteúdo relevante produzido durante o chat sem transformar sugestões visuais em regras funcionais definitivas.

Deve ser usado como:

- Memória do projeto;
- Briefing de UI/UX;
- Referência para designers;
- Referência para desenvolvedores;
- Base para novos prompts;
- Base para criação de histórias e tarefas;
- Referência para futura implementação do frontend.

Antes de implementar regras de negócio, validar explicitamente os pontos ainda abertos identificados neste documento.
