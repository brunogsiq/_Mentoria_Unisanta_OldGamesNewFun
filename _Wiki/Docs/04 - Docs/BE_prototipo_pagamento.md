# Backend: Pagamento

## Objetivo
Gerenciar cartões do usuário, métodos de pagamento tokenizados e execução de cobranças.

## Endpoints
- `GET /api/payments/cards` — lista cartões tokenizados do usuário.
- `POST /api/payments/cards` — registra método de pagamento via token (ex.: Stripe token).
- `POST /api/payments/charge` — efetua cobrança com `paymentMethodId` tokenizado.
- `DELETE /api/payments/cards/{id}` — remove método tokenizado.

## Segurança / Conformidade
- NÃO armazenar número de cartão em texto; usar tokenização via provedor (Stripe, Adyen).
- Seguir PCI-DSS: usar providers, HTTPS, logs mínimos e masking.

## Notas de implementação
- Usar webhooks do provedor para confirmar transações.
- `inputmode="numeric"` é recomendado no front-end; backend deve validar formato e CVC via provedor.