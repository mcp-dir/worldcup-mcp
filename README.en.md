# Copa do Mundo 2026

### Copa do Mundo 2026 for Claude, ChatGPT and AI agents

Schedules and results for the 2026 FIFA World Cup in natural language: today's matches, kickoff times, scores, groups, standings, the knockout bracket, teams and stadiums. Data updates automatically during the tournament. Free.

- 📊 **8 tools**
- 🔒 **Read-only**
- 💬 **Works with any MCP client**: Claude Desktop, Cursor, VS Code, Cline, Continue
- 🔑 **Magic-link login (no password)**

[Portuguese version](README.md) · [Full docs (PT-BR)](docs/)

---

## One-click install

### Claude (Web and Desktop)

[➕ Open in Claude and connect](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Add custom connector** → name `Copa do Mundo 2026`, URL `https://api.mcp.ai/p_worldcup`.

### Cursor

[➕ Install in Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=worldcup&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF93b3JsZGN1cCJ9)

### VS Code (Copilot Chat)

[➕ Install in VS Code](vscode:mcp/install?name=worldcup&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_worldcup%22%7D)

### Any other MCP-over-HTTP client

```
https://api.mcp.ai/p_worldcup
```

---

## 8 tools

| Tool | Description |
|---|---|
| `worldcup_matches` | Jogos da Copa do Mundo 2026 com placar e horário. |
| `worldcup_schedule` | Calendário do torneio agrupado por data. |
| `worldcup_results` | Resultados (placares finais) dos jogos já encerrados. |
| `worldcup_groups` | Composição dos grupos (12 grupos de 4 seleções) com as equipes e os jogos de cada grupo. |
| `worldcup_standings` | Classificação (tabela) dos grupos: pontos, jogos, vitórias, empates, derrotas, saldo de gols. |
| `worldcup_bracket` | Chaveamento do mata-mata (16 avos até a final) com os confrontos e os classificados conhecidos. |
| `worldcup_teams` | Seleções participantes (48 no total) com ranking FIFA e confederação. |
| `worldcup_venues` | Estádios-sede (16 nos EUA, México e Canadá): cidade, capacidade e os jogos de cada sede. |

---

## Pricing

Free.

---

## License

MIT — see [LICENSE](LICENSE). The MCP server at `api.mcp.ai/p_worldcup` is proprietary (hosted); this repo (manifests, docs, skills) is MIT.
