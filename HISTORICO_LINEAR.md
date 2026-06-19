# Histórico de sincronização — BHub Tech × Linear

Log cumulativo de tudo que é puxado do Linear a cada sincronização dos painéis `bhub-projeto-tech-v3.html` (Autopilot) e `bhub-projetos-tech-portfolio.html` (Portfólio: 10 projetos · Autopilot + Cockpit + Hub).
A cada execução (12h e 19h), uma nova seção é **acrescentada no topo** — nada é apagado. Trilha de auditoria da evolução dos projetos Tech.

Convenções: saúde = farol do Project Update (No prazo / Em risco / Off track) · % = milestone do Linear · data alvo da entrega = maior `dueDate` entre as sub-issues · "A definir" = sem `dueDate` no Linear.
**Regra de %: projeto nunca é exibido como 100% concluído — quando o milestone bate 100%, o painel limita a 90% e mantém o projeto "em andamento".**
**Cada execução registra a ⏱ duração (início → fim) no cabeçalho do snapshot, para acompanhar o tempo de atualização ao longo do tempo.**

---

## 2026-06-19 · ~22h UTC — squad HUB (lead + Solicitações DP) · ⏱ ~2 min

- **Solicitações DP** movido do squad Cockpit para o squad **HUB** (marcos da Matriz realinhados para área Hub).
- Lead do squad **HUB** padronizado como **Gabriel Bicalho Carvalho** (Solicitações DP + GDocs multi-CNPJ + GDocs acompanhamento). Squad HUB agora com 3 projetos.

---

## 2026-06-19 · ~21h30 UTC — Offboarding adicionado + report do Cadastro Único · ⏱ ~4 min

"Atualizar tudo": fechei os reports restantes de 19/06.
- **Offboarding estruturado de cliente** (Cockpit, O5) **adicionado ao painel** (15ª entrada) — 🔴 Off track/bloqueado desde 01/06 (sem PM/eng dedicados). Marcos M1–M3 (Pendente) na Matriz; report 19/06 incluído.
- **Cadastro Único** — report 19/06 (Daniel Pereira) incluído; saúde corrigida para 🟡 **Em risco** (era No prazo): decisão de CPF aprovada (16/06), M1 1/4, dependência da carga massiva (Cléber, 23/06).

Painel agora com **15 entradas** (13 do deck + GDocs desmembrado em 2 + Offboarding, que não está no deck). Dashboard: **6 No prazo · 7 Em risco · 2 Off track**. Consolidado de 19/06 com 13 projetos reportando; pausados: PMI Digital e Hubcount.

---

## 2026-06-19 · ~21h UTC — reports do Hub que não tinham entrado + Cockpit 100% · ⏱ ~5 min

Gabriel sinalizou que "as coisas do Hub não subiram direto": os dois GDocs **reportaram em 19/06** (14:42), mas o painel ainda não tinha esses updates no REPORTS — então apareciam como **pausados** no Consolidado da semana. Corrigido. Adicionados 3 Project Updates de 19/06 (fiéis ao Linear):
- **GDocs multi-CNPJ** → 🟢 No prazo · GD1.M1 **100%** (liberação ampla em produção, destaque no all hands; sem regressão). Próximo: 1ª leitura da taxa de substituição.
- **GDocs acompanhamento** → 🟢 No prazo · GD2.M1 **100%** (painel de acompanhamento em produção, à frente do target 22/06). Próximo: adoção pelo operador.
- **Cockpit 100%** → 🟢 No prazo · decisão de domésticas aprovada (16/06); M1 entregue, M2 (Top 200) 1/4. pctLinear 8→30; marco e marcos da Matriz atualizados (M1 Concluído, M2 Em andamento).

Consolidado de 19/06 agora com 11 projetos reportando; pausados na semana: PMI Digital (bloqueado), Cadastro Único e Hubcount (backlog, sem report). Dashboard segue 7 No prazo · 6 Em risco · 1 bloqueado. (Obs.: há também um update novo de "Offboarding estruturado de cliente" — projeto que não está no deck dos 13 nem no painel; pendente de decisão se entra.)

---

## 2026-06-19 · ~20h UTC — alinhamento com o Weekly Tech (4 projetos novos) + ajustes visuais · ⏱ ~7 min

Comparação do painel (10) com o deck Weekly Tech 19/06 (13 projetos): faltavam 4 projetos, todos em status **"Ideia"/backlog** no Linear (por isso não tinham entrado no painel, que cobria os em execução). Adicionados ao Portfólio (agora 14 entradas — o deck conta 13 porque agrupa os 2 GDocs como um só "Cockpit 100%"):
- **PMI Digital — completude + handshake M&A** (O1, Cockpit) — 🔴 Off track (bloqueado desde 01/06, despriorizado).
- **Cockpit 100% — mapa de completude PJ/PF/Foreign** (O3, Cockpit) — 🟢 No prazo · M1 8%.
- **Cadastro Único de Cliente — entidade canônica** (O3, Cockpit) — 🟢 No prazo · M1 1/4.
- **Hubcount — relatórios customizáveis** (O5, Contábil) — 🟢 No prazo · pré-Spec (M1 15/07).

Resultado: Dashboard agora **7 No prazo · 6 Em risco · 1 bloqueado**, batendo com o deck. Marcos dos 4 vieram de `list_milestones`; entram na Matriz (área = squad). Observação: o rótulo "Cockpit 100%" no deck é sobrecarregado — aparece para os GDocs (slide 5) e para a completude cadastral/bancária (slide 12); no Linear são projetos distintos.

Ajustes visuais: **Matriz mais compacta** (colunas/pílulas estreitas, classe `.mtx`) para caber os ~14 projetos; **legenda do Dashboard** com mais contraste (branco .72); **cor do squad Contábil** trocada para violeta (#7c3aed), distinta do ciano do Hub. Também: "report"→"reporte" em todos os textos visíveis e **clique no nome do projeto no Reporte Semanal** abre a aba do projeto.

---

## 2026-06-19 · ~19h UTC — ajustes de visualização (Matriz + Gantt + Dashboard + Sinergias) · ⏱ ~5 min

Mudanças estruturais nos painéis (marcos reais lidos do Linear via `list_milestones`):
- **Matriz tarefa × projeto** agora cobre os 10 projetos (antes só os motores Fiscal/DP). Incluído o squad **Contábil** (tarefas já existentes) e os 6 projetos **Cockpit/Hub** via seus marcos do Linear: Solicitações DP (DP1.M1–M3), Triagem OCR (M1–M5), Copiloto Samurai (M1–M3), BPO Financeiro (M1–M2), GDocs multi-CNPJ (GD1.M1), GDocs acompanhamento (GD2.M1).
- **Gantt de entregas**: linha tracejada separando cada projeto (nos dois painéis), leitura mais fácil.
- **Dashboard**: legenda "X de Y issues dos motores" trocada por "média do % de avanço (milestone) dos N projetos — report semanal" (o 56% e os faróis já derivam de pctLinear/health, ou seja, do report semanal; sync 2×/dia mantém atualizado).
- **Aba "Sinergias" removida** do detalhe do projeto (nos dois painéis) — nenhum dos 10 projetos tinha sinergia cadastrada no Linear.

Marcos/progresso lidos do Linear (19/06): Solicitações DP M1 85%, M2/M3 0% · Triagem OCR M1 20%, M4 83%, demais 0% · Samurai e BPO 0% (bloqueados) · GDocs GD1.M1 e GD2.M1 100% (exibidos como 90% na régua de % do projeto). Agendador atualizado para refrescar os `marcos` Cockpit/Hub a cada rodada.

---

## 2026-06-19 · ~18h UTC — sync (novos reports Cockpit) · ⏱ ~3 min

Dois Project Updates novos no Linear (postados ~17–18h de 19/06):
- **Copiloto Samurai** → 🔴 **bloqueado**: projeto parado, execução depende só do Daniel (alocado em DP/Cockpit), sem previsão de retomada. Saúde Em risco · % 10 (M1 em andamento).
- **BPO Financeiro** → 🔴 **bloqueado**: demanda do CFO (painel financeiro); faturamento não padronizado (pagamentos fora do sistema) trava o escopo do discovery. Saúde Em risco · % 10 (M1, 1/4 issues).

Ambos saíram de "pausado" para reportando na semana 19/06 no Consolidado. Demais 8 projetos sem mudança. Portfólio: 10 projetos · avanço médio 56% · 4 No prazo · 6 Em risco · 0 Off track.

---

## 2026-06-19 · 16:57 UTC — sync manual ("rodar agora") · ⏱ ~4 min (execução manual nesta sessão; cronometragem automática a partir das próximas rodadas)

Verificação: painéis refletem os Project Updates de 19/06 do Linear — sem mudanças desde a última montagem. Portfólio: **10 projetos · avanço médio 56%** · 4 No prazo · 6 Em risco · 0 Off track · 17 bloqueios · 6 ações de mitigação abertas.

| Projeto | Squad | Saúde | % milestone | Bloqueios |
|---|---|---|---|---|
| Motor Fiscal SN | Fiscal | Em risco | 24% (Cálculo SN; Classificação 52%) | 4 |
| RPA Fiscal | Fiscal | No prazo | 80% | 0 |
| Motor Trabalhista (DP) | DP | Em risco | 68% (Pró-Labore; Folha s/ apont. 18%) | 8 |
| Motor Contábil | Contábil | Em risco | 26% | 4 |
| Solicitações DP | Cockpit | Em risco | 85% (DP1.M1 V1+piloto) | 1 |
| Triagem OCR | Cockpit | No prazo | 75% (M2 ✓ · M3 em curso) | 0 |
| Copiloto Samurai | Cockpit | Em risco | 15% (M2 parado — capacidade) | 1 |
| BPO Financeiro | Cockpit | Em risco | 5% (Discovery M1) | 1 |
| GDocs multi-CNPJ | Hub | No prazo | 90% — em andamento (GD1.M1 no ar) | 0 |
| GDocs acompanhamento | Hub | No prazo | 90% — em andamento (GD2.M1 no ar) | 0 |

Mudanças vs. snapshot 12h: incorporados os squads **Cockpit** (4 projetos) e **Hub** (2 projetos) ao portfólio — antes o log cobria só os 4 motores. Datas das entregas dos motores inalteradas (Fiscal E1 03/07, E2 17/07, E4/E5 31/07; DP E1–E7 31/07; RPA E1/E2 03/07, E4 19/06; Contábil "A definir"). Pausados nesta semana: Copiloto Samurai e BPO Financeiro (último report 12/06). **Nova regra aplicada:** milestones em 100% (GDocs multi-CNPJ e acompanhamento) passam a ser exibidos como **90% · em andamento** — projeto nunca aparece como 100% concluído.

---

## 2026-06-19 · 12h — snapshot inicial

Avanço médio do portfólio: **50%** · Saúde: 1 No prazo · 3 Em risco · 0 Off track · Bloqueios: 14 · Ações de mitigação abertas: 6.

### Motor Fiscal SN — 🟡 Em risco · 24% (milestone Motor de Cálculo SN; Classificação SN 52%)
Lead: Jeisy Sousa · Cycle 3 (08–22/06).
- Entregas: E1 (FIS-299) → 03/07 · E2 (FIS-300) → 17/07 · E3 (FIS-301) → A definir · E4 (FIS-302) → 31/07 · E5 (FIS-303) → 31/07.
- Atrasadas: 0. Concluídas no painel: 2/22 issues.
- Diff semana: Classificação SN 60% → 52% · Cálculo SN 12% → 24%.
- Bloqueio operacional: decisão Jettax × Unecont (captura de notas), Jeni + Jorge, prazo 20/06 (FIS-124).

### RPA Fiscal — 🟢 No prazo · 80% (Construção de RPAs)
Lead: Jeisy Sousa · Cycle 3.
- Entregas: E1 (FIS-284) → 03/07 · E2 (FIS-285) → 03/07 · E3 (FIS-286) → A definir · E4 (FIS-287) → 19/06 · E1–E5 de rollout (FIS-351 a 355) → A definir.
- Atrasadas: 0. Concluídas: 12/27 issues.
- Diff semana: Construção de RPAs 75% → 80%.
- Sem bloqueios externos (workaround de município com API privada em produção).

### Motor Trabalhista (DP) — 🟡 Em risco · 68% (Construção Pró-Labore SN; Folha s/ apont. 18%)
Lead: Jeniffer Dauricio · Cycle 3.
- Entregas: E1–E6 (DP-113 a DP-118) → 31/07 · E7 (DP-135) → 31/07.
- Atrasadas: 0. Concluídas: 6/24 issues.
- Diff semana: Folha s/ apontamento 22% → 18%.
- Bloqueios operacionais: base de DEV sem dados de produção (Dan + Felipe, requer CPO, prazo 16/06) · acesso à API DataPrev / consignado (externo).

### Motor Contábil — 🟡 Em risco · 26% (Construção Motor Contábil Entregue)
Lead: Andressa Rodrigues · Cycle 3 · confiança do milestone 🔴 baixa.
- Entregas: E1–E8 (CTB-31 a CTB-39) → todas A definir (nenhuma issue com dueDate no Linear ainda).
- Atrasadas: 0. Concluídas: 1/30 issues.
- Diff semana: Construção Motor Contábil 7% → 26%.
- Bloqueios operacionais: decisões técnicas D1–D5 (comitê Jorge + Fernando, prazo 20/06) · Ledger Midaz na AWS dev (Paulo Dias, prazo 20/06).

### Reports semanais no painel (histórico, por projeto)
6 Project Updates por motor, de 15/05 a 19/06 (24 no total): 15/05 · 22/05 · 29/05 · 02–03/06 · 12/06 · 19/06.
- Fiscal SN: No prazo (15–22/05) → Em risco a partir de 28/05 (incidente de classificação automática).
- RPA: No prazo em todas as semanas.
- DP: No prazo (15–29/05) → Em risco a partir de 02/06 (API Cockpit / base de dados).
- Contábil: desprioritizado em 15/05 → discovery (22/05–02/06) → Em risco na construção (12–19/06).

---

<!-- Novas sincronizações entram ACIMA desta linha, sempre no topo da seção de histórico. -->
