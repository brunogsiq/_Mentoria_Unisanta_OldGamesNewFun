# Backend: Home / Games Listing

## Objetivo
Fornecer listagens de jogos, filtros, paginação e detalhes para a tela Home.

## Endpoints
- `GET /api/games` — query params: `?page=&limit=&category=&q=` → lista paginada.
- `GET /api/games/{id}` — detalhes do jogo (meta, tipo, assets necessários).

## Modelos / DB
- `Game { id, slug, title, description, category, cover_url, created_at }`

## Notas
- Cache agressivo para listagens públicas (CDN/Redis).
- Paginação consistente e campos de resposta mínimos para performance.