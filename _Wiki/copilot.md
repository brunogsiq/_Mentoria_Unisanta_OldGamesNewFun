# Solicitação do Usuário

Você é um engenheiro de software sênior especialista em desenvolvimento web acessível e aplicações escaláveis.

Seu objetivo é construir uma plataforma web chamada Old Games New FUN, focada em jogos clássicos para pessoas da terceira idade, priorizando simplicidade, acessibilidade e facilidade de uso.

A plataforma será um portal de jogos antigos (retrô), com foco em usuários idosos (60+), que possuem pouca familiaridade com tecnologia.

Objetivos principais:

- Interface extremamente simples
- Navegação intuitiva (mínimo de cliques)
- Letras grandes e legíveis
- Botões grandes e bem espaçados
- Baixa carga cognitiva (evitar excesso de informação)
- Feedback visual claro (ações, erros, sucesso)

ARQUITETURA DO PROJETO

Frontend: HTML, CSS, JavaScript (ou React se necessário)
Backend: Node.js (Express ou similar)
Armazenamento inicial: localStorage ou mock API (evolutivo para banco real)

Implemente as seguintes funcionalidades:

FE - Tela Cadastro
BFF - Cadastro de usuário
FE - Tela Login
BFF - Login
FE - Tela Esqueci a senha
BFF - Recuperação de senha
FE - Tela Meu Perfil
BFF - Dados do usuário
FE - Seção Avatar
BFF - Atualização de avatar
FE - Dados pessoais
BFF - Atualização de dados pessoais
FE - Dados de pagamento
BFF - Atualização de pagamento

Cada jogo deve ter FE + BFF:

Jogo da Forca
Jogo da Velha
Xadrez
Dama
Cobrinha (Snake)
Clone Candy Crush (simplificado)
Paciência
Spider Solitaire

🚪 SISTEMA

FE - Tela sair (logout)
BFF - Encerrar sessão
Aplicar boas práticas de acessibilidade para idosos:

Fonte mínima: 18px+
Botões grandes (mínimo 48px altura)
Alto contraste (ex: fundo escuro + texto claro ou vice-versa)
Evitar textos longos
Ícones simples e familiares
Feedback visual em todas as ações
Evitar múltiplas etapas
Sempre mostrar "Voltar" visível
Evitar menus escondidos

DIRETRIZES DOS JOGOS

Jogos devem ser simples e rápidos
Salvar progresso quando possível
Interface limpa, sem distrações
Controles simples (clique ou toque)
Instruções curtas antes de iniciar

QUALIDADE E BOAS PRÁTICAS

Código modular
Separação clara de responsabilidades
Componentização no frontend
APIs REST simples no backend
Tratamento de erros amigável ao usuário
Logs básicos no backend

ESTRUTURA DE PASTAS (SUGESTÃO)

/frontend
/pages
/components
/styles
/services

/backend
/routes
/controllers
/services
/models

ENTREGAS ESPERADAS

Estrutura inicial do projeto
Implementação das telas principais
Integração FE + BFF
Implementação de pelo menos 1 jogo completo (ex: Jogo da Velha)
Base pronta para expansão dos outros jogos

REGRAS IMPORTANTES

Sempre priorizar simplicidade sobre sofisticação
Evitar complexidade desnecessária
Código deve ser legível e fácil de manter
Pensar sempre no usuário idoso

OBJETIVO FINAL

Criar uma plataforma funcional, simples e agradável, onde idosos consigam acessar, entender e jogar sem dificuldades, promovendo entretenimento e inclusão digital.


# Resposta do Copilot

Vou inserir o conteúdo sugerido para _Wiki/copilot.md. Abaixo está o texto pronto — se quiser que eu grave o arquivo, responda “gravar” e eu criarei no repositório.

--- (conteúdo para `_Wiki/copilot.md`) ---

# Solicitação ao Copilot — Old Games New FUN

## TL;DR
Plataforma web simples e acessível para idosos (60+). Frontend leve (HTML/CSS/JS), backend Node.js/Express, persistência inicial em localStorage/mock. Priorizar legibilidade, navegação mínima e feedback claro.

## Objetivo
Criar um portal de jogos retrô com UX destinada a usuários idosos: interface limpa, fontes grandes, botões amplos, alto contraste e fluxo simples (mínimo de cliques).

## Requisitos principais
- Fonte mínima: 18px+
- Botões: altura mínima 48px, espaçamento amplo
- Alto contraste e foco visível
- Feedback claro (ações, erros, sucesso)
- Sempre exibir “Voltar”
- Evitar menus escondidos e etapas múltiplas

## Arquitetura proposta
- Frontend: HTML / CSS / JavaScript (sem React inicialmente)
- Backend: Node.js + Express (API REST simples)
- Autenticação: JWT simples (revogação em memória)
- Persistência inicial: localStorage + mock em memória / JSON
- Servir frontend estático via Express

## Funcionalidades (FE + BFF)
- Autenticação:
  - Registro (`/api/auth/register`)
  - Login (`/api/auth/login`)
  - Esqueci senha (`/api/auth/forgot`)
  - Logout (`/api/auth/logout`)
- Perfil do usuário:
  - Ver/Atualizar perfil (`/api/user/profile`)
  - Avatar (`/api/user/avatar`)
  - Dados pessoais e pagamento (`/api/user/personal`, `/api/user/payment`)
- Jogos:
  - Endpoints genéricos de progresso: `/api/games/:id/save`, `/api/games/:id/load`
  - Implementar ao menos: Tic-Tac-Toe (completo, FE+BFF)
  - Base pronta para adicionar: Forca, Xadrez, Dama, Snake, Candy Crush clone, Paciência, Spider Solitaire

## Diretrizes dos jogos
- Simples, rápidos e sem distrações
- Controles por clique/toque
- Instruções curtas antes do jogo
- Salvar progresso quando possível

## Boas práticas de qualidade
- Código modular e legível
- Separação de responsabilidades (routes/controllers/services)
- Logs básicos no backend e mensagens amigáveis ao usuário
- Testes manuais de fluxo principal e checagem de acessibilidade (contraste, foco, tamanhos)

## Estrutura de pastas sugerida
- public/
  - index.html, login.html, register.html, forgot.html, dashboard.html, profile.html
  - games/tic-tac-toe.html
  - css/style.css
  - js/app.js, js/games/
- src/
  - server.js
  - routes/auth.js, routes/user.js, routes/games.js
  - controllers/
  - services/
- data/ (opcional) users.json

## Entregas mínimas esperadas
- Scaffold do backend (Express) e frontend estático
- Páginas principais: login, registro, esqueci senha, dashboard, perfil
- Integração FE ↔ BFF básica (registro/login/profile)
- Jogo completo: Tic-Tac-Toe com salvamento
- README com instruções de setup

## Próximos passos recomendados
1. Confirmar Node.js mínimo (recomendo >=16).
2. Autorizar criação de scaffold + Tic-Tac-Toe (ou apenas scaffold).
3. Inicializar `package.json` e instalar `express`.