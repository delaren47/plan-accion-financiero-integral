# Implementation Notes — PAFI

Notas de diseño append-only. Captura el **porqué** de las decisiones, no el qué (eso vive en los deliverables).

---

## 2026-07-17 — Relanzamiento: P0 deuda

Relanzamiento de PAFI con un único foco P0: eliminar la deuda de tarjeta de crédito. Rituales del plan de 90 días originales quedan parqueados (ver P3 en `DEBT_MASTER_PLAN.md`).

### Decisiones de diseño

**El repo se queda público; `private/` es el plano de datos.**
- El repo es público y `vault-sync` hace `git add -A` + push cada 15 min. Eso obliga a defensa en capas para los datos financieros personales:
  1. **`.gitignore`** — `private/` ignorado. Primera línea y defensa primaria (nada dentro se trackea).
  2. **Hook anti-PII de pre-commit** — bloquea `.csv` / `.xlsx` como segunda capa por si algo se escapa del gitignore.
  3. **`*.pdf` gitignored** — tercera capa para los estados de cuenta crudos.
- La metodología (pública) y los números (privados) quedan físicamente separados. `DEBT_MASTER_PLAN.md` se puede leer sin exponer un peso.

**Avalancha sobre bola de nieve.**
- Con CAT mexicano de 60-120%, minimizar interés total pesa más que la victoria psicológica temprana de la bola de nieve. Se ordena por CAT/tasa descendente. Regla México documentada: pagar antes de la fecha de **corte** (no sólo antes del vencimiento) porque el interés se calcula sobre saldo promedio diario.

**Protocolo de ingesta.**
- Alfredo suelta cualquier documento financiero en `private/ingesta/`; en sesión dice "procesa la ingesta"; Claude extrae, hace append a los CSV, mueve el archivo a `procesado/AAAA-MM/` y regenera el DASHBOARD. Baja la fricción de captura a cero, que es lo que sostiene el hábito.

### Preguntas abiertas

- **Backup de `private/`.** Local-only hoy, sin respaldo. Decidir: repo espejo privado vs. iCloud vs. Time Machine. Riesgo real de pérdida total si falla el disco.
- **¿Hacer el repo privado más adelante?** Simplificaría la defensa en capas, pero se pierde la cara pública de la metodología. Pendiente.
- **Retro de cierre del plan de 90 días original.** Sigue pendiente (actual vs. meta $12K MRR). Sólo Alfredo tiene los números reales — no se puede cerrar sin él.
