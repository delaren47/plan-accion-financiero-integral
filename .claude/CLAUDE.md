# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is an operational repository for a 90-day financial action plan to transition from debt to profitability through quick wins, retainer conversions, and scalable white-label automation packages. The repository is structured around execution, not just documentation.

**Core Business Model**: Execute "fast cash wins" (48-72h deliverables), convert them to monthly retainers, and scale through white-label products (Knotie-AI voice agents, LancePilot WhatsApp automation, Climbo reputation management) under Delaren Consulting LLC (Wyoming).

## Documentation & Development

### Building and Serving Documentation

This repository uses **MkDocs** with Material theme to publish documentation to GitHub Pages.

```bash
# Activate virtual environment (Python 3.14)
source .venv/bin/activate

# Install MkDocs and dependencies (first time only)
pip install mkdocs mkdocs-material

# Serve documentation locally at http://127.0.0.1:8000
mkdocs serve

# Build static site to site/ directory
mkdocs build

# Deploy to GitHub Pages (gh-pages branch)
mkdocs gh-deploy
```

**Note**: There's no `requirements.txt` in the root; dependencies are managed in the virtual environment.

### Linting

Markdown files are automatically linted on push/PR via GitHub Actions (`.github/workflows/markdown-lint.yml`). The workflow uses `articulate/actions-markdownlint@v1`.

## Repository Architecture

### Directory Structure & Purpose

- **`docs/`** — MkDocs source files for the operational website
  - Primary navigation files: `roadmap_30_60_90.md`, `ofertas_y_precios.md`, `kpis_mensuales_semanales.md`, `validacion_rapida.md`, `llc_cumplimiento_fiscal.md`
  - Research subdirectories contain market analysis and opportunity validation documents

- **`sales/`** — Sales execution materials
  - `guion_cold_openings.md` — cold outreach scripts
  - `email_templates.md` — email templates
  - `propuesta_base.md` — base proposal template

- **`automation/`** — White-label product/package definitions
  - `lancepilot/` — WhatsApp campaign automation templates
  - `knotie/` — Voice AI agent packages
  - `climbo/` — Reputation management offerings

- **`ops/`** — Operational tracking
  - `crm_simple.csv` — CSV-based CRM for leads/clients

- **`finance/`** — Financial tracking and templates
  - `flujo_caja_semanal.csv` — weekly cash flow tracking
  - `ar_tracking.csv` — accounts receivable / DSO tracking
  - `factura_template.md` — invoice template

- **`legal/`** — Legal and compliance documents
  - `revenue_sharing_agreement.md` — revenue-share agreement template
  - `checklist_llc_boi_irs.md` — BOI/IRS compliance checklist for Wyoming LLC

### GitHub Project Workflow

The repository is designed to work with GitHub Projects using a kanban-style board with these columns:

1. **Backlog** — Ideas and opportunities
2. **Esta semana** — This week's commitments with dates
3. **En curso** — In delivery/production
4. **Revisión** — QA/client review
5. **Hecho** — Closed with retrospective and metrics

### Issue Templates

Two specialized issue templates drive the core business process:

- **Fast Cash Win** (`.github/ISSUE_TEMPLATE/fast-cash-win.md`)
  - For quick deliverables (48-72h turnaround)
  - Tracks: 50% upfront payment, delivery deadline, success case/testimonial
  - Labels: `fast-cash`, `prioridad-alta`

- **Retainer Conversion** (`.github/ISSUE_TEMPLATE/retainer-conversion.md`)
  - For converting one-time clients to monthly recurring revenue
  - Tracks: proposal meeting, approval, first monthly payment
  - Labels: `retainer`, `ventas`

### Pull Request Template

PRs must specify:
- Impact on the 30/60/90 roadmap
- Affected KPIs
- Documentation updates

## Key Operational Principles

1. **Measurement Culture**: Every lead and payment must be recorded. Weekly KPI tracking (cash flow, AR/DSO, close rate) is mandatory.

2. **Execution Over Planning**: This repo prioritizes actionable templates and tracking CSVs over theoretical documentation.

3. **Rapid Validation**: The `docs/validacion_rapida.md` document outlines the methodology for testing offers before building full solutions.

4. **Co-selling Model**: The `ops/` directory supports a co-selling arrangement (referenced in revenue sharing agreement).

## Working with This Repository

- **Language**: All documentation, templates, and workflows are in Spanish
- **Git Workflow**: Main branch is `main`, standard GitHub Flow
- **Site URL**: https://delaren47.github.io/plan-accion-financiero-integral/
- **License**: MIT License under Delaren Consulting LLC

When adding new automation packages, quick wins, or sales materials, maintain the existing CSV/markdown template structure and update relevant KPI tracking files in `finance/`.
