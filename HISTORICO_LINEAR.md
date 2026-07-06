# Histórico de sincronização — BHub Tech × Linear

Log cumulativo de tudo que é puxado do Linear a cada sincronização dos painéis `bhub-projeto-tech-v3.html` (Autopilot) e `bhub-projetos-tech-portfolio.html` (Portfólio: 10 projetos · Autopilot + Cockpit + Hub).
A cada execução (12h e 19h), uma nova seção é **acrescentada no topo** — nada é apagado. Trilha de auditoria da evolução dos projetos Tech.

Convenções: saúde = farol do Project Update (No prazo / Em risco / Off track) · % = milestone do Linear · data alvo da entrega = maior `dueDate` entre as sub-issues · "A definir" = sem `dueDate` no Linear.
**Regra de %: o painel exibe o % real do milestone do Linear, incluindo 100% quando o projeto está concluído. (O teto antigo de 90% foi removido em 19/06, confirmado com Gabriel Bicalho — GDocs estão realmente 100%.)**
**Cada execução registra a ⏱ duração (início → fim) no cabeçalho do snapshot, para acompanhar o tempo de atualização ao longo do tempo.**

---

## 2026-07-06 · 22h11 UTC — snapshot · ⏱ 5m 49s (run de segunda-feira)

**Run de segunda (06/07, tarde UTC).** Varredura `get_status_updates` (type:project, orderBy createdAt, limit 6): **nenhum Project Update novo para os 15 projetos do portfólio** desde o sync anterior (06/07 01h34 UTC). O único update criado depois da última run é o **Espelhamento de docs (Gestta → Hub)** (06/07 01h59 UTC, 🟡 At risk) — projeto de sustentação Tech, **fora dos 15 do portfólio**, não aplicado aos painéis. Os demais updates recentes (Hidra · Manutenção, BHules — Motor de Classificação, Open Finance opt-in, SSOT) são de 03/07 e/ou fora do portfólio — já tratados em runs anteriores. Semana de reporte vigente segue 29/06–03/07.

**Deriva de milestone observada (NÃO aplicada — convenção: pctLinear acompanha o Project Update semanal, não a variação intra-semana):** via `list_projects` (includeMilestones) os milestones-alvo evoluíram desde o report de 03/07 — Motor Fiscal SN "Construção | Motor de Cálculo SN" **39% → 41%**; Motor Trabalhista "Pró-Labore SN" **72% → 74%**; Motor Contábil 36% (estável). Sem novo report semanal, os painéis mantêm os valores reportados em 03/07. Deriva registrada aqui para auditoria; será incorporada quando o próximo Project Update (semana 06/07–10/07) for postado.

**Aplicado nesta run:** apenas os **subtítulos** dos dois dashboards → **06/07** (data de hoje). Nenhuma alteração de dados/REPORTS/CONSOLIDADO/marcos — os 15 projetos permanecem idênticos ao snapshot anterior.

**Não** alterado: aba Sinergias, legenda "X de Y issues dos motores", teto de 90% (segue removido), Matriz compacta (.mtx), Contábil em violeta (#7c3aed), textos/click do Reporte Semanal (openDealById). Lógica/JS intactos.

**Validação:** os 2 `<script>` de cada painel extraídos → `node --check` (OK nos 4) + smoke test com DOM stub rodando o boot (renderDashboard/OKR/Exec/Projetos/Raid/Reports → 6 render fns por painel) → **PASS** nos dois. Edição em `.tmp` + validação + `mv` (arquivos só gravados após passar).

**Snapshot dos 15 projetos do portfólio (pctLinear · saúde):**

| Projeto | pctLinear | Saúde |
| -- | -- | -- |
| motor-fiscal-sn | 39% | 🟡 Em risco |
| rpa-fiscal | 82% | 🟡 Em risco |
| motor-trabalhista | 72% | 🟡 Em risco |
| motor-contabil | 36% | 🟡 Em risco |
| solicitacoes-dp | 99% | 🟡 Em risco |
| triagem-ocr | 72% | 🟢 No prazo |
| copiloto-samurai | 0% | 🔴 Off track (Geladeira) |
| bpo-financeiro | 10% | 🟡 Em risco |
| gdocs-multicnpj | 100% | 🟢 No prazo (Encerrado) |
| gdocs-acompanhamento | 100% | 🟢 No prazo (Encerrado) |
| pmi-digital | 0% | 🔴 Off track (Geladeira) |
| cockpit-100 | 90% | 🟢 No prazo |
| cadastro-unico | 6% | 🟡 Em risco |
| hubcount | 0% | 🟢 No prazo (Descoberta) |
| offboarding | 0% | 🔴 Off track (Geladeira) |

**Mudança vs. run anterior:** nenhuma nos dados dos 15 projetos (só subtítulo → 06/07). Deriva de milestone dos motores registrada mas não aplicada (aguarda próximo report semanal).

---

## 2026-07-06 · 01h34 UTC — snapshot · ⏱ 206m 9s (run de fim de semana)

**Run de domingo (05/07, madrugada UTC de 06/07).** Varredura `get_status_updates` (type:project, orderBy createdAt, −P4D e −P2D): **nenhum Project Update novo no fim de semana** (04–05/07). A postagem mais recente do Linear é o **Hidra · Manutenção** (03/07 23:10 UTC) — projeto de sustentação Contábil, **fora dos 15 do portfólio**, não aplicado aos painéis. Motores sem update novo → dados mantidos do sync de 03/07.

**Catch-up aplicado (1 report que a run de 03/07 22h14 não capturou):** o Project Update de **Cadastro Único / SSOT** ("Sincronização de informações de sistemas satélites e o cockpit (SSOT)") de **03/07 16:07 (Marina Alves, 🟡 Em risco)** estava dentro da semana reportada mas não fora incorporado. Aplicado agora:
- **cadastro-unico**: saúde **No prazo → Em risco** (corpo do update: "Em atenção"; health Linear = atRisk). Novo ownership (liderança → **Dan Jesus**, time **ACDA**); COCKPIT-268 concluída; semana concentrada em reorg de backlog (COCKPIT-391/392/393) sem avanço visível de execução. `pctLinear` mantido em **6%** (milestone M1 "Diagnóstico e regras de reconciliação" 6,25%; M2–M3 e demais 0% — confirmado via `list_milestones`). marcos mantidos.
- **REPORTS** do portfólio: **76 → 77** (entrada cadastro-unico 03/07 adicionada; nada apagado).
- **CONSOLIDADO** (semana 2026-07-03): adicionado item de cadastro-unico; **nota corrigida** — antes dizia "Cadastro Único ... sem report na semana", agora reflete que reportou (🟡 Em risco, novo ownership/reorg). BPO Financeiro segue sem report.
- **Subtítulos** dos dois dashboards → **05/07**.

**Não** alterado: aba Sinergias, legenda "X de Y issues dos motores", teto de 90% (segue removido), Matriz compacta (.mtx), Contábil em violeta (#7c3aed), textos/click do Reporte Semanal (openDealById). Lógica/JS intactos — só dados/REPORTS/CONSOLIDADO editados via script.

**Validação:** os 2 `<script>` de cada painel extraídos → `node --check` (OK nos 4) + smoke test com DOM stub rodando o boot (renderDashboard/OKR/Exec/Projetos/Raid/Reports) → **PASS** nos dois. Edição em `.tmp` + validação + `mv` (arquivos só gravados após passar).

**Snapshot dos 15 projetos do portfólio (pctLinear · saúde):**

| Projeto | pctLinear | Saúde |
| -- | -- | -- |
| motor-fiscal-sn | 39% | 🟡 Em risco |
| rpa-fiscal | 82% | 🟡 Em risco |
| motor-trabalhista | 72% | 🟡 Em risco |
| motor-contabil | 36% | 🟡 Em risco |
| solicitacoes-dp | 99% | 🟡 Em risco |
| triagem-ocr | 72% | 🟢 No prazo |
| copiloto-samurai | 0% | 🔴 Off track (Geladeira) |
| bpo-financeiro | 10% | 🟡 Em risco |
| gdocs-multicnpj | 100% | 🟢 No prazo (Encerrado) |
| gdocs-acompanhamento | 100% | 🟢 No prazo (Encerrado) |
| pmi-digital | 0% | 🔴 Off track (Geladeira) |
| cockpit-100 | 90% | 🟢 No prazo |
| cadastro-unico | 6% | 🟡 Em risco *(mudou de No prazo)* |
| hubcount | 0% | 🟢 No prazo (Descoberta) |
| offboarding | 0% | 🔴 Off track (Geladeira) |

**Mudança vs. run anterior:** apenas **cadastro-unico** (No prazo → Em risco, +1 report, item no CONSOLIDADO). Demais 14 projetos inalterados.

---

## 2026-07-03 · 22h14 UTC — snapshot · ⏱ 11m 11s (Linear reconectado)

**Conector do Linear voltou a funcionar** (a run das 15h07 havia falhado por conexão invalidada). Esta execução absorveu **3 Project Updates novos** que foram postados à tarde, **depois** do sync completo das 12h37 — exatamente os updates semanais dos motores que, no sync da manhã, ainda não existiam (a manhã usara milestone/issues como proxy). Varredura: `get_status_updates` (type:project, orderBy createdAt, −P3D, limit 8) + `list_projects`/`list_milestones` (por ID) do Motor Contábil.

**Novos Project Updates da semana (29/06–03/07) — adicionados a REPORTS do portfólio (append-only):**
- **Motor Fiscal SN** 🟡 At risk (Jeisy Sousa, 03/07 14h28): Motor de Cálculo (DAS) saiu do zero — repo (FIS-397), API base do General Ledger (FIS-398), integração com o BHules (FIS-399); Terraform em revisão (FIS-400), observabilidade em andamento (FIS-439). Gate de validação pelo operador (FIS-279) e Adapter SERPRO/e-CAC (FIS-330) concluídos; doc de pré-requisitos por obrigação (FIS-248) concluído. **Milestone Construção | Motor de Cálculo SN 29% → 39%** (v2 Oct/31 criado, 0%). FIS-279 marcada Concluída nos painéis.
- **Motor Trabalhista** 🟡 At risk (Andressa, 03/07 13h06): 3 das 4 entregas críticas de 03/07 concluídas — eSocial (DP-101), Readiness Anomalia 1 (DP-103), Anomalia 2 pós-cálculo (DP-134). DP-107 (disparo automático) em andamento; DP-109 iniciada. 3 itens due hoje não iniciados (DP-165 tabelas fiscais/IR Lei 15.270, DP-139 validação, DP-143 lista piloto consignado). **Milestone Pró-Labore SN 66% → 72%.**
- **RPA Fiscal** 🟡 At risk (Jeisy Sousa, 03/07 13h03): épico **E4 · Painel & observabilidade fechado** (FIS-287; infra dashboard FIS-232 concluída 01/07); Motor de Trigger BHules→RPA (FIS-260) detalhado em 9 sub-issues (FIS-430–438, due 06/07); bug FIS-257 corrigido. Testes por município (FIS-351) sem execução pela 3ª semana → Cobertura 100% em 0%, meta 31/07 inatingível. **Milestone Construção de RPAs 88% → 82%; target 31/07 → 31/08; saúde No prazo → Em risco.** FIS-287 marcada Concluída nos painéis.

**Também postados em 03/07 mas fora dos 15 do portfólio (não aplicados):** BHules — Motor de Classificação (projeto próprio, apartado do Motor Fiscal SN em 01/07; cobertura 100% da base SN); Open Finance opt-in; SSOT; Projeto Contexto; Gestor de Tarefas e Documentos.

**Motor Contábil:** sem update novo nesta janela (o de 03/07 já entrara na manhã). Milestone confirmado em **36%** via `list_projects`/milestones — mantido.

**CONSOLIDADO** da semana 2026-07-03 regravado (itens dos 3 motores atualizados do 26/06 para o report real de 03/07; nota da semana reescrita). **Subtítulos** dos dois dashboards já em 03/07 — mantidos. **Não** mexido: aba Sinergias, legenda "X de Y issues", teto de 90% (segue removido), Matriz compacta, Contábil em violeta, texto/click do Reporte Semanal.

**Validação:** os 2 `<script>` de cada painel extraídos → `node --check` (OK) + smoke test (DOM stub rodando o boot renderDashboard/OKR/Exec/Projetos/Raid/Reports) → **PASS** nos dois. Arquivos gravados só após passar (edição em `.tmp` + validação + `mv`).

**Snapshot dos 15 projetos do portfólio (pctLinear · saúde):**

| Projeto | % | Saúde |
| --- | --- | --- |
| Motor Fiscal SN | 39 | Em risco |
| RPA Fiscal | 82 | Em risco |
| Motor Trabalhista | 72 | Em risco |
| Motor Contábil | 36 | Em risco |
| Solicitações DP | 99 | Em risco |
| Triagem/OCR | 72 | No prazo |
| Copiloto Samurai | 0 | Off track (Geladeira) |
| BPO Financeiro | 10 | Em risco |
| GDocs multi-CNPJ | 100 | No prazo (Encerrado) |
| GDocs acompanhamento | 100 | No prazo (Encerrado) |
| PMI Digital | 0 | Off track (Geladeira) |
| Cockpit 100% | 90 | No prazo |
| Cadastro Único | 6 | No prazo |
| Hubcount | 0 | No prazo |
| Offboarding | 0 | Off track (Geladeira) |

> Nota: o `pctLinear` exibido é o milestone-cabeçalho de cada projeto. Solicitações DP (99 = milestone V1) e Triagem/OCR (72) têm sub-milestones críticos citados nos reports em patamar menor (DP: V3 51%; OCR: regras auditáveis 57%) — valores narrados no corpo do update, não no headline. Sem alteração nesses dois nesta run (sem update novo).

---

## 2026-07-03 · 15h07 UTC — run sem sync · ⏱ 2m 30s (conector Linear invalidado)

**⚠️ Execução não conseguiu sincronizar — conector do Linear desconectado.** Todas as chamadas ao MCP do Linear (`list_projects`, `get_status_updates`, `list_issues`) retornaram *"The user's connection to this connector was invalidated. The user needs to reconnect it."*. Como esta é uma run agendada (sem usuário presente), não foi possível reconectar.

**Ação tomada:** nenhum dado dos painéis foi alterado — não havia dados novos do Linear para aplicar. Os painéis permanecem no estado do último sync bem-sucedido (12h37 UTC de hoje, que já fez o re-sync completo da semana 29/06–03/07). Entrada registrada apenas para trilha de auditoria (append-only). **Ação necessária: reconectar o conector do Linear** para que a próxima execução volte a sincronizar normalmente.

---

## 2026-07-03 · 12h37 UTC — snapshot · ⏱ ~11m (relógio do sandbox instável; o ambiente avançou de 30/06 para 03/07 durante a run)

**Re-sync completo da semana de 29/06–03/07** (complementa o snapshot parcial das 12h, que só pegou task-status + subtítulo). Varredura: `get_status_updates` (type:project, orderBy createdAt, −P6D, limit 30) + `list_milestones` dos 4 motores + `list_issues` (updatedAt) de Fiscal/DP/RPA. **5 Project Updates novos da semana** foram absorvidos nos painéis (antes só havia reportes de 26/06).

**Novos Project Updates da semana (adicionados a REPORTS — append-only, nada apagado):**
- **Motor Contábil** 🟡 At risk (Andressa, 03/07): experiência contábil no Cockpit (pendências ao operador + telas do Gestor de Tarefas) finalizada pela Elaine, seguirá ao Jorge; dev de todas as frentes em andamento. Milestone construção **38% → 36%**.
- **Triagem/OCR** 🟢 On track (Ana Caroline, 03/07): Universo de documentos **65% → 100%** (02/07); Regras auditáveis **43% → 56,5%**; Fundação de confiança da classificação iniciada (proxy na API, 33%). pctLinear 65 → 57 (milestone ativo).
- **Cockpit 100%** 🟢 On track (Ana Caroline, 03/07): cobertura **100% PJ+PF+Estrangeiros** entregue 30/06; em estabilização (25%, janela 30d, 17/07). pctLinear 85 → 90.
- **Solicitações DP** 🟡 At risk (Gabriel Bicalho, 02/07): gestor de tarefas no Cockpit (fila geral, devolver à fila sem cancelar, filtros); validações inteligentes (Férias ok + Admissão); design reformulações forms HUB. **V3 15% → 51%**, V2.2 19% → 33%, V2.1 52% (novo). pctLinear 97 → 51 (milestone V3, crítico do gate Autopilot).
- **Hubcount** 🟢 On track (Andressa, 03/07): sem avanços; início previsto 01/08.

**Motores sem Project Update novo (último 26/06) — atualizados por milestone/issues:**
- **Motor Fiscal SN:** milestone Construção | Motor de Cálculo SN **29% → 38%** (38,46%). Tarefas: FIS-330 (Adapter SERPRO) Concluída; FIS-329 (API DAS) e FIS-279 (Anomalia 2) Em andamento; FIS-276 Refinado. Saúde Em risco mantida.
- **Motor Trabalhista:** Pró-Labore SN **66% → 72%** (72,39%); Folha s/ apontamento 17,86%. Tarefas concluídas: DP-101 (eSocial), DP-103 (Readiness Anomalia 1), DP-134 (Anomalia 2). Saúde Em risco mantida.
- **RPA Fiscal:** milestone Construção de RPAs **88% → 82%** (reconciliação com o valor real do Linear). Saúde No prazo mantida.

**CONSOLIDADO** regravado para a semana 2026-07-03 (deriva dos REPORTS; projeto sem reporte na semana = pausado). **Subtítulo** dos dois dashboards em 03/07. **Não** mexido: aba Sinergias, legenda "X de Y issues", teto de 90% (permanece removido), Matriz compacta, Contábil em violeta, texto/click do Reporte Semanal.

**Validação:** os 2 `<script>` de cada painel extraídos → `node --check` OK + smoke test (DOM stub renderizando dashboard/exec/projetos/raid/reports/okr/deps) → **PASS** nos dois. Salvo somente após passar.

**Snapshot dos 15 projetos do portfólio (pctLinear · saúde):**

| Projeto | % | Saúde |
| --- | --- | --- |
| Motor Fiscal SN | 38 | Em risco |
| RPA Fiscal | 82 | No prazo |
| Motor Trabalhista | 72 | Em risco |
| Motor Contábil | 36 | Em risco |
| Solicitações DP | 51 | Em risco |
| Triagem/OCR | 57 | No prazo |
| Copiloto Samurai | 0 | Off track (Geladeira) |
| BPO Financeiro | 10 | Em risco |
| GDocs multi-CNPJ | 100 | No prazo (Encerrado) |
| GDocs acompanhamento | 100 | No prazo (Encerrado) |
| PMI Digital | 0 | Off track (Geladeira) |
| Cockpit 100% | 90 | No prazo |
| Cadastro Único | 6 | No prazo |
| Hubcount | 0 | No prazo |
| Offboarding | 0 | Off track (Geladeira) |

---

## 2026-07-03 · 12h UTC (run 2 — completa os Project Updates da semana) — snapshot · ⏱ relógio do ambiente saltou 30/06→03/07 durante a run (tempo efetivo não mensurável)

**Run de sexta-feira (03/07) — 2ª execução do dia, completa os Project Updates da semana 29/06–03/07.** A run anterior (07-03 · 12h) rodou antes de os updates semanais serem postados e concluiu "sem novidades desde 26/06"; esta varredura (`get_status_updates` type:project, orderBy createdAt, createdAt≥2026-06-27) encontrou **5 Project Updates novos** in-scope, agora refletidos.

**Novos Project Updates capturados (portfólio):**
- **Solicitações DP** (02/07 · Gabriel · 🟡 Em risco): gestor de tarefas do operador no Cockpit (fila geral, devolver-à-fila sem cancelar, navegação, filtros unificados); validações inteligentes (Férias concluído + Admissão); design das reformulações dos forms do HUB (pós-V1) concluído. Milestones: **V1 97→99% · V2.1 forms 52% · V2.2 gestor Cockpit 19→33% · V3 form inteligente+motor 15→51%**. pctLinear 97→99. Target 31/07→31/10.
- **Cockpit 100%** (03/07 · Ana Caroline · 🟢 No prazo): **cobertura 100% da base (PJ+PF+Estrangeiros) entregue (30/06)**; entra em estabilização (30 dias, 25%, prev. 17/07). pctLinear 85→90. Marcos: 5 concluídos + estável (25%) + resultado medido (pendente).
- **Triagem / OCR** (03/07 · Ana Caroline · 🟢 No prazo): **Universo de documentos mapeado 65→100%** (02/07); **Regras de triagem auditáveis 43→57%**; nova **Fundação de confiança da classificação 33%** (proxy exposto na API); nova frente "Conta bancária obrigatória em pontos de entrada de extrato" 25%. pctLinear 65→72.
- **Motor Contábil** (03/07 · Andressa · 🟡 Em risco): experiência contábil no Cockpit (pendências p/ operador + telas do Gestor de Tarefas) finalizada pela Elaine, vai ao Jorge validar/encaixar no dev; todas as frentes em andamento. Milestone Construção **38→36%**. Atualizado nos DOIS painéis.
- **Hubcount** (03/07 · Andressa · 🟢 No prazo): sem avanço — Descoberta, início previsto **01/08** (statusProjeto Ideia→Descoberta; início 01/07→01/08). pctLinear 0.

**Motores sem Project Update novo no momento do sync (últimos = 26/06):** Motor Fiscal SN, Motor Trabalhista, RPA Fiscal — pctLinear/marcoLinear/health preservados do reporte de 26/06; tarefas seguem no estado das issues (ex.: FIS-330 e-CAC Concluído; DP-103/DP-107/DP-134 due 03/07). Cadastro Único e BPO Financeiro sem report na semana; Copiloto Samurai, PMI Digital e Offboarding na Geladeira; GDocs multi-CNPJ e GDocs acompanhamento encerrados (100%).

**Também nesta run:** subtítulo dos dashboards mantido em **· 03/07**; **CONSOLIDADO → semana 2026-07-03** (nota + 8 itens: 3 motores carregados de 26/06 + Motor Contábil, Triagem/OCR, Cockpit 100%, Solicitações DP, Hubcount); **REPORTS**: +1 no Autopilot (Motor Contábil) e +5 no Portfólio (append-only, nada apagado).

**Snapshot dos 15 projetos do portfólio (pctLinear · saúde) — média 46% · No prazo 7 · Em risco 5 · Off track 3:**

| Projeto | % | Saúde |
| -- | -- | -- |
| Motor Fiscal SN | 29 | Em risco |
| RPA Fiscal | 88 | No prazo |
| Motor Trabalhista | 66 | Em risco |
| Motor Contábil | 36 | Em risco |
| Solicitações DP | 99 | Em risco |
| Triagem OCR | 72 | No prazo |
| Copiloto Samurai | 0 | Off track |
| BPO Financeiro | 10 | Em risco |
| GDocs multi-CNPJ | 100 | No prazo |
| GDocs acompanhamento | 100 | No prazo |
| PMI Digital | 0 | Off track |
| Cockpit 100% | 90 | No prazo |
| Cadastro Único | 6 | No prazo |
| Hubcount | 0 | No prazo |
| Offboarding | 0 | Off track |

Validação: extraídos os 2 `<script>` de cada painel · `node --check` OK nos 4 blocos · smoke test com DOM stub (Proxy) executou renderDashboard/OKR/Exec/Projetos/Raid/Reports/Deps sem erro nos dois painéis (SMOKE PASS) · REPORTS (29 Autopilot · 73 Portfólio) e CONSOLIDADO válidos como JSON. Só então salvo e publicado.

---

## 2026-07-03 · 12h UTC — snapshot · ⏱ ~8m (relógio do sandbox instável nesta run)

**Run de quinta-feira (re-sync).** Varredura do Linear: `get_status_updates` (type:project, orderBy createdAt, −P8D, limit 10) e `list_issues` dos 4 motores (updatedAt −PT8H, desde a run anterior). **Nenhum Project Update novo desde 26/06** — o update mais recente em qualquer projeto continua sendo Open Finance (26/06 22:18); Motor Fiscal SN, Motor Trabalhista, Certificado Digital, Central de Ajuda, Pesquisa de Satisfação e os projetos Cockpit também são de 26/06 e já refletidos nos painéis. Portanto REPORTS, CONSOLIDADO, MATRIZ, pctLinear, saúde e marcoLinear dos 15 projetos permanecem inalterados (append-only preservado).

**Mudança real no nível de tarefa exibida (via list_issues, régua de status) — atualizada nos DOIS painéis:**
- **Motor Fiscal SN:** `FIS-330` [Adapter — histórico SERPRO (e-CAC), sub de FIS-300/E2 · Cálculo & emissão do DAS] passou de **Pendente → Concluído** em 03/07 12:16 (due 03/07; assignee Paulo Contieri). Primeira integração externa do Motor de Cálculo (consulta de histórico via API SERPRO/e-CAC) entregue. A entrega-mãe FIS-300 (E2) segue *Em andamento* (FIS-331 pendente, FIS-259 refinado).

**Atividade de issue observada na janela (não altera entregas-mãe nem as tarefas diretas exibidas):**
- **Motor Fiscal SN:** `FIS-335` [bug de correlação de CFOP, sub de FIS-371] segue *Concluído* (fechado em 19/06). `HUB-501` [Design — refinar dependências do Motor Fiscal / COCKPIT-521] segue *Pendente* (Hub/Design, não exibida).
- **Motor Contábil:** `HUB-496`/`HUB-497`/`HUB-498` [Design da experiência do operador no workflow do Motor Contábil / COCKPIT-537] seguem *Pendente* (Hub/Design, não exibidas). Nenhuma sub-issue de construção CTB alterada na janela.
- **RPA Fiscal · Motor Trabalhista:** sem atividade de issue na janela.

**Drift de milestone (informativo — pctLinear segue o reporte semanal; sem reporte novo, sem alteração no painel):** sem variação material reportada desde a run anterior.

- **Subtítulo dos dashboards:** "Linear · 02/07" → **"Linear · 03/07"** nos dois painéis.
- pctLinear/health/marcoLinear e a MATRIZ (Cockpit/Hub/backlog) sem alteração — dependem de Project Update/milestone, e não houve reporte novo.

**Snapshot dos 15 projetos do portfólio (pctLinear · saúde):**

| Projeto | % | Saúde |
| -- | -- | -- |
| Motor Fiscal SN | 29 | Em risco |
| RPA Fiscal | 88 | No prazo |
| Motor Trabalhista | 66 | Em risco |
| Motor Contábil | 38 | Em risco |
| Solicitações DP | 97 | Em risco |
| Triagem OCR | 65 | No prazo |
| Copiloto Samurai | 0 | Off track |
| BPO Financeiro | 10 | Em risco |
| GDocs multi-CNPJ | 100 | No prazo |
| GDocs acompanhamento | 100 | No prazo |
| PMI Digital | 0 | Off track |
| Cockpit 100% | 85 | No prazo |
| Cadastro Único | 6 | No prazo |
| Hubcount | 0 | No prazo |
| Offboarding | 0 | Off track |

Validação: extraídos os 2 `<script>` de cada painel · `node --check` OK nos 4 blocos (Autopilot 2 scripts · Portfólio 2 scripts) · smoke test com DOM stub (Proxy) executou data+logic chamando renderDashboard/renderExec/renderProjetos/renderRaid/renderReports/renderOKR/renderDeps sem erro nos dois painéis (SMOKE PASS). Só então salvo e publicado.


## 2026-07-02 · 15h UTC — snapshot · ⏱ 4m 30s

**Run de quinta-feira (meio de semana).** Varredura do Linear: `get_status_updates` (type:project, orderBy createdAt, limit 6) e `list_issues` dos 4 motores (updatedAt −P1D). **Nenhum Project Update novo desde 26/06** — o update mais recente em qualquer projeto continua sendo Open Finance (26/06 22:18); todos os demais (Certificado Digital, Motor Fiscal SN, Central de Ajuda, Pesquisa de Satisfação, Motor Trabalhista) também são de 26/06 e já refletidos nos painéis. Portanto REPORTS, CONSOLIDADO, MATRIZ, pctLinear, saúde e marcoLinear dos 15 projetos permanecem inalterados (append-only preservado).

**Mudanças reais no nível de tarefa exibida (via list_issues, régua de status) — atualizadas nos DOIS painéis:**
- **Motor Fiscal SN:** `FIS-279` [Anomalia 2 — gate de validação da apuração, sub de FIS-299/E1] passou de **Pendente → Em andamento** em 02/07 13:36 (due 03/07; assignee Paulo Dias). Reflete o gate de validação da apuração entrando em construção.
- **Motor Trabalhista (DP):** `DP-103` [Readiness check — Anomalia 1, sub de DP-135] **concluída em 02/07 14:39** (due 03/07 — entregue antes do prazo; Paulo Dias). Primeiro dos 4 itens due 03/07 do ciclo a fechar.

**Atividade de issue observada na janela (nível neto / planejamento — não altera entregas-mãe nem as tarefas diretas exibidas):**
- **Motor Fiscal SN:** sob `FIS-329` (API do DAS, já *Em andamento* no painel) — `FIS-398` [código básico da API] e `FIS-399` [integração BHules] **concluídas 01/07**, `FIS-400` [infra AWS Terraform] *Em andamento* (due 06/07). `HUB-499` [Cockpit — suporte ao workflow ApuracaoFiscal] segue *Pendente*.
- **Motor Trabalhista (DP):** `DP-162` e `DP-154` (refator do disparador de fechamento) passaram a *Em andamento* em 02/07; `DP-161` [Restate service dp-reports-engine] *Em revisão*; `DP-167`/`DP-168` (eSocial→Restate) concluídas em 01/07. Novas issues criadas: `DP-183` [provisão férias/13º — folha sem apontamento] e `DP-179` [validar BRD FGTS consignado], ambas *Pendente* (backlog).
- **RPA Fiscal · Motor Contábil:** sem atividade relevante na janela.

**Drift de milestone (informativo — pctLinear segue o reporte semanal; sem reporte novo, sem alteração no painel):** sem variação material desde a run anterior.

- **Subtítulo dos dashboards:** "Linear · 01/07" → **"Linear · 02/07"** nos dois painéis.
- pctLinear/health/marcoLinear e a MATRIZ (Cockpit/Hub/backlog) sem alteração — dependem de Project Update/milestone, e não houve reporte novo.

**Snapshot dos 15 projetos do portfólio (pctLinear · saúde):**

| Projeto | % | Saúde |
| -- | -- | -- |
| Motor Fiscal SN | 29 | Em risco |
| RPA Fiscal | 88 | No prazo |
| Motor Trabalhista | 66 | Em risco |
| Motor Contábil | 38 | Em risco |
| Solicitações DP | 97 | Em risco |
| Triagem OCR | 65 | No prazo |
| Copiloto Samurai | 0 | Off track |
| BPO Financeiro | 10 | Em risco |
| GDocs multi-CNPJ | 100 | No prazo |
| GDocs acompanhamento | 100 | No prazo |
| PMI Digital | 0 | Off track |
| Cockpit 100% | 85 | No prazo |
| Cadastro Único | 6 | No prazo |
| Hubcount | 0 | No prazo |
| Offboarding | 0 | Off track |

Validação: extraídos os 2 `<script>` de cada painel · `node --check` OK nos 4 blocos (Autopilot 74301+45110 chars · Portfólio 127844+55578 chars) · smoke test com DOM stub executou data+logic chamando dashboard/exec/projetos/raid/reports sem erro nos dois painéis. Só então publicado.

## 2026-07-01 · 22h UTC — snapshot · ⏱ 5m 40s

**Segunda run da quarta-feira (re-sync noturno).** Varredura do Linear: `get_status_updates` (type:project, orderBy createdAt, limit 6 × 2 páginas) e `list_issues` dos 4 motores (updatedAt −PT7H). **Nenhum Project Update novo desde 26/06** — os updates mais recentes em qualquer projeto continuam sendo os de 26/06 (Open Finance 22:18, Certificado Digital, Motor Fiscal SN, Central de Ajuda, Pesquisa de Satisfação, Motor Trabalhista, Cockpit GTO/Triagem/Sincronização etc.), todos já refletidos nos painéis. Portanto REPORTS, CONSOLIDADO, MATRIZ, pctLinear, saúde e marcoLinear dos 15 projetos permanecem inalterados (append-only preservado).

**Atividade de issue observada desde a run das 16h (mesma competência, nível neto — não altera as entregas-mãe nem as tarefas diretas exibidas nos painéis):**
- **Motor Fiscal SN:** sob `FIS-329` (API do DAS, já *Em andamento* no painel) — `FIS-398` [código básico da API baseado no General Ledger] **concluída 01/07**, `FIS-399` [integração com o BHules] **concluída 01/07**, `FIS-400` [infra AWS Terraform] passou a **Em andamento**. Sem entrega-mãe (E1–E5) concluída.
- **Motor Trabalhista (DP):** sob `DP-101` (eSocial, já concluída na run das 16h) — `DP-167` [migrar services do eSocial p/ Restate] e `DP-168` [ajustar nomenclatura adapter] **concluídas**.
- **RPA Fiscal:** lote de sub-issues de refinamento criado hoje sob `FIS-260` (Motor de Trigger de escrituração) — `FIS-430`…`FIS-438` (polling BHules, orquestração DMN, contrato de resposta, observabilidade, anti-perda), todas em **Refinado** (planejamento, não iniciadas). `FIS-260` segue *Refinado*.
- **Motor Contábil:** sem atividade na janela.

**Drift de milestone (informativo — pctLinear segue o reporte semanal, precedente das runs anteriores; sem reporte novo, sem alteração no painel):** Construção Motor de Cálculo SN 29% → 34,56% · Construção Pró-Labore SN 66% → 71,56% · Folha s/ apontamento 18% → 17,86%. RPA e Contábil sem milestone novo relevante.

- **Subtítulo dos dashboards**: já em "Linear · 01/07" (definido na run das 16h de hoje) — sem alteração nesta run.
- **Nenhuma edição de dados nos HTML nesta run** — não houve reporte novo nem mudança no nível de entrega-mãe/tarefa exibido. Único arquivo alterado: este `HISTORICO_LINEAR.md` (append-only).

**Snapshot dos 15 projetos do portfólio (pctLinear · saúde):**

| Projeto | % | Saúde |
| -- | -- | -- |
| Motor Fiscal SN | 29 | Em risco |
| RPA Fiscal | 88 | No prazo |
| Motor Trabalhista | 66 | Em risco |
| Motor Contábil | 38 | Em risco |
| Solicitações DP | 97 | Em risco |
| Triagem OCR | 65 | No prazo |
| Copiloto Samurai | 0 | Off track |
| BPO Financeiro | 10 | Em risco |
| GDocs multi-CNPJ | 100 | No prazo |
| GDocs acompanhamento | 100 | No prazo |
| PMI Digital | 0 | Off track |
| Cockpit 100% | 85 | No prazo |
| Cadastro Único | 6 | No prazo |
| Hubcount | 0 | No prazo |
| Offboarding | 0 | Off track |

Validação: extraídos os 2 `<script>` de cada painel · `node --check` OK nos 4 blocos (Autopilot 74291+45110 chars · Portfólio 127834+55578 chars) · smoke test com DOM stub chamou dashboard/exec/projetos/raid/reports sem erro nos dois painéis. Só então publicado.

## 2026-07-01 · 16h UTC — snapshot · ⏱ 73m 43s

**Run de meio de semana (quarta-feira).** Varredura completa do Linear: `get_status_updates` (type:project, orderBy createdAt, limit 6) e `list_issues` dos 4 motores (updatedAt −P5D). **Nenhum Project Update novo foi publicado desde 26/06** — os 6 updates mais recentes (Open Finance 26/06 22:18, Certificado Digital, Motor Fiscal SN, Central de Ajuda, Pesquisa de Satisfação, Motor Trabalhista) são todos de 26/06 e já estavam refletidos nos painéis. Portanto REPORTS, CONSOLIDADO, pctLinear e saúde dos 15 projetos permanecem inalterados (append-only preservado).

**Mudanças reais no nível de issue (via list_issues, régua de status)** — houve execução entre 29/06 e 01/07, refletida no board dos dois painéis:
- **Motor Trabalhista (DP):** `DP-101` [Envio da folha ao eSocial] **concluída em 01/07** (fechou após a migração Terraform→Restate, exatamente como o report de 26/06 antecipava). `DP-134` [Anomalia 2 — validação pós-cálculo] **concluída em 01/07** (era due 03/07 — entregue antes do prazo). `DP-109` [Distribuição pós-gate] e `DP-67` [Admissão — migração Azure→AWS] passaram a **Em andamento**.
- **Motor Fiscal SN:** `FIS-329` [Motor de Cálculo Fiscal — API de apuração do DAS] passou a **Em andamento** (a "API de cálculo em andamento" citada no report de 26/06 agora refletida no board). Sem entregas-mãe concluídas na janela.
- `progresso` do Motor Trabalhista atualizado para citar DP-101/DP-134 concluídas.
- **Subtítulo dos dashboards**: "Linear · 29/06" → "Linear · 01/07" nos dois painéis.
- pctLinear/health/marcoLinear e a MATRIZ (Cockpit/Hub/backlog) sem alteração — dependem de Project Update/milestone, e não houve reporte novo.

**Snapshot dos 15 projetos do portfólio (pctLinear · saúde):**

| Projeto | % | Saúde |
| -- | -- | -- |
| Motor Fiscal SN | 29 | Em risco |
| RPA Fiscal | 88 | No prazo |
| Motor Trabalhista | 66 | Em risco |
| Motor Contábil | 38 | Em risco |
| Solicitações DP | 97 | Em risco |
| Triagem OCR | 65 | No prazo |
| Copiloto Samurai | 0 | Off track |
| BPO Financeiro | 10 | Em risco |
| GDocs multi-CNPJ | 100 | No prazo |
| GDocs acompanhamento | 100 | No prazo |
| PMI Digital | 0 | Off track |
| Cockpit 100% | 85 | No prazo |
| Cadastro Único | 6 | No prazo |
| Hubcount | 0 | No prazo |
| Offboarding | 0 | Off track |

Validação: extraídos os 2 `<script>` de cada painel · `node --check` OK nos 4 · smoke test com DOM stub renderizou dashboard/exec/projetos/raid/reports sem erro (Autopilot avg 55% · 28 reports; Portfólio avg 46% · 68 reports). Só então salvos.

## 2026-06-29 · 10h UTC — snapshot · ⏱ 5m 2s

**Run de início de semana (segunda-feira).** Varredura completa do Linear: `get_status_updates` (type:project, orderBy createdAt) e `list_issues` dos 4 motores. **Nenhum Project Update novo foi publicado desde a run de fechamento de 26/06** — o reporte mais recente em qualquer projeto é de 26/06 22:18 UTC (Open Finance, fora dos 15 do portfólio), já posterior aos reportes dos motores. Os 6 updates mais recentes (Open Finance, Certificado Digital, Motor Fiscal SN, Central de Ajuda, Pesquisa de Satisfação, Motor Trabalhista) são todos de 26/06 e já estavam refletidos nos painéis. As issues dos motores aparecem com `updatedAt` de 29/06 ~02:43 UTC, mas trata-se de re-indexação em lote (status, `dueDate` e `completedAt` idênticos ao snapshot de 26/06) — sem mudança real de estado.

**Mudanças aplicadas:**
- **Subtítulo dos dashboards**: "Linear · 26/06" → "Linear · 29/06" nos dois painéis (reflete a data da sincronização de hoje).
- **REPORTS / CONSOLIDADO / MATRIZ / dependências**: sem alteração — não houve reporte novo na semana nem mudança de milestone/status no Linear. Entradas antigas preservadas (append-only).
- **pctLinear e saúde dos 15 projetos**: reafirmados, sem alteração em relação a 26/06.

**Snapshot dos 15 projetos do portfólio (pctLinear · saúde):**

| Projeto | % | Saúde |
| -- | -- | -- |
| Motor Fiscal SN | 29 | Em risco |
| RPA Fiscal | 88 | No prazo |
| Motor Trabalhista | 66 | Em risco |
| Motor Contábil | 38 | Em risco |
| Solicitações DP | 97 | Em risco |
| Triagem OCR | 65 | No prazo |
| Copiloto Samurai | 0 | Off track |
| BPO Financeiro | 10 | Em risco |
| GDocs multi-CNPJ | 100 | No prazo |
| GDocs acompanhamento | 100 | No prazo |
| PMI Digital | 0 | Off track |
| Cockpit 100% | 85 | No prazo |
| Cadastro Único | 6 | No prazo |
| Hubcount | 0 | No prazo |
| Offboarding | 0 | Off track |

**Dashboard após sync:** Portfólio (15 projetos) — 7 No prazo · 5 Em risco · 3 Off track · média pctLinear ~46%. Autopilot (4 motores) — 1 No prazo (RPA) · 3 Em risco (Fiscal, Trabalhista, Contábil). **Validação:** os 2 `<script>` de cada painel passaram em `node --check` + smoke test (DOM stub, render de dashboard/OKR/exec/projetos/raid/reports/deps sem exceção) antes de salvar.

---

## 2026-06-26 · 22h UTC — snapshot · ⏱ 7m 5s

**Sync de fechamento do dia — incorpora o Project Update do Motor Fiscal SN publicado às 18h23 UTC**, depois da run das 15h. Esse era o único reporte da semana ainda ausente dos painéis (o último capturado era de 19/06). Demais projetos sem alteração desde a run das 15h.

**Mudanças aplicadas:**
- **Motor Fiscal SN** (ambos os painéis): novo Project Update 26/06 (Jeisy Sousa / publicado por Jeniffer, 🟡 Em risco, em melhora). **Target do projeto 31/07 → 31/08** (`alvo` atualizado nos dois painéis). Maior salto de confiabilidade do BHules desde o incidente de maio: causa-raiz dos erros de classificação resolvida (trava de crédito ICMS 5/5, "sistema imunológico" com revogação rastreável, 747 decisões antigas removidas, trava anti-regressão) — tudo em produção. **14.861 notas reprocessadas com segurança** (77,8% conformes; nada enviado ao cliente); R$ 5,07 mi em créditos identificados. BHules confirmado como fonte única de notas (Jorge, 26/06). Milestones Linear: Classificação SN **52% → 45%**, Cálculo SN **24% → 29%** (pctLinear 29 mantido). Bloqueios: decisão Jettax × Unecont travada; ~936 notas em revisão aguardando decisão; integração c/ Motor Contábil e suporte Cockpit/Hub em triage (31/07).
- **REPORTS**: +1 no Autopilot (motor-fiscal-sn) · +1 no Portfólio (motor-fiscal-sn). **CONSOLIDADO** (semana 2026-06-26) → 14 itens; nota atualizada (Motor Fiscal SN saiu de "sem novo Project Update" para reporte 26/06).
- **Subtítulo dos dashboards**: "Linear · 25/06" → "Linear · 26/06" nos dois painéis.
- **Sem novo reporte na semana** (sem alteração): BPO Financeiro (último 19/06). Copiloto Samurai e PMI Digital seguem na Geladeira; Offboarding na Geladeira (23/06); GDocs ×2 encerrados (100%).

**Snapshot dos 15 projetos do portfólio (pctLinear · saúde):**

| Projeto | % | Saúde |
| -- | -- | -- |
| Motor Fiscal SN | 29 | Em risco |
| RPA Fiscal | 88 | No prazo |
| Motor Trabalhista | 66 | Em risco |
| Motor Contábil | 38 | Em risco |
| Solicitações DP | 97 | Em risco |
| Triagem OCR | 65 | No prazo |
| Copiloto Samurai | 0 | Off track |
| BPO Financeiro | 10 | Em risco |
| GDocs multi-CNPJ | 100 | No prazo |
| GDocs acompanhamento | 100 | No prazo |
| PMI Digital | 0 | Off track |
| Cockpit 100% | 85 | No prazo |
| Cadastro Único | 6 | No prazo |
| Hubcount | 0 | No prazo |
| Offboarding | 0 | Off track |

**Dashboard após sync:** Portfólio (15 projetos) — 7 No prazo · 5 Em risco · 3 Off track · média pctLinear ~46%. Autopilot (4 motores) — 1 No prazo (RPA) · 3 Em risco (Fiscal, Trabalhista, Contábil). **Validação:** os 2 `<script>` de cada painel passaram em `node --check` + smoke test (DOM stub, render dos 6 views sem exceção, reporte fiscal e subtítulo conferidos) antes de salvar.

---

## 2026-06-26 · 15h UTC — snapshot · ⏱ 10m 52s

**Sync de complemento da semana de 26/06 — Project Updates publicados após a execução das 12h.** A run das 12h rodou com o relógio do ambiente em 22/06 e capturou apenas parte dos reportes; entre ~11h48 e ~14h50 UTC entraram (ou foram lidos agora) updates de 4 projetos do portfólio que ainda não estavam nos painéis. Esta run incorpora esses reportes nos dois painéis e mantém todo o histórico anterior.

**Mudanças aplicadas (ambos os painéis quando motor; senão portfólio):**
- **Motor Trabalhista** (ambos): novo Project Update 26/06 (Andressa, 🟡 Em risco). **Target do projeto 31/07 → 31/08.** Ciclo de construção em andamento — DP-103 (Readiness Anomalia 1, Paulo Dias), DP-134 (Anomalia 2, Reginaldo) e DP-107 (disparo via EventBridge, Sávio) iniciados, due 03/07; nova DP-165 (tabelas fiscais → dp-rules, faixa de isenção de IR Lei 15.270). eSocial DP-101 atrasou por migração de infra (Terraform → Restate), fecha na próxima semana. Milestones Linear: Pró-Labore SN **65,89%** · Folha s/ apont. **17,86%** (pctLinear 66 mantido).
- **Triagem OCR** (portfólio): novo Update 26/06 (Ana Caroline, 🟢 No prazo). pctLinear **75 → 65** · marcoLinear corrigido (milestone "Top 5 tipos roteados" está em **0% / a iniciar 20/07**, não entregue). Milestones: M1 Universo mapeado **64,71%** · Regras auditáveis **43,48%** · Top 5 0%. Entregas: BHUB-48 (extractor lxml NFS-e SP), COCKPIT-522.
- **Cockpit 100%** (portfólio): novo Update 26/06 (Ana Caroline, 🟢 No prazo). **Cobertura 100% PJ+PF concluída (subida em massa de CPF em 25/06).** pctLinear **30 → 85** · status "Ideia" → "Construção" · marcos M1/M2/M3 → **Concluído** (100% no Linear) + M4 estabilidade em andamento. Milestones de cobertura todos 100%; "Estável em produção (30 dias)" 0%.
- **Cadastro Único** (portfólio): novo Update 26/06 reportado sob o projeto **"Sincronização de informações de sistemas satélites e o Cockpit (SSOT)"** (Ana Caroline, 🟢 No prazo) — marcos batem exatamente (reconciliação · Top 200 inconsistentes · Dashboard ≥75%). pctLinear **25 → 6** · health **Em risco → No prazo** · target **31/07 → 31/08**. M1 reconciliação **6,25%** (10/07). *Escolha autônoma: tratado como o mesmo projeto do Cadastro Único, dado o casamento de marcos e a ausência de update separado na semana.*
- **REPORTS**: +1 no Autopilot (motor-trabalhista) · +4 no Portfólio (motor-trabalhista, triagem-ocr, cockpit-100, cadastro-unico). **CONSOLIDADO** (semana 2026-06-26) → 13 itens; nota atualizada (Motor Trabalhista, Triagem, Cockpit 100% e Cadastro Único saíram de "sem report").
- **Sem novo reporte na semana** (sem alteração): Motor Fiscal SN (último 19/06), BPO Financeiro. Copiloto Samurai e PMI Digital seguem na Geladeira; Offboarding na Geladeira (23/06); GDocs ×2 encerrados (100%); RPA Fiscal (88%), Motor Contábil (38%) e Solicitações DP (97%) já refletidos na run das 12h.

**Snapshot dos 15 projetos do portfólio (pctLinear · saúde):**

| Projeto | % | Saúde |
| -- | -- | -- |
| Motor Fiscal SN | 29 | Em risco |
| RPA Fiscal | 88 | No prazo |
| Motor Trabalhista | 66 | Em risco |
| Motor Contábil | 38 | Em risco |
| Solicitações DP | 97 | Em risco |
| Triagem OCR | 65 | No prazo |
| Copiloto Samurai | 0 | Off track |
| BPO Financeiro | 10 | Em risco |
| GDocs multi-CNPJ | 100 | No prazo |
| GDocs acompanhamento | 100 | No prazo |
| PMI Digital | 0 | Off track |
| Cockpit 100% | 85 | No prazo |
| Cadastro Único | 6 | No prazo |
| Hubcount | 0 | No prazo |
| Offboarding | 0 | Off track |

**Dashboard após sync:** Portfólio (15 projetos) — 7 No prazo · 5 Em risco · 3 Off track · média pctLinear ~46%. Autopilot (4 motores) — 1 No prazo (RPA) · 3 Em risco (Fiscal, Trabalhista, Contábil). **Validação:** os 2 `<script>` de cada painel passaram em `node --check` + smoke test (DOM stub, render sem exceção) antes de salvar.

---

## 2026-06-26 · 12h UTC — snapshot · ⏱ ~8m *(relógio do ambiente avançou 22→26/06 durante a execução; duração real ~8 min)*

**Semana de 26/06 — novos Project Updates capturados.** Esta sync incorpora os reportes da semana de 26/06 publicados no Linear (o ciclo anterior eram refreshes de milestone em 25/06). 10 Project Updates novos lidos via `get_status_updates` — 8 dentro do portfólio + os motores RPA Fiscal e Contábil. **Motor Fiscal SN e Motor Trabalhista sem novo reporte** (último 19/06): `pctLinear` mantido pelo milestone real do Linear (live).

**Mudanças aplicadas:**
- **Motor Contábil** (ambos painéis): `pctLinear` **30% → 38%** · Jorge iniciou o ciclo de construção (14+ sub-issues em andamento; discovery CTB-1 e spike Midaz CTB-3 concluídos; Git desbloqueado) · target **31/07 → 31/08** · 🟡 Em risco.
- **RPA Fiscal** (ambos): **88%** · Painel de controle interno **FIS-188 concluído (23/06)** · `marcoLinear` "(88%)" · 🟢 No prazo.
- **Solicitações DP** (portfólio): `pctLinear` **85% → 97%** (DP1.M1) · validação dos forms do HUB encerrada, validações inteligentes em construção · marcos atualizados (M1 97% · M2 19% · M3 15% · +M4) · 🟡 Em risco.
- **GDocs multi-CNPJ** e **GDocs acompanhamento**: **encerrados (100%)** · status → "Encerrado" · 🟢 No prazo.
- **Copiloto Samurai**: → **Geladeira** · 🟡 → 🔴 Off track · `pctLinear` 10% → 0% (milestones zerados; retomada Q4 FY26).
- **PMI Digital**: confirmado **Geladeira** · 🔴 Off track · retomada Q4 FY26.
- **Hubcount**: aguardando apresentação dos MVPs · Spec → 31/08 · 0% · 🟢 No prazo.
- **Offboarding**: já em Geladeira desde 23/06 — mantido · 🔴 Off track.
- **REPORTS**: +8 no Portfólio (rpa, contábil, soldp, gdocs ×2, samurai, pmi, hubcount) · +2 no Autopilot (rpa, contábil). **CONSOLIDADO** → semana **2026-06-26** (9 itens). Subtítulo do Dashboard: data dinâmica (auto-hoje).
- **Sem reporte na semana** (sem alteração de dados): Motor Fiscal SN, Motor Trabalhista, Triagem OCR, BPO Financeiro, Cockpit 100%, Cadastro Único.

**Milestones lidos do Linear (% real):** Classificação SN **44,52%** · Motor de Cálculo SN **28,68%** · RPA Construção **87,63%** · Pró-Labore SN **65,94%** · Folha s/ apont. **17,86%** · Motor Contábil Entregue **38%** (report 26/06).

**Dashboard após sync:** Autopilot (4 motores) média **~55%** · 1 No prazo · 3 Em risco. Portfólio (15 projetos) média **~44%** · 6 No prazo · 6 Em risco · 3 Off track.

| Projeto | Squad | Saúde | % (milestone) | Δ desde 25/06 22h |
| -- | -- | -- | -- | -- |
| Motor Fiscal SN | Fiscal | 🟡 Em risco | 29% (Cálculo SN) | — (sem reporte · Classif. 45%) |
| RPA Fiscal | Fiscal | 🟢 No prazo | 88% (Construção RPAs) | — · FIS-188 concluído |
| Motor Trabalhista (DP) | DP | 🟡 Em risco | 66% (Pró-Labore SN) | — (sem reporte · Folha 18%) |
| Motor Contábil | Contábil | 🟡 Em risco | 38% (Motor Entregue) | +8 · construção iniciada |
| Solicitações DP | Hub | 🟡 Em risco | 97% (DP1.M1) | +12 · forms validados |
| Triagem OCR | Cockpit | 🟢 No prazo | 75% | — (sem reporte) |
| Copiloto Samurai | Cockpit | 🔴 Off track | 0% (geladeira) | health 🟡→🔴 · −10 |
| BPO Financeiro | Cockpit | 🟡 Em risco | 10% (bloqueado) | — (sem reporte) |
| GDocs multi-CNPJ | Hub | 🟢 No prazo | 100% (encerrado) | — · projeto encerrado |
| GDocs acompanhamento | Hub | 🟢 No prazo | 100% (encerrado) | — · projeto encerrado |
| PMI Digital | Cockpit | 🔴 Off track | 0% (geladeira) | — |
| Cockpit 100% | Cockpit | 🟢 No prazo | 30% | — (sem reporte) |
| Cadastro Único | Cockpit | 🟡 Em risco | 25% | — (sem reporte) |
| Hubcount | Contábil | 🟢 No prazo | 0% (pré-spec) | — · aguardando MVPs |
| Offboarding | Cockpit | 🔴 Off track | 0% (geladeira) | — |

**Validação:** os 2 `<script>` de cada painel passaram em `node --check` + smoke test (jsdom renderizando dashboard/exec/projetos/raid/reports). `REPORTS`/`CONSOLIDADO` reparsáveis (`;` final preservado). Painéis salvos só após validação OK.

---

## 2026-06-25 · 22h UTC — snapshot · ⏱ 5m 47s

**Refresh de milestones dos motores — recomputação do `progress` real no Linear desde a sync das 15h.** Nenhum Project Update novo dos 15 projetos do portfólio na semana: os mais recentes na fila do Linear são **Procurações no Cockpit** (26/06) e **Design System v1.4.1** (24/06) — ambos fora dos painéis — e Offboarding/Geladeira (23/06), já refletido. Hub (solicitacoes-dp, gdocs-multicnpj, gdocs-acompanhamento) reconferido — sem reporte novo. O `progress` real dos milestones de **Cálculo SN** e **Pró-Labore SN** recomputou para baixo (escopo expandido com novas issues nas milestones), então `pctLinear` foi atualizado nos **dois painéis** para refletir o valor real.

**Mudanças aplicadas (ambos os painéis):**
- `pctLinear` Motor Fiscal SN (Motor de Cálculo SN): **30% → 29%** (milestone real 28,68%).
- `pctLinear` Motor Trabalhista (Pró-Labore SN): **70% → 66%** (milestone real 66,27%).
- `pctLinear` Motor Contábil (Motor Entregue): **30% → 30%** (milestone real 29,92%, sem mudança).
- `pctLinear` RPA Fiscal (Construção de RPAs): **88% → 88%** (milestone real 87,63%, sem mudança).
- `marco` Motor Fiscal SN: "M1 Classificação **42%** · M2 Cálculo **27%**" → "M1 Classificação **45%** · M2 Cálculo **29%**".
- `marco` Motor Trabalhista: "M1 **68%** · M2 **22%**" → "M1 **66%** · M2 **18%**".
- Subtítulo do Dashboard: data dinâmica (auto-hoje) — já em **25/06**.
- `REPORTS`, `CONSOLIDADO`, `marcos` (Cockpit/Hub/backlog), `dependencias`, `health`/faróis: **sem alteração** (nenhum reporte novo dos 15 projetos).

**Milestones lidos do Linear (% real):** Classificação SN **44,52%** · Motor de Cálculo SN **28,68%** · RPA Construção **87,63%** · Pró-Labore SN **66,27%** · Folha s/ apont. **17,86%** · Motor Contábil Entregue **29,92%**.

**Dashboard após refresh:** Autopilot (4 motores) média **~53%** · 1 No prazo · 3 Em risco. Portfólio (15 projetos) média **~43%** · 6 No prazo · 7 Em risco · 2 Off track. (Faróis/health inalterados — sem novo Project Update.)

| Projeto | Squad | Saúde | % (milestone) | Δ desde 25/06 15h |
| -- | -- | -- | -- | -- |
| Motor Fiscal SN | Fiscal | 🟡 Em risco | 29% (Cálculo SN) | −1 · Classif. 42→45% |
| RPA Fiscal | Fiscal | 🟢 No prazo | 88% (Construção RPAs) | — |
| Motor Trabalhista (DP) | DP | 🟡 Em risco | 66% (Pró-Labore SN) | −4 · Folha s/ apont. 18% |
| Motor Contábil | Contábil | 🟡 Em risco | 30% (Motor Entregue) | — |
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
| Offboarding | Cockpit | 🔴 Off track | 0% (geladeira) | — |

**Validação:** os 2 `<script>` de cada painel passaram em `node --check` + smoke test (DOM stub renderizando dashboard/exec/projetos/raid/reports). Sem teto de 90% (GDocs = 100% real). Painéis salvos só após validação OK.

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
