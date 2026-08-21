---
name: worldcup-mcp
description: Skill da REST API do Copa do Mundo 2026 na MCP.AI: 8 endpoints em /api/worldcup. Horários e resultados da Copa do Mundo 2026 (FIFA World Cup) por linguagem natural: jogos de hoje, que horas joga a sua seleção, placares, grupos, tabela de classificação, chaveamento do mata-mata, seleções e estádios. Dados atualizados automaticamente durante o torneio. Grátis. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Copa do Mundo 2026 — REST API skill

Você tem acesso à **Copa do Mundo 2026** REST API na MCP.AI.

> Horários e resultados da Copa do Mundo 2026 (FIFA World Cup) por linguagem natural: jogos de hoje, que horas joga a sua seleção, placares, grupos, tabela de classificação, chaveamento do mata-mata, seleções e estádios. Dados atualizados automaticamente durante o torneio. Grátis.

## Base URL

```
https://api.mcp.ai/api/worldcup
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/worldcup/bracket \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/worldcup/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (8)

#### `worldcup_bracket`

Chaveamento do mata-mata (16 avos até a final) com os confrontos e os classificados conhecidos. _(POST /api/worldcup/bracket)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `stage` | string | Não | Limita a uma fase: 'round32', 'round16', 'quarter', 'semi', 'final'. |

#### `worldcup_groups`

Composição dos grupos (12 grupos de 4 seleções) com as equipes e os jogos de cada grupo. _(POST /api/worldcup/groups)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `group` | string | Não | Letra do grupo (ex.: 'A'). Omita para todos os grupos. |

#### `worldcup_matches`

Jogos da Copa do Mundo 2026 com placar e horário. _(POST /api/worldcup/matches)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `date` | string | Não | Data no formato YYYY-MM-DD. Omita para os jogos de hoje. |
| `team` | string | Não | Nome da seleção (ex.: 'Brasil', 'Argentina', 'France'). |
| `group` | string | Não | Letra do grupo (ex.: 'A', 'B', ... 'L'). |
| `stage` | string | Não | Fase: 'group', 'round32', 'round16', 'quarter', 'semi', 'final'. |
| `status` | string | Não | Filtra por status do jogo. (scheduled, live, finished) |
| `timezone` | string | Não | Fuso IANA para os horários (ex.: 'America/Sao_Paulo'). Default UTC. |

#### `worldcup_results`

Resultados (placares finais) dos jogos já encerrados. _(POST /api/worldcup/results)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `date` | string | Não | Data (YYYY-MM-DD). |
| `team` | string | Não | Nome da seleção. |
| `group` | string | Não | Letra do grupo. |

#### `worldcup_schedule`

Calendário do torneio agrupado por data. _(POST /api/worldcup/schedule)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `date` | string | Não | Filtra um dia específico (YYYY-MM-DD). |
| `stage` | string | Não | Filtra por fase (ex.: 'group', 'round16', 'final'). |
| `timezone` | string | Não | Fuso IANA para os horários. Default UTC. |

#### `worldcup_standings`

Classificação (tabela) dos grupos: pontos, jogos, vitórias, empates, derrotas, saldo de gols. _(POST /api/worldcup/standings)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `group` | string | Não | Letra do grupo. Omita para a tabela de todos os grupos. |

#### `worldcup_teams`

Seleções participantes (48 no total) com ranking FIFA e confederação. _(POST /api/worldcup/teams)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `team` | string | Não | Nome da seleção para o perfil. Omita para a lista completa. |
| `confederation` | string | Não | Filtra por confederação (ex.: 'CONMEBOL', 'UEFA', 'CONCACAF'). |

#### `worldcup_venues`

Estádios-sede (16 nos EUA, México e Canadá): cidade, capacidade e os jogos de cada sede. _(POST /api/worldcup/venues)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `city` | string | Não | Filtra por cidade-sede. |
| `venue` | string | Não | Filtra por nome do estádio. |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_worldcup` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
