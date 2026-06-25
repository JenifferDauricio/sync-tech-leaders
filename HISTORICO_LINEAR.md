# Histórico de sincronização — BHub Tech × Linear

Log cumulativo de tudo que é puxado do Linear a cada sincronização dos painéis `bhub-projeto-tech-v3.html` (Autopilot) e `bhub-projetos-tech-portfolio.html` (Portfólio: 10 projetos · Autopilot + Cockpit + Hub).
A cada execução (12h e 19h), uma nova seção é **acrescentada no topo** — nada é apagado. Trilha de auditoria da evolução dos projetos Tech.

Convenções: saúde = farol do Project Update (No prazo / Em risco / Off track) · % = milestone do Linear · data alvo da entrega = maior `dueDate` entre as sub-issues · "A definir" = sem `dueDate` no Linear.
**Regra de %: o painel exibe o % real do milestone do Linear, incluindo 100% quando o projeto está concluído. (O teto antigo de 90% foi removido em 19/06, confirmado com Gabriel Bicalho — GDocs estão realmente 100%.)**
**Cada execução registra a ⏱ duração (início → fim) no cabeçalho do snapshot, para acompanhar o tempo de atualização ao longo do tempo.**

---

## 2026-06-25 · 15h UTC — snapshot · ⏱ 6m 12s

**Refresh de milestones dos motores — avanço real desde a sync das 12h.** Nenhum Project Update novo dos 15 projetos na semana (o último é Design System v1.4.1 de 24/06, fora dos painéis; Offboarding/Geladeira de 23/06 já refletido). Hub (solicitacoes-dp, gdocs-multicnpj, gdocs-acompanhamento) reconferido — sem reporte novo. Mas o `progress` real dos milestones dos 4 motores subiu desde 12h (issues concluídas ao longo do dia), então `pctLinear` foi atualizado nos **dois painéis**.

**Mudanças aplicadas (ambos os painéis):**
- `pctLinear` Motor Fiscal SN (Motor de Cálculo SN): **27% → 30%**.
- `pctLinear` RPA Fiscal (Construção de RPAs): **87% → 88%**.
- `pctLinear` Motor Trabalhista (Pró-Labore SN): **69% → 70%**.
- `pctLinear` Motor Contábil (Motor Entregue): **28% → 30%**.
- `marcoLinear` Motor Fiscal SN: "(Classificação SN em **42%**)" → "(Classificação SN em **45%**)".
- Subtítulo do Dashboard: já em **25/06** (hoje) nos dois painéis — sem alteração.
- `REPORTS`, `CONSOLIDADO`, `marcos` (Cockpit/Hub/backlog), `dependencias`: **sem alteração** (nenhum reporte novo dos 15 projetos).

**Milestones lidos do Linear (% real):** Classificação SN **45%** · Motor de Cálculo SN **30%** · RPA Construção **88%** · Pró-Labore SN **70%** · Folha s/ apont. **18%** (sem variação) · Motor Contábil **30%**.

**Dashboard após refresh:** Autopilot (4 motores) média **~54%** · 1 No prazo · 3 Em risco. Portfólio (15 projetos) média **~44%** · 6 No prazo · 7 Em risco · 2 Off track. (Faróis/health inalterados — sem novo Project Update.)

| Projeto | Squad | Saúde | % (milestone) | Δ desde 25/06 12h |
| -- | -- | -- | -- | -- |
| Motor Fiscal SN | Fiscal | 🟡 Em risco | 30% (Cálculo SN) | +3 · Classif. 42%→45% |
| RPA Fiscal | Fiscal | 🟢 No prazo | 88% (Construção RPAs) | +1 |
| Motor Trabalhista (DP) | DP | 🟡 Em risco | 70% (Pró-Labore SN) | +1 · Folha s/ apont. 18% |
| Motor Contábil | Contábil | 🟡 Em risco | 30% (Motor Entregue) | +2 |
| Solicitações DP | Hub | 🟡 Em risco | 85% | — |
| Triagem OCR | Cockpit | 🟢 No prazo | 75% | — |
| Copiloto Samurai | Cockpit | 🟡 Em risco | 10% (bloqueado) | — |
| BPO Financeiro | Cockpit | 🟡 Em risco | 10% (bloqueado) | — |
| GDocs multi-CNPJ | Hub | 🟢 No prazo | 100% | — |
| GDocs acompanhamento | Hub | 🟢 No prazo | 100% | — |
| PMI Digital | Cockpit | 🔴 Off track | 0% (bloqueado) | — |
| Cockpit 100% | Cockpit | 🟢 No prazo | 30% | — |
| Cadastro Único | Cockpit | 🟡 Em risco | 25% | — |
| Hubcount | Contábil | 🟢 No prazo | 0% (pré-spec) | — |
| Offboarding | Cockpit | 🔴 Off track | 0% (Geladeira) | — |

**Observações:** apenas DADOS (% dos milestones) atualizados — nenhuma alteração de lógica/JS. Marcos de Cockpit/Hub/backlog não re-puxados nesta execução (sem reporte/atividade nova; sem cruzar limiares 0%/100%). Validação: 2 blocos `<script>` por painel, `node --check` + smoke test (DOM stub; dashboard/okr/exec/projetos/raid/reports executados sem erro) — ambos OK.

---

## 2026-06-25 · 12h UTC — snapshot · ⏱ 859m 28s (intervalo do agendador; processamento ativo ~2 min)

**Nenhum Project Update novo dos 15 projetos monitorados na semana.** Desde a última sync (24/06 15h11) o único update novo no Linear é *Design System v1.4.1* (24/06 11h27, Arthur Moreira, 🟢 On track — fix do DatePicker CDSG-10, locale pt-BR), que **não faz parte dos 15 projetos dos painéis** → fora de REPORTS/CONSOLIDADO. Hub (solicitacoes-dp, gdocs-multicnpj, gdocs-acompanhamento) conferido — sem reporte novo na semana; status mantidos. Offboarding (Geladeira, 23/06) já refletido no snapshot anterior. Esta execução refez o *refresh do % real dos milestones* dos motores via `list_milestones` (todos sem variação) e atualizou o subtítulo do Dashboard para 25/06.

**Mudanças aplicadas:**
- Subtítulo do Dashboard (**ambos os painéis**): "dados e reportes do Linear · 23/06" → "· 25/06".
- Milestones (refresh, % real, **sem variação**): Classificação SN **42%** (41,90%) · Motor de Cálculo SN **27%** (26,52%) · RPA Construção **87%** (87,37%) · Pró-Labore SN **69%** (69,25%) · Folha s/ apont. **18%** (17,86%) · Motor Contábil **28%** (28,28%).
- `pctLinear` dos motores: **sem alteração** (27 / 87 / 69 / 28). `REPORTS`, `CONSOLIDADO` e `marcos`: **sem alteração** (nenhum reporte novo dos 15 projetos).

**Dashboard após refresh:** Autopilot (4 motores) média **53%** · 1 No prazo · 3 Em risco. Portfólio (15 projetos) média **43%** · 6 No prazo · 7 Em risco · 2 Off track. (Faróis inalterados.)

| Projeto | Squad | Saúde | % (milestone) | Δ desde 24/06 15h11 |
| -- | -- | -- | -- | -- |
| Motor Fiscal SN | Fiscal | 🟡 Em risco | 27% (Cálculo SN) | — · Classif. 42% |
| RPA Fiscal | Fiscal | 🟢 No prazo | 87% (Construção RPAs) | — |
| Motor Trabalhista (DP) | DP | 🟡 Em risco | 69% (Pró-Labore SN) | — · Folha s/ apont. 18% |
| Motor Contábil | Contábil | 🟡 Em risco | 28% (Motor Entregue) | — |
| Solicitações DP | Hub | 🟡 Em risco | 85% | — |
| Triagem OCR | Cockpit | 🟢 No prazo | 75% | — |
| Copiloto Samurai | Cockpit | 🟡 Em risco | 10% (bloqueado) | — |
| BPO Financeiro | Cockpit | 🟡 Em risco | 10% (bloqueado) | — |
| GDocs multi-CNPJ | Hub | 🟢 No prazo | 100% | — |
| GDocs acompanhamento | Hub | 🟢 No prazo | 100% | — |
| PMI Digital | Cockpit | 🔴 Off track | 0% (bloqueado) | — |
| Cockpit 100% | Cockpit | 🟢 No prazo | 30% | — |
| Cadastro Único | Cockpit | 🟡 Em risco | 25% | — |
| Hubcount | Contábil | 🟢 No prazo | 0% (pré-spec) | — |
| Offboarding | Cockpit | 🔴 Off track | 0% (Geladeira) | — |

**Observações:** subtítulo do Dashboard atualizado para 25/06 nos dois painéis. Sem alteração em lógica/JS — apenas o dado de data. Validação: 2 blocos `<script>` por painel, `node --check` + smoke test (DOM stub; renders dashboard/okr/exec/projetos/raid/reports executados sem erro) — ambos OK.

---


## 2026-06-24 · 15h11 UTC — snapshot · ⏱ 5m 51s

**Nenhum Project Update novo dos 15 projetos monitorados na semana.** O único update novo no Linear desde a última sync (23/06 22h13) é *Design System v1.4.1* (24/06 11h27, Arthur Moreira, 🟢 On track) — fix + update no DatePicker (CDSG-10, locale pt-BR), publicado em `@bhubai/bhub-design-system@1.4.1`. **Design System não faz parte dos 15 projetos dos painéis**, portanto não entra em REPORTS/CONSOLIDADO. Offboarding (Geladeira, 23/06) já refletido no snapshot anterior. Esta execução fez o *refresh do % real dos milestones* dos motores via `list_milestones`. Hub (solicitacoes-dp, gdocs-multicnpj, gdocs-acompanhamento) conferido — sem reporte novo na semana; status mantidos.

**Mudanças aplicadas:**
- Milestones (refresh, % real): **Motor de Cálculo SN 29→27%** (26,52%) · Classificação SN **42%** (41,90%, sem mudança) · RPA Construção **87%** (87,37%) · Pró-Labore **69%** (69,03%) · Folha s/ apont. **18%** (17,86%) · Motor Contábil **28%** (28,28%).
- `motor-fiscal-sn`: `pctLinear` 29→27 (nos dois painéis) · `marco` "M1 Classificação 42% · M2 Cálculo 27%" (era 38%/12%).
- `REPORTS`, `CONSOLIDADO` e `marcos`: **sem alteração** (nenhum reporte novo dos 15 projetos). Total de reportes inalterado.

**Dashboard após refresh:** Autopilot (4 motores) média **53%** · 1 No prazo · 3 Em risco. Portfólio (15 projetos) média **43%** · 6 No prazo · 7 Em risco · 2 Off track. (Faróis inalterados.)

| Projeto | Squad | Saúde | % (milestone) | Δ desde 23/06 22h13 |
| -- | -- | -- | -- | -- |
| Motor Fiscal SN | Fiscal | 🟡 Em risco | 27% (Cálculo SN) | 29→27 · Classif. 42 |
| RPA Fiscal | Fiscal | 🟢 No prazo | 87% (Construção RPAs) | — |
| Motor Trabalhista (DP) | DP | 🟡 Em risco | 69% (Pró-Labore SN) | — · Folha s/ apont. 18% |
| Motor Contábil | Contábil | 🟡 Em risco | 28% (Motor Entregue) | — |
| Solicitações DP | Hub | 🟡 Em risco | 85% | — |
| Triagem OCR | Cockpit | 🟢 No prazo | 75% | — |
| Copiloto Samurai | Cockpit | 🟡 Em risco | 10% (bloqueado) | — |
| BPO Financeiro | Cockpit | 🟡 Em risco | 10% (bloqueado) | — |
| GDocs multi-CNPJ | Hub | 🟢 No prazo | 100% | — |
| GDocs acompanhamento | Hub | 🟢 No prazo | 100% | — |
| PMI Digital | Cockpit | 🔴 Off track | 0% (bloqueado) | — |
| Cockpit 100% | Cockpit | 🟢 No prazo | 30% | — |
| Cadastro Único | Cockpit | 🟡 Em risco | 25% | — |
| Hubcount | Contábil | 🟢 No prazo | 0% (pré-spec) | — |
| Offboarding | Cockpit | 🔴 Off track | 0% (Geladeira) | — |

**Observações:** subtítulo do Dashboard auto-deriva de `new Date()` → 24/06. Sem alteração em lógica/JS — apenas dados (pctLinear/marco dos motores). Validação: 2 blocos `<script>` por painel, `node --check` + smoke test (DOM stub, renders executados sem erro) — ambos OK.

---


## 2026-06-23 · 22h13 UTC — snapshot · ⏱ 8m 13s

**1 novo Project Update na semana** — *Offboarding estruturado de cliente* (23/06, Ana Caroline): projeto **movido para a Geladeira** no Linear (`Status: Geladeira`, 🔴 Off track). Não será priorizado neste quarter — correções no processo operacional reduziram a urgência da demanda; **reavaliação em Q3/2026**. Nenhum outro projeto reportou desde 19/06 (lote já refletido nos snapshots anteriores). Esta execução também fez o *refresh do % real dos milestones* dos motores.

**Mudanças aplicadas:**
- `REPORTS` (Portfólio): **+1 entrada** — Offboarding 23/06 (Off track). Total 55 reportes; nenhum apagado.
- Offboarding: `statusProjeto` → "Geladeira" · `marcoLinear`/`marco` → "Geladeira (23/06) — despriorizado no quarter; reavaliação em Q3/2026" · `progresso` atualizado.
- `CONSOLIDADO` (semana 19/06): nota acrescida com a decisão de Geladeira do Offboarding em 23/06.
- Milestones (refresh): **Motor de Cálculo SN 28→29%** (29,31%) · **Classificação SN 44→42%** (41,90%) · **Motor Contábil 29→28%** (28,28%). Pró-Labore 68,81% e RPA Construção 87,12% sem mudança material.

**Dashboard após refresh:** Autopilot (4 motores) média **53%** · 1 No prazo · 3 Em risco. Portfólio (15 projetos) média **43%** · 6 No prazo · 7 Em risco · 2 Off track. (Faróis inalterados.)

| Projeto | Squad | Saúde | % (milestone) | Δ desde 17h09 |
| -- | -- | -- | -- | -- |
| Motor Fiscal SN | Fiscal | 🟡 Em risco | 29% (Cálculo SN) | 28→29 · Classif. 44→42 |
| RPA Fiscal | Fiscal | 🟢 No prazo | 87% (Construção RPAs) | — |
| Motor Trabalhista (DP) | DP | 🟡 Em risco | 69% (Pró-Labore SN) | — · Folha s/ apont. 18% |
| Motor Contábil | Contábil | 🟡 Em risco | 28% (Motor Entregue) | 29→28 |
| Solicitações DP | Hub | 🟡 Em risco | 85% | — |
| Triagem OCR | Cockpit | 🟢 No prazo | 75% | — |
| Copiloto Samurai | Cockpit | 🟡 Em risco | 10% (bloqueado) | — |
| BPO Financeiro | Cockpit | 🟡 Em risco | 10% (bloqueado) | — |
| GDocs multi-CNPJ | Hub | 🟢 No prazo | 100% | — |
| GDocs acompanhamento | Hub | 🟢 No prazo | 100% | — |
| PMI Digital | Cockpit | 🔴 Off track | 0% (bloqueado) | — |
| Cockpit 100% | Cockpit | 🟢 No prazo | 30% | — |
| Cadastro Único | Cockpit | 🟡 Em risco | 25% | — |
| Hubcount | Contábil | 🟢 No prazo | 0% (pré-spec) | — |
| Offboarding | Cockpit | 🔴 Off track | 0% (Geladeira) | status → Geladeira (23/06) |

**Observações:** subtítulo do Dashboard segue em 23/06. Sem alteração em lógica/JS — apenas dados/REPORTS/CONSOLIDADO. Validação: 2 blocos `<script>` por painel, `node --check` + smoke test (Dashboard/Exec/Projetos/RAID/Reports renderizados) — ambos OK.

---


## 2026-06-23 · 17h09 UTC — snapshot · ⏱ 35m 27s

**Sem novos Project Updates na semana** — o lote mais recente no Linear segue sendo o de 19/06 (já refletido no snapshot de 22/06). Esta execução fez o *refresh do % real dos milestones* (que alimenta o Dashboard) e atualizou o status de algumas issues que avançaram entre 20–23/06. `REPORTS`, `CONSOLIDADO` e `marcos` permanecem inalterados (nenhum reporte novo).

**Dashboard após refresh:** Autopilot (4 motores) média **53%** · 1 No prazo · 3 Em risco. Portfólio (15 projetos) média **43%** · 6 No prazo · 7 Em risco · 2 Off track.

| Projeto | Squad | Saúde | % (milestone) | Δ desde 22/06 |
| -- | -- | -- | -- | -- |
| Motor Fiscal SN | Fiscal | 🟡 Em risco | 28% (Cálculo SN) | 24→28 · Classif. 52→44 |
| RPA Fiscal | Fiscal | 🟢 No prazo | 87% (Construção RPAs) | 80→87 |
| Motor Trabalhista (DP) | DP | 🟡 Em risco | 69% (Pró-Labore SN) | 68→69 · Folha s/ apont. 18% |
| Motor Contábil | Contábil | 🟡 Em risco | 29% (Motor Entregue) | 26→29 |
| Solicitações DP | Hub | 🟡 Em risco | 85% | — |
| Triagem OCR | Cockpit | 🟢 No prazo | 75% | — |
| Copiloto Samurai | Cockpit | 🟡 Em risco | 10% (bloqueado) | — |
| BPO Financeiro | Cockpit | 🟡 Em risco | 10% (bloqueado) | — |
| GDocs multi-CNPJ | Hub | 🟢 No prazo | 100% | — |
| GDocs acompanhamento | Hub | 🟢 No prazo | 100% | — |
| PMI Digital | Cockpit | 🔴 Off track | 0% (bloqueado) | — |
| Cockpit 100% | Cockpit | 🟢 No prazo | 30% | — |
| Cadastro Único | Cockpit | 🟡 Em risco | 25% | — |
| Hubcount | Contábil | 🟢 No prazo | 0% (pré-spec) | — |
| Offboarding | Cockpit | 🔴 Off track | 0% (bloqueado) | — |

**O que mudou nas issues (verificado no Linear, 20–23/06):**
- **FIS-188** Painel RPA de controle interno → **Concluído** (completado 23/06).
- **FIS-193** Escrituração NFS-e tomados (Parte 2) → **Em revisão** (era Em andamento).
- **FIS-287** E4 · Painel & observabilidade RPA → **Em andamento** (era Em revisão).
- **DP-58** Empréstimo consignado em folha → **Concluído** (completado 22/06).
- **DP-103 / DP-106 / DP-107 / DP-109** (fechamento de folha) → **Refinado** (eram Pendente).
- Milestones: Cálculo SN 28,45% · Classificação SN 43,75% · RPA Construção 87,12% · Pró-Labore 68,81% · Folha s/ apont. 17,86% · Motor Contábil 28,69%.
- Subtítulo do Dashboard atualizado para 23/06. Nenhuma alteração em lógica/JS — apenas dados.

---

## 2026-06-22 · 16h16 UTC — snapshot · ⏱ 71m 28s

Re-execução do dia (3ª carga de 22/06). **Sem novos Project Updates no Linear desde 19/06** — `get_status_updates` (type:project, orderBy createdAt, limit 6) retorna os 6 updates mais recentes do workspace, todos de 19/06; o mais novo segue sendo **Copiloto Samurai, 19/06 18:04 UTC**. Logo %, saúde, marcos, REPORTS, CONSOLIDADO e marcos dos 15 projetos permanecem os da carga de 19/06.

> Nota de cronometragem: a ⏱ é wall-clock medida do primeiro ao último `date +%s` (inclui latência de ferramentas/LLM e o tempo de conectar a pasta). Processamento ativo de sincronização ≈ poucos minutos.

Estado dos painéis nesta execução (nada a alterar nos dados):
- Subtítulo do Dashboard já em **· 22/06** nos dois painéis (v3 linha 449 · portfólio linha 555) — sem alteração.
- CONSOLIDADO do portfólio na semana **2026-06-19** (semana de report mais recente) — mantido.
- Sem novas entradas em REPORTS / CONSOLIDADO / marcos (nenhum report novo na semana). **Hub conferido** (solicitacoes-dp, gdocs-multicnpj, gdocs-acompanhamento) — os três reportaram em 19/06 (Gabriel Carvalho); nenhum ficou pausado indevidamente.
- Escolha autônoma registrada: com zero Project Updates novos no workspace desde 19/06, não foi refeito o pull de 250 issues/milestones — os painéis já refletem a carga de 19/06 validada nas execuções anteriores (mesma conduta das cargas de 12h e 11h55).
- **Validação:** `node --check` dos 2 scripts inline por painel — OK. Smoke test (DOM stub com `scrollTo`/`matchMedia`) renderizando dashboard/exec/projetos/raid/reports/deps/okr + `openDealById` em todos os projetos — **ambos OK**. Contagens: **v3 → 4 motores · 24 reports · 14 dependências · maxPct 80** · **portfólio → 15 projetos · 4 motores · 54 reports · 17 dependências · CONSOLIDADO semana 2026-06-19 · maxPct 100** (confirma que o teto de 90% segue removido — GDocs em 100%).
- Publicado no GitHub (push de `HISTORICO_LINEAR.md`; os 4 demais arquivos sem alteração → "nothing to commit" nesse subconjunto).

**Snapshot dos 15 projetos (sem alteração vs. carga de 19/06):**

| Projeto | Squad | OKR | Saúde | % milestone (Linear) |
| -- | -- | -- | -- | -- |
| Motor Fiscal SN | Fiscal | O4 | 🟡 Em risco | 24% — Construção Motor de Cálculo SN (Classificação SN 52%) |
| RPA Fiscal | Fiscal | O4 | 🟢 No prazo | 80% — Construção de RPAs (Escrituração e guias) |
| Motor Trabalhista (DP) | DP | O4 | 🟡 Em risco | 68% — Construção Pró-Labore SN (Folha s/ apont. 18%) |
| Motor Contábil | Contábil | O4 | 🟡 Em risco | 26% — Construção Motor Contábil Entregue |
| Solicitações DP | Hub | O4 | 🟡 Em risco | 85% — DP1.M1 V1 no ar + piloto (Carnevale/BLN) |
| Triagem de Documentos (OCR) | Cockpit | O4 | 🟢 No prazo | 75% — M2 entregue · M3 em andamento |
| Copiloto Samurai | Cockpit | O4 | 🟡 Em risco | 10% — M1 em andamento · BLOQUEADO (Daniel indisponível) |
| BPO Financeiro | Cockpit | O5 | 🟡 Em risco | 10% — M1 Discovery (30/06) · BLOQUEADO |
| GDocs multi-CNPJ | Hub | O2 | 🟢 No prazo | 100% — GD1.M1 no ar |
| GDocs acompanhamento | Hub | O3 | 🟢 No prazo | 100% — GD2.M1 no ar |
| PMI Digital | Cockpit | O1 | 🔴 Off track | 0% — bloqueado desde 01/06 (despriorizado) |
| Cockpit 100% | Cockpit | O3 | 🟢 No prazo | 30% — M2 Top 200 grupos (1/4) |
| Cadastro Único | Cockpit | O3 | 🟡 Em risco | 25% — M1 em andamento (1/4) |
| Hubcount | Contábil | O5 | 🟢 No prazo | 0% — Pré-Spec · M1 (Spec) 15/07 |
| Offboarding estruturado | Cockpit | O5 | 🔴 Off track | 0% — M1 não iniciado (sem PM/eng) |

Dashboard: **6 No prazo · 7 Em risco · 2 Off track**. Consolidado 19/06 mantido: 13 projetos reportando; pausados: PMI Digital e Hubcount.

---

## 2026-06-22 · 11h55 UTC — snapshot · ⏱ 5m 15s

Re-execução do dia (após a carga das 12h). **Sem novos Project Updates no Linear desde 19/06** — `get_status_updates` (type:project, orderBy createdAt, limit 8) retorna os 8 updates mais recentes do workspace, todos de 19/06 (mais novo: **Copiloto Samurai, 19/06 18:04 UTC**). Logo %, saúde e marcos dos 15 projetos seguem os da carga de 19/06.

Estado dos painéis nesta execução (nada a alterar nos dados):
- Subtítulo do Dashboard já em **· 22/06** nos dois painéis (v3 linha 449 · portfólio linha 555).
- CONSOLIDADO do portfólio na semana **2026-06-19** (semana de report mais recente) — mantido.
- Sem novas entradas em REPORTS / CONSOLIDADO / marcos (nenhum report novo na semana). Hub conferido (solicitacoes-dp, gdocs-multicnpj, gdocs-acompanhamento) — os três já reportaram em 19/06; nenhum ficou pausado indevidamente.
- **Validação:** `node --check` (compile) dos 2 scripts inline por painel — OK. Smoke test (DOM stub) renderizando dashboard/exec/projetos/raid/reports/deps/okr + `openDealById` — **ambos OK**. Contagens: **v3 → 4 motores · 24 reports · 14 dependências** · **portfólio → 15 projetos · 54 reports · 17 dependências**.
- Publicado no GitHub (push de `HISTORICO_LINEAR.md`; os 4 demais arquivos sem alteração → "nothing to commit" nesse subconjunto).

**Snapshot dos 15 projetos (sem alteração vs. carga de 19/06):**

| Projeto | Squad | OKR | Saúde | % milestone (Linear) |
| -- | -- | -- | -- | -- |
| Motor Fiscal SN | Fiscal | O4 | 🟡 Em risco | 24% — Construção Motor de Cálculo SN (Classificação SN 52%) |
| RPA Fiscal | Fiscal | O4 | 🟢 No prazo | 80% — Construção de RPAs (Escrituração e guias) |
| Motor Trabalhista (DP) | DP | O4 | 🟡 Em risco | 68% — Construção Pró-Labore SN (Folha s/ apont. 18%) |
| Motor Contábil | Contábil | O4 | 🟡 Em risco | 26% — Construção Motor Contábil Entregue |
| Solicitações DP | Hub | O4 | 🟡 Em risco | 85% — DP1.M1 V1 no ar + piloto (Carnevale/BLN) |
| Triagem de Documentos (OCR) | Cockpit | O4 | 🟢 No prazo | 75% — M2 entregue · M3 em andamento |
| Copiloto Samurai | Cockpit | O4 | 🟡 Em risco | 10% — M1 em andamento · BLOQUEADO (Daniel indisponível) |
| BPO Financeiro | Cockpit | O5 | 🟡 Em risco | 10% — M1 Discovery (30/06) · BLOQUEADO |
| GDocs multi-CNPJ | Hub | O2 | 🟢 No prazo | 100% — GD1.M1 no ar |
| GDocs acompanhamento | Hub | O3 | 🟢 No prazo | 100% — GD2.M1 no ar |
| PMI Digital | Cockpit | O1 | 🔴 Off track | 0% — bloqueado desde 01/06 (despriorizado) |
| Cockpit 100% | Cockpit | O3 | 🟢 No prazo | 30% — M2 Top 200 grupos (1/4) |
| Cadastro Único | Cockpit | O3 | 🟡 Em risco | 25% — M1 em andamento (1/4) |
| Hubcount | Contábil | O5 | 🟢 No prazo | 0% — Pré-Spec · M1 (Spec) 15/07 |
| Offboarding estruturado | Cockpit | O5 | 🔴 Off track | 0% — M1 não iniciado (sem PM/eng) |

Dashboard: **6 No prazo · 7 Em risco · 2 Off track**. Consolidado 19/06 mantido: 13 projetos reportando; pausados: PMI Digital e Hubcount.

---

## 2026-06-22 · 12h UTC — snapshot · ⏱ ~4 min (tempo ativo)

> Nota de cronometragem: o relógio da sessão saltou de 20/06 para 22/06 durante a execução, então o diff bruto início→fim (~2.682 min) é artefato de relógio e **não** representa o processamento. Tempo ativo de sincronização ≈ 4 min.

Execução de fim de semana. **Sem novos Project Updates no Linear desde a sincronização de 19/06** — varredura `get_status_updates` (type:project, orderBy createdAt) confirma que o update mais recente do workspace é Copiloto Samurai, 19/06 18:04 UTC. Portanto %, saúde e marcos dos 15 projetos **permanecem os da carga de 19/06** (Portfólio já tinha as 21 entradas de 19/06; v3 já tinha os 4 reports de motores de 19/06).

Validação cruzada dos diffs de 19/06 contra os painéis (todos batem, nada a alterar):
- Motor Fiscal SN: Classificação 60→52% · Cálculo 12→24% → `pctLinear:24` ✓
- RPA Fiscal: Construção de RPAs 75→80% → `pctLinear:80` ✓
- Motor Trabalhista: Folha s/ apont. 22→18% (Pró-Labore 68%) → `pctLinear:68` ✓
- Motor Contábil: Construção 7→26% → `pctLinear:26` ✓

Alterações desta execução:
- **Subtítulo do Dashboard** atualizado para a data de hoje (**· 22/06**) nos dois painéis (v3 e portfólio).
- Sem novas entradas em REPORTS, CONSOLIDADO ou marcos (nenhum report novo na semana). Hub conferido (solicitacoes-dp, gdocs-multicnpj, gdocs-acompanhamento) — todos já com report de 19/06; nenhum ficou pausado indevidamente.
- **Validação:** `node --check` nos 4 scripts inline (2 por painel) — OK. Smoke test (DOM stub) renderizando dashboard/exec/projetos/raid/reports/deps/okr + `openDealById` — **ambos OK** (v3: 4 motores · 24 reports · portfólio: 15 projetos · 54 reports).

**Snapshot dos 15 projetos (sem alteração vs. carga de 19/06):**

| Projeto | Squad | OKR | Saúde | % milestone (Linear) |
| -- | -- | -- | -- | -- |
| Motor Fiscal SN | Fiscal | O4 | 🟡 Em risco | 24% — Construção Motor de Cálculo SN (Classificação SN 52%) |
| RPA Fiscal | Fiscal | O4 | 🟢 No prazo | 80% — Construção de RPAs (Escrituração e guias) |
| Motor Trabalhista (DP) | DP | O4 | 🟡 Em risco | 68% — Construção Pró-Labore SN (Folha s/ apont. 18%) |
| Motor Contábil | Contábil | O4 | 🟡 Em risco | 26% — Construção Motor Contábil Entregue |
| Solicitações DP | Hub | O4 | 🟡 Em risco | 85% — DP1.M1 V1 no ar + piloto (Carnevale/BLN) |
| Triagem de Documentos (OCR) | Cockpit | O4 | 🟢 No prazo | 75% — M2 entregue · M3 em andamento |
| Copiloto Samurai | Cockpit | O4 | 🟡 Em risco | 10% — M1 em andamento · BLOQUEADO (Daniel indisponível) |
| BPO Financeiro | Cockpit | O5 | 🟡 Em risco | 10% — M1 Discovery (30/06) · BLOQUEADO |
| GDocs multi-CNPJ | Hub | O2 | 🟢 No prazo | 100% — GD1.M1 no ar |
| GDocs acompanhamento | Hub | O3 | 🟢 No prazo | 100% — GD2.M1 no ar |
| PMI Digital | Cockpit | O1 | 🔴 Off track | 0% — bloqueado desde 01/06 (despriorizado) |
| Cockpit 100% | Cockpit | O3 | 🟢 No prazo | 30% — M2 Top 200 grupos (1/4) |
| Cadastro Único | Cockpit | O3 | 🟡 Em risco | 25% — M1 em andamento (1/4) |
| Hubcount | Contábil | O5 | 🟢 No prazo | 0% — Pré-Spec · M1 (Spec) 15/07 |
| Offboarding estruturado | Cockpit | O5 | 🔴 Off track | 0% — M1 não iniciado (sem PM/eng) |

Dashboard: **6 No prazo · 7 Em risco · 2 Off track**. Consolidado 19/06 mantido: 13 projetos reportando; pausados: PMI Digital e Hubcount.

---

## 2026-06-19 · 22h UTC — snapshot · ⏱ 5m 27s

Re-execução no mesmo dia. Sem novos Project Updates no Linear desde a sincronização anterior (último update: Copiloto Samurai, 18:04 UTC) — portanto %, saúde e marcos permanecem os da última carga. Esta execução fez **higiene de dados**:

- **REPORTS (Portfólio):** removidas **2 entradas duplicadas de 19/06** — `gdocs-multicnpj` e `gdocs-acompanhamento` apareciam duas vezes na mesma semana (double-add da execução anterior). Mantida a entrada mais recente de cada; histórico de semanas anteriores preservado (56 → 54 reports).
- **Consolidado (Portfólio):** corrigida a `nota` da semana 19/06 — dizia incorretamente que *"Copiloto Samurai e BPO Financeiro: último report em 12/06"*, mas ambos reportaram em 19/06. Nota agora reflete que **PMI Digital e Hubcount** são os únicos sem report na semana (despriorizado / pré-spec).
- Painel Autopilot (`v3`): sem mudanças de dados (motores inalterados, sem duplicatas).
- Validação: `node --check` nos 4 scripts inline + smoke test (DOM stub) renderizando dashboard/exec/projetos/raid/reports + deal + abas de reports — **ambos os painéis OK**.

**Snapshot dos 15 projetos (sem alteração vs. carga anterior):**

| Projeto | Squad | OKR | Saúde | % milestone (Linear) |
| -- | -- | -- | -- | -- |
| Motor Fiscal SN | Fiscal | O4 | 🟡 Em risco | 24% — Construção Motor de Cálculo SN (Classificação SN 52%) |
| RPA Fiscal | Fiscal | O4 | 🟢 No prazo | 80% — Construção de RPAs (Escrituração e guias) |
| Motor Trabalhista (DP) | DP | O4 | 🟡 Em risco | 68% — Construção Pró-Labore SN (Folha s/ apont. 18%) |
| Motor Contábil | Contábil | O4 | 🟡 Em risco | 26% — Construção Motor Contábil Entregue |
| Solicitações DP | Hub | O4 | 🟡 Em risco | 85% — DP1.M1 V1 no ar + piloto (Carnevale/BLN) |
| Triagem de Documentos (OCR) | Cockpit | O4 | 🟢 No prazo | 75% — M2 entregue · M3 em andamento |
| Copiloto Samurai | Cockpit | O4 | 🟡 Em risco | 10% — M1 em andamento · BLOQUEADO (Daniel indisponível) |
| BPO Financeiro | Cockpit | O5 | 🟡 Em risco | 10% — M1 Discovery (30/06) · BLOQUEADO |
| GDocs multi-CNPJ | Hub | O2 | 🟢 No prazo | 100% — GD1.M1 no ar |
| GDocs acompanhamento | Hub | O3 | 🟢 No prazo | 100% — GD2.M1 no ar |
| PMI Digital | Cockpit | O1 | 🔴 Off track | 0% — bloqueado desde 01/06 (despriorizado) |
| Cockpit 100% | Cockpit | O3 | 🟢 No prazo | 30% — M2 Top 200 grupos (1/4) |
| Cadastro Único | Cockpit | O3 | 🟡 Em risco | 25% — M1 em andamento (1/4) |
| Hubcount | Contábil | O5 | 🟢 No prazo | 0% — Pré-Spec · M1 (Spec) 15/07 |
| Offboarding estruturado | Cockpit | O5 | 🔴 Off track | 0% — M1 não iniciado (sem PM/eng) |

Dashboard: **6 No prazo · 7 Em risco · 2 Off track**. Consolidado 19/06: 13 projetos reportando; pausados: PMI Digital e Hubcount.

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
