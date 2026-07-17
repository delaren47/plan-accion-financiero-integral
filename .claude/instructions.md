# Project Instructions - Plan Acción Financiero Integral

This file provides Claude Code with project-specific workflows and context when working in this repository.

> **Nota de relanzamiento (2026-07-17):** el proyecto es ahora **P0 — eliminación de deuda de tarjeta de crédito** (ver `DEBT_MASTER_PLAN.md`). El workflow central es la **ingesta financiera** y el ritual **Money Friday** (secciones abajo). Los workflows de negocio (standup, weekly, monthly, new-lead, deal-closed) siguen siendo válidos para el trabajo de ingresos **P1**, pero no son el foco por default.

---

## Quick Context

**Project Type:** Personal-finance command center (P0 debt elimination) + internal business venture (P1/P3)
**Status:** Active — P0 debt elimination (relaunched 2026-07-17)
**Owner:** Alfred (Delaren Consulting LLC)
**Command:** `/pafi` (loads full context from `~/.claude/references/internal/active/plan-accion-financiero-integral/`)

---

## Workflow P0 — Ingesta financiera

El workflow principal en P0. Convierte estados de cuenta crudos en datos estructurados bajo `private/` (gitignored, nunca versionado).

1. **Trigger:** Alfredo dice **"procesa la ingesta"** — o existen archivos en `private/ingesta/`.
2. **Leer** cada archivo en `private/ingesta/` (PDFs, CSVs, screenshots).
3. **Por cada estado de cuenta**, extraer: acreedor, saldo, tasa / CAT, fecha de corte, fecha límite de pago, pago mínimo, pago para no generar intereses, y los movimientos del período.
4. **Escribir** (append-first, sólo filas identificadas; sin rewrites masivos):
   - `private/deudas/deudas_registro.csv` — una fila por tarjeta; actualizar `saldo` + fecha `actualizado`.
   - `private/deudas/pagos_deuda.csv` — append de cada pago.
   - `private/ledger/ingresos.csv` — append de ingresos.
   - `private/ledger/gastos.csv` — append de gastos.
   - Cualquier cargo recurrente detectado → `private/ledger/suscripciones_saas.csv` con decisión `pendiente`.
5. **Archivar:** mover el archivo procesado a `private/ingesta/procesado/YYYY-MM/`.
6. **Regenerar** `private/DASHBOARD.md`: totales, tasa ponderada, interés/mes, próximas fechas de corte y límite, total de SaaS.
7. **Reportar** a Alfredo: qué cambió, anomalías (cargos no reconocidos, subidas de tasa), y la única acción de mayor impacto.

**Guard:** los números reales viven SÓLO en `private/`. Nunca copiar saldos a docs versionados ni al sitio MkDocs.

## Workflow P0 — Money Friday

Ritual semanal de 15 min (viernes):

1. Procesar la ingesta pendiente (ver workflow arriba) si hay archivos nuevos.
2. Refrescar `private/DASHBOARD.md`.
3. Registrar los pagos de la semana en `private/deudas/pagos_deuda.csv`.
4. Decidir el excedente semanal y aplicarlo contra la tarjeta de **mayor CAT** (avalancha — ver `DEBT_MASTER_PLAN.md`).
5. Revisar las próximas fechas de corte para no perder ninguna.

---

## Project Workflows

> Los workflows de esta sección son de negocio (P1 ingresos / P3 parqueado). Válidos, pero secundarios al P0.

### Daily Standup Workflow
When user asks for daily standup or progress update:

1. Read current week's KPIs from `docs/kpis_mensuales_semanales.md`
2. Check `ops/crm_simple.csv` for pipeline updates
3. Review `finance/flujo_caja_semanal.csv` for cash flow status
4. Check GitHub Issues for in-progress work
5. Provide brief summary:
   - What was done yesterday
   - What's planned today
   - Any blockers

### Weekly Review Workflow (Every Friday 4pm)
When user requests weekly review:

1. Calculate 10 weekly KPIs from tracking files:
   - `ops/crm_simple.csv` (leads, pipeline, proposals)
   - `finance/flujo_caja_semanal.csv` (revenue, cash flow)
   - GitHub Issues (deals closed, velocity)
2. Generate dashboard using template from `docs/kpis_mensuales_semanales.md`
3. Create weekly note in `~/.claude/references/internal/active/plan-accion-financiero-integral/notes/`
4. Identify top wins, blockers, and next week priorities

### Monthly Retrospective Workflow (Last day of month)
When user requests monthly review:

1. Calculate 15 monthly KPIs
2. Generate trends vs. previous month
3. Analyze revenue mix (Fast/Retainer/White-label %)
4. Create monthly retrospective note
5. Recommend strategic adjustments

### New Lead Workflow
When user mentions new lead:

1. Add to `ops/crm_simple.csv` with all required fields
2. Calculate weighted pipeline value
3. Suggest next actions based on lead stage
4. Update weekly KPI tracking

### Deal Closed Workflow
When a deal is closed:

1. Update CRM status to appropriate stage
2. Record payment in `finance/flujo_caja_semanal.csv`
3. Create/update invoice in `finance/`
4. Close GitHub Issue
5. Prompt for testimonial request
6. Suggest retainer conversion opportunity

### Proposal Creation Workflow
When user needs to create proposal:

1. Read `sales/propuesta_base.md` template
2. Personalize with client context from CRM
3. Include relevant pricing from `docs/ofertas_y_precios.md`
4. Add appropriate case study/testimonial
5. Generate proposal document
6. Create GitHub Issue with `propuesta-enviada` label

---

## Key Operational Principles

### Measurement First
- Every lead must be tracked in CRM
- Every payment must be recorded in cash flow
- Weekly KPI review is mandatory (Friday 4pm)
- No assumptions - verify with data

### Execution Over Planning
- Prioritize actionable tasks over documentation
- Ship fast, iterate based on feedback
- Done is better than perfect
- 72h hard deadline for fast cash wins

### Client-Centric
- 50% upfront payment is non-negotiable (protects cash flow)
- No scope creep - stick to proposal or create new one
- Over-communicate during delivery
- Ask for testimonial after every win

---

## File Organization Rules

### When Creating New Documents
- Sales materials → `sales/`
- Automation templates → `automation/`
- Financial records → `finance/`
- Legal documents → `legal/`
- Documentation → `docs/` (MkDocs format)

### When Updating Tracking Files
- CRM: Add rows, never delete (mark as "No Calificado" or "No Interesado")
- Cash flow: One row per week, update weekly
- AR tracking: Update payment status when received

### When Creating GitHub Issues
Use appropriate template:
- Fast Cash Win: `.github/ISSUE_TEMPLATE/fast-cash-win.md`
- Retainer Conversion: `.github/ISSUE_TEMPLATE/retainer-conversion.md`

---

## Common Tasks & Commands

### Generate Weekly KPI Dashboard
```bash
# Read tracking files
# Calculate 10 weekly KPIs
# Output formatted dashboard using template
# Create note in ~/.claude/references/internal/active/plan-accion-financiero-integral/notes/
```

### Update CRM with New Lead
```bash
# Prompt for: fecha, origen, empresa, contacto, email, telefono, etapa, prob_cierre, valor_usd, notas
# Add row to ops/crm_simple.csv
# Recalculate weighted pipeline value
```

### Create Proposal
```bash
# Use sales/propuesta_base.md template
# Personalize with client info from CRM
# Include pricing from docs/ofertas_y_precios.md
# Save to sales/proposals/[client-name]-propuesta.md
```

### Deploy Documentation Updates
```bash
source .venv/bin/activate
mkdocs gh-deploy
```

---

## Language Preferences

- **All client-facing materials:** Spanish
- **All documentation in docs/:** Spanish
- **Internal code/technical:** English OK
- **CRM/tracking files:** Spanish field names preferred

---

## Git Workflow

### Commit Messages
Use conventional commits format:
```
feat: add new fast cash win offering
fix: correct pricing in propuesta_base.md
docs: update roadmap with week 2 progress
chore: update CRM with 5 new leads
```

### Pull Requests
Not typically used (single developer), but if needed:
- Specify impact on 30/60/90 roadmap
- List affected KPIs
- Note documentation updates

---

## Reminders & Guardrails

### Non-Negotiables
- 50% upfront payment on all fast cash wins
- 72h hard deadline (scope creep = new proposal)
- Weekly KPI review every Friday 4pm
- Every lead tracked in CRM
- 1 day off per week mandatory

### Red Flags
- If close rate <10% → Review pricing or qualification
- If DSO >30 days → Accelerate collections
- If churn >10% → Review service quality
- If burnout signs → Reduce to max 2 fast wins/week

---

## Integration with Internal Projects System

This project is part of Alfred's internal projects system:

**Location:** `~/.claude/references/internal/active/plan-accion-financiero-integral/`

**Related Projects:**
- **ada** (Alfredo 3.0 Life OS) - Personal development system
  - pafi supports Pillar 3 (Wealth & Security) and Pillar 4 (Work & Legacy)

**Commands:**
- `/pafi` - Quick context and morning briefing
- `/internal pafi` - Full context load (not yet implemented)

---

## Troubleshooting

### "CRM file not found"
Check path: `ops/crm_simple.csv` (relative to repo root)

### "MkDocs build fails"
```bash
source .venv/bin/activate
pip install mkdocs mkdocs-material
mkdocs build
```

### "GitHub Pages not updating"
```bash
mkdocs gh-deploy --force
```

---

**Last Updated:** 2026-07-17
**Owner:** Alfred
