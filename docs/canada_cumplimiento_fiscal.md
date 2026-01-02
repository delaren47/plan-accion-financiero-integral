# Cumplimiento Fiscal Canadá (CRA)

**Guía de Compliance para Operaciones en Canadá**
**Jurisdicción:** Canadá
**Autoridad Fiscal:** Canada Revenue Agency (CRA)
**Tipo de Entidad:** Corporation (Federal o Provincial)

---

## Resumen Ejecutivo

Operar un negocio en Canadá ofrece:
1. **Acceso al mercado norteamericano:** Segunda economía de América del Norte
2. **Tax efficiency:** Small business deduction (9% federal en primeros $500k CAD)
3. **Tratado fiscal USA-Canadá:** Evita doble tributación
4. **Credibilidad:** Entidad canadiense para clientes locales e internacionales
5. **Sistema tributario predecible:** Estructura clara y bien documentada

**Compliance Timeline:**
- **Business Number (BN):** Inmediatamente después de incorporación
- **T2 Corporate Tax Return:** 6 meses después del fin del año fiscal
- **GST/HST Filing:** Mensual, trimestral o anual (según revenue)
- **Instalments:** Último día de cada mes (si tax owed >$3,000)
- **T4/T5 Slips:** Último día de febrero (año siguiente)
- **Provincial Annual Return:** Varía por provincia (anual)

---

## Obligaciones Federales (CRA)

### 1. Business Number (BN)

**¿Qué es?**
Identificador único de 9 dígitos para tu negocio en Canadá (equivalente al EIN en USA).

**Cuándo obtenerlo:**
✅ **Inmediatamente** después de incorporar tu empresa (antes de abrir cuenta bancaria).

**Cómo obtenerlo:**
1. **Online:** CRA My Business Account - https://www.canada.ca/en/revenue-agency/services/e-services/e-services-businesses/business-account.html
2. **Por teléfono:** 1-800-959-5525 (Business Enquiries)
3. **Por correo:** Form RC1 (Request for a Business Number)

**Tiempo:** 5-10 minutos online, BN asignado inmediatamente

**Costo:** $0 (gratis)

**Program Accounts vinculados al BN:**
- **RC (Corporate Income Tax):** Para T2 returns
- **RT (GST/HST):** Para impuesto al valor agregado
- **RP (Payroll Deductions):** Para empleados
- **RZ (GST/HST rebates):** Para devoluciones
- **RM (Import-Export):** Para comercio internacional

**Documentación:**
- Guardar BN confirmation letter en `legal/canada/bn_confirmation.pdf`
- Usar BN en:
  - Apertura de cuenta bancaria
  - Facturas a clientes canadienses
  - Filings de impuestos
  - Correspondencia con CRA

---

### 2. Corporate Income Tax (T2 Return)

**¿Qué es?**
Declaración anual de impuestos corporativos en Canadá.

**Tax Rates 2026:**

| Tipo de Ingreso | Federal Rate | Provincial Rate (Promedio) | Combined Rate |
|-----------------|--------------|---------------------------|---------------|
| **Small Business Income** (primeros $500k CAD si CCPC) | 9% | 2-4% | **11-13%** |
| **General Corporate Income** (>$500k o non-CCPC) | 15% | 11-16% | **26-31%** |

**CCPC (Canadian-Controlled Private Corporation):**
- Definición: Corporación privada controlada por residentes canadienses
- **Benefit:** Small business deduction del 9% federal en primeros $500,000 CAD de active business income
- **Resultado:** Combined tax rate de solo 11-13% (vs. 26-31% general rate)
- **Requisito:** Mayoría de shareholders deben ser residentes canadienses

**Provincial Tax Rates (2026):**
| Provincia | Small Business Rate | General Rate | Small Business Limit |
|-----------|---------------------|--------------|---------------------|
| Ontario | 3.2% | 11.5% | $500,000 |
| British Columbia | 2.0% | 12.0% | $500,000 |
| Alberta | 2.0% | 8.0% | $500,000 |
| Quebec | 3.2% | 11.5% | $500,000 |
| Manitoba | 0% | 12.0% | $500,000 |
| Saskatchewan | 0% | 12.0% | $600,000 |

**Filing Deadlines:**
- **Deadline to File:** 6 meses después del fin del año fiscal
  - Ejemplo: Año fiscal termina Dec 31, 2026 → T2 due Jun 30, 2027
- **Deadline to Pay:**
  - **CCPC:** 3 meses después del fin del año fiscal
  - **Non-CCPC:** 2 meses después del fin del año fiscal

**Penalidad por Late Filing:**
- 5% del tax unpaid + 1% por mes (máximo 12 meses)
- Ejemplo: $10,000 owed, 3 meses tarde = $500 (5%) + $300 (3 × 1%) = **$800 penalty**

**Cómo Filing:**
1. **Tax Software:** TurboTax Business, TaxCycle, Profile
2. **CPA/Accountant:** Recomendado para primer año (Cost: $1,500-$3,000 CAD)
3. **Efile:** Preferred method (electronic filing)

**Información Requerida:**
- Financial statements (Balance Sheet, Income Statement, Cash Flow)
- Schedule 1 (Net Income/Loss)
- Schedule 8 (Capital Cost Allowance - depreciación)
- Schedule 50 (Shareholder information)
- GIFI (General Index of Financial Information) - código contable estándar

**Documentación:**
- Guardar T2 filed en `legal/canada/tax_filings/t2_[YEAR].pdf`
- Mantener records por 6 años (CRA audit period)

---

### 3. GST/HST (Goods and Services Tax / Harmonized Sales Tax)

**¿Qué es?**
Impuesto al valor agregado (similar al IVA en México o VAT en Europa).

**Registration Threshold:**
- **Obligatorio:** Si revenue >$30,000 CAD en últimos 4 trimestres consecutivos
- **Voluntary:** Si revenue <$30,000 (beneficio: recuperar GST/HST paid on expenses vía ITCs)

**Rates by Province (2026):**

| Provincia | Type | Rate | Breakdown |
|-----------|------|------|-----------|
| **Ontario** | HST | 13% | 5% federal + 8% provincial |
| **Nova Scotia** | HST | 15% | 5% federal + 10% provincial |
| **New Brunswick** | HST | 15% | 5% federal + 10% provincial |
| **Newfoundland & Labrador** | HST | 15% | 5% federal + 10% provincial |
| **PEI** | HST | 15% | 5% federal + 10% provincial |
| **British Columbia** | GST + PST | 5% + 7% | GST 5%, separate PST 7% |
| **Alberta** | GST only | 5% | No provincial tax |
| **Saskatchewan** | GST + PST | 5% + 6% | GST 5%, separate PST 6% |
| **Manitoba** | GST + RST | 5% + 7% | GST 5%, separate RST 7% |
| **Quebec** | GST + QST | 5% + 9.975% | GST 5%, separate QST 9.975% |

**Filing Frequency:**
- **Annual:** Revenue <$1.5 million CAD (deadline: 3 meses después del fiscal year-end)
- **Quarterly:** Revenue $1.5M - $6M CAD (deadline: 1 mes después del quarter-end)
- **Monthly:** Revenue >$6M CAD (deadline: último día del mes siguiente)

**Input Tax Credits (ITCs):**
- **Concepto:** Recuperar el GST/HST que pagaste en gastos del negocio
- **Ejemplo:**
  - Cobraste GST: $5,000
  - Pagaste GST en expenses: $2,000 (ITC)
  - **Net GST owed:** $5,000 - $2,000 = **$3,000**
- **Eligible expenses:** Office supplies, software, professional services, travel, etc.

**Zero-Rated vs. Exempt:**
- **Zero-rated (0%):** Basic groceries, prescription drugs, exports (still eligible for ITCs)
- **Exempt:** Healthcare, education, residential rent (NOT eligible for ITCs)
- **Consulting services:** 5-15% GST/HST (depends on province)

**Cómo Registrar:**
1. Online: CRA My Business Account (instant registration)
2. Form RC1 (Request for BN and Program Accounts)

**Cómo Filing:**
1. **GST/HST Netfile:** https://www.canada.ca/en/revenue-agency/services/e-services/e-services-businesses/gst-hst-netfile.html
2. **CRA My Business Account**
3. **Software:** QuickBooks Online, FreshBooks, Wave (integrated filing)

**Penalidad por Late Filing:**
- 1% del amount owing + 0.25% por mes
- Plus: interest compounding daily

**Documentación:**
- Guardar GST/HST returns en `legal/canada/tax_filings/gst_hst_[YEAR]_[PERIOD].pdf`
- Mantener invoices y receipts por 6 años

---

### 4. Corporate Tax Instalments

**¿Qué es?**
Pagos mensuales estimados de impuestos corporativos (como quarterly estimated taxes en USA).

**Cuándo Required:**
- Si total tax owed >$3,000 en current year AND en either de los 2 años previos

**Payment Schedule:**
- **Frecuencia:** Mensual
- **Deadline:** Último día de cada mes
- **Cantidad:** 1/12 del estimated annual tax

**Calculation Methods:**
1. **Prior-year method:** Basado en tax paid el año anterior
2. **Current-year method:** Basado en estimated current-year income
3. **Prior-year first + current-year second:** Hybrid approach

**Ejemplo:**
- 2025 tax owed: $48,000
- 2026 estimated tax: $60,000
- **Monthly instalment:** $60,000 / 12 = **$5,000/month**

**Cómo Pagar:**
1. **Online Banking:** Add CRA as payee (usar BN como account number)
2. **CRA My Payment:** https://www.canada.ca/en/revenue-agency/services/e-services/payment-save-time-pay-online.html
3. **Wire Transfer:** For large amounts

**Penalidad por Underpayment:**
- Interest charged en shortfall (tasa CRA prescribed rate + 4%)
- No flat penalty, solo interest

**Documentación:**
- Track payments en `finance/canada/tax_instalments.csv`

---

### 5. Provincial Corporate Tax

**¿Cómo funciona?**
Cada provincia cobra su propio corporate income tax, pero CRA lo administra (excepto Quebec y Alberta en ciertos casos).

**Filing:**
- **Integrated with T2:** Completas un solo T2 form, CRA distribuye a provincias
- **Quebec excepción:** Debe filing separado (Formulario CO-17 con Revenu Québec)

**Provincial Rates:** (Ver tabla en sección 2)

**Provincial Tax Credits:**
- Varían por provincia (R&D credits, film credits, etc.)
- Consultar provincial tax authority

---

### 6. Foreign Reporting Requirements

**T1135 (Foreign Income Verification Statement)**

**¿Qué es?**
Reporte de propiedades extranjeras (foreign property) con costo >$100,000 CAD.

**Cuándo Required:**
- Si en algún momento del año tuviste foreign property >$100,000 CAD

**Foreign Property incluye:**
- Cuentas bancarias extranjeras
- Acciones en corporaciones extranjeras
- Bienes raíces fuera de Canadá
- Deudas owed by non-residents

**Deadline:**
- Filing deadline del T2 (6 meses después del fiscal year-end)

**Penalidad por no filing:**
- $25/día (min $100, max $2,500)
- Más: gross negligence penalties si intencional

**T1134 (Information Return Relating to Foreign Affiliates)**

**¿Qué es?**
Reporte de foreign affiliates (subsidiarias extranjeras).

**Cuándo Required:**
- Si corporation tiene >10% de shares en foreign corporation

**Deadline:**
- 15 meses después del fin del fiscal year

**Documentación:**
- Guardar T1135/T1134 en `legal/canada/foreign_reporting/`

---

## Obligaciones Provinciales

### 1. Provincial Business Registration

**¿Por qué necesario?**
Si incorporas federalmente (Corporations Canada) pero operas en provincias, debes registrarte como extra-provincial corporation.

**Ontario Extra-Provincial Licence:**
- **Costo:** $330 + $30 annual return
- **Portal:** https://www.ontario.ca/page/register-extra-provincial-corporation
- **Deadline:** Antes de hacer negocios en Ontario

**BC Extra-Provincial Registration:**
- **Costo:** $350 + $53.95 annual report
- **Portal:** https://www.bcregistry.gov.bc.ca/
- **Deadline:** Antes de operating en BC

**Alberta Extra-Provincial Registration:**
- **Costo:** $275 + $40 annual return
- **Portal:** https://www.alberta.ca/extra-provincial-registration.aspx
- **Deadline:** Antes de transacting business en Alberta

**Quebec Registration (Registraire des entreprises):**
- **Costo:** $378 (incorporation) + $46 (annual update)
- **Portal:** https://www.registreentreprises.gouv.qc.ca/
- **Idioma:** Formularios en francés (requisito)

**Recommended Strategy:**
- **Federal incorporation:** Si planeas operar en múltiples provincias
- **Provincial incorporation:** Si solo operarás en una provincia (más barato)

---

### 2. Provincial Annual Returns

**Ontario Annual Return (Form 1):**
- **Deadline:** Aniversario de incorporation
- **Costo:** $30 online
- **Información:** Directors, registered office address, shares issued
- **Portal:** https://www.ontario.ca/page/file-annual-return

**BC Annual Report:**
- **Deadline:** Dentro de 2 meses del aniversario
- **Costo:** $53.95
- **Información:** Directors, officers, registered office
- **Portal:** https://www.bcregistry.gov.bc.ca/

**Alberta Annual Return:**
- **Deadline:** Aniversario de incorporation
- **Costo:** $40
- **Portal:** https://www.alberta.ca/corporate-registry-annual-returns.aspx

**Penalidad por Late Filing:**
- $25-$100 late fee (depende de provincia)
- Eventual dissolution si 2+ años sin filing

---

### 3. Provincial Sales Tax (PST) - Non-HST Provinces

**British Columbia PST (7%):**
- **Registration:** Si revenue >$10,000/año
- **Filing:** Monthly (si >$120k revenue) o Quarterly
- **Portal:** https://www2.gov.bc.ca/gov/content/taxes/sales-taxes

**Saskatchewan PST (6%):**
- **Registration:** Obligatorio si vendes taxable goods/services
- **Filing:** Monthly, quarterly, o annual
- **Portal:** https://www.saskatchewan.ca/business/taxes-licensing-and-reporting/sales-tax

**Manitoba RST (Retail Sales Tax - 7%):**
- **Registration:** Obligatorio si vendes retail goods
- **Filing:** Monthly
- **Portal:** https://www.gov.mb.ca/finance/taxation/retail.html

**Quebec QST (Quebec Sales Tax - 9.975%):**
- **Registration:** Si revenue >$30,000
- **Filing:** Mensual, trimestral o anual (same as GST)
- **Portal:** https://www.revenuquebec.ca/
- **Note:** Quebec administra su propio QST (no CRA)

**Consulting Services:**
- **BC PST:** Generalmente exento
- **SK/MB/QC:** Consultar si servicios profesionales son taxable

---

## Obligaciones de Nómina (Payroll)

### 1. Payroll Deductions

**Canada Pension Plan (CPP) - 2026 Rates:**
- **Employee contribution:** 5.95% de pensionable earnings (hasta $68,500 max)
- **Employer contribution:** 5.95% (matching)
- **Max annual contribution:** $4,076 (employee) + $4,076 (employer) = **$8,152 total**
- **Exemption:** Primeros $3,500 de earnings son exempt

**Employment Insurance (EI) - 2026 Rates:**
- **Employee contribution:** 1.66% de insurable earnings (hasta $63,200 max)
- **Employer contribution:** 2.32% (1.4× employee rate)
- **Max annual contribution:** $1,049 (employee) + $1,468 (employer) = **$2,517 total**

**Income Tax Withholding:**
- **Federal tax:** Progressive rates (15% - 33%)
- **Provincial tax:** Varía por provincia (5% - 25.75%)
- **Calculation:** Use CRA Payroll Deductions Online Calculator - https://www.canada.ca/en/revenue-agency/services/e-services/e-services-businesses/payroll-deductions-online-calculator.html

**Ejemplo (Ontario, $60,000 salary):**
- **CPP:** $3,356 (employee) + $3,356 (employer)
- **EI:** $996 (employee) + $1,394 (employer)
- **Income tax:** ~$8,500 federal + ~$3,200 provincial (withheld from employee)
- **Employer total cost:** $60,000 + $3,356 + $1,394 = **$64,750**

---

### 2. T4 / T4A / T5 Slips

**T4 Slip (Statement of Remuneration Paid):**
- **Para quién:** Employees (salarios)
- **Información:** Total pay, CPP, EI, income tax withheld
- **Deadline:** Último día de febrero (año siguiente)
- **Filing:** CRA (online via Internet File Transfer)

**T4A Slip (Statement of Pension, Retirement, Annuity, and Other Income):**
- **Para quién:** Contractors, freelancers (si pagos >$500)
- **Información:** Fees paid, no withholdings (contractor responsable de sus taxes)
- **Deadline:** Último día de febrero

**T5 Slip (Statement of Investment Income):**
- **Para quién:** Shareholders (dividends)
- **Información:** Dividends paid (eligible vs. non-eligible)
- **Deadline:** Último día de febrero

**Penalidad por Late Filing:**
- $25 per slip (min $100, max $2,500)
- Ejemplo: 10 employees, late T4s = **$250 penalty**

**Cómo Filing:**
1. **Internet File Transfer:** https://www.canada.ca/en/revenue-agency/services/e-services/e-services-businesses/internet-file-transfer.html
2. **Payroll software:** QuickBooks Payroll, Wagepoint, Rise (automated)
3. **CPA/Payroll service:** For larger teams

---

### 3. Payroll Remittance Schedule

**Remittance Frequency:**
- **Quarterly Remitter:** Average monthly withholding <$3,000 en previous calendar year
  - Deadline: 15th del mes after quarter end
- **Monthly Remitter:** Average monthly withholding $3,000 - $25,000
  - Deadline: 15th del mes siguiente
- **Accelerated Remitter:** Average monthly withholding >$25,000
  - Deadline: Dos veces al mes (based on payment dates)

**Ejemplo (Monthly Remitter):**
- January payroll run (Jan 31): Remit CPP + EI + income tax by **Feb 15**

**Penalidad por Late Remittance:**
- 3% si 1-3 días tarde
- 5% si 4-5 días tarde
- 7% si 6-7 días tarde
- 10% si 8+ días tarde
- **Plus:** Daily compound interest

**Cómo Remit:**
1. **Online banking:** Add CRA as payee (usar RP account number del BN)
2. **CRA My Payment**
3. **Wire transfer**

---

## Obligaciones Bancarias

### 1. Business Bank Account

**¿Por qué obligatorio?**
- Separar finanzas personales del negocio (corporate veil protection)
- Professional invoicing y payments
- Required para filings limpios

**Cuándo abrir:**
✅ **Inmediatamente** después de obtener BN (antes de primer ingreso)

**Documentos Requeridos:**
- Business Number (BN) confirmation
- Articles of Incorporation (federal o provincial certificate)
- Directors' resolution (authorizing account opening)
- Government-issued ID del signing officer
- Proof of address

**Bancos Recomendados para Small Business:**

| Bank | Monthly Fee | Min Balance (to waive fee) | Pros |
|------|-------------|---------------------------|------|
| **RBC** | $15.95 | $5,000 | International services, good for USA-Canada |
| **TD** | $16.95 | $5,000 | Strong online banking, Visa Debit |
| **Scotiabank** | $14.95 | $4,000 | Good for LATAM connections |
| **BMO** | $17.50 | $5,000 | Business credit cards |
| **EQ Bank** | $0 | $0 | No fees, online-only |
| **Simplii** | $0 | $0 | No fees (owned by CIBC) |

**Recommended for Delaren Consulting:**
- **Primary:** RBC (strong international, USD accounts)
- **Secondary:** EQ Bank (fee-free for low-balance periods)

**Costo:**
- RBC/TD/Scotia: $15-$17/mes (waived con $5k balance)
- EQ/Simplii: $0/mes

**Documentación:**
- Guardar account opening docs en `legal/canada/bank_account_docs.pdf`

---

### 2. FINTRAC Reporting (Si Aplicable)

**FINTRAC (Financial Transactions and Reports Analysis Centre of Canada):**
- Anti-money laundering agency

**Large Cash Transaction Report:**
- Required si recibes >$10,000 CAD en cash en single transaction
- Banks auto-report, pero consultor unlikely to receive cash

**Suspicious Transaction Report:**
- Required si sospechas money laundering o terrorist financing
- Consultar con accountant si dudas

---

## Incorporación de Negocio

### 1. Federal Incorporation (Canada Business Corporations Act)

**¿Qué es?**
Incorporar bajo ley federal canadiense (Corporations Canada).

**Pros:**
- Operar en todas las provincias con un solo registration
- Name protection nacional
- Más prestige (perceived)

**Cons:**
- Más caro que provincial ($200 federal + $300-$500 extra-provincial por provincia)
- Extra-provincial registration needed en cada provincia donde operes

**Costo:**
- **Incorporation:** $200 online, $250 by mail
- **Name reservation (opcional):** $20
- **NUANS name search:** $20-$50 (pre-requisito)

**Cómo Incorporar:**
1. **Portal:** https://ised-isde.canada.ca/site/corporations-canada/en
2. **Online filing:** Corporations Canada Online Filing Centre
3. **Tiempo:** 1-3 días hábiles (online)

**Documentos Requeridos:**
- **Articles of Incorporation:** Define nombre, clase de acciones, restricciones
- **Initial Registered Office Address:** Dirección en Canadá
- **First Board of Directors:** Mínimo 25% residentes canadienses
- **NUANS Report:** Búsqueda de nombre corporativo (válido 90 días)

---

### 2. Provincial Incorporation

**Ontario (Business Corporations Act):**
- **Costo:** $300 online
- **Portal:** https://www.ontario.ca/page/business-corporations-act
- **Tiempo:** 1-2 días hábiles

**British Columbia (Business Corporations Act):**
- **Costo:** $350 online
- **Portal:** https://www.bcregistry.gov.bc.ca/
- **Tiempo:** 1-2 días

**Alberta (Business Corporations Act):**
- **Costo:** $275 online
- **Portal:** https://www.alberta.ca/business-corporations-act.aspx
- **Tiempo:** 1-3 días

---

### 3. Federal vs. Provincial: Decision Matrix

| Factor | Federal | Provincial |
|--------|---------|-----------|
| **Cost** | $200 + extra-prov registrations ($300-$500 each) | $275-$350 one-time |
| **Name protection** | All of Canada | One province only |
| **Operational scope** | All provinces | Primarily one province |
| **Annual returns** | Federal + cada provincia | One province |
| **Complexity** | Higher (multiple registrations) | Lower (single jurisdiction) |
| **Best for** | Multi-province operations, national brand | Single-province focus, lower cost |

**Recomendación para Delaren Consulting:**
- **Si clientes en múltiples provincias:** Federal incorporation
- **Si enfoque en 1-2 provincias:** Provincial (Ontario o BC)

---

## Checklist de Cumplimiento Anual

### Enero
- [ ] Remit December payroll deductions (Jan 15)
- [ ] Corporate tax instalment payment (Jan 31)

### Febrero
- [ ] Remit January payroll deductions (Feb 15)
- [ ] Corporate tax instalment payment (Feb 28)
- [ ] Issue T4/T4A/T5 slips (Feb 28)
- [ ] File T4/T4A/T5 Summary with CRA (Feb 28)

### Marzo
- [ ] Remit February payroll deductions (Mar 15)
- [ ] Corporate tax instalment payment (Mar 31)
- [ ] Pay annual tax balance (if Dec 31 year-end and CCPC) (Mar 31)

### Abril
- [ ] Remit March payroll deductions (Apr 15)
- [ ] Corporate tax instalment payment (Apr 30)
- [ ] File GST/HST Annual Return (if Dec 31 year-end and annual filer) (Apr 30)

### Mayo
- [ ] Remit April payroll deductions (May 15)
- [ ] Corporate tax instalment payment (May 31)

### Junio
- [ ] Remit May payroll deductions (Jun 15)
- [ ] File T2 Corporate Tax Return (if Dec 31 year-end) (Jun 30)
- [ ] Corporate tax instalment payment (Jun 30)

### Julio
- [ ] Remit June payroll deductions (Jul 15)
- [ ] Corporate tax instalment payment (Jul 31)

### Agosto
- [ ] Remit July payroll deductions (Aug 15)
- [ ] Corporate tax instalment payment (Aug 31)

### Septiembre
- [ ] Remit August payroll deductions (Sep 15)
- [ ] Corporate tax instalment payment (Sep 30)

### Octubre
- [ ] Remit September payroll deductions (Oct 15)
- [ ] Corporate tax instalment payment (Oct 31)

### Noviembre
- [ ] Remit October payroll deductions (Nov 15)
- [ ] Corporate tax instalment payment (Nov 30)

### Diciembre
- [ ] Remit November payroll deductions (Dec 15)
- [ ] Review year-end planning con CPA
- [ ] Deductible expenses antes del Dec 31 (si beneficia)
- [ ] Corporate tax instalment payment (Dec 31)
- [ ] Provincial annual return (si aniversario en diciembre)

---

## Costos Anuales de Compliance (Estimados 2026)

| Ítem | Frecuencia | Costo (CAD) |
|------|------------|-------------|
| **Federal Incorporation (one-time)** | One-time | $200 |
| **NUANS Name Search** | One-time | $20-$50 |
| **Extra-Provincial Registration (per province)** | One-time | $275-$350 |
| **T2 Corporate Tax Filing (CPA)** | Anual | $1,500-$3,000 |
| **GST/HST Filing (if annual)** | Anual | $0-$500 |
| **Provincial Annual Return** | Anual | $30-$100 |
| **Registered Office Service** | Anual | $100-$300 |
| **Accounting Software** (QuickBooks, Xero) | Mensual | $30-$100/mo = $360-$1,200/yr |
| **Bookkeeping Service (opcional)** | Mensual | $300-$800/mo = $3,600-$9,600/yr |
| **Payroll Processing (if employees)** | Mensual | $50-$150/mo = $600-$1,800/yr |
| **Business Bank Account** | Mensual | $0-$17/mo = $0-$204/yr |
| **Legal (contract review)** | As needed | $500-$2,000 |
| **TOTAL (Bootstrap - Sin empleados)** | **Anual** | **$3,200-$8,000** |
| **TOTAL (Con bookkeeping)** | **Anual** | **$7,000-$17,000** |

**Recomendación Año 1 (Bootstrap):**
- DIY bookkeeping con software → **$360-$1,200**
- CPA solo para T2 filing → **$1,500-$3,000**
- Federal incorporation → **$200**
- Extra-prov (Ontario) → **$330**
- Registered office → **$100**
- GST/HST filing (anual, self-file) → **$0**
- **Total Año 1:** **~$3,200-$5,000 CAD** (~$2,400-$3,750 USD)

**Año 2+ (Crecimiento):**
- Agregar bookkeeping service → **+$3,600-$9,600**
- **Total Año 2+:** **$7,000-$15,000 CAD**

---

## Recursos y Herramientas

### Canada Revenue Agency (CRA)
- **CRA Website:** https://www.canada.ca/en/revenue-agency.html
- **My Business Account:** https://www.canada.ca/en/revenue-agency/services/e-services/e-services-businesses/business-account.html
- **Business Number (BN) Registration:** https://www.canada.ca/en/services/taxes/business-number.html
- **T2 Corporation Income Tax:** https://www.canada.ca/en/revenue-agency/services/tax/businesses/topics/corporations/corporation-income-tax-return.html
- **GST/HST for Businesses:** https://www.canada.ca/en/revenue-agency/services/tax/businesses/topics/gst-hst-businesses.html
- **Payroll Deductions Calculator:** https://www.canada.ca/en/revenue-agency/services/e-services/e-services-businesses/payroll-deductions-online-calculator.html
- **Business Enquiries Phone:** 1-800-959-5525

### Corporations Canada
- **Incorporation Portal:** https://ised-isde.canada.ca/site/corporations-canada/en
- **Online Filing Centre:** https://ised-isde.canada.ca/site/corporations-canada/en/online-filing-centre
- **NUANS Name Search:** https://nuans.com/

### Provincial Portals
- **Ontario Business Registry:** https://www.ontario.ca/page/business-registry
- **BC Registry Services:** https://www.bcregistry.gov.bc.ca/
- **Alberta Corporate Registry:** https://www.alberta.ca/corporate-registry.aspx
- **Quebec Registraire des entreprises:** https://www.registreentreprises.gouv.qc.ca/

### Banking
- **RBC Business Banking:** https://www.rbcroyalbank.com/business/
- **TD Small Business Banking:** https://www.td.com/ca/en/small-business
- **Scotiabank Business Banking:** https://www.scotiabank.com/ca/en/small-business.html
- **EQ Bank Business:** https://www.eqbank.ca/business
- **Simplii Business:** https://www.simplii.com/en/business.html

### Accounting Software
- **QuickBooks Online:** $30-$90/mo - https://quickbooks.intuit.com/ca/
- **Xero:** $15-$78/mo - https://www.xero.com/ca/
- **Wave Accounting:** Free - https://www.waveapps.com/
- **FreshBooks:** $19-$60/mo - https://www.freshbooks.com/

### Payroll Software
- **Wagepoint:** $30-$60/mo - https://wagepoint.com/
- **Rise:** $29-$99/mo - https://www.hellorise.com/
- **QuickBooks Payroll:** Add-on to QuickBooks

### CPAs Especialistas (Cross-Border USA-Canada)
- Buscar "cross-border accountant Canada USA" en tu provincia
- Costo T2 filing: $1,500-$3,000 CAD
- Costo tax planning: $200-$400/hora

---

## Penalties y Consecuencias de No Compliance

| Violación | Penalidad |
|-----------|-----------|
| **Late T2 filing** | 5% del tax unpaid + 1% por mes (max 12 meses) |
| **Late GST/HST filing** | 1% del amount owing + 0.25% por mes + interest |
| **Late payroll remittance** | 3-10% penalty (escalates con delays) + interest |
| **Late T4/T5 slips** | $25 por slip (min $100, max $2,500) |
| **Late T1135 filing** | $25/día (min $100, max $2,500) |
| **Late tax payment** | Interest diario (CRA prescribed rate + 4%) |
| **No GST/HST registration (when required)** | Penalty + interest en uncollected GST/HST |
| **Gross negligence** | 50% del tax evaded (intencional) |

**Ejemplo (Late T2):**
- Tax owed: $20,000
- 4 meses de retraso
- Penalty: $1,000 (5%) + $800 (4 × 1%) = **$1,800**
- Plus: interest compounding daily

---

## Próximos Pasos (Action Items)

### Mes 1 (Enero 2026)

#### Si aún no has incorporado:
- [ ] Decidir federal vs. provincial incorporation
- [ ] NUANS name search
- [ ] Incorporar (Corporations Canada o provincial)
- [ ] Obtener BN (Business Number)
- [ ] Registrar para GST/HST (si revenue proyectado >$30k)
- [ ] Abrir business bank account (RBC o EQ Bank)

#### Si ya incorporaste:
- [ ] Verificar que BN ya obtenido
- [ ] Registrar extra-provincial (si federal y operando en provincias)
- [ ] Setup accounting software (QuickBooks o Wave)
- [ ] Contratar CPA para T2 filing (research 2-3 quotes)
- [ ] Calendar reminders para monthly instalments

### Mes 2 (Febrero 2026)
- [ ] File T4/T4A/T5 slips (si tuviste payroll en 2025)
- [ ] Review bookkeeping (P&L, balance sheet)
- [ ] Preparar documentos para T2 (if Dec 31, 2025 year-end → due Jun 30, 2026)

### Mes 3 (Marzo 2026)
- [ ] Pay corporate tax balance (if CCPC con Dec 31 year-end)
- [ ] GST/HST quarterly filing (if quarterly filer)
- [ ] Mid-quarter financial review

### Mes 4-6 (Abril-Junio 2026)
- [ ] File T2 return (Jun 30 if Dec 31, 2025 year-end)
- [ ] File GST/HST annual return (Apr 30 if Dec 31 year-end and annual filer)
- [ ] Review Q2 performance, adjust pricing si necesario

---

**Última Actualización:** 2 de enero, 2026
**Próxima Revisión:** 1 de abril, 2026 (Post tax season)
**Jurisdicción:** Canadá (Federal + Provincial)
**Disclaimer:** Este documento es informativo. Consulta con un CPA canadiense para advice específico a tu situación y provincia.
