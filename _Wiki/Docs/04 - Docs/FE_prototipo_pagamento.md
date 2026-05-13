# prototipo_pagamento.md

# Tela: Pagamento

## Objetivo
Permitir ao usuário gerenciar métodos de pagamento e inserir cartão com segurança.

## Componentes
- Sidebar / Navegação
- Card de pagamento (formulário)
- Campo Nome do titular
- Campo Número do cartão (mascarado)
- Campo Validade
- Campo CVC
- Botão Salvar
- Lista de métodos salvos (cartões)

## Estrutura visual
Card central com formulário → Ações: Salvar, Voltar → Lista de cartões abaixo

## CSS recomendado (pedaço)
.payment-form {
  max-width: 45rem; /* 720px */
  background: var(--color-surface);
  border-radius: var(--radius-lg);
  padding: 2.5rem; /* 40px */
  box-shadow: var(--shadow-card);
}
.payment-row {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1.25rem; /* 20px */
}
.card-number {
  font-family: monospace;
  letter-spacing: 0.125rem; /* 2px */
}

## Notas de acessibilidade e segurança
- Usar inputmode="numeric" para número e CVC.
- Fornecer máscara visual (e manter valor real apenas no front-end temporariamente).
- Confirmar ação sensível (ex.: remover cartão) com modal.
