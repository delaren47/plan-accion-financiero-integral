# CLAUDE.md — PAFI (Plan Acción Financiero Integral)

**Updated:** 2026-05-28

90-day financial action plan: debt → profitability via fast-cash wins (48-72h deliverables) → monthly retainers → white-label products (Knotie-AI voice, LancePilot WhatsApp, Climbo reputation), under Delaren Consulting LLC (Wyoming). This is a markdown + CSV PM repo, not a code product. Read `~/.claude/CLAUDE.md` for global prefs.

The published MkDocs site (`docs/` → GitHub Pages) is the public face; day-to-day PM happens in `ops/`, `finance/`, `sales/`. The detailed AI workflows live in **`.claude/instructions.md`** — read it for standup / weekly / monthly / new-lead / deal-closed procedures.

---

## 1. Commands & rituals

- `/pafi` — load full project context (session opener).
- **Daily standup** → append a dated entry to `ops/standup_diario.md` (template at top of file). See `.claude/instructions.md`.
- **Weekly review** (Fridays 4pm) → `ops/review_semanal.md`; recompute KPIs from `ops/crm_simple.csv` + `finance/flujo_caja_semanal.csv`.
- **Monthly retrospective** (last day of month) → trends + revenue mix per `.claude/instructions.md`.
- Active pending work tracked in `ops/P1_ITEMS_PENDIENTES.md`.
- Site preview (optional): `source .venv/bin/activate && mkdocs serve`. Deploy = `mkdocs gh-deploy`.

## 2. Folder map

| Folder | Purpose | Mutability |
|---|---|---|
| `docs/` | MkDocs source: roadmap, ofertas, KPIs, validación, fiscal-compliance guides | edit; publishes to Pages |
| `ops/` | Standup, weekly review, P1 items, CRM CSV, daily-activities CSV | edit (append-first) |
| `finance/` | Cash-flow / AR-tracking / fixed-costs / invoice-log CSVs + factura template | **CSV-guarded** (see rules) |
| `sales/` | Cold-opening scripts, email + proposal templates | edit |
| `automation/` | White-label package defs (lancepilot / knotie / climbo) | edit |
| `legal/` | Revenue-share agreement, BOI/IRS LLC checklist | edit carefully |
| `templates/` | Fast-cash-win / retainer / white-label deliverable templates | edit |
| `site/` | MkDocs **build output** — generated, gitignored | never hand-edit |

## 3. Hard rules

- **Financial CSV guard:** never overwrite or bulk-mutate `finance/*.csv` or `ops/crm_simple.csv`. Only **append rows** or **update a specific identified row**, and only after explicit confirmation from Alfredo. These hold real ledger / pipeline data.
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
