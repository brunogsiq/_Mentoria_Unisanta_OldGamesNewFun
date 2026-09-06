# Documentação Consolidada do Chat — Mentoria Unisanta / Old Games New FUN

## 1. Identificação do Projeto

**Projeto:** Old Games New FUN  
**Contexto:** Mentoria Unisanta  
**Tipo de solução:** Plataforma web de jogos clássicos  
**Foco inicial:** Desktop-first  
**Público-alvo principal:** Pessoas idosas / terceira idade  
**Objetivo central:** Disponibilizar jogos clássicos em uma interface simples, acessível, legível, amigável e visualmente consistente.

---

## 2. Objetivo desta documentação

Este documento consolida, em um único Markdown, as decisões, protótipos, referências visuais, documentação de UI/UX, estrutura de telas, componentes, identidade visual, imagens geradas e recomendações discutidas ao longo do chat.

O objetivo é preservar o contexto relevante antes da exclusão da conversa, permitindo que o desenvolvimento, a documentação acadêmica, os testes, os refinamentos de UX/UI e as futuras evoluções do projeto continuem sem perda de informação.

---

# 3. Visão Geral do Produto

A plataforma **Old Games New FUN** foi concebida como um ambiente web dedicado a jogos clássicos e casuais, com ênfase em:

- simplicidade de navegação;
- baixo esforço cognitivo;
- alta legibilidade;
- botões amplos;
- contraste visual;
- poucos elementos simultâneos por tela;
- linguagem simples;
- feedback visual claro;
- reutilização de componentes;
- consistência entre telas;
- facilidade de uso para pessoas idosas.

A interface usa como base uma identidade visual composta principalmente por azul escuro, amarelo e branco, com elementos arredondados, cards com bordas suaves, sombras discretas, ícones grandes e tipografia forte e legível.

---

# 4. Identidade Visual Consolidada

## 4.1 Nome da plataforma

**OLD GAMES NEW FUN**

O conceito da marca une nostalgia e modernidade:

- **OLD GAMES** representa os jogos clássicos;
- **NEW FUN** reforça a ideia de nova diversão e nova experiência;
- o controle de videogame funciona como símbolo principal da marca.

## 4.2 Paleta principal definida

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

# 5. Tipografia e Acessibilidade

A plataforma foi documentada com foco em pessoas idosas.

## Diretrizes principais

- Nenhum texto principal deve ter menos de `18px`.
- Botões devem ter altura mínima de `56px`.
- Títulos devem ser grandes e facilmente identificáveis.
- Ações principais devem usar contraste forte.
- Navegação não deve depender apenas de menus ocultos.
- Telas internas devem ter sempre uma forma clara de voltar.
- Áreas clicáveis devem ser grandes.
- Estados de foco devem ser visíveis.
- Mensagens e labels devem ser simples e diretas.

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

---

# 6. Mapa de Telas Definido

Foi consolidado um mapa visual da aplicação com 17 itens principais.

## 6.1 Autenticação

1. Tela de Login
2. Tela de Cadastro
3. Tela Esqueci Senha

## 6.2 Home

4. Tela Home — Seleção de Jogos

## 6.3 Jogos

5. Jogo da Velha
6. Forca
7. Damas
8. Xadrez
9. Cobrinha
10. Candy Crush Simplificado
11. Paciência
12. Spider Solitaire

## 6.4 Perfil

13. Meu Perfil — Visão Geral
14. Editar Dados Pessoais
15. Alterar Avatar
16. Dados de Pagamento

## 6.5 Sistema

17. Logout — Ação / Modal de confirmação

---

# 7. Protótipos Visuais Armazenados

Foram enviados e considerados referência visual oficial do projeto os seguintes protótipos:

- protótipo geral com Login, Cadastro, Home, Tela de Jogo e Perfil;
- mapa completo das telas;
- Tela de Cadastro;
- Tela de Login;
- Tela Esqueci a Senha;
- Tela Home;
- conjunto de telas dos Jogos;
- Perfil;
- Dados Pessoais;
- Avatar;
- Pagamento;
- Sair / Logout.

Esses protótipos passaram a ser usados como base para desenvolvimento visual, componentização, documentação funcional, QA visual, refinamento UI/UX, elaboração de backlog, material acadêmico e futuras apresentações do projeto.

---

# 8. Componentes Globais Documentados

## 8.1 Header / Topbar

Usado em telas internas, principalmente Home, Jogos e Perfil.

### Deve conter

- logotipo;
- nome da plataforma;
- saudação do usuário;
- ícone de perfil;
- ação de sair, quando aplicável.

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

## 8.2 Card Base

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

## 8.3 Botão Primário

Usado em Entrar, Cadastrar, Salvar e Novo Jogo.

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

## 8.4 Botão Secundário

Usado em Voltar, Criar conta e Cancelar.

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

## 8.5 Botão de Perigo

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

## 8.6 Campo de Formulário

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

# 9. Componentização por Tela

## 9.1 Tela de Login

### Objetivo

Permitir que o usuário acesse a plataforma de forma simples.

### Componentes

1. Área de branding
2. Card de login
3. Campo de e-mail
4. Campo de senha
5. Botão Entrar
6. Separador “ou”
7. Botão Criar conta
8. Link Esqueci minha senha
9. Card de dica inferior

### Estrutura visual

```text
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

## 9.2 Tela de Cadastro

### Objetivo

Permitir criação de conta com poucos campos e linguagem simples.

### Componentes

- Logo lateral ou superior
- Card de cadastro
- Nome completo
- E-mail
- Senha
- Confirmar senha
- Botão Cadastrar
- Link “Já tenho uma conta”

## 9.3 Tela Esqueci Senha

### Objetivo

Permitir recuperação de senha por e-mail.

### Componentes

- Logo
- Título “Esqueci minha senha”
- Texto explicativo
- Campo E-mail
- Botão Enviar instruções
- Link Voltar para login

## 9.4 Home — Seleção de Jogos

### Objetivo

Permitir que o usuário escolha rapidamente um jogo.

### Componentes

- Header
- Título “Escolha um jogo para jogar”
- Grid de cards de jogos
- Botão Meu Perfil
- Botão Sair

### Card de jogo

Cada card deve conter ícone grande, nome do jogo e área clicável ampla.

## 9.5 Tela Base de Jogo

Estrutura reaproveitável para todos os jogos.

### Componentes

- Header do jogo
- Botão Voltar
- Título
- Área principal do jogo
- Painel lateral de status
- Botões de ação
- Área de dica/instrução

```css
.game-layout {
  display: grid;
  grid-template-columns: 1fr 320px;
  gap: 32px;
  padding: 40px;
}
```

---

# 10. Jogos Documentados

## 10.1 Jogo da Velha

Componentes: tabuleiro 3x3, indicador de turno, placar, Reiniciar e Voltar.

```css
.tic-tac-toe-board {
  width: 420px;
  height: 420px;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  border: 3px solid var(--color-primary);
}
```

## 10.2 Forca

Componentes: desenho da forca, palavra oculta, letras disponíveis, letras erradas, vidas restantes, Dica e Voltar.

## 10.3 Damas

Componentes: tabuleiro 8x8, peças, Novo jogo, Voltar e status.

## 10.4 Xadrez

Compartilha a estrutura base do tabuleiro 8x8, adaptada às peças e regras do xadrez.

## 10.5 Cobrinha

Componentes: área de jogo, pontuação, nível, Pausar e Voltar.

## 10.6 Candy Crush Simplificado

Componentes: grid de doces, pontos, nível, movimentos restantes, Reiniciar e Voltar.

## 10.7 Paciência

Componentes: área de cartas, pilhas de cartas, Novo jogo e Voltar.

## 10.8 Spider Solitaire

Compartilha estrutura visual de jogo de cartas com disposição própria.

---

# 11. Perfil do Usuário

## 11.1 Meu Perfil — Visão Geral

Componentes: sidebar, avatar, nome, e-mail, cards de estatísticas, atalhos e botão Voltar para Home.

Estatísticas vistas no protótipo: Jogos jogados, Conquistas e Partidas.

## 11.2 Editar Dados Pessoais

Campos: Nome completo, E-mail, Data de nascimento e Telefone. Ações: Salvar alterações e Voltar.

## 11.3 Alterar Avatar

Componentes: avatar atual, lista/carrossel de avatares, seleção visual, Salvar e Voltar.

```css
.avatar-option--selected {
  border-color: var(--color-secondary);
}
```

## 11.4 Dados de Pagamento

Campos: Titular do cartão, Número do cartão mascarado, Validade e CVC.

---

# 12. Modal de Logout

### Objetivo

Confirmar se o usuário deseja sair.

### Componentes

- overlay escurecido;
- caixa modal;
- ícone de saída;
- título “Sair da conta?”;
- texto “Tem certeza que deseja sair?”;
- botão Cancelar;
- botão Sair.

```css
.modal-overlay {
  position: fixed;
  inset: 0;
  background: rgba(0, 0, 0, 0.55);
  display: flex;
  align-items: center;
  justify-content: center;
}
```

---

# 13. Regras Gerais para a Equipe

1. A plataforma é web desktop-first.
2. Todo botão deve ter altura mínima de `56px`.
3. Nenhum texto importante deve ter menos de `18px`.
4. As telas devem usar alto contraste.
5. Não usar menus escondidos como única forma de navegação.
6. Sempre existir botão “Voltar” em telas internas.
7. Jogos devem ter área visual grande.
8. Cada tela deve ser componentizada para reaproveitamento.
9. CSS deve ser organizado por responsabilidade.

```text
styles/
├── base.css
├── tokens.css
├── buttons.css
├── forms.css
├── cards.css
├── layout.css
├── games.css
├── profile.css
└── modal.css
```

---

# 14. Logo Gerado no Chat

Foi solicitada e gerada uma proposta de logotipo para a plataforma.

## Características

- controle de videogame amarelo;
- texto “OLD GAMES” em branco;
- texto “NEW FUN” em amarelo;
- estilo moderno, amigável e limpo;
- forte contraste;
- coerência com a paleta azul/amarelo;
- adequado para cabeçalhos, login e materiais institucionais.

O logotipo gerado passou a servir como referência visual da marca.

---

# 15. Avatares Gerados

Foi solicitada uma coleção de figuras para uso como avatares.

Foi gerado um conjunto visual com seis personagens idosos, seguindo o estilo amigável da plataforma.

## Características

- ilustração digital/cartoon;
- busto/rosto;
- fundo circular;
- expressões positivas;
- variedade de cabelo;
- homens e mulheres;
- coerência visual entre os personagens;
- boa leitura em tamanho pequeno.

## Exemplos presentes

- homem idoso de óculos e camisa verde;
- mulher idosa loira de óculos;
- homem grisalho de óculos;
- homem idoso de cabelo branco;
- mulher idosa de cabelo branco;
- homem idoso careca com barba.

## Uso planejado

- seleção de avatar;
- perfil;
- onboarding;
- personalização de usuário.

---

# 16. Figuras / Ícones dos Jogos Gerados

Foi solicitado um conjunto visual de figuras para representar individualmente os jogos.

A geração contemplou referências visuais para:

- Jogo da Velha;
- Forca;
- Damas;
- Xadrez;
- Cobrinha;
- Candy Crush;
- Paciência;
- Spider Solitaire.

Também foram gerados elementos complementares relacionados aos jogos, como letras, erros, variação pontuada do jogo da velha e cartas simplificadas.

## Direção visual

- ícones grandes;
- cores vivas;
- formas amigáveis;
- fundo branco;
- sombras discretas;
- legibilidade em cards;
- compatibilidade com a Home.

---

# 17. Documento `prototipo.md`

Foi enviado e analisado um arquivo com documentação de componentização UI/UX.

Esse arquivo passou a ser tratado como referência oficial para:

- Design System;
- arquitetura visual;
- componentes;
- CSS;
- organização de tela;
- acessibilidade;
- desenvolvimento frontend.

A documentação contempla objetivo, cores, tipografia, header, cards, botões, campos de formulário, login, cadastro, recuperação de senha, home, telas de jogo, jogos específicos, perfil, dados pessoais, avatar, pagamento, modal de logout e regras gerais.

---

# 18. Análise da Documentação

Foi feita uma avaliação geral do material.

## Pontos positivos identificados

- visão geral clara;
- definição de público-alvo;
- princípios de acessibilidade;
- mapa de telas;
- Design System;
- componentização;
- estrutura de botões;
- cards;
- formulários;
- organização visual;
- base suficiente para iniciar o frontend.

## Avaliação registrada

**Qualidade estimada:** `8,5 / 10`

A documentação foi considerada suficiente para iniciar o desenvolvimento visual.

---

# 19. Recomendações de Evolução da Documentação

Foi recomendado complementar o material com capítulos de produto, arquitetura e QA.

## 19.1 Arquitetura Frontend

```text
src/
├── assets/
├── components/
├── pages/
├── services/
├── styles/
├── utils/
├── routes/
└── app.js
```

## 19.2 Regras de Negócio — exemplos sugeridos

- autenticação necessária para acessar jogos;
- avatar padrão para nova conta;
- estatísticas atualizadas após partidas;
- logout encerrando sessão.

> **Importante:** esses itens foram apresentados como exemplos de regras que poderiam ser documentadas. Não devem ser tratados automaticamente como requisitos oficiais enquanto não forem aprovados formalmente.

## 19.3 Banco de Dados — entidades sugeridas

```text
Usuários
Jogos
Partidas
Pontuações
Avatares
Pagamentos
```

Essas entidades representam uma proposta inicial e precisam ser refinadas antes da implementação.

## 19.4 Fluxo conceitual sugerido

```text
Login
 ↓
Home
 ↓
Selecionar Jogo
 ↓
Jogar
 ↓
Salvar Estatísticas
 ↓
Perfil
```

## 19.5 Casos de Uso sugeridos

```text
UC01 - Realizar Login
UC02 - Criar Conta
UC03 - Recuperar Senha
UC04 - Jogar Jogo da Velha
UC05 - Alterar Avatar
UC06 - Realizar Logout
```

## 19.6 MVPs sugeridos

### MVP 1

- Login;
- Cadastro;
- Home;
- Jogo da Velha.

### MVP 2

- Forca;
- Damas;
- Perfil.

### MVP 3

- Xadrez;
- Cobrinha;
- Pagamentos.

> Essa divisão é sugestiva e deve ser validada conforme o escopo acadêmico e o produto final.

---

# 20. QA — Plano de Testes Sugerido

Foi recomendado que a documentação futura contemple:

- testes funcionais;
- testes de usabilidade;
- testes de acessibilidade;
- testes responsivos;
- testes de performance;
- testes de segurança.

---

# 21. Backlog Inicial Sugerido

Uma possível organização em User Stories foi indicada:

```text
US01 - Login
US02 - Cadastro
US03 - Recuperação de Senha
US04 - Home
US05 - Perfil
US06 - Jogo da Velha
...
```

A numeração final e os critérios de aceite ainda precisam ser definidos formalmente.

---

# 22. Estado Atual do Projeto

## Já definido

- nome da plataforma;
- identidade visual;
- cores;
- tipografia;
- público-alvo;
- princípios de UX;
- mapa de telas;
- protótipos;
- estrutura visual;
- componentes globais;
- telas de autenticação;
- home;
- perfil;
- oito jogos;
- modal de logout;
- logo;
- conjunto de avatares;
- ícones dos jogos;
- documentação CSS inicial;
- organização proposta do frontend.

## Parcialmente definido

- arquitetura final do frontend;
- regras de negócio;
- entidades de domínio;
- banco de dados;
- fluxos completos;
- casos de uso;
- backlog formal;
- critérios de aceite;
- plano de testes;
- modelo de autenticação;
- persistência;
- API/backend;
- pagamentos reais ou simulados.

## Ainda não consolidado

- stack tecnológica definitiva;
- framework frontend;
- backend;
- banco de dados real;
- modelagem de dados;
- autenticação;
- infraestrutura;
- deploy;
- CI/CD;
- integrações;
- observabilidade;
- telemetria;
- analytics;
- segurança detalhada;
- requisitos não funcionais;
- critérios formais de acessibilidade WCAG;
- responsividade mobile/tablet;
- estratégia de monetização.

---

# 23. Recomendações para a Próxima Etapa

1. Consolidar requisitos funcionais.
2. Separar protótipo visual de regra de negócio.
3. Definir backlog.
4. Criar critérios de aceite.
5. Definir stack tecnológica.
6. Estruturar arquitetura frontend.
7. Definir necessidade de backend.
8. Modelar banco de dados.
9. Definir autenticação.
10. Implementar MVP.
11. Criar testes.
12. Validar acessibilidade.
13. Preparar documentação acadêmica.
14. Preparar demonstração.

---

# 24. Sugestão de Stack para Estudo / Mentoria

Caso o objetivo seja uma plataforma didática, uma evolução coerente é:

## Frontend inicial

- HTML;
- CSS;
- JavaScript.

## Evolução opcional

- React ou Vue.

## Backend futuro

- Node.js;
- Express.

## Banco de dados

- SQLite para ambiente local;
- PostgreSQL para evolução;
- Firebase/Supabase como alternativa de implementação rápida.

## Controle de versão

- Git;
- GitHub.

## Deploy

- GitHub Pages para frontend estático;
- Vercel;
- Netlify;
- Render;
- Railway.

---

# 25. Separação Importante: Protótipo x Regra de Negócio

Um ponto importante para as próximas etapas é que **o protótipo representa a intenção visual da solução, mas não deve ser tratado automaticamente como especificação funcional completa**.

Exemplo: se a tela mostra “Pagamento”, isso não significa que já estejam definidos gateway, validação de cartão, recorrência, moeda, cobrança, estorno, PCI DSS, tokenização ou bandeiras aceitas.

Essas informações precisam ser documentadas antes da implementação.

---

# 26. Diretrizes para QA Futuro

Para evitar invenção de requisitos no planejamento de testes:

- usar apenas requisitos aprovados;
- não inferir comportamento pelo protótipo;
- registrar lacunas;
- criar pontos de atenção;
- separar UI esperada de regra de negócio;
- validar critérios de aceite antes da automação;
- priorizar fluxos críticos;
- documentar evidências;
- rastrear testes até User Story ou requisito.

---

# 27. Possível Estrutura de Repositório

```text
old-games-new-fun/
├── docs/
│   ├── requisitos/
│   ├── ux-ui/
│   ├── qa/
│   ├── arquitetura/
│   └── imagens/
├── src/
│   ├── assets/
│   │   ├── logos/
│   │   ├── avatars/
│   │   └── games/
│   ├── components/
│   ├── pages/
│   ├── services/
│   ├── styles/
│   ├── utils/
│   └── routes/
├── tests/
├── README.md
└── package.json
```

---

# 28. Organização Recomendada dos Assets

```text
src/assets/
├── logos/
│   ├── logo-main.png
│   ├── logo-icon.png
│   └── logo-horizontal.png
├── avatars/
│   ├── avatar-01.png
│   ├── avatar-02.png
│   ├── avatar-03.png
│   ├── avatar-04.png
│   ├── avatar-05.png
│   └── avatar-06.png
└── games/
    ├── tic-tac-toe.png
    ├── hangman.png
    ├── checkers.png
    ├── chess.png
    ├── snake.png
    ├── candy-crush.png
    ├── solitaire.png
    └── spider-solitaire.png
```

---

# 29. Checklist de Continuidade

Quando o projeto for retomado em outro chat, revisar:

- [ ] nome e marca;
- [ ] logo;
- [ ] paleta;
- [ ] tipografia;
- [ ] protótipos;
- [ ] avatares;
- [ ] ícones dos jogos;
- [ ] telas mapeadas;
- [ ] Design System;
- [ ] componentes globais;
- [ ] acessibilidade;
- [ ] stack;
- [ ] backlog;
- [ ] critérios de aceite;
- [ ] casos de uso;
- [ ] arquitetura;
- [ ] banco;
- [ ] autenticação;
- [ ] testes;
- [ ] deploy.

---

# 30. Resumo Executivo

O projeto **Old Games New FUN** já possui uma base visual e documental madura para iniciar uma implementação de frontend.

Os maiores avanços obtidos neste chat foram:

- definição da identidade do produto;
- criação de protótipos consistentes;
- documentação do Design System;
- componentização;
- definição das telas;
- criação de marca;
- criação de avatares;
- criação de figuras dos jogos;
- organização de princípios de acessibilidade;
- recomendação de evolução para arquitetura, backlog e QA.

O próximo salto de maturidade deve ocorrer na formalização dos requisitos e na separação clara entre o que é visual, o que é regra de negócio, o que é arquitetura, o que é planejamento e o que é teste.

Com essa separação, o projeto pode ser utilizado tanto como atividade de mentoria/Unisanta quanto como projeto de portfólio ou desenvolvimento real.

---

# 31. Referência Temporal

**Consolidação realizada em:** 05/09/2026  
**Projeto:** Mentoria Unisanta — Old Games New FUN

---

# 32. Observação Final

Este documento foi criado especificamente para preservar o contexto deste chat antes de sua exclusão.

Sempre que o projeto for retomado, este Markdown deve ser tratado como **checkpoint consolidado da conversa**, mas novas decisões funcionais devem ser validadas antes de implementadas, principalmente em autenticação, banco de dados, pagamentos, regras dos jogos, persistência, integrações, segurança e requisitos não funcionais.
