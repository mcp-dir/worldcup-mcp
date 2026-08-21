# Ferramentas

Copa do Mundo 2026 expõe 8 ferramentas (todas somente leitura).

### 1. `worldcup_matches`
**Input**: `date` (opcional), `team` (opcional), `group` (opcional), `stage` (opcional), `status` (opcional), `timezone` (opcional)

Jogos da Copa do Mundo 2026 com placar e horário.

### 2. `worldcup_schedule`
**Input**: `date` (opcional), `stage` (opcional), `timezone` (opcional)

Calendário do torneio agrupado por data.

### 3. `worldcup_results`
**Input**: `date` (opcional), `team` (opcional), `group` (opcional)

Resultados (placares finais) dos jogos já encerrados.

### 4. `worldcup_groups`
**Input**: `group` (opcional)

Composição dos grupos (12 grupos de 4 seleções) com as equipes e os jogos de cada grupo.

### 5. `worldcup_standings`
**Input**: `group` (opcional)

Classificação (tabela) dos grupos: pontos, jogos, vitórias, empates, derrotas, saldo de gols.

### 6. `worldcup_bracket`
**Input**: `stage` (opcional)

Chaveamento do mata-mata (16 avos até a final) com os confrontos e os classificados conhecidos.

### 7. `worldcup_teams`
**Input**: `team` (opcional), `confederation` (opcional)

Seleções participantes (48 no total) com ranking FIFA e confederação.

### 8. `worldcup_venues`
**Input**: `city` (opcional), `venue` (opcional)

Estádios-sede (16 nos EUA, México e Canadá): cidade, capacidade e os jogos de cada sede.

## Prompts de exemplo

```
Que horas joga o Brasil hoje na Copa?
Quais os jogos de hoje da Copa do Mundo?
Como está a tabela do grupo do Brasil?
Mostra o chaveamento do mata-mata
```
