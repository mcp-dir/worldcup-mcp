# Copa do Mundo 2026

### Copa do Mundo 2026 para Claude, ChatGPT e agentes de IA

Horários e resultados da Copa do Mundo 2026 (FIFA World Cup) por linguagem natural: jogos de hoje, que horas joga a sua seleção, placares, grupos, tabela de classificação, chaveamento do mata-mata, seleções e estádios. Dados atualizados automaticamente durante o torneio. Grátis.

- 📊 **8 ferramentas**
- 🔒 **Somente leitura**
- 💬 **Funciona com qualquer cliente MCP**: Claude Desktop, Cursor, VS Code, Cline, Continue
- 🔑 **Login via magic-link (sem senha)**

[English version](README.en.md) · [Documentação completa](docs/) · [Skill pra agentes](skills/)

---

## Instalar em 1 clique

### Claude (Web e Desktop)

A Anthropic unificou a instalação de MCPs em `claude.ai/customize/connectors`. **O mesmo link serve pra Claude Web e Claude Desktop** (basta estar logado):

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

**Manual** (se o deeplink não abrir): [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → cole **Nome** `Copa do Mundo 2026` e **URL** `https://api.mcp.ai/p_worldcup`.

### Cursor

[➕ Instalar Copa do Mundo 2026 no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=worldcup&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF93b3JsZGN1cCJ9)

### VS Code (Copilot Chat)

[➕ Instalar Copa do Mundo 2026 no VS Code](vscode:mcp/install?name=worldcup&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_worldcup%22%7D)

### ChatGPT, Manus, OpenClaw e mais 40+ clientes

Funciona em qualquer cliente MCP que suporte **MCP over HTTP**. A URL do servidor é sempre:

```
https://api.mcp.ai/p_worldcup
```

Detalhes por cliente: [INSTALL.md](INSTALL.md).

---

## Exemplos de uso

```
Que horas joga o Brasil hoje na Copa?
Quais os jogos de hoje da Copa do Mundo?
Como está a tabela do grupo do Brasil?
Mostra o chaveamento do mata-mata
```

---

## 8 ferramentas disponíveis

| Tool | Descrição |
|---|---|
| `worldcup_matches` | Jogos da Copa do Mundo 2026 com placar e horário. |
| `worldcup_schedule` | Calendário do torneio agrupado por data. |
| `worldcup_results` | Resultados (placares finais) dos jogos já encerrados. |
| `worldcup_groups` | Composição dos grupos (12 grupos de 4 seleções) com as equipes e os jogos de cada grupo. |
| `worldcup_standings` | Classificação (tabela) dos grupos: pontos, jogos, vitórias, empates, derrotas, saldo de gols. |
| `worldcup_bracket` | Chaveamento do mata-mata (16 avos até a final) com os confrontos e os classificados conhecidos. |
| `worldcup_teams` | Seleções participantes (48 no total) com ranking FIFA e confederação. |
| `worldcup_venues` | Estádios-sede (16 nos EUA, México e Canadá): cidade, capacidade e os jogos de cada sede. |

Detalhe de cada tool: [docs/ferramentas.md](docs/ferramentas.md)

---

## Preços

Grátis.

---

## Privacidade & LGPD

- **Somente leitura**, nenhuma ferramenta altera dados na origem.
- **Sub-processadores**: o LLM host que você escolher (Claude, ChatGPT, Cursor, agente próprio). Lista completa em [docs/privacidade-lgpd.md](docs/privacidade-lgpd.md).
- Os dados retornados pelas tools são enviados ao **LLM host que você escolher**, sub-processador fora do nosso controle. Recomendamos planos com opt-out de treinamento.

---

## Perguntas frequentes

**O servidor é open source?**
O servidor é proprietário (hosted). Este repositório é o wrapper público com manifestos, docs e skills — tudo MIT.

**Posso usar com agente próprio (não Claude/Cursor)?**
Sim — qualquer cliente que suporte MCP over HTTP. URL: `https://api.mcp.ai/p_worldcup`.


---

## Suporte

- 📧 [worldcup@mcp.ai](mailto:worldcup@mcp.ai)
- 🐛 [GitHub Issues](https://github.com/mcp-dir/worldcup-mcp/issues)
- 📄 [docs/](docs/)

---

## Licença

MIT — veja [LICENSE](LICENSE). O servidor MCP em `api.mcp.ai/p_worldcup` é proprietário (hosted); este repositório (manifestos, docs, skills) é MIT.
