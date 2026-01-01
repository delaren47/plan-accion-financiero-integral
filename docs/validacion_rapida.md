# Validación Rápida de Ofertas

**Metodología:** Test antes de construir. Vende antes de desarrollar.

---

## Filosofía de Validación

### Principio Core
**"No construyas nada que nadie haya pedido."**

En un plan de 90 días con recursos limitados, cada hora cuenta. La validación rápida nos permite:
1. **Reducir riesgo:** Probar demand antes de invertir tiempo/dinero
2. **Iterar rápido:** Ajustar oferta basado en feedback real
3. **Generar traction:** Primeros clientes son mejores validadores que encuestas
4. **Conservar recursos:** No desarrollar features que nadie pagará

### Mentalidad
- **Bias hacia acción:** Validar en días, no semanas
- **Low-fidelity primero:** MVP, no producto pulido
- **Customer discovery > Product development**
- **Sell the outcome, not the feature**

---

## Framework de Validación (4 Fases)

```
Fase 1: Research Rápido (4-8 horas)
         ↓
Fase 2: Smoke Test (24-48 horas)
         ↓
Fase 3: Pre-Venta / Piloto (3-7 días)
         ↓
Fase 4: Build to Order (post-validación)
```

---

## Fase 1: Research Rápido (4-8 horas)

### Objetivo
Validar que el problema existe y hay willingness to pay.

### Actividades

#### 1.1 Desk Research (2 horas)
- [ ] Google Trends: ¿La keyword tiene volumen de búsqueda?
- [ ] Reddit/Forums: ¿La gente se queja de este problema?
- [ ] Competitor analysis: ¿Ya existen soluciones? ¿A qué precio?
- [ ] LinkedIn: ¿Hay demanda de este skill?

**Ejemplo:**
```
Oferta: Chatbot AI para restaurantes
Google Trends: "chatbot para restaurantes" - Interés creciente
Reddit r/restaurateurs: 15 threads en últimos 3 meses quejándose de atención telefónica
Competitors: Slang.ai ($299/mes), Popmenu ($199/mes)
LinkedIn Jobs: 40 job postings "restaurant automation" en LATAM
Conclusión: ✅ Problema validado, mercado existente, pricing range conocido
```

---

#### 1.2 Quick Surveys (2 horas)
- [ ] Encuesta de 5 preguntas a 20 contactos target
- [ ] Focus: Pain points, budget, willingness to pay
- [ ] Tool: Google Forms, TypeForm, o directo por WhatsApp

**Template de Encuesta:**
```
1. ¿Cuál es tu mayor frustración con [ÁREA]? (open-ended)
2. ¿Cuánto tiempo/dinero pierdes por este problema al mes? (estimación)
3. Si existiera una solución que [OUTCOME], ¿la usarías? (Sí/No/Tal vez)
4. ¿Cuánto pagarías por esa solución? (rango múltiple choice)
5. ¿Estarías dispuesto a un piloto de 30 días? (Sí/No)
```

**Criterio de Validación:**
- >60% responde "Sí" a pregunta 3
- >40% selecciona budget alineado con tu pricing
- >3 personas dicen "Sí" a piloto

---

#### 1.3 Competitor Teardown (2 horas)
- [ ] Identificar top 3 competidores
- [ ] Analizar pricing, features, reviews
- [ ] Identificar gaps en su oferta
- [ ] Definir tu diferenciador (speed, price, niche, quality)

**Ejemplo:**
```
Competitor 1: Slang.ai - $299/mes, enterprise focus, slow setup (14 días)
Competitor 2: Popmenu - $199/mes, feature-heavy, complejo
Gap identificado: No hay opción <$200 con setup rápido (<48h)
Tu diferenciador: $150/mes, setup en 48h, enfoque en PyMEs
```

---

#### 1.4 Pricing Hypothesis (1 hora)
- [ ] Definir 3 tiers de pricing (Low/Mid/High)
- [ ] Calcular margin mínimo viable
- [ ] Anchoring: Mostrar tier alto primero

**Template:**
```
Tier 1 (Básico):   $[X] - Profit margin >60%
Tier 2 (Standard): $[Y] - Profit margin >70% (recommended)
Tier 3 (Premium):  $[Z] - Profit margin >80%
```

---

### Deliverable Fase 1
**One-pager:** "Validation Brief"
- Problema identificado
- Evidencia de demand (surveys, competitor analysis)
- Pricing hypothesis
- Go/No-Go recommendation

**Criterio Go:**
- ✅ >5 pain points mencionados en research
- ✅ >3 competitors activos (señal de mercado)
- ✅ >40% survey respondents willing to pay en rango objetivo

**Criterio No-Go:**
- ❌ Mercado inexistente o saturado sin diferenciador claro
- ❌ Willingness to pay <50% del costo de entrega
- ❌ Problema "nice to have" no "must have"

---

## Fase 2: Smoke Test (24-48 horas)

### Objetivo
Validar demand real con landing page + CTA antes de construir producto.

### Actividades

#### 2.1 Landing Page Rápida (4 horas)
**Tool:** Carrd.co, Unicorn Platform, o HTML simple

**Estructura de Landing:**
```
HERO:
- Headline: [Outcome específico en <72h]
- Subheadline: [Para quién, qué problema resuelve]
- CTA: "Reserva tu Spot" o "Pre-Ordena Ahora"

PROBLEMA:
- 3 pain points visuales (icons + texto corto)

SOLUCIÓN:
- "Cómo funciona" (3 steps máximo)
- Deliverables incluidos (bullet points)

PRUEBA SOCIAL:
- Testimonials (si tienes) o "Trusted by [industry]"

PRICING:
- 3 tiers con pricing visible
- CTA en cada tier

FAQ:
- 5 preguntas más comunes

FOOTER:
- Email de contacto
```

**Ejemplo Real:**
```
Headline: "Chatbot AI para tu Restaurante en 48 Horas"
Subheadline: "Automatiza reservas y responde FAQs 24/7. Sin código, sin complicaciones."
CTA: "Reserva tu Setup → $150 (50% off primeros 10 clientes)"
```

---

#### 2.2 Traffic al Landing (24 horas)
**Budget:** $50-$100 USD
**Channels:**
- Facebook/Instagram Ads (target: dueños de restaurantes en tu ciudad)
- LinkedIn Ads (target: job title "Restaurant Owner")
- Email directo a tu red (50 contactos)
- Post en grupos de Facebook/LinkedIn relevantes

**Métrica de Éxito:**
- >100 visitors
- >5% CTR en CTA
- >3 form submissions o pre-orders

---

#### 2.3 Análisis de Resultados (2 horas)
**Trackear:**
- Visitors (Google Analytics)
- Bounce rate (target: <70%)
- Time on page (target: >30 segundos)
- CTA clicks (target: >5%)
- Form submissions (target: >3)

**Herramientas:**
- Google Analytics
- Hotjar (heatmaps, recordings)
- Facebook Pixel

---

### Deliverable Fase 2
**Smoke Test Report:**
- Traffic stats (visitors, bounce, time on page)
- Conversion rate (CTA clicks / visitors)
- Leads generados (form submissions)
- Feedback cualitativo (si hubo conversaciones)
- Go/No-Go para Fase 3

**Criterio Go:**
- ✅ >3 leads genuinos (no amigos/familia)
- ✅ CTR >5% en CTA principal
- ✅ Bounce rate <70%

**Criterio No-Go:**
- ❌ 0 leads después de 100 visitors
- ❌ Bounce rate >85%
- ❌ Feedback negativo sobre pricing (demasiado caro)

---

## Fase 3: Pre-Venta / Piloto (3-7 días)

### Objetivo
Cerrar 3-5 clientes pilotos que paguen (aunque sea 50% descuento) ANTES de construir producto completo.

### Actividades

#### 3.1 Outreach a Leads del Smoke Test (1 día)
- [ ] Follow-up email a todos los form submissions
- [ ] Call a los 3 leads más calificados
- [ ] Pitch: "Piloto de 30 días a 50% descuento"

**Email Template:**
```
Subject: Re: [Nombre Empresa] - Piloto Chatbot AI

Hola [Nombre],

Gracias por tu interés en [Producto]. Estamos abriendo 5 spots para un piloto de 30 días.

Qué incluye:
- Setup completo en 48h
- [Lista de deliverables]
- Soporte dedicado durante 30 días

Inversión: $75 (50% off - solo primeros 5 clientes)

¿Te interesa? Responde este email y agendamos 15 min para detalles.

Saludos,
[Tu nombre]
```

---

#### 3.2 Pre-Venta Pitch Call (2-3 días)
**Estructura de Call (15 min):**
1. **Intro (2 min):** Quién eres, por qué creaste esto
2. **Discovery (5 min):** Sus pain points específicos, impacto en negocio
3. **Demo/Mockup (5 min):** Wireframe o mockup de cómo funcionaría para ellos
4. **Close (3 min):** Pricing, términos, CTA

**Cierre de Piloto:**
- "Tengo 5 spots para piloto. Precio: $75 (50% off). Pago hoy, delivery en 5 días."
- "Si funciona bien, price normal es $150/mes. Si no, refund completo."

**Criterio de Éxito:**
- Cerrar 3/5 pilotos
- Cobrar al menos 50% upfront

---

#### 3.3 Entregar Piloto (MVP) (7 días max)
**Scope del MVP:**
- Core feature solamente (no bells and whistles)
- Manual > Automation (si acelera delivery)
- Template > Custom (personalización mínima)

**Ejemplo - Chatbot AI Piloto:**
- ✅ Chatbot funcional con 10 FAQs
- ✅ Integración WhatsApp o web widget
- ❌ Integración con CRM (manual por ahora)
- ❌ Multi-idioma (solo español)
- ❌ Analytics avanzado (Google Analytics básico)

**Quality Bar:**
- Debe resolver el problema core
- UI/UX aceptable (no perfecta)
- Sin bugs críticos

---

#### 3.4 Feedback Loop (Durante Piloto)
- [ ] Check-in semanal con cada cliente piloto
- [ ] Documentar: qué funciona, qué no, feature requests
- [ ] Ajustar MVP basado en feedback (si es rápido)

**Template Check-in:**
```
Semana 1: "¿El chatbot está respondiendo bien? ¿Algún problema?"
Semana 2: "¿Has notado reducción en llamadas? ¿Qué mejorarías?"
Semana 3: "En escala 1-10, ¿qué tan probable es que continues después del piloto?"
```

---

### Deliverable Fase 3
**Pilot Results Report:**
- Número de pilotos cerrados y entregados
- Revenue generado ($)
- Feedback consolidado (quotes de clientes)
- Conversion rate (piloto → cliente pagando full price)
- Feature requests prioritizados
- Pricing refinado basado en feedback

**Criterio Go (Build Full Product):**
- ✅ >3 pilotos entregados
- ✅ >70% de pilotos quieren continuar a full price
- ✅ NPS >7 promedio
- ✅ ROI claro para el cliente (time/money saved)

**Criterio Pivot:**
- 🔄 <50% quieren continuar → Ajustar pricing o value prop
- 🔄 Feature requests consistentes → Agregar feature antes de escalar

**Criterio No-Go:**
- ❌ 0 pilotos cerrados después de 15 calls
- ❌ Pilotos cancelan antes de terminar 30 días
- ❌ Feedback: "Es nice to have, pero no critical"

---

## Fase 4: Build to Order (Post-Validación)

### Objetivo
Escalar oferta validada con confianza, construyendo solo lo que clientes pagan.

### Actividades

#### 4.1 Productizar MVP
- [ ] Templates reutilizables en `/templates/`
- [ ] Documentación de proceso de entrega
- [ ] Pricing final basado en pilots
- [ ] Sales collateral (one-pager, case study de piloto)

---

#### 4.2 Marketing Launch
- [ ] Landing page refinada con testimonials de pilotos
- [ ] Case study (PDF de 2 páginas con resultados)
- [ ] LinkedIn/Facebook organic posts
- [ ] Cold email campaign a 100 prospectos

---

#### 4.3 Scale Operations
- [ ] Onboarding checklist estandarizado
- [ ] Delivery en <72h consistentemente
- [ ] Conversion a retainer (upsell después de fast win)

---

## Checklist de Validación por Producto

### Fast Cash Win: Auditoría de Accesibilidad
- [ ] **Research:** ¿Empresas en LATAM tienen obligación legal de accesibilidad? (compliance driver)
- [ ] **Smoke Test:** Landing "Evita multas por accesibilidad - Auditoría en 48h"
- [ ] **Piloto:** 3 sitios auditados, entrega reporte + plan de remediación
- [ ] **Validación:** >2/3 contratan servicio de implementación después

---

### Retainer: Gestión de Email Marketing
- [ ] **Research:** ¿PyMEs latinas usan email marketing? ¿Cuánto pagan?
- [ ] **Smoke Test:** Landing "4 campañas al mes + analytics por $800"
- [ ] **Piloto:** 2 clientes, entregar 2 campañas en primer mes
- [ ] **Validación:** >1/2 renuevan después de mes 1

---

### White-Label: Knotie-AI Voice Agent
- [ ] **Research:** ¿Restaurantes/clínicas pierden clientes por no contestar teléfono?
- [ ] **Smoke Test:** Landing "Voice AI que contesta 24/7 por $3,500"
- [ ] **Piloto:** 1 restaurante, setup básico en 7 días
- [ ] **Validación:** Cliente reporta >20 llamadas automatizadas en primer mes

---

## Métricas de Validación (Dashboard)

| Fase | Métrica Clave | Target | Fuente |
|------|---------------|--------|--------|
| **Fase 1: Research** | Competitor count | >3 activos | Manual research |
| **Fase 1: Research** | Survey "Sí pagaría" | >40% | Google Forms |
| **Fase 2: Smoke Test** | Landing visitors | >100 | Google Analytics |
| **Fase 2: Smoke Test** | CTA conversion | >5% | Analytics |
| **Fase 2: Smoke Test** | Leads generados | >3 | Form submissions |
| **Fase 3: Piloto** | Pilotos cerrados | >3 | CRM |
| **Fase 3: Piloto** | Piloto→Full conversion | >70% | Follow-up calls |
| **Fase 3: Piloto** | NPS | >7 | Survey |

---

## Templates de Validación

### Template: Validation Brief (Fase 1)
```markdown
# Validation Brief: [Nombre de Oferta]

**Fecha:** [DD/MM/YYYY]
**Owner:** Alfred

## Problema Identificado
[Descripción 2-3 frases]

## Evidencia de Demand
- Google Trends: [link + screenshot]
- Reddit/Forums: [X threads encontrados, links]
- Survey Results: [X/Y respondieron "Sí pagaría"]

## Competitor Analysis
| Competitor | Pricing | Gap Identificado |
|------------|---------|------------------|
| [Nombre 1] | $X/mes  | [Gap]            |
| [Nombre 2] | $Y/mes  | [Gap]            |

## Pricing Hypothesis
- Básico: $[X] (margin: [Y]%)
- Standard: $[X] (margin: [Y]%) ← Recomendado
- Premium: $[X] (margin: [Y]%)

## Recomendación
[✅ GO | ❌ NO-GO | 🔄 PIVOT]

**Razón:** [1-2 frases]

**Próximo Paso:** [Si GO: "Proceder a Fase 2 - Smoke Test"]
```

---

### Template: Smoke Test Report (Fase 2)
```markdown
# Smoke Test Report: [Nombre de Oferta]

**Fecha:** [DD/MM/YYYY]
**Duración:** [X horas de tráfico]
**Budget:** $[X] USD

## Traffic Stats
- Visitors: [X]
- Bounce Rate: [X]%
- Avg Time on Page: [X]s
- Traffic Sources: [FB: X%, LinkedIn: Y%, Email: Z%]

## Conversion Metrics
- CTA Clicks: [X] ([Y]% conversion)
- Form Submissions: [X]
- Qualified Leads: [X]

## Qualitative Feedback
- [Quote 1 de interesado]
- [Quote 2 de interesado]

## Cost per Lead
- Total Spend: $[X]
- Leads: [Y]
- CPL: $[X/Y]

## Recomendación
[✅ GO | ❌ NO-GO | 🔄 PIVOT]

**Razón:** [1-2 frases]

**Próximo Paso:** [Si GO: "Proceder a Fase 3 - Piloto con 5 clientes"]
```

---

### Template: Pilot Results Report (Fase 3)
```markdown
# Pilot Results Report: [Nombre de Oferta]

**Fecha:** [DD/MM/YYYY]
**Pilotos:** [X cerrados, Y entregados]

## Financials
- Revenue Generado: $[X]
- Avg Deal Size: $[X/Y]
- Conversion Pilot→Full: [X/Y] = [Z]%

## Client Feedback
| Cliente | NPS | Quote | Continue? |
|---------|-----|-------|-----------|
| [Nombre 1] | [X/10] | "[Quote]" | ✅ Sí |
| [Nombre 2] | [X/10] | "[Quote]" | ❌ No |

## Feature Requests (Top 3)
1. [Feature 1] - [X/Y clientes pidieron]
2. [Feature 2] - [X/Y clientes pidieron]
3. [Feature 3] - [X/Y clientes pidieron]

## ROI Reportado por Clientes
- [Cliente 1]: Ahorró [X horas/semana] = $[Y]/mes
- [Cliente 2]: Generó [X leads adicionales] = $[Y] revenue

## Pricing Refinement
- Precio Piloto: $[X]
- Precio Full Propuesto: $[Y]
- Justificación: [Basado en ROI cliente]

## Recomendación
[✅ GO FULL PRODUCT | 🔄 PIVOT | ❌ KILL]

**Razón:** [1-2 frases]

**Próximo Paso:** [Si GO: "Productizar MVP, crear templates, launch marketing"]
```

---

## Errores Comunes a Evitar

### ❌ Error 1: Construir sin validar
**Síntoma:** "Tengo una idea genial, voy a construirla y luego busco clientes"
**Riesgo:** Semanas invertidas en producto que nadie quiere
**Fix:** Smoke test ANTES de escribir código

### ❌ Error 2: Confundir interés con commitment
**Síntoma:** "10 personas dijeron que les interesa" (pero nadie pagó)
**Riesgo:** Falsa validación, demand no real
**Fix:** Cobrar al menos 50% upfront en piloto

### ❌ Error 3: Pilotos gratis o muy baratos
**Síntoma:** "Voy a regalar pilotos para ganar traction"
**Riesgo:** Clientes no comprometidos, feedback sesgado
**Fix:** Mínimo 50% del precio final para pilotos

### ❌ Error 4: Scope creep en MVP
**Síntoma:** "Voy a agregar X, Y, Z features antes de lanzar"
**Riesgo:** Never-ending development, delay en revenue
**Fix:** MVP = Minimum. Solo core feature.

### ❌ Error 5: Ignorar feedback negativo
**Síntoma:** "Este cliente no entendió el producto" (después de 3 quejas similares)
**Riesgo:** Product-market fit inexistente
**Fix:** Si >2 clientes dicen lo mismo, probablemente tienen razón

---

## Casos de Uso: Validación en 48 Horas

### Caso 1: Chatbot AI para Restaurantes
**Lunes AM:** Desk research (2h) → 5 competitors, pricing $200-$400/mes
**Lunes PM:** Survey a 20 dueños de restaurantes (2h) → 12/20 dicen "Sí pagaría"
**Martes AM:** Landing en Carrd (4h) → "Chatbot AI en 48h por $150"
**Martes PM:** $50 en Facebook Ads → 80 visitors, 5 form submissions
**Miércoles:** Follow-up calls → 2/5 cierran piloto a $75
**Resultado:** ✅ Validado. Construir MVP para entregar Viernes.

---

### Caso 2: Dashboard de KPIs (Fracaso Productivo)
**Lunes:** Research + Survey → Solo 3/20 dicen "pagaría", pricing target $50/mes
**Martes:** Landing + $30 FB Ads → 60 visitors, 0 form submissions
**Miércoles:** Análisis → Bounce rate 92%, avg time 8 segundos
**Resultado:** ❌ No validado. KILL. Pivotear a otra oferta. Ahorro: 2 semanas de development.

---

## Próximos Pasos

**Para Usar Este Framework:**
1. [ ] Seleccionar 1 oferta para validar (de `ofertas_y_precios.md`)
2. [ ] Completar Fase 1 en 1 día
3. [ ] Si GO → Fase 2 en 2 días
4. [ ] Si GO → Fase 3 en 1 semana
5. [ ] Si GO → Build to Order y scale

**Validar en Enero (Primeras 2 Semanas):**
- Semana 1: Fast Cash Win #1 (Auditoría Accesibilidad)
- Semana 2: Retainer #1 (Email Marketing) o White-Label (Knotie básico)

---

**Última Actualización:** 31 de diciembre, 2025
**Próxima Revisión:** 7 de enero, 2026
**Owner:** Alfred (Delaren Consulting LLC)
