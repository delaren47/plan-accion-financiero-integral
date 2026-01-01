# KPIs Mensuales y Semanales

**Sistema de Medición - Plan Acción Financiero Integral**
**Filosofía:** "Lo que se mide, se mejora. Lo que no se mide, se olvida."

---

## Resumen Ejecutivo

Este documento define los KPIs (Key Performance Indicators) que se trackean de manera **semanal** y **mensual** para asegurar el éxito del plan de 90 días.

**Principios de Medición:**
1. **Simplicidad:** Máximo 15 KPIs activos simultáneamente
2. **Accionabilidad:** Cada KPI debe informar una decisión concreta
3. **Automatización:** Calcular automáticamente siempre que sea posible
4. **Accountability:** Cada KPI tiene un owner y target claro
5. **Cadencia Fija:** Viernes 4pm review semanal, último día del mes review mensual

---

## KPIs Semanales (Tracking Viernes 4pm)

### Categoría 1: Ventas y Pipeline

#### KPI-W1: Leads Nuevos Agregados al CRM
**Definición:** Número de nuevos leads contactados y agregados al CRM esta semana
**Cálculo:** Count de filas nuevas en `ops/crm_simple.csv` con `fecha` en rango de semana
**Target:**
- Semanas 1-4: 10 leads/semana
- Semanas 5-8: 15 leads/semana
- Semanas 9-13: 20 leads/semana

**Fuente de Datos:** `ops/crm_simple.csv`
**Owner:** Alfred
**Acción si Red (<50% target):** Aumentar cold calling a 10 llamadas/día

---

#### KPI-W2: Actividades de Prospección Completadas
**Definición:** Suma de llamadas + emails + reuniones realizadas esta semana
**Cálculo:** Manual tracking en standup diario
**Target:**
- Calls: 15-20/semana
- Emails: 25-30/semana
- Reuniones: 3-5/semana
- **Total actividades:** 45-55/semana

**Fuente de Datos:** `ops/standup_diario.md`
**Owner:** Alfred + Hermano (co-selling)
**Acción si Red:** Bloquear 2h diarias solo para prospección

---

#### KPI-W3: Pipeline Value (Weighted)
**Definición:** Suma de (valor_usd × prob_cierre) de todas las oportunidades en pipeline
**Cálculo:**
```
Pipeline Value = SUM(valor_usd × prob_cierre) for all rows in CRM
```
**Target:**
- Semanas 1-4: $10,000 weighted pipeline
- Semanas 5-8: $25,000 weighted pipeline
- Semanas 9-13: $50,000 weighted pipeline

**Fuente de Datos:** `ops/crm_simple.csv` (campos: `valor_usd`, `prob_cierre`)
**Owner:** Alfred
**Acción si Red:** Agregar 10 leads nuevos ASAP

---

#### KPI-W4: Propuestas Enviadas
**Definición:** Número de propuestas formales enviadas esta semana
**Cálculo:** Count de issues con label `propuesta-enviada` creados esta semana
**Target:**
- Semanas 1-4: 2 propuestas/semana
- Semanas 5-8: 3 propuestas/semana
- Semanas 9-13: 4 propuestas/semana

**Fuente de Datos:** GitHub Issues con label `propuesta-enviada`
**Owner:** Alfred
**Acción si Red:** Revisar quality de leads, ajustar targeting

---

### Categoría 2: Ingresos y Cash Flow

#### KPI-W5: Deals Cerrados Esta Semana
**Definición:** Número de fast cash wins + retainers cerrados con firma/pago esta semana
**Cálculo:** Count de issues moved to "Hecho" esta semana
**Target:**
- Semanas 1-4: 1 deal/semana
- Semanas 5-8: 2 deals/semana
- Semanas 9-13: 2-3 deals/semana

**Fuente de Datos:** GitHub Project Board (columna "Hecho")
**Owner:** Alfred
**Acción si Red:** Revisar objeciones comunes, ajustar pitch

---

#### KPI-W6: Ingresos Cobrados Esta Semana
**Definición:** Total USD depositados en cuenta bancaria esta semana
**Cálculo:** `ingresos_cobrados` en `flujo_caja_semanal.csv` para semana actual
**Target:**
- Semanas 1-4: $1,000/semana (promedio)
- Semanas 5-8: $2,500/semana (promedio)
- Semanas 9-13: $4,000/semana (promedio)

**Fuente de Datos:** `finance/flujo_caja_semanal.csv`
**Owner:** Alfred
**Acción si Red:** Acelerar cobro de invoices pendientes, push para cerrar deals

---

#### KPI-W7: Cash Flow Neto Semanal
**Definición:** Ingresos cobrados - Gastos pagados esta semana
**Cálculo:** `flujo` en `flujo_caja_semanal.csv` (auto-calculado)
**Target:**
- Semanas 1-4: Negativo OK (inversión inicial)
- Semanas 5-8: Break-even (flujo >= $0)
- Semanas 9-13: Positivo ($1,500+/semana)

**Fuente de Datos:** `finance/flujo_caja_semanal.csv`
**Owner:** Alfred
**Acción si Red:** Reducir gastos no-esenciales, acelerar cobros

---

### Categoría 3: Eficiencia Operacional

#### KPI-W8: Tiempo de Entrega Promedio (Fast Cash Wins)
**Definición:** Promedio de horas desde kickoff hasta delivery de fast cash wins cerrados esta semana
**Cálculo:** Manual tracking en GitHub Issue body
**Target:** <72 horas (preferiblemente 48-60h)

**Fuente de Datos:** GitHub Issues (campos custom: `horas_estimadas`, `horas_reales`)
**Owner:** Alfred
**Acción si Red:** Revisar templates, identificar bottlenecks, rechazar scope creep

---

#### KPI-W9: DSO (Days Sales Outstanding) - Semanal Snapshot
**Definición:** Promedio de días entre invoice date y pago recibido para invoices cerrados esta semana
**Cálculo:**
```
DSO = AVG(fecha_pago - fecha_invoice) for invoices paid this week
```
**Target:** <15 días (ideal: <7 días con 50% upfront model)

**Fuente de Datos:** `finance/ar_tracking.csv`
**Owner:** Alfred
**Acción si Red:** Follow-up agresivo a 7/14 días, re-enviar invoice

---

#### KPI-W10: Issue Velocity (GitHub)
**Definición:** Número de issues cerrados esta semana (all types)
**Cálculo:** Count de issues moved to "Hecho" esta semana
**Target:** 5-10 issues/semana

**Fuente de Datos:** GitHub Project Board
**Owner:** Alfred
**Acción si Red:** Breakdown large issues, remove blockers, pair con hermano

---

## KPIs Mensuales (Tracking Último Día del Mes)

### Categoría 1: Revenue Metrics

#### KPI-M1: MRR (Monthly Recurring Revenue)
**Definición:** Suma de todos los retainers activos al final del mes
**Cálculo:**
```
MRR = SUM(monthly_fee) for all active retainers
```
**Target:**
- Fin Mes 1 (Enero): $500-$1,500
- Fin Mes 2 (Febrero): $6,000-$10,000
- Fin Mes 3 (Marzo): $12,000-$15,000

**Fuente de Datos:** `ops/crm_simple.csv` filtrado por `etapa = "Retainer Activo"`
**Owner:** Alfred
**Acción si Red:** Acelerar conversiones de fast cash → retainer, ofrecer incentivos

---

#### KPI-M2: Total Revenue (Ingresos Acumulados del Mes)
**Definición:** Suma de todos los ingresos cobrados en el mes (fast wins + retainers + white-label)
**Cálculo:**
```
Total Revenue = SUM(ingresos_cobrados) for all weeks in month
```
**Target:**
- Mes 1: $5,000-$8,000
- Mes 2: $10,000-$15,000
- Mes 3: $15,000-$20,000

**Fuente de Datos:** `finance/flujo_caja_semanal.csv`
**Owner:** Alfred
**Acción si Red:** Push para cerrar pipeline, ofrecer early bird discounts

---

#### KPI-M3: Revenue Mix (% por Tipo de Producto)
**Definición:** Distribución porcentual de revenue por tipo: Fast Wins / Retainers / White-Label
**Cálculo:**
```
Fast Wins %   = (Revenue Fast Wins / Total Revenue) × 100
Retainers %   = (MRR × 1 mes / Total Revenue) × 100
White-Label % = (Revenue White-Label / Total Revenue) × 100
```
**Target (evolución):**
- Mes 1: 80% Fast / 10% Retainer / 10% White-Label
- Mes 2: 50% Fast / 40% Retainer / 10% White-Label
- Mes 3: 30% Fast / 50% Retainer / 20% White-Label

**Fuente de Datos:** Manual categorization en `finance/flujo_caja_semanal.csv`
**Owner:** Alfred
**Acción si Red:** Focus en conversión a retainers, push white-label sales

---

### Categoría 2: Pipeline & Conversión

#### KPI-M4: Close Rate (Win Rate)
**Definición:** Porcentaje de propuestas enviadas que se convierten en deals cerrados
**Cálculo:**
```
Close Rate = (Deals Cerrados / Propuestas Enviadas) × 100
```
**Target:**
- Mes 1: >10%
- Mes 2: >15%
- Mes 3: >20%

**Fuente de Datos:** GitHub Issues (labels: `propuesta-enviada`, `deal-cerrado`)
**Owner:** Alfred
**Acción si Red:** Revisar pitch deck, mejorar qualification de leads, ajustar pricing

---

#### KPI-M5: Conversion Rate (Fast Cash → Retainer)
**Definición:** Porcentaje de fast cash wins que se convierten en retainer en los siguientes 60 días
**Cálculo:**
```
Conversion Rate = (Fast Wins → Retainer / Total Fast Wins Delivered) × 100
```
**Target:**
- Mes 1: >20% (baseline)
- Mes 2: >30%
- Mes 3: >40%

**Fuente de Datos:** Tracking manual en GitHub Issues
**Owner:** Alfred
**Acción si Red:** Mejorar follow-up post-delivery, crear retainer pitch deck

---

#### KPI-M6: Average Deal Size
**Definición:** Valor promedio en USD de todos los deals cerrados en el mes
**Cálculo:**
```
Avg Deal Size = Total Revenue / Number of Deals Closed
```
**Target:**
- Mes 1: $700-$900
- Mes 2: $1,200-$1,500
- Mes 3: $1,500-$2,000

**Fuente de Datos:** `finance/flujo_caja_semanal.csv` + GitHub Issues
**Owner:** Alfred
**Acción si Red:** Upsell a paquetes más grandes, bundle offers

---

### Categoría 3: Finanzas y Salud del Negocio

#### KPI-M7: DSO Mensual (Days Sales Outstanding)
**Definición:** Promedio de días entre invoice date y pago recibido para todos los invoices del mes
**Cálculo:**
```
DSO = AVG(fecha_pago - fecha_invoice) for all invoices closed in month
```
**Target:** <20 días (ideal: <15 días)

**Fuente de Datos:** `finance/ar_tracking.csv`
**Owner:** Alfred
**Acción si Red:** Implementar auto-debit, penalizar late payments, follow-up sistemático

---

#### KPI-M8: Cash Flow Positivo (% de Semanas)
**Definición:** Porcentaje de semanas del mes con flujo neto positivo (ingresos > gastos)
**Cálculo:**
```
Cash Flow Positivo % = (Semanas con flujo > 0 / Total Semanas en Mes) × 100
```
**Target:**
- Mes 1: 50% (2/4 semanas)
- Mes 2: 75% (3/4 semanas)
- Mes 3: 100% (4/4 semanas)

**Fuente de Datos:** `finance/flujo_caja_semanal.csv`
**Owner:** Alfred
**Acción si Red:** Reducir gastos, acelerar cobros, diferir pagos no-urgentes

---

#### KPI-M9: AR Pendiente (Accounts Receivable Outstanding)
**Definición:** Total USD en invoices enviados pero aún no cobrados al final del mes
**Cálculo:**
```
AR Pendiente = SUM(monto_invoice) for invoices with status != "Pagado"
```
**Target:** <$3,000 (maximum)

**Fuente de Datos:** `finance/ar_tracking.csv`
**Owner:** Alfred
**Acción si Red:** Collection calls, payment plans, legal letter para >60 días

---

### Categoría 4: Cliente y Producto

#### KPI-M10: Retainer Churn Rate
**Definición:** Porcentaje de retainers que cancelan en el mes vs. total de retainers activos al inicio del mes
**Cálculo:**
```
Churn Rate = (Retainers Cancelados / Retainers Inicio Mes) × 100
```
**Target:** <10% mensual

**Fuente de Datos:** `ops/crm_simple.csv`
**Owner:** Alfred
**Acción si Red:** Exit interview con cliente, ofrecer discount para retener, mejorar service quality

---

#### KPI-M11: NPS (Net Promoter Score)
**Definición:** Score de recomendación del cliente (escala 0-10)
**Cálculo:**
```
NPS = % Promoters (9-10) - % Detractors (0-6)
```
**Target:**
- Mes 1: >50 (baseline)
- Mes 2: >60
- Mes 3: >70

**Fuente de Datos:** Survey post-delivery (Google Form)
**Owner:** Alfred
**Acción si Red:** Analizar feedback, mejorar pain points, over-deliver

---

#### KPI-M12: Testimoniales Obtenidos
**Definición:** Número de testimoniales/reviews positivos capturados en el mes
**Cálculo:** Count de archivos en `sales/testimonials/`
**Target:**
- Mes 1: 3-5 testimonials
- Mes 2: 5-8 testimonials
- Mes 3: 8-12 testimonials

**Fuente de Datos:** `sales/testimonials/` directory
**Owner:** Alfred
**Acción si Red:** Request testimonial en email post-delivery, incentivizar con discount

---

### Categoría 5: Actividad y Esfuerzo

#### KPI-M13: Total Horas Trabajadas
**Definición:** Total de horas trabajadas en el negocio en el mes (billable + non-billable)
**Cálculo:** Manual time tracking
**Target:** 160-200 horas/mes (40-50h/semana)

**Fuente de Datos:** Time tracking tool (Toggl o manual)
**Owner:** Alfred
**Acción si Red (>200h):** Contratar VA, automatizar tareas repetitivas, rechazar low-value work

---

#### KPI-M14: Reuniones de Prospección Realizadas
**Definición:** Número total de reuniones (calls, Zoom, in-person) con prospectos en el mes
**Cálculo:** Manual count en `ops/standup_diario.md`
**Target:**
- Mes 1: 12-15 reuniones
- Mes 2: 15-20 reuniones
- Mes 3: 20-25 reuniones

**Fuente de Datos:** `ops/standup_diario.md`
**Owner:** Alfred
**Acción si Red:** Increase outbound, optimize calendar, batch reuniones en 2 días/semana

---

#### KPI-M15: Paquetes White-Label Vendidos
**Definición:** Número de paquetes white-label (Knotie, LancePilot, Climbo) vendidos en el mes
**Cálculo:** Count de GitHub Issues con label `white-label` cerrados
**Target:**
- Mes 1: 0-1
- Mes 2: 1-2
- Mes 3: 2-3

**Fuente de Datos:** GitHub Issues (label: `white-label`)
**Owner:** Alfred
**Acción si Red:** Crear case study, ofrecer piloto gratuito, ajustar pricing

---

## Dashboard Semanal (Template)

```
=== WEEKLY KPI DASHBOARD ===
Semana: [Número] (Fecha inicio - Fecha fin)

📊 VENTAS & PIPELINE
- Leads Nuevos:              [X] / Target: [Y]  [🔴🟡🟢]
- Actividades Prospección:   [X] / Target: [Y]  [🔴🟡🟢]
- Pipeline Value (Weighted): $[X] / Target: $[Y] [🔴🟡🟢]
- Propuestas Enviadas:       [X] / Target: [Y]  [🔴🟡🟢]

💰 INGRESOS & CASH FLOW
- Deals Cerrados:            [X] / Target: [Y]  [🔴🟡🟢]
- Ingresos Cobrados:         $[X] / Target: $[Y] [🔴🟡🟢]
- Cash Flow Neto:            $[X] / Target: $[Y] [🔴🟡🟢]

⚙️ OPERACIONES
- Tiempo Entrega Promedio:   [X]h / Target: <72h [🔴🟡🟢]
- DSO Snapshot:              [X] días / Target: <15 [🔴🟡🟢]
- Issue Velocity:            [X] / Target: [Y]  [🔴🟡🟢]

📝 HIGHLIGHTS DE LA SEMANA
- Wins: [Describe 2-3 wins principales]
- Blockers: [Describe 1-2 blockers actuales]
- Acción Siguiente Semana: [Top 3 prioridades]
```

---

## Dashboard Mensual (Template)

```
=== MONTHLY KPI DASHBOARD ===
Mes: [Nombre del Mes] 2026

💵 REVENUE METRICS
- MRR:                       $[X] / Target: $[Y] [🔴🟡🟢]
- Total Revenue:             $[X] / Target: $[Y] [🔴🟡🟢]
- Revenue Mix:               Fast: [X]% | Retainer: [Y]% | White-Label: [Z]%

🎯 PIPELINE & CONVERSIÓN
- Close Rate:                [X]% / Target: [Y]% [🔴🟡🟢]
- Fast→Retainer Conv:        [X]% / Target: [Y]% [🔴🟡🟢]
- Average Deal Size:         $[X] / Target: $[Y] [🔴🟡🟢]

💸 FINANZAS
- DSO Mensual:               [X] días / Target: <20 [🔴🟡🟢]
- Cash Flow Positivo:        [X]% semanas / Target: [Y]% [🔴🟡🟢]
- AR Pendiente:              $[X] / Target: <$3,000 [🔴🟡🟢]

👥 CLIENTE & PRODUCTO
- Retainer Churn:            [X]% / Target: <10% [🔴🟡🟢]
- NPS:                       [X] / Target: [Y] [🔴🟡🟢]
- Testimoniales:             [X] / Target: [Y] [🔴🟡🟢]

⏱️ ACTIVIDAD
- Horas Trabajadas:          [X]h / Target: 160-200h [🔴🟡🟢]
- Reuniones Prospección:     [X] / Target: [Y] [🔴🟡🟢]
- White-Label Vendidos:      [X] / Target: [Y] [🔴🟡🟢]

📈 TRENDS (vs. Mes Anterior)
- MRR: [↑↓→] [X]%
- Total Revenue: [↑↓→] [X]%
- Close Rate: [↑↓→] [X]%
- DSO: [↑↓→] [X] días

📝 RETROSPECTIVA MENSUAL
- Top 3 Wins: [Describe]
- Top 3 Learnings: [Describe]
- Top 3 Acciones Próximo Mes: [Describe]
```

---

## Sistema de Semáforos (Red/Yellow/Green)

| Status | Criteria | Acción |
|--------|----------|--------|
| 🟢 **Green** | >90% of target | Mantener curso, documentar best practices |
| 🟡 **Yellow** | 70-89% of target | Light course correction, monitor closely |
| 🔴 **Red** | <70% of target | Immediate intervention required, ejecutar mitigación |

---

## Automatización de KPIs

### Scripts Recomendados

#### Script 1: `ops/calculate_weekly_kpis.sh`
```bash
# Pseudo-código (implementar en Semana 2)
# Lee CRM, flujo_caja, GitHub API
# Calcula KPIs W1-W10
# Genera dashboard en markdown
# Envia resumen por email/Slack
```

#### Script 2: `ops/calculate_monthly_kpis.sh`
```bash
# Pseudo-código (implementar en Semana 4)
# Consolida data de 4 semanas
# Calcula KPIs M1-M15
# Genera trends vs. mes anterior
# Crea PDF report para stakeholders
```

---

## Responsabilidades de Medición

| Rol | Responsabilidad | Frecuencia |
|-----|-----------------|------------|
| **Alfred** | Update CRM daily | Diaria |
| **Alfred** | Update flujo_caja_semanal.csv | Semanal (Viernes) |
| **Alfred** | Run weekly KPI review | Semanal (Viernes 4pm) |
| **Alfred** | Run monthly KPI deep dive | Mensual (último día) |
| **Hermano (Co-selling)** | Report leads y actividades | Semanal |

---

## Escalamiento de KPIs (Post Día 90)

A partir del Día 91, considerar agregar:
- **Customer Acquisition Cost (CAC)**
- **Lifetime Value (LTV)**
- **LTV:CAC Ratio**
- **Monthly Burn Rate**
- **Runway (months of cash remaining)**
- **Employee/VA Productivity Metrics**

---

**Última Actualización:** 31 de diciembre, 2025
**Próxima Revisión:** 7 de enero, 2026 (Primera Weekly Review)
**Owner:** Alfred (Delaren Consulting LLC)
