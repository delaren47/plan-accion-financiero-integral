# DEBT MASTER PLAN — Metodología para salir de deuda de tarjeta de crédito

**Actualizado:** 2026-07-17

> Este documento es **sólo metodología**. Cero números personales. Los datos reales viven en `private/` (gitignored, local-only). El repo es público.

---

## Objetivo y por qué

Salir de la deuda de tarjeta de crédito (TC). Es el P0 del proyecto, por encima de todo lo demás.

El problema es la aritmética mexicana: las TC en México cobran CAT de 60% a 120% anual. A esas tasas, el interés no es un costo, es una fuga que ahoga el flujo cada mes. Con ingreso low-ticket y limitado, cada peso que se va en intereses es un peso que nunca ataca el capital. Mientras la deuda revolvente siga viva, cualquier avance en ingresos se lo come el banco.

La meta no es "administrar" la deuda. Es matarla y no volver a caer.

---

## Prioridades del proyecto

| Prioridad | Foco | Estado |
|---|---|---|
| **P0** | Eliminar la deuda de TC | activo |
| **P1** | Ingresos low-ticket como acelerador de pagos | activo, subordinado a P0 |
| **P2** | Compliance de la LLC — mínimo viable (no dejar que se vuelva multa/problema) | mantenimiento |
| **P3** | PAFI original (white-label, retainers) | parqueado hasta bajar la deuda |

Cada peso extra generado en P1 va directo al plan de pago de P0. P2 se mantiene al mínimo para no crear nuevos pasivos. P3 espera.

---

## Fase 0 — Visibilidad (semana 1)

No se puede atacar lo que no se mide.

1. Ingesta de **todos** los estados de cuenta: cada tarjeta, cada crédito, últimos 2-3 meses. Débito también, para ver el flujo real.
2. Inventario completo en `private/deudas/deudas_registro.csv`: saldo, límite, tasa anual, CAT, día de corte, día límite de pago, pago mínimo, pago para no generar intereses, MSI pendientes.
3. Auditoría SaaS: cada cargo recurrente detectado en la ingesta se registra en `private/ledger/suscripciones_saas.csv` con su nivel de uso real.

Salida de la fase: una foto exacta de cuánto se debe, a qué tasa, y cuándo cae cada fecha.

---

## Fase 1 — Detener la sangría (stop the bleeding)

Antes de acelerar pagos, cerrar las fugas obvias.

- **Cancelar o hacer downgrade** de todo SaaS con uso `casi_nunca`. Ese dinero se redirige al plan de deuda.
- **Domiciliar el pago mínimo** de cada tarjeta como red de seguridad contra moratorios y reportes negativos. El mínimo domiciliado es sólo el piso: los pagos reales se hacen manualmente por encima del mínimo. La domiciliación existe para que un descuido nunca dispare intereses moratorios ni marque el Buró.
- **Identificar cargos no reconocidos** en la ingesta: suscripciones zombie, dobles cobros, cargos que no cuadran. Aclarar o cancelar.

Salida de la fase: gasto recurrente podado y ningún riesgo de moratorio por olvido.

---

## Fase 2 — Estrategia avalancha

Ordenar todas las deudas por **CAT/tasa descendente**. Todo el excedente mensual va a la tarjeta más cara; a las demás sólo el mínimo. Cuando cae la más cara, ese excedente rueda a la siguiente. Repetir.

**Por qué avalancha y no bola de nieve (snowball):** con tasas mexicanas de 60-120% CAT, la diferencia de costo entre atacar la deuda más cara vs. la más chica es enorme. La bola de nieve (pagar primero la de saldo más pequeño) da una victoria psicológica temprana, pero a estas tasas el costo de ignorar la tarjeta más cara se dispara. La avalancha minimiza el interés total pagado — que es exactamente la fuga que estamos matando.

**Regla clave de México — fecha de CORTE, no fecha límite:** el interés se calcula sobre el **saldo promedio diario** del periodo. Pagar **antes de la fecha de corte** baja ese promedio y por lo tanto los intereses del ciclo. Pagar sólo antes de la fecha límite de pago evita el moratorio, pero no reduce los intereses ya devengados. Entonces: el abono fuerte va **antes del corte**, no sólo antes del vencimiento.

**Meta intermedia por tarjeta:** llevar cada tarjeta a su "pago para no generar intereses" del ciclo. Una tarjeta que se paga completa antes del corte deja de generar interés revolvente — deja de sangrar aunque aún tenga MSI corriendo.

---

## Fase 3 — Reestructura (si los números no dan)

Sólo si el flujo no alcanza para la avalancha. Opciones ordenadas de **menor a mayor costo/riesgo**:

1. **Transferencia de saldo a tasa baja.** Mover saldo de una TC cara a una promoción de tasa baja (o cero por N meses). El más barato si califica.
2. **Préstamo personal de consolidación.** Un préstamo con tasa menor que la TC para liquidar las tarjetas y quedar con un solo pago más barato. Sirve sólo si la tasa es realmente menor y no se vuelven a usar las tarjetas.
3. **Reestructura directa con el banco.** Negociar plazo/tasa con la institución. **Advertencia:** una reestructura puede quedar marcada en Buró de Crédito.
4. **Quita (último recurso).** Negociar pagar menos del total. Daña el Buró de forma seria y por años. Sólo cuando no hay otra salida.

**ADVERTENCIA explícita:** nunca contratar "reparadoras de deuda" comerciales. Cobran comisiones altas, piden dejar de pagar (lo que destroza el Buró), y a menudo dejan al deudor peor. Si se necesita orientación, el recurso correcto es **CONDUSEF** (gratuito, es el organismo público de defensa del usuario financiero).

---

## Reglas de oro

- **No prepagar MSI sin intereses.** Un MSI a 0% no cuesta nada por esperar. Cada peso disponible ataca primero la deuda revolvente cara. Prepagar un MSI sin intereses es regalar liquidez que rendiría muchísimo más matando CAT de 90%.
- **Micro-fondo colchón primero.** Antes de la avalancha agresiva, apartar un colchón chico (aunque sea 2-5K MXN). Sin colchón, cualquier imprevisto vuelve a la TC y se recae. El colchón es lo que rompe el ciclo.
- **Monitorear el Buró de Crédito.** Hay 1 reporte gratis al año en Buró de Crédito y otro en Círculo de Crédito — escalonarlos da visibilidad ~semestral sin costo.
- **Todo cargo recurrente detectado en ingesta va a `suscripciones_saas.csv`.** Sin excepción. Es la única forma de que no se acumulen fugas nuevas.

---

## Ritual semanal — "Money Friday" (15 min)

Cada viernes, 15 minutos:

1. Revisar `private/DASHBOARD.md`.
2. Registrar los pagos de la semana en `pagos_deuda.csv`.
3. Decidir el excedente de la semana: cuánto sobra y a qué tarjeta va.
4. Checar próximas fechas de **corte** (no sólo de pago) para cronometrar el abono fuerte.

Corto, fijo, sin ceremonia. La consistencia semanal es lo que hace bajar la métrica reina.

---

## Métricas P0

| Métrica | Qué mide |
|---|---|
| **Deuda total** | Saldo agregado de todas las TC. |
| **Tasa ponderada** | Tasa promedio ponderada por saldo. |
| **Intereses / mes** | **La métrica reina. Debe bajar cada mes.** Si no baja, el plan no funciona. |
| **# tarjetas en "pago no intereses"** | Cuántas tarjetas ya no generan interés revolvente. |
| **Fecha proyectada de deuda cero** | Proyección de cuándo llega a cero al ritmo actual. |

---

## Nota final

Los números reales viven en `private/` (gitignored, local-only). Este documento es sólo la metodología — se puede leer sin exponer un solo peso.
