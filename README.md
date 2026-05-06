# Old Games New FUN

Old Games New FUN é um portal de jogos retrô pensado e desenhado para pessoas da terceira idade (60+). O foco do projeto é promover entretenimento, inclusão digital e socialização através de jogos clássicos, entregues com interface extremamente simples, alta legibilidade e navegação intuitiva.

Objetivo
- Proporcionar uma experiência digital segura e agradável para idosos com baixa familiaridade tecnológica.
- Minimizar carga cognitiva: poucas etapas, ações claras e feedback imediato.
- Promover autonomia e diversão por meio de jogos simples e familiares.

Público-alvo
- Pessoas com 60 anos ou mais
- Usuários com pouca experiência em computação ou dispositivos móveis
- Centros de convivência, lares de idosos e familiares que queiram introduzir jogos como atividade

Principais telas (UX simplificada)
- Tela de Cadastro: formulário simples, campos grandes e instruções curtas.
- Tela de Login: entrada direta, opção visível de "Esqueci a senha".
- Tela Esqueci a senha: recuperação assistida com passos mínimos.
- Dashboard (Seleção de Jogos): cartas grandes por jogo, botão claro de "Iniciar" e descrição curta.
- Tela Meu Perfil: avatar, dados pessoais e informações de pagamento, com botões grandes para editar.
- Tela de Jogo: área de jogo central, instruções curtas no topo, botão "Voltar" sempre visível e controles grandes.
- Logout: ação única e reversível, botão visível na interface principal.

Tipos de jogos (prioridade para MVP)
- Jogo da Velha (Tic-Tac-Toe) — objetivo: linha, coluna ou diagonal.
- Jogo da Forca — objetivo: adivinhar palavras com dicas curtas.
- Cobrinha (Snake) — controles simples por toque/clique.
- Dama — versão básica com regras simplificadas.
- Xadrez — versão reduzida (opcional para fases seguintes).
- Clone Candy Crush (simplificado) — mecânica de combinar peças em telas curtas.
- Paciência e Spider Solitaire — versões com interface limpa e passos guiados.

Diretrizes de acessibilidade e design
- Fonte mínima: 18px ou maior.
- Botões: altura mínima de 48px, espaçamento amplo entre elementos.
- Alto contraste de cores e foco de teclado visível.
- Texto curto, ícones familiares e linguagem direta.
- Feedback visual claro para ações, erros e sucessos.

Valor de negócio
- Inclusão digital: facilita o acesso de idosos a atividades lúdicas digitais.
- Socialização: jogos simples podem ser usados em grupos e eventos.
- Escalabilidade: arquitetura pensada para evoluir de mock/localStorage para backends reais.

Entrega mínima esperada (MVP)
- Estrutura do projeto com páginas principais (Cadastro, Login, Dashboard, Perfil).
- Integração básica entre interface e backend mock para autenticação e armazenamento de progresso.
- Implementação completa de pelo menos um jogo (recomendado: Jogo da Velha).

# Estrutura atual do projeto:

├── Backend
│   ├── login
│   │   └── teste.cs
│   └── register
│       └── teste.cs
├── Frontend
│   ├── css
│   │   └── teste.css
│   └── html
│       ├── login
│       │   └── teste.html
│       └── register
│           └── teste.html
├── _Wiki
│   ├── copilot.md
│   └── git.md
└── README.md