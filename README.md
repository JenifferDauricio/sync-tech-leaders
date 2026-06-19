# BHub Tech — Painéis de Projetos

Painéis estáticos (HTML único, sem backend) de acompanhamento dos projetos Tech, alimentados pelo Linear.

- `index.html` — página inicial (links pros painéis)
- `bhub-projetos-tech-portfolio.html` — Portfólio (projetos Tech · 5 squads: Fiscal, DP, Contábil, Cockpit, Hub) — alinhado ao Weekly Tech. Abas: Dashboard, Objetivos (OKR), Visão Executiva (Board · Gantt · Matriz), Projetos, Ações de Mitigação e Reporte Semanal (Consolidado + histórico).
- `bhub-projeto-tech-v3.html` — Autopilot (4 motores: Fiscal SN, RPA, Trabalhista/DP, Contábil)
- `HISTORICO_LINEAR.md` — trilha de sincronização (append-only, atualizada 2×/dia · 12h e 19h)

## Atualização automática
Tarefa agendada `sync-bhub-tech-linear` (12h e 19h) lê o Linear, atualiza os dois painéis + o histórico e publica no GitHub. Dashboard (% médio e faróis) e Matriz derivam do reporte semanal/marcos do Linear.

## No ar
`https://jenifferdauricio.github.io/sync-tech-leaders/`

## Publicar (GitHub Pages)
1. Suba estes arquivos num repositório.
2. Settings → Pages → branch `main` / `(root)` → Save.
3. Em ~1 min: `https://SEU-USUARIO.github.io/SEU-REPO/`
