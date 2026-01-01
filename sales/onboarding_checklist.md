# Checklist de Onboarding de Clientes

**Delaren Consulting LLC**
**Objetivo:** Onboarding fluido que maximiza satisfacción del cliente y minimiza fricción.

---

## Filosofía de Onboarding

**Principios:**
1. **Speed to value:** Cliente ve progreso en <24h desde firma
2. **Clear communication:** Expectativas claras en cada etapa
3. **Proactive updates:** No esperar a que el cliente pregunte
4. **Upsell sutil:** Identificar oportunidades de retainer sin ser pushy

**Timeframes:**
- **Fast Cash Wins:** Kickoff en <24h, entrega en 48-72h
- **Retainers:** Kickoff en <48h, primer deliverable en semana 1
- **White-Label:** Kickoff en <72h, MVP en 7-14 días

---

## Fase 1: Post-Firma (0-24 horas)

### ✅ Tareas Inmediatas

#### 1.1 Confirmar Pago (Within 2 hours)
- [ ] Verificar que pago de 50% upfront fue recibido
- [ ] Si no recibido: Enviar invoice reminder con link de pago
- [ ] Registrar pago en `finance/ar_tracking.csv`
- [ ] Update CRM status a "Cliente Activo"

**Si pago no recibido en 24h:**
- Pausar inicio de trabajo
- Call al cliente para resolver
- Política: No se inicia trabajo sin 50% upfront

---

#### 1.2 Welcome Email (Within 4 hours de firma)

**Template:**
```
Subject: 🎉 ¡Bienvenido a Delaren Consulting! - Próximos Pasos

Hola [Nombre],

¡Gracias por confiar en nosotros para [proyecto]!

Confirmación de proyecto:
━━━━━━━━━━━━━━━━━━━━━━━━━━━
Servicio: [Fast Cash Win / Retainer / White-Label]
Scope: [Breve descripción]
Timeline: [Kickoff fecha] → [Delivery fecha]
Inversión: $[Total] (50% pagado, 50% on delivery)

Próximos pasos inmediatos:
━━━━━━━━━━━━━━━━━━━━━━━━━━━
1. ✅ Pago de 50% recibido (Gracias!)
2. 📅 Kickoff call agendado: [Fecha/Hora] → [Zoom link]
3. 📋 Pre-work: Por favor completa este form antes del kickoff → [Google Form link]

Qué esperar en el kickoff:
━━━━━━━━━━━━━━━━━━━━━━━━━━━
- Confirmar scope y deliverables (15 min)
- Obtener accesos/información necesaria (10 min)
- Alinear expectativas y timeline (5 min)
Duración total: 30 min

¿Preguntas antes del kickoff?
Responde este email o llámame: [Teléfono]

¡Nos vemos pronto!

Alfred
Delaren Consulting LLC
alfred@delaren.com
```

---

#### 1.3 Agendar Kickoff Call (Same day)
- [ ] Enviar Calendly link o proponer 3 time slots
- [ ] Confirmar zona horaria del cliente
- [ ] Crear Zoom meeting con recording activado
- [ ] Agregar a Google Calendar con reminder 1h antes
- [ ] Enviar calendar invite con agenda adjunta

**Agenda del Kickoff (adjuntar al invite):**
```
AGENDA - Kickoff Call [Nombre Cliente]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Duración: 30 minutos
Fecha: [DD/MM/YYYY] a las [HH:MM]

1. Intro y bienvenida (5 min)
   - Presentaciones del equipo
   - Overview del proyecto

2. Scope confirmation (10 min)
   - Deliverables específicos
   - Timeline y milestones
   - Success criteria

3. Info gathering (10 min)
   - Accesos necesarios
   - Brand assets (si aplica)
   - Contactos clave

4. Q&A y próximos pasos (5 min)
   - Clarificaciones
   - Communication plan
```

---

#### 1.4 Enviar Pre-Work Form (Same day)

**Google Form con campos:**
1. Información de la empresa
   - Nombre legal
   - Website URL
   - Industria/sector
   - Tamaño (# empleados)

2. Contactos clave
   - Punto de contacto principal (nombre, email, teléfono)
   - Decision maker (si es diferente)
   - Contacto técnico (si aplica)

3. Project-specific questions (varía según servicio)
   - **Para Accesibilidad:** URLs de 10 páginas clave
   - **Para Email Marketing:** Plataforma actual, tamaño de lista
   - **Para Chatbot:** FAQs más comunes, tone of voice preferido

4. Brand assets
   - Logo (upload)
   - Colores de marca (hex codes)
   - Fonts (si es custom)

5. Communication preferences
   - Mejor horario para updates
   - Canal preferido (email, WhatsApp, Slack)
   - Frecuencia de updates (diario, 2x semana, semanal)

---

#### 1.5 Crear GitHub Issue (Same day)
- [ ] Crear issue en GitHub Project con label apropiado
- [ ] Template: Fast Cash Win / Retainer Conversion
- [ ] Asignar a Alfred o Hermano
- [ ] Move a columna "Esta semana"
- [ ] Agregar deadline en title o description

**Issue Title Format:**
```
[CLIENTE] - [TIPO] - [SERVICIO] - Due [FECHA]
Ej: "Restaurante La Cocina - Fast Win - Chatbot AI - Due 3/enero"
```

---

## Fase 2: Kickoff Call (24-72 horas post-firma)

### ✅ Durante la Llamada

#### 2.1 Opening (5 min)
- [ ] Gracias por elegir Delaren Consulting
- [ ] Intro del equipo (Alfred + Hermano si co-selling)
- [ ] Confirmar que recibieron welcome email y completaron pre-work
- [ ] Explicar agenda y duración (30 min)

---

#### 2.2 Scope Confirmation (10 min)
- [ ] Revisar deliverables específicos (leer 1 por 1)
- [ ] Confirmar timeline:
  - Start date: [Hoy o mañana]
  - Delivery date: [48-72h para fast win, o milestone para retainer]
  - Q&A session: [Post-delivery]
- [ ] Definir success criteria:
  - "Este proyecto es exitoso si..."
  - Métricas específicas (si aplican)

**Red flags to watch:**
- Cliente agrega scope no incluido → "Eso sería un add-on por $X adicional"
- Cliente unclear on deliverables → Re-explicar, enviar por escrito post-call
- Timeline unrealistic → Negociar o rechazar

---

#### 2.3 Info Gathering (10 min)

**Accesos necesarios (por tipo de servicio):**

| Servicio | Accesos Requeridos |
|----------|-------------------|
| **Auditoría Web** | URL del sitio (público, no login) |
| **Email Marketing** | Mailchimp/Brevo admin access, CSV de contactos |
| **Chatbot AI** | Acceso al sitio web (FTP o CMS), lista de FAQs |
| **WhatsApp Automation** | WhatsApp Business API access, base de datos de contactos |
| **Dashboard KPIs** | Read access a Google Analytics, CRM export |

**Documentar en call notes:**
- [ ] Username/passwords (guardar en password manager)
- [ ] Links a plataformas
- [ ] Contacto técnico si hay issues de acceso

**Brand Assets:**
- [ ] Confirmar que subieron logo y colores en pre-work form
- [ ] Si no: Pedir que lo envíen por email en <24h

---

#### 2.4 Communication Plan (3 min)
- [ ] Explicar cómo haremos updates:
  - **Fast Cash Wins:** Update a mid-point (24-36h), entrega final
  - **Retainers:** Weekly update email los viernes
  - **White-Label:** Updates cada 3-4 días + milestone demos

- [ ] Confirmar canal preferido:
  - Email (default)
  - WhatsApp (si es urgente)
  - Slack (si tienen workspace)

- [ ] Expectativa de respuesta:
  - "Responderé en <24h hábiles"
  - "Urgencias: WhatsApp directo"

---

#### 2.5 Q&A y Cierre (2 min)
- [ ] "¿Alguna pregunta antes de que comencemos?"
- [ ] Recap de próximos pasos:
  1. Yo empiezo trabajo hoy/mañana
  2. Update en [X días]
  3. Delivery en [Fecha específica]
  4. Q&A session post-delivery

- [ ] "Gracias por tu tiempo. ¡Manos a la obra!"

---

### ✅ Post-Kickoff (Within 2 hours)

#### 2.6 Enviar Call Summary Email
```
Subject: 📝 Resumen - Kickoff Call [Nombre Cliente]

Hola [Nombre],

Gracias por la excelente kickoff call. Aquí el resumen:

Scope confirmado:
━━━━━━━━━━━━━━━━━━
- [Deliverable 1]
- [Deliverable 2]
- [Deliverable 3]

Timeline:
━━━━━━━━━━━━━━━━━━
- Start: [Hoy]
- Update: [Fecha mid-point]
- Delivery: [Fecha final]

Accesos recibidos:
━━━━━━━━━━━━━━━━━━
✅ [Acceso 1]
✅ [Acceso 2]
⏳ [Pendiente: X - por favor enviar antes del [fecha]]

Próximo contacto:
━━━━━━━━━━━━━━━━━━
Te enviaré update el [Fecha] con progreso.

¿Alguna corrección o adición?

¡A trabajar!

Alfred
```

#### 2.7 Update Project Management
- [ ] Move GitHub issue a "En curso"
- [ ] Update CRM notes con key info del kickoff
- [ ] Set calendar reminders para mid-point update y delivery
- [ ] Si hay accesos pendientes: Follow-up task en 24h

---

## Fase 3: Durante la Ejecución (Días 1-3 para Fast Win)

### ✅ Comunicación Proactiva

#### 3.1 Mid-Point Update (24-36h en fast win, weekly en retainer)
- [ ] Enviar progreso update sin que el cliente pregunte
- [ ] Mostrar preview o screenshot si es posible
- [ ] Confirmar que vamos on track para deadline

**Email Template:**
```
Subject: 🚀 Progreso Update - [Proyecto]

Hola [Nombre],

Quick update de donde estamos:

Completado hasta ahora:
━━━━━━━━━━━━━━━━━━━━━━━━
✅ [Task 1]
✅ [Task 2]
🔄 [Task 3 - en progreso]

Preview:
━━━━━━━━━━━━━━━━━━━━━━━━
[Screenshot o brief description de lo que llevas]

Timeline:
━━━━━━━━━━━━━━━━━━━━━━━━
✅ On track para delivery el [Fecha]

¿Preguntas o feedback?

Alfred
```

---

#### 3.2 Manejo de Blockers
**Si encuentras un blocker:**
1. **Identifica ASAP** (no esperes 24h)
2. **Email/WhatsApp al cliente** explicando:
   - Qué blocker
   - Impacto en timeline (cuántos días de delay)
   - Qué necesitas del cliente para desblocar
3. **Propón alternativa** si es posible
4. **Update GitHub issue** con label "Bloqueado"

**Email Template:**
```
Subject: ⚠️ Blocker - Acción Requerida [Proyecto]

Hola [Nombre],

He encontrado un blocker que necesita tu ayuda:

Blocker:
━━━━━━━━━━━━━━━━━━
[Descripción del problema]

Impacto:
━━━━━━━━━━━━━━━━━━
Esto nos retrasa [X días] del deadline original.

Necesito de ti:
━━━━━━━━━━━━━━━━━━
[Acción específica que el cliente debe hacer]

Timeline ajustado:
━━━━━━━━━━━━━━━━━━
Si recibo [X] antes del [Fecha], puedo entregar el [Nueva fecha].

Alternativa:
━━━━━━━━━━━━━━━━━━
[Si hay workaround, explicar]

¿Podemos resolver esto hoy?

Alfred
```

---

## Fase 4: Pre-Delivery (24h antes de entrega)

### ✅ Quality Check

#### 4.1 Internal Review
- [ ] Revisar todos los deliverables contra checklist original
- [ ] Spell check y grammar check (especialmente en PDFs)
- [ ] Screenshots legibles y profesionales
- [ ] Todos los links funcionan
- [ ] Branding del cliente aplicado (logo, colores)
- [ ] No hay placeholder text tipo "Lorem ipsum" o "[INSERT HERE]"

#### 4.2 Test Run (si aplica)
- [ ] **Chatbot:** Probar 10 conversaciones diferentes
- [ ] **Email:** Enviar test email a ti mismo
- [ ] **Dashboard:** Verificar que data loads correctamente
- [ ] **Automation:** Run 3 test scenarios

#### 4.3 Package Deliverables
- [ ] Todos los archivos en 1 folder ZIP o Google Drive folder
- [ ] Naming convention: `[Cliente]_[Servicio]_[Fecha]`
- [ ] README.txt explicando qué contiene cada archivo
- [ ] Credentials file (si aplica) con passwords generados

---

## Fase 5: Delivery (Día de Entrega)

### ✅ Envío de Deliverables

#### 5.1 Delivery Email
```
Subject: ✅ Entrega Completa - [Proyecto] - [Nombre Cliente]

Hola [Nombre],

¡Tu [servicio] está listo! 🎉

Deliverables incluidos:
━━━━━━━━━━━━━━━━━━━━━━━━
📄 [Deliverable 1] → [Link o attachment]
📄 [Deliverable 2] → [Link o attachment]
📄 [Deliverable 3] → [Link o attachment]

Cómo acceder:
━━━━━━━━━━━━━━━━━━━━━━━━
[Instrucciones paso a paso si es técnico]

Próximos pasos:
━━━━━━━━━━━━━━━━━━━━━━━━
1. Revisa los deliverables
2. Agenda nuestra Q&A session (30 min) → [Calendly link]
3. Invoice de 50% final → [Adjunto o link]

Recordatorio de pago:
━━━━━━━━━━━━━━━━━━━━━━━━
50% restante: $[X] USD
Due: Al recibir entrega (hoy)
Métodos: Zelle / Wise / Stripe

¿Preguntas antes del Q&A?

¡Espero que te encante el resultado!

Alfred
Delaren Consulting LLC
```

#### 5.2 Enviar Invoice Final (Same time)
- [ ] Generar invoice de 50% restante
- [ ] Adjuntar a delivery email o enviar separado
- [ ] Incluir payment instructions claras
- [ ] Set reminder para follow-up en 7 días si no pagan

---

#### 5.3 Agendar Q&A Session
- [ ] Enviar Calendly link en delivery email
- [ ] Target: Q&A en next 2-5 días
- [ ] Duración: 30 min
- [ ] Agenda:
  - Walkthrough de deliverables (15 min)
  - Preguntas del cliente (10 min)
  - Next steps / upsell (5 min)

---

## Fase 6: Post-Delivery (1-7 días después)

### ✅ Q&A Session

#### 6.1 Durante el Q&A
- [ ] Screen share y walkthrough de cada deliverable
- [ ] Explicar cómo usar/implementar
- [ ] Documentar preguntas en notes para future reference
- [ ] Identificar pain points adicionales (oportunidad de upsell)

#### 6.2 Upsell a Retainer (Si aplica)
**Momento ideal:** Últimos 5 min del Q&A

**Script:**
"[Nombre], basado en lo que hemos trabajado juntos, veo [X oportunidad]. Tengo un retainer mensual de $[Y] que incluye:
- [Benefit 1 relacionado al proyecto actual]
- [Benefit 2]
- [Benefit 3]

¿Te interesa que te envíe una propuesta?"

**Si dicen "Sí":**
- [ ] Enviar propuesta en <24h
- [ ] Create GitHub issue: Retainer Conversion
- [ ] Follow-up en 3-5 días

**Si dicen "No":**
- [ ] "No problem. Si cambias de opinión, avísame."
- [ ] Agregar a CRM con nota: "Retainer no ahora, revisar en 60 días"

---

### ✅ Cierre Administrativo

#### 6.3 Request Testimonial (Within 24h de Q&A)
```
Subject: 🙏 Quick Favor - Testimonial

Hola [Nombre],

Me alegra mucho que estés satisfecho con [proyecto].

¿Podrías tomarme 2 minutos para dejar un testimonial?

Esto me ayudaría muchísimo:
━━━━━━━━━━━━━━━━━━━━━━━━
📝 Google Form → [Link]

O si prefieres, responde estas 3 preguntas:
1. ¿Qué problema resolvimos?
2. ¿Cómo fue trabajar con nosotros?
3. ¿Recomendarías nuestros servicios?

Gracias de antemano!

Alfred
```

**Incentivo (opcional):**
- Ofrecer 10% descuento en próximo servicio por testimonial
- Solo si es genuino y positivo

---

#### 6.4 Follow-Up de Pago (Si no pagaron aún)

**Día 3 post-delivery:**
```
Subject: Reminder - Invoice [#XXXX]

Hola [Nombre],

Espero que estés disfrutando de [deliverable].

Recordatorio amigable:
Invoice #[XXXX] por $[X] vence hoy.

[Payment link]

¿Algún problema con el pago?

Alfred
```

**Día 7 post-delivery:**
```
Subject: 2nd Reminder - Invoice [#XXXX] Overdue

Hola [Nombre],

Invoice #[XXXX] por $[X] está vencida desde hace 4 días.

Por favor confirma status de pago.

Si hay algún issue con los deliverables que está causando el retraso, resolvámoslo ASAP.

Alfred
```

**Día 14 post-delivery:**
- [ ] Phone call directo
- [ ] Si no responden: Pause future work, considerar collection agency

---

#### 6.5 Close GitHub Issue
- [ ] Move issue a "Hecho"
- [ ] Agregar retrospective notes:
  - Qué funcionó bien
  - Qué mejorar para próxima vez
  - Learnings técnicos
- [ ] Update CRM:
  - Status: "Cliente Completado"
  - Add tag: "Retainer Candidato" si aplicó

---

#### 6.6 Update KPIs
- [ ] Registrar en `finance/flujo_caja_semanal.csv`
- [ ] Update DSO en `finance/ar_tracking.csv`
- [ ] Calcular NPS si enviaste survey

---

## Checklist de Red Flags

### 🚩 During Onboarding

| Red Flag | Acción |
|----------|--------|
| Cliente no paga 50% upfront en 48h | Pausar trabajo, call para resolver |
| Cliente cancela/reschedula kickoff >2 veces | Re-evaluar commitment, considerar refund |
| Cliente unclear on requirements en kickoff | Enviar scope document por escrito, pedir confirmación |
| Cliente pide scope creep sin pagar | "Eso sería $X adicional. ¿Procedo?" |
| Cliente no da accesos necesarios | Blocker, adjust timeline o cancel si >7 días |

### 🚩 During Execution

| Red Flag | Acción |
|----------|--------|
| Cliente no responde a updates (>48h) | WhatsApp/call directo |
| Cliente cambia requirements mid-project | "Eso requiere nueva propuesta. ¿Paramos o continuamos con scope original?" |
| Cliente pide features fuera de scope | Documentar para upsell post-delivery |

### 🚩 Post-Delivery

| Red Flag | Acción |
|----------|--------|
| Cliente no paga final 50% en 7 días | Follow-up agresivo, pause future work |
| Cliente unhappy con deliverable | Emergency call para resolver, ofrecer revision (1x gratis) |
| Cliente ghostea después de delivery | Mark como bad debt después de 30 días, no trabajar con ellos de nuevo |

---

## Templates de Archivos

### Carpeta de Entrega (Google Drive)
```
[Cliente]_[Servicio]_[Fecha]/
├── README.txt
├── Deliverables/
│   ├── [Deliverable_1].pdf
│   ├── [Deliverable_2].xlsx
│   └── [Deliverable_3].zip
├── Assets/
│   ├── Logo_Cliente.png
│   └── Screenshots/
└── Credentials.txt (si aplica)
```

### README.txt Template
```
ENTREGA - [Cliente] - [Servicio]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Fecha de Entrega: [DD/MM/YYYY]
Proyecto: [Nombre del proyecto]
Delaren Consulting LLC

CONTENIDO:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

1. Deliverables/
   - [Deliverable_1].pdf: [Descripción]
   - [Deliverable_2].xlsx: [Descripción]

2. Assets/
   - Logo y screenshots utilizados

3. Credentials.txt
   - Accesos generados (si aplica)

INSTRUCCIONES:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

[Paso a paso para usar los deliverables]

SOPORTE:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

¿Preguntas? Contacta:
Alfred - alfred@delaren.com
WhatsApp: [Número]

Q&A Session incluida: 30 min
Agenda aquí → [Calendly link]
```

---

**Owner:** Alfred (Delaren Consulting LLC)
**Última Actualización:** 31 de diciembre, 2025
**Versión:** 1.0
