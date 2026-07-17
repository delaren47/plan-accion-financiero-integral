# CLAUDE.md — PAFI (Plan Acción Financiero Integral)

**Updated:** 2026-07-17

> ✅ **ACTIVO desde 2026-07-17 — P0: eliminación de deuda TC.** Plan canónico: `DEBT_MASTER_PLAN.md`. Estado: `STATUS.md`. Acciones inmediatas: `NEXT_ACTIONS.md`.

Command center de finanzas personales de Alfredo, con prioridades: **P0** eliminación de deuda de tarjeta de crédito (estrategia avalancha, ver `DEBT_MASTER_PLAN.md`); **P1** ingresos low-ticket como acelerador de pago de deuda; **P2** compliance mínimo de la LLC; **P3** plan de negocio original — parqueado. This is a markdown + CSV PM repo, not a code product. Read `~/.claude/CLAUDE.md` for global prefs.

Historia (P3, parqueado): el plan de 90 días original iba de deuda → rentabilidad vía fast-cash wins → retainers mensuales → productos white-label (Knotie-AI voz, LancePilot WhatsApp, Climbo reputación), bajo Delaren Consulting LLC (Wyoming). Falta su retro de cierre — actual vs meta $12K MRR; sólo Alfredo tiene esos números (ver `NEXT_ACTIONS.md` / `ops/`).

El sitio MkDocs publicado (`docs/` → GitHub Pages) es la cara pública; el PM del día a día vive en `private/` (P0) y en `ops/`, `finance/`, `sales/` (P1/P3). Los workflows detallados de la IA viven en **`.claude/instructions.md`** — léelo para la ingesta financiera P0, Money Friday, y los procedimientos de negocio (standup / weekly / monthly / new-lead / deal-closed).

---

## 1. Commands & rituals

- `/pafi` — load full project context (session opener).
- **Money Friday** (viernes, 15 min) — ritual central en P0: procesar ingesta pendiente, actualizar `private/DASHBOARD.md`, registrar pagos, decidir el excedente semanal contra la tarjeta de mayor CAT. See `.claude/instructions.md`.
- **Ingesta financiera** — "procesa la ingesta" (o hay archivos en `private/ingesta/`) → ver `.claude/instructions.md` (Workflow P0 — Ingesta financiera).
- **Daily standup** (opcional durante P0) → append a dated entry a `ops/standup_diario.md`.
- **Weekly / monthly review** (negocio P1/P3) → `ops/`; recompute KPIs from `ops/crm_simple.csv` + `finance/flujo_caja_semanal.csv`. See `.claude/instructions.md`.
- Active pending work tracked in `ops/P1_ITEMS_PENDIENTES.md` y `NEXT_ACTIONS.md`.
- Site preview (optional): `source .venv/bin/activate && mkdocs serve`. Deploy = `mkdocs gh-deploy`.

## 2. Folder map

| Folder | Purpose | Mutability |
|---|---|---|
| `private/` | Data financiera personal (gitignored, local-only): ingesta, deudas, ledger, dashboard | **NUNCA commitear — fuera de git por diseño** |
| `docs/` | MkDocs source: roadmap, ofertas, KPIs, validación, fiscal-compliance guides | edit; publishes to Pages |
| `ops/` | Standup, weekly review, P1 items, CRM CSV, daily-activities CSV | edit (append-first) |
| `finance/` | Cash-flow / AR-tracking / fixed-costs / invoice-log CSVs + factura template | **CSV-guarded** (see rules) |
| `sales/` | Cold-opening scripts, email + proposal templates | edit |
| `automation/` | White-label package defs (lancepilot / knotie / climbo) | edit |
| `legal/` | Revenue-share agreement, BOI/IRS LLC checklist | edit carefully |
| `templates/` | Fast-cash-win / retainer / white-label deliverable templates | edit |
| `site/` | MkDocs **build output** — generated, gitignored | never hand-edit |

## 3. Hard rules

- **Privacy guard:** `private/` está gitignored y **nunca** debe commitearse, force-add-earse, ni tener su contenido copiado a archivos versionados o al sitio MkDocs. Los números financieros personales (saldos, movimientos) viven **SÓLO** bajo `private/`. Los docs versionados llevan metodología, nunca saldos reales. El repo es público y se auto-sincroniza cada 15 min.
- **Financial CSV guard:** never overwrite or bulk-mutate `finance/*.csv`, `ops/crm_simple.csv`, `private/deudas/*.csv` ni `private/ledger/*.csv`. Los CSV de `private/` los gestiona el workflow de ingesta: **append-first**, actualizar sólo una fila identificada; los rewrites masivos requieren confirmación explícita de Alfredo. These hold real ledger / pipeline data.
- **Never** `git push --force` to `main`.
- Commit **only** when Alfredo asks. Never `git add .`/`-A` — stage explicit paths.
- Never `--no-verify` / skip hooks. Markdown is linted on push (GitHub Actions).
- `site/` and `.venv/` are generated/gitignored — never hand-edit or commit.
- Dates in filenames and CSV rows: **ISO 8601** (`YYYY-MM-DD`).
- Language routing: conversation = Spanish (MX) with diacritics; all repo content/docs = Spanish (project convention); commit messages = English (Canadian).

## 4. Workflow

1. New lead → append to `ops/crm_simple.csv` (all fields), recompute weighted pipeline, log next action.
2. Deal closed → update CRM row + add AR row to `finance/ar_tracking.csv`; reflect in weekly KPIs.
3. Deliverables start from `templates/` (fast-cash / retainer / white-label).
4. Fiscal-compliance edits → corresponding `docs/*_cumplimiento_fiscal*.md`.
5. Close each working day with a standup entry.

## 5. Out of scope

- Personal journaling → `personal-os`. Cross-project knowledge → `my-second-brain`.
- Not a code product — no app to build/test beyond the MkDocs static site.
- GitHub Projects kanban (Backlog / Esta semana / En curso / Revisión / Hecho) is optional tracking, not the source of truth — `ops/` is.
