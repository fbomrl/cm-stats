# CM Stats Tracker

Dashboard pessoal para acompanhar carreira de técnico no **Championship Manager 01/02** (versão atualizada).

🔴 **[Ver Dashboard →](https://SEU_USUARIO.github.io/cm-stats-tracker)**

---

## Funcionalidades

- **Elenco** — tabela de jogadores com KPIs, filtros de ordenação, bandeiras e editor de posição
- **Campo** — pitch SVG com formações (4-4-2 / 4-3-3 / 3-5-2), modo Auto e Manual
- **Campeonatos** — histórico de competições e painel de títulos
- **Múltiplas carreiras** — seletor no header, cor do clube dinâmica

## Estrutura

```
cm-stats-tracker/
├── index.html              ← dashboard principal
├── careers.json            ← lista de carreiras
├── careers/
│   └── braga-2025/
│       ├── players.json
│       ├── tournaments.json
│       └── meta.json
└── README.md
```

## Adicionar nova carreira

1. Criar pasta `careers/NOME-DA-CARREIRA/`
2. Criar `players.json`, `tournaments.json`, `meta.json`
3. Adicionar entrada em `careers.json`

## Atualizar stats via screenshot

Enviar ao assistente de IA 3 prints por temporada:
1. Todos os jogadores + **Gols**
2. Todos os jogadores + **Assistências**
3. Todos os jogadores + **Presenças**

O assistente lê os valores e atualiza o `players.json`.

**Regra de presenças:** `"10 (9)"` = somar = 19 presenças totais.
