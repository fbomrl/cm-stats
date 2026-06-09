# CM Stats — Protocolo de Atualização de Temporada

> Arquivo de referência para o assistente de IA. Ler antes de qualquer atualização.

---

## REGRAS FIXAS

- **Nome dos jogadores:** sempre exatamente como aparece no jogo (CM 01/02 atualizado)
- **Presenças:** `X (Y)` = X titular + Y substituto = somar os dois
- **Jogadores em azul escuro** = emprestados a outro clube → **ignorar** nos prints
- **Jogadores que não aparecem nos prints** = saíram do clube
- **Temporada em andamento:** nunca fechar totals até confirmação explícita do usuário
- **Nomes repetidos entre prints:** contar apenas uma vez

---

## JOGADORES QUE SAÍRAM DO CLUBE

Quando um jogador sai do clube:
- Manter o histórico dele no `players.json` (não deletar)
- Adicionar `"left_club": true` no objeto do jogador
- No dashboard, exibir `!` após o nome com tooltip: **"Saiu do clube"**

---

## CHECKLIST PÓS-PRINTS (fazer a cada atualização)

### 1. Jogadores novos (não existem no JSON ainda)
Perguntar ao usuário:
- [ ] **Nacionalidade principal** (país + código ISO para bandeira)
- [ ] **Segunda nacionalidade** (se tiver)
- [ ] **Posição principal** (GO / ZG / LE / LD / VL / MC / ME / MD / MA / AE / AD / AC / CA)
- [ ] **Posição secundária** (se tiver)

### 2. Jogadores existentes (já estão no JSON)
- [ ] Adicionar nova entrada em `seasons[]` com a temporada atual
- [ ] Recalcular `totals` (appearances, goals, assists, seasons_count)
- [ ] Recalcular `career_totals`

### 3. Temporada
- [ ] **Nome da temporada** — ex: `2025/26` (confirmar com usuário se não estiver claro)
- [ ] **Temporada encerrada?** — só fechar totals após confirmação explícita

### 4. Campeonatos (só após encerramento da temporada)
- [ ] Primeira Liga
- [ ] Taça de Portugal
- [ ] Supertaça
- [ ] Champions League
- [ ] Europa League
- [ ] Recopa Europeia
- [ ] Mundial de Clubes

---

## POSIÇÕES DISPONÍVEIS

| Grupo | Código | Nome |
|---|---|---|
| Goleiro | GO | Goleiro |
| Defesa | ZG | Zagueiro |
| Defesa | LE | Lateral Esquerdo |
| Defesa | LD | Lateral Direito |
| Meia | VL | Volante |
| Meia | MC | Meia Central |
| Meia | ME | Meia Esquerdo |
| Meia | MD | Meia Direito |
| Meia | MA | Meia Atacante |
| Atacante | AE | Atacante Esquerdo |
| Atacante | AD | Atacante Direito |
| Atacante | AC | Atacante de Centro |
| Atacante | CA | Centro Avante |

---

## CÓDIGOS ISO DE BANDEIRAS (circle-flags)

| País | Código |
|---|---|
| Brasil | br |
| Portugal | pt |
| Espanha | es |
| França | fr |
| Argentina | ar |
| Uruguai | uy |
| Colômbia | co |
| Itália | it |
| Alemanha | de |
| Holanda | nl |
| Camarões | cm |
| Senegal | sn |
| Costa do Marfim | ci |
| Nigéria | ng |
| Bélgica | be |
| Croácia | hr |
| Rep. Tcheca | cz |
| Inglaterra | gb-eng |
| Geórgia | ge |
| Suécia | se |
| Angola | ao |
| Guiné-Bissau | gw |

---

## HISTÓRICO DE ELENCO

### Temporada 2025/26 (em andamento)

**Jogadores confirmados no elenco:**
Igor Gomes, Rúben Neves, Gabriel Magalhães, Alessandro Nunziante, Luca Meirelles, Angeliño, Daniel Silva, Malang Sarr, Breno Vereza, Serge Daura, Danilo, Ricardo Horta, Rodrigo Zalazar, Fábio Vieira, Gabriel Gorgulho, Dell, Saba Kharebashvili, Willam Fernando, Thierry Henry, Arthur, Ruan Pablo, Figueiredo, Mário Martín, Marcos Cabrobó, Robson, Gustaf Lagerbielke, Chissumba, Julio Fidelis, Romário Cunha, Tiago Ferreira, Mycael

**Jogadores novos (pendente nacionalidade/posição):**
Dell, Saba Kharebashvili, Willam Fernando, Thierry Henry, Arthur, Ruan Pablo, Figueiredo, Mário Martín, Marcos Cabrobó, Robson, Gustaf Lagerbielke, Chissumba, Julio Fidelis, Romário Cunha, Tiago Ferreira, Mycael, Fábio Vieira

**Saíram do clube (comparado ao elenco anterior):**
SERGE DAURA ✓ (ainda no clube), GUSTAVO ZABARELLI ?, FRAN NAVARRO ?, PAULO OLIVEIRA ?, ANGELIÑO ✓, RÚBEN NEVES ✓, LUKAS ZUCCARELLO ?, GABRIEL MOSCARDO ?, VÍCTOR GÓMEZ ?, JOÃO MOUTINHO ?, GABRIEL GORGULHO ✓, LUKAS HORNICEK ?, ALESSANDRO NUNZIANTE ✓
*(confirmar saídas definitivas com usuário)*
