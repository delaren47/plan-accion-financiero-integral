# Template: Auditoría de Accesibilidad Web

**Servicio:** Fast Cash Win - Auditoría WCAG 2.1
**Tiempo de Entrega:** 48-72 horas
**Precio:** $800 USD

---

## Deliverables

1. Reporte ejecutivo (PDF de 5-8 páginas)
2. Issue tracker (Excel con issues priorizados)
3. Plan de remediación (con estimaciones de esfuerzo)
4. Sesión de Q&A (30 min, post-entrega)

---

## Proceso de Ejecución

### Paso 1: Kickoff Call (30 min)
- [ ] Obtener URL del sitio web
- [ ] Identificar 10 páginas clave para auditar
- [ ] Confirmar compliance target: WCAG 2.1 Level AA
- [ ] Acordar fecha de entrega (48-72h desde ahora)

### Paso 2: Análisis Automatizado (2 horas)
**Herramientas:**
- axe DevTools (Chrome extension)
- WAVE (Web Accessibility Evaluation Tool)
- Lighthouse (Google Chrome)

**Output:**
- Screenshots de issues detectados
- Automated scan report (JSON export)

### Paso 3: Review Manual (4 horas)
**Áreas a probar:**
- [ ] Navegación por teclado (Tab, Enter, Esc)
- [ ] Contraste de colores (Text vs. Background)
- [ ] Alt text en imágenes
- [ ] Form labels y error messages
- [ ] Heading structure (H1-H6)
- [ ] Landmarks (nav, main, footer, aside)
- [ ] Focus indicators
- [ ] Screen reader compatibility (NVDA o VoiceOver)

**Documentar:**
- Severity: Critical / High / Medium / Low
- WCAG criterion violated (ej: 1.4.3 Contrast Minimum)
- Current state (screenshot)
- Recommendation (how to fix)

### Paso 4: Reporte Ejecutivo (3 horas)

**Estructura del PDF:**

#### Portada
- Logo del cliente
- "Auditoría de Accesibilidad Web WCAG 2.1 Level AA"
- Fecha
- Prepared by: Delaren Consulting LLC

#### Executive Summary (1 página)
- Overall compliance score (0-100%)
- Total issues found: [X]
  - Critical: [X]
  - High: [X]
  - Medium: [X]
  - Low: [X]
- Top 3 issues a resolver inmediatamente
- Estimated effort para full compliance: [X horas/semanas]

#### Methodology (0.5 páginas)
- Páginas auditadas (lista de 10 URLs)
- Tools utilizados
- WCAG 2.1 Level AA como estándar

#### Detailed Findings (3-4 páginas)
Para cada issue crítico/alto:
```
Issue #[X]: [Título descriptivo]
━━━━━━━━━━━━━━━━━━━━━━━━━━━
Severity: [Critical/High]
WCAG Criterion: [Ej: 1.4.3 Contrast Minimum]
Pages Affected: [X de 10]

Description:
[Descripción del problema]

Impact:
[Quién se ve afectado y cómo]

Current State:
[Screenshot con issue highlighted]

Recommendation:
[Paso a paso para remediar]

Estimated Effort: [X horas]
```

#### Remediation Plan (1-2 páginas)

**Tabla priorizada:**
| Priority | Issue | Pages | Effort | Timeline |
|----------|-------|-------|--------|----------|
| P0 | [Issue crítico 1] | 8/10 | 4h | Week 1 |
| P0 | [Issue crítico 2] | 10/10 | 6h | Week 1 |
| P1 | [Issue alto 1] | 3/10 | 2h | Week 2 |
| ... | ... | ... | ... | ... |

**Phased Approach:**
- **Fase 1 (Week 1-2):** Resolver issues P0 (critical)
- **Fase 2 (Week 3-4):** Resolver issues P1 (high)
- **Fase 3 (Week 5-6):** Resolver issues P2 (medium)
- **Fase 4 (Ongoing):** Best practices para prevenir regression

#### Next Steps (1 página)
1. Review este reporte con equipo técnico
2. Priorizar issues basado en impact vs. effort
3. Considerar contratar servicio de implementación ($800-$1,500/mes retainer)
4. Agendar sesión de Q&A (30 min incluida)
5. Re-audit en 60 días para medir progreso

#### Appendix
- Glossary de términos de accesibilidad
- WCAG 2.1 Level AA checklist completo
- Recursos adicionales (links a W3C, MDN)

### Paso 5: Issue Tracker (Excel) (1 hora)

**Columnas:**
- Issue ID
- Page URL
- Issue Title
- Description
- WCAG Criterion
- Severity
- Current State (screenshot link)
- Recommendation
- Estimated Effort (hours)
- Status (Not Started / In Progress / Done)
- Assigned To
- Notes

**Formato:**
- Filtros en headers
- Conditional formatting (red para Critical, yellow para High)
- Totales al final (SUM de effort)

### Paso 6: Q&A Session (30 min)

**Agenda:**
1. **Walkthrough del reporte (10 min)**
   - Explicar top 3 issues
   - Mostrar ejemplos en vivo en el sitio

2. **Preguntas del cliente (15 min)**
   - Clarificaciones técnicas
   - Priorización de esfuerzos

3. **Next steps y upsell (5 min)**
   - Proponer retainer de implementación
   - Ofrecer training a equipo dev

---

## Checklist de Entrega

**Antes de enviar al cliente:**
- [ ] PDF reviewed (sin typos, screenshots legibles)
- [ ] Excel tested (filtros funcionan, fórmulas correctas)
- [ ] Email de entrega drafted (ver template abajo)
- [ ] Q&A session agendada en calendario

**Email de Entrega:**
```
Subject: ✅ Auditoría de Accesibilidad - [Nombre Cliente]

Hola [Nombre],

Adjunto encuentras:
1. Reporte Ejecutivo de Accesibilidad (PDF)
2. Issue Tracker con todos los hallazgos (Excel)

Resumen:
- Total issues encontrados: [X]
- Compliance score: [Y]%
- Esfuerzo estimado para full compliance: [Z] horas

Top 3 prioridades:
1. [Issue crítico 1]
2. [Issue crítico 2]
3. [Issue alto 1]

Próximos pasos:
- Agendar sesión de Q&A (30 min) → [Link a Calendly]
- Review del reporte con tu equipo técnico
- Considerar plan de implementación

¿Preguntas?

Saludos,
Alfred
Delaren Consulting LLC
```

---

## Timing Breakdown

| Actividad | Tiempo |
|-----------|--------|
| Kickoff call | 0.5h |
| Análisis automatizado | 2h |
| Review manual | 4h |
| Reporte ejecutivo | 3h |
| Issue tracker | 1h |
| Q&A session | 0.5h |
| **Total** | **11 horas** |

**Margen:** $800 / 11h = $72/hora (excelente margen)

---

## Upsell a Retainer

**Durante Q&A session, proponer:**

"Basado en esta auditoría, implementar todas las remediaciones tomaría aproximadamente [X] horas. Puedo ofrecerte un retainer mensual de $800-$1,500 que incluye:

- Implementación de fixes priorizados
- Testing continuo
- Soporte para tu equipo dev
- Re-audits trimestrales

¿Te interesa discutir esto más a fondo?"

**Close rate target:** >40% de auditorías → retainer

---

## Learnings y Edge Cases

### Common Pitfalls
- **Cliente no sabe qué páginas auditar:** Sugerir homepage + top 5 landing pages por analytics
- **Sitio muy grande (100+ páginas):** Limitar a sample de 10 páginas representativas
- **Cliente pide WCAG AAA:** Explicar que AA es el estándar, AAA es muy restrictivo

### Best Practices
- Usar screenshots con annotations (arrows, highlights) para claridad
- Priorizar issues que afectan >50% de páginas
- Incluir code snippets en recommendations cuando sea posible

### Tools Alternatives
- **Pa11y:** CLI tool para CI/CD integration
- **Tenon.io:** Paid service con mejor reporting
- **Siteimprove:** Enterprise-level (expensive)

---

**Template Owner:** Alfred
**Última Actualización:** 31 de diciembre, 2025
**Versión:** 1.0
