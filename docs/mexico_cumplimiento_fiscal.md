# Cumplimiento Fiscal México (SAT)

**Guía de Compliance para Operaciones en México**
**Jurisdicción:** México
**Autoridad Fiscal:** Servicio de Administración Tributaria (SAT)
**Tipo de Entidad:** Persona Moral (Sociedad Anónima de Capital Variable - SA de CV, o Sociedad de Responsabilidad Limitada - S de RL)

---

## Resumen Ejecutivo

Operar un negocio en México implica:
1. **Acceso al mercado LATAM:** Puerta de entrada a América Latina (130 millones de habitantes)
2. **Complejidad fiscal alta:** Sistema tributario detallado con múltiples obligaciones mensuales
3. **CFDI obligatorio:** Facturación electrónica para TODAS las transacciones
4. **Contador obligatorio:** Prácticamente imposible cumplir sin contador/CPA mexicano
5. **Costos operativos elevados:** $6,000-$15,000 USD anuales en compliance

**Compliance Timeline Crítico:**
- **RFC (Tax ID):** Inmediatamente después de constitución
- **e.firma/FIEL:** Dentro de 30 días de RFC (cita presencial en SAT)
- **ISR Mensual (Provisional):** Día 17 del mes siguiente
- **IVA Mensual:** Día 17 del mes siguiente
- **DIOT:** Día 17 del mes siguiente (si causante de IVA)
- **Contabilidad Electrónica:** Día 25 del mes siguiente (balanza de comprobación)
- **ISR Anual:** 31 de marzo del año siguiente
- **CFDI:** Emitir dentro de 72 horas de cada transacción

**⚠️ ADVERTENCIA:** El sistema fiscal mexicano es UNO DE LOS MÁS COMPLEJOS del mundo. Contratar contador mexicano NO es opcional, es **obligatorio** para compliance exitoso.

---

## Obligaciones Federales (SAT)

### 1. RFC (Registro Federal de Contribuyentes)

**¿Qué es?**
Identificador fiscal único de 13 caracteres para personas morales en México (equivalente al EIN en USA o BN en Canadá).

**Formato:**
- Ejemplo: **ABC123456XYZ**
  - ABC = Iniciales de razón social
  - 123456 = Fecha de constitución (YYMMDD)
  - XYZ = Homoclave (asignada por SAT)

**Cuándo obtenerlo:**
✅ **Inmediatamente** después de constituir la empresa (requisito para abrir cuenta bancaria, contratar, facturar).

**Requisitos Previos:**
1. **Acta Constitutiva:** Escritura pública notariada
2. **Inscripción en Registro Público de Comercio**
3. **Poder Notarial del Representante Legal** (si aplica)
4. **CURP del Representante Legal** (Clave Única de Registro de Población)

**Cómo Obtenerlo:**
1. **Portal SAT:** https://www.sat.gob.mx/tramites/28753/obten-tu-rfc-con-la-clave-unica-de-registro-de-poblacion-curp
2. **Presencial:** Oficina SAT con cita previa (recomendado para primera vez)
3. **A través de Notario:** Algunos notarios incluyen RFC en el acta constitutiva

**Documentos Requeridos:**
- Acta Constitutiva certificada
- Comprobante de domicilio fiscal (recibo CFE, agua, predial <3 meses)
- Identificación oficial del representante legal (INE/Pasaporte)
- CURP del representante legal

**Tiempo:** 1-5 días hábiles (online) o inmediato (presencial en SAT si todo correcto)

**Costo:** $0 (gratis)

**⚠️ IMPORTANTE:** El domicilio fiscal en RFC debe coincidir con el domicilio en Acta Constitutiva. Cualquier cambio requiere aviso al SAT dentro de 10 días.

**Documentación:**
- Guardar Constancia de Situación Fiscal en `legal/mexico/rfc_constancia.pdf`
- Usar RFC en:
  - Facturas CFDI (emisor y receptor)
  - Contratos
  - Declaraciones fiscales
  - Cuenta bancaria

---

### 2. e.firma / FIEL (Firma Electrónica Avanzada)

**¿Qué es?**
Certificado digital que sirve como firma electrónica para realizar TODOS los trámites ante el SAT. **SIN e.firma NO PUEDES:**
- Presentar declaraciones fiscales
- Emitir CFDI (facturas electrónicas)
- Consultar tu buzón tributario
- Realizar trámites en línea con SAT

**Componentes:**
- **Certificado (.cer):** Archivo público
- **Llave privada (.key):** Archivo privado (NUNCA compartir)
- **Contraseña:** Para usar la llave privada

**Vigencia:** 4 años (renovación obligatoria)

**Cómo Obtenerla:**
1. **Generar solicitud (.req):** Portal SAT - https://www.sat.gob.mx/tramites/28523/solicita-tu-certificado-de-e-firma-portable
2. **Agendar cita presencial:** https://citas.sat.gob.mx/
3. **Acudir a oficina SAT con:**
   - Solicitud (.req) impresa y en USB
   - Acta Constitutiva original y copia
   - Poder Notarial (si no eres administrador único)
   - Identificación oficial (INE/Pasaporte vigente)
   - Comprobante de domicilio fiscal
4. **Recibir e.firma:** SAT entrega archivos .cer y .key + contraseña

**Tiempo:**
- Generar solicitud: 15-30 minutos
- Cita presencial: 1-2 semanas de espera (depende de disponibilidad)
- Emisión en oficina: Mismo día (si documentos correctos)

**Costo:** $0 (gratis)

**Renovación (cada 4 años):**
- Proceso similar, pero desde 60 días antes de vencimiento hasta 30 días después
- **Penalidad por NO renovar a tiempo:** Bloqueo de buzón tributario, imposibilidad de facturar

**⚠️ CRÍTICO:**
- La e.firma es TU FIRMA LEGAL. Guardar archivos .cer y .key en lugar SEGURO (USB encriptado, password manager).
- Si pierdes la llave privada (.key), debes tramitar NUEVA e.firma (proceso completo desde cero).
- NUNCA compartir archivos o contraseña con terceros (ni contador, excepto en sesión supervisada).

**Documentación:**
- Guardar .cer y .key en `legal/mexico/efirma/` (ENCRIPTADO)
- Anotar fecha de vencimiento en calendario (renovar 60 días antes)

---

### 3. ISR (Impuesto Sobre la Renta - Corporate Income Tax)

**¿Qué es?**
Impuesto federal sobre utilidades de personas morales.

**Tasa:** **30% flat** (sin small business deduction como Canadá)

**Ejercicio Fiscal:** Año calendario (1 de enero - 31 de diciembre)

**Declaraciones:**

#### A) **Pagos Provisionales Mensuales (ISR Mensual)**

**Deadline:** Día **17 del mes siguiente**

**Cálculo:**
```
ISR Mensual = (Ingresos Acumulados - Deducciones Autorizadas Acumuladas - PTU pagada) × 30%
              - ISR retenido de meses previos - Pagos provisionales previos
```

**Ejemplo (Mes 6 - Junio):**
- Ingresos acumulados (Ene-Jun): $500,000 MXN
- Deducciones acumuladas: $300,000 MXN
- Utilidad gravable acumulada: $200,000 MXN
- ISR causado (30%): $60,000 MXN
- ISR pagado en meses 1-5: $45,000 MXN
- **ISR a pagar en Junio:** $60,000 - $45,000 = **$15,000 MXN**

**Cómo Presentar:**
1. Portal SAT con e.firma: https://www.sat.gob.mx/declaracion/
2. Software contable (ContPAQi, Aspel, COI)
3. A través de contador (recomendado)

**⚠️ IMPORTANTE:** Cálculo complejo. **Contador obligatorio** para evitar errores.

---

#### B) **Declaración Anual de ISR**

**Deadline:** **31 de marzo** del año siguiente

**Contenido:**
- Estado de posición financiera (Balance General)
- Estado de resultados (Estado de Pérdidas y Ganancias)
- Conciliación contable-fiscal
- Determinación de ISR anual
- Información de socios/accionistas
- PTU (Participación de Trabajadores en las Utilidades) a repartir (10% de utilidad fiscal)

**Ajustes Fiscales:**
- Deducciones no autorizadas (multas, propinas, donativos no deducibles)
- Ingresos no acumulables
- Pérdidas fiscales de años anteriores (pueden compensarse)

**Cómo Presentar:**
- Portal SAT con e.firma
- **Altamente recomendado:** Contador CPA certificado

**Costo Contador:**
- Declaración anual: $1,000-$3,000 USD (depende de complejidad)

**Penalidad por No Presentar:**
- 20-30% del ISR omitido
- Recargos: 1.13% mensual
- Multas adicionales: $1,800-$36,000 MXN (~$90-$1,800 USD)

---

### 4. IVA (Impuesto al Valor Agregado - Value Added Tax)

**¿Qué es?**
Impuesto federal sobre consumo (equivalente al GST/HST en Canadá o VAT en Europa).

**Tasa General:** **16%**

**Tasas Especiales:**
- **0%:** Exportaciones, alimentos básicos, medicinas
- **Exento:** Servicios educativos, médicos, renta de vivienda, transporte público

**Mecánica:**
```
IVA a Pagar = IVA Cobrado (trasladado) - IVA Pagado (acreditable)
```

**Ejemplo:**
- Facturaste servicios: $100,000 MXN + IVA $16,000 = **$116,000 MXN**
- Pagaste gastos: $40,000 MXN + IVA $6,400 = **$46,400 MXN**
- **IVA a pagar:** $16,000 - $6,400 = **$9,600 MXN**

**Declaración Mensual:**
- **Deadline:** Día **17 del mes siguiente**
- **Cómo Presentar:** Portal SAT con e.firma o contador
- **Formato:** Declaración electrónica

**IVA Acreditable (Recuperable):**
- Solo si tienes CFDI válido del proveedor
- Solo si gasto es deducible para ISR
- Solo si IVA está desglosado correctamente en CFDI

**Servicios de Consultoría:**
- **A clientes mexicanos:** 16% IVA
- **A clientes extranjeros (exportación de servicios):** **0% IVA** (si se cumplen requisitos de lugar de prestación)
  - Requisitos: Servicio usado/aprovechado en el extranjero, cobro en moneda extranjera, cliente sin establecimiento en México

**IVA en Saldo a Favor:**
- Si IVA acreditable > IVA trasladado: Saldo a favor
- **Opciones:**
  1. Compensar contra ISR u otros impuestos
  2. Solicitar devolución (proceso lento: 40-60 días, puede requerir auditoría)

**Penalidad por Presentación Tardía:**
- 0.75-1.00% del IVA omitido por mes
- Recargos: 1.13% mensual
- Multas: $1,800-$36,000 MXN

**⚠️ CRÍTICO:** IVA es impuesto AL FLUJO. Aunque estés en pérdida fiscal (ISR $0), **DEBES pagar IVA** si cobraste más IVA del que pagaste.

---

### 5. CFDI 4.0 (Comprobante Fiscal Digital por Internet - Factura Electrónica)

**¿Qué es?**
Sistema de facturación electrónica **OBLIGATORIO** para TODAS las transacciones comerciales en México.

**Versión Actual:** CFDI 4.0 (vigente desde enero 2023)

**Requisitos:**
- Tener RFC activo
- Tener e.firma válida
- Contratar un **PAC (Proveedor Autorizado de Certificación)**

---

#### A) **PAC (Proveedor Autorizado de Certificación)**

**¿Qué hace?**
Intermediario autorizado por SAT que:
1. Valida tu CFDI contra esquemas XML del SAT
2. Asigna UUID (folio fiscal único)
3. Timbra la factura (sello digital SAT)
4. Envía XML al SAT
5. Te devuelve XML y PDF timbrados

**Proveedores Recomendados:**

| PAC | Costo Mensual | Timbres Incluidos | Pros |
|-----|---------------|-------------------|------|
| **Facturama** | $199 MXN (~$10 USD) | 250 | Fácil de usar, API robusta |
| **Bind ERP** | $299-$599 MXN | 500-Ilimitados | ERP completo incluido |
| **Aspel Facture** | $1,200 MXN (~$60 USD) | Ilimitados | Integración con Aspel COI/NOI |
| **ContPAQi Factura** | $800 MXN (~$40 USD) | Ilimitados | Integración con ContPAQi |
| **Descarga Masiva (Free)** | $0 | Consulta | Solo para descargar CFDI recibidos |

**Recomendación para Delaren Consulting:**
- **Año 1 (<50 facturas/mes):** Facturama ($199 MXN/mes)
- **Año 2+ (>50 facturas/mes):** Bind ERP ($599 MXN/mes) o ContPAQi

---

#### B) **Tipos de CFDI**

| Tipo | Uso | Cuándo Emitir |
|------|-----|---------------|
| **Ingreso** | Venta de bienes/servicios | Cuando cobras a cliente |
| **Egreso** | Nota de crédito, devolución | Cuando devuelves dinero a cliente |
| **Traslado** | Movimiento de mercancías | Transporte de bienes (sin venta) |
| **Nómina** | Recibo de pago a empleados | Cada pago de nómina |
| **Pago** | Complemento de pago | Cuando recibes pago PARCIAL de factura (si facturaste en "pago en parcialidades o diferido") |

**Uso Común (Consultoría):** CFDI de **Ingreso** (99% de los casos)

---

#### C) **Requisitos del CFDI 4.0**

**Datos Obligatorios:**
1. **Emisor:**
   - RFC
   - Razón social
   - Régimen fiscal (ej: 601 - General de Ley Personas Morales)
   - Domicilio fiscal (código postal)

2. **Receptor:**
   - RFC (si es persona física sin actividad empresarial: **XAXX010101000**)
   - Razón social o nombre
   - Domicilio fiscal (código postal)
   - Régimen fiscal
   - Uso del CFDI (ej: G03 - Gastos en general, P01 - Por definir)

3. **Conceptos:**
   - Descripción del servicio/producto
   - Cantidad
   - Unidad de medida (Clave SAT: ej. E48 - Servicio)
   - Clave producto/servicio (Clave SAT: ej. 85121801 - Servicios de consultoría de negocios)
   - Precio unitario
   - Importe
   - IVA trasladado (16%, 0%, o exento)

4. **Forma de Pago:**
   - Código SAT (ej: 01 - Efectivo, 03 - Transferencia, 04 - Tarjeta)

5. **Método de Pago:**
   - **PUE (Pago en Una Exhibición):** Pago completo inmediato
   - **PPD (Pago en Parcialidades o Diferido):** Pago parcial o futuro (requiere CFDI de "Pago" después)

6. **Moneda:**
   - MXN (Peso mexicano) o USD, EUR, etc. (requiere tipo de cambio SAT del día)

**Archivo Generado:**
- **XML:** Archivo estructurado para SAT (obligatorio)
- **PDF:** Representación visual para cliente (recomendado)

---

#### D) **Timing de Emisión**

**Regla General:** Emitir CFDI **dentro de 72 horas** de realizada la operación.

**Excepciones:**
- **Servicios de hospedaje:** Al check-out
- **Servicios personales:** Al finalizar servicio o pago (lo que ocurra primero)

**⚠️ PENALIDAD:** $3,000-$10,000 MXN (~$150-$500 USD) por cada CFDI emitido fuera de plazo.

---

#### E) **Cancelación de CFDI**

**Reglas (CFDI 4.0):**
- **Menos de $5,000 MXN:** Puedes cancelar sin aceptación del receptor (24 horas después de emisión)
- **Más de $5,000 MXN:** Requiere aceptación del receptor (cliente debe aprobar cancelación en su portal SAT)
- **Plazo:** Cliente tiene 72 horas para aceptar/rechazar

**Motivos de Cancelación:**
- 01: Comprobante emitido con errores con relación
- 02: Comprobante emitido con errores sin relación
- 03: No se llevó a cabo la operación
- 04: Operación nominativa relacionada en factura global

**Proceso:**
1. Solicitar cancelación en PAC
2. Si >$5,000 MXN, esperar aceptación de receptor
3. Si acepta: Cancelación exitosa (generar Nota de Crédito si corresponde)
4. Si rechaza o no responde en 72h: CFDI queda vigente

---

#### F) **Retención de Impuestos (CFDI de Retenciones)**

Si contratas servicios profesionales o arrendas, debes retener impuestos:
- **ISR:** 10% (servicios profesionales)
- **IVA:** 2/3 (en algunos casos)

**Obligación:** Emitir CFDI de Retenciones al prestador de servicios.

---

### 6. DIOT (Declaración Informativa de Operaciones con Terceros)

**¿Qué es?**
Reporte mensual de TODAS tus compras (proveedores) si eres contribuyente de IVA.

**Deadline:** Día **17 del mes siguiente**

**Información Requerida:**
- RFC de cada proveedor
- Nombre/razón social
- Monto de operaciones
- IVA pagado (16%, 0%, exento)
- Tipo de proveedor (nacional, extranjero)

**Formato:** Archivo de texto (.txt) generado por software contable

**Cómo Presentar:**
1. Generar archivo .txt desde software (ContPAQi, Aspel, Excel con macro)
2. Subir a portal SAT con e.firma

**Penalidad por No Presentar:**
- $1,000-$15,000 MXN (~$50-$750 USD)

**⚠️ IMPORTANTE:** Aunque NO tengas proveedores en el mes, debes presentar DIOT "en ceros".

---

### 7. Contabilidad Electrónica

**¿Qué es?**
Obligación de subir tu contabilidad EN FORMATO XML al SAT mensualmente.

**Componentes:**

#### A) **Catálogo de Cuentas (Chart of Accounts)**

**¿Qué es?**
Lista de todas tus cuentas contables (activos, pasivos, capital, ingresos, gastos) en formato XML.

**Requisito:** Usar código agrupador SAT para cada cuenta.

**Ejemplo:**
- 100 Activo → Código SAT: 100.00.00
- 101 Bancos → Código SAT: 102.01.00

**Cuándo Presentar:**
- Primera vez: Al iniciar operaciones (1er mes)
- Actualizaciones: Solo si modificas catálogo (agregar/eliminar cuentas)

**Cómo Generar:**
- Software contable (ContPAQi, Aspel NOI, CONTPAQi)
- **Contador obligatorio** (asignar códigos SAT correctamente)

---

#### B) **Balanza de Comprobación (Trial Balance)**

**¿Qué es?**
Resumen mensual de movimientos y saldos de TODAS tus cuentas contables.

**Deadline:** Día **25 del mes siguiente** (más tiempo que ISR/IVA)

**Formato:** XML con estructura específica SAT

**Información:**
- Cuenta contable
- Saldo inicial
- Cargos del periodo
- Abonos del periodo
- Saldo final

**Cómo Presentar:**
1. Generar XML desde software contable
2. Validar con herramienta SAT
3. Subir a portal SAT con e.firma

**Penalidad por No Presentar:**
- $1,000-$15,000 MXN (~$50-$750 USD)

---

#### C) **Auxiliares de Cuentas y Pólizas (On Request)**

**¿Qué es?**
Detalle transaccional de cada cuenta (auxiliar) y comprobantes contables (pólizas).

**Cuándo Presentar:** Solo si SAT lo solicita (auditoría, fiscalización)

**Plazo:** 3 días hábiles desde solicitud

**Formato:** XML

---

### 8. REPSE (Registro de Prestadoras de Servicios Especializados)

**¿Qué es?**
Registro obligatorio si prestas "servicios especializados" o outsourcing a otras empresas.

**¿Aplica a Consultoría?**
- **Posiblemente SÍ** si prestas servicios de TI, contabilidad, legal, RRHH, etc. a otras empresas mexicanas

**Autoridad:** STPS (Secretaría del Trabajo y Previsión Social), NO SAT

**Portal:** https://repse.stps.gob.mx/

**Requisitos:**
- RFC activo
- e.firma
- Opinión de cumplimiento positiva (32D) de SAT
- Opinión de cumplimiento IMSS
- Constancia de situación fiscal

**Vigencia:** 1 año (renovación anual)

**Costo:** $0 (registro) pero requiere tiempo de contador/abogado

**Penalidad por No Tener REPSE (si requerido):**
- Cliente NO puede deducir tus servicios fiscalmente
- Multas a cliente: $200,000-$4,000,000 MXN (~$10,000-$200,000 USD)
- Probable pérdida de contrato

**⚠️ ACCIÓN:** Consultar con contador si tus servicios califican como "especializados" bajo la Ley Federal del Trabajo.

---

## Obligaciones Estatales (Estado/Municipal)

### 1. Impuesto Sobre Nómina (Payroll Tax)

**¿Qué es?**
Impuesto estatal sobre el monto total de salarios pagados.

**Tasa:** Varía por estado (2-3%)

| Estado | Tasa | Base |
|--------|------|------|
| **Ciudad de México (CDMX)** | 3% | Total de erogaciones por salarios |
| **Jalisco (Guadalajara)** | 2% | Total de erogaciones |
| **Nuevo León (Monterrey)** | 3% | Total de erogaciones |
| **Querétaro** | 3% | Total de erogaciones |
| **Estado de México** | 3% | Total de erogaciones |

**Declaración:** Mensual (fecha varía por estado, generalmente día 17)

**Ejemplo (CDMX):**
- Salarios pagados en mes: $100,000 MXN
- **ISN a pagar:** $100,000 × 3% = **$3,000 MXN**

**Exenciones:**
- Algunos estados exentan si tienes <5 empleados
- Consultar ley local

**Cómo Pagar:**
- Portal estatal (ej: CDMX - https://oficinavirtual.finanzas.cdmx.gob.mx/)

**⚠️ IMPORTANTE:** Aunque no tengas empleados, si pagas honorarios asimilados a salarios, puede causar ISN.

---

### 2. Permiso de Funcionamiento Municipal (Business License)

**¿Qué es?**
Licencia municipal para operar negocio en domicilio fiscal.

**Autoridad:** Gobierno Municipal/Delegacional

**Costo:** Varía $500-$5,000 MXN (~$25-$250 USD) dependiendo de:
- Tamaño del local
- Giro del negocio
- Municipio

**Vigencia:**
- Indefinida (algunos municipios)
- Anual (otros municipios, requiere refrendo)

**Requisitos:**
- Licencia de uso de suelo (zonificación)
- Visto bueno de protección civil (si aplica)
- Comprobante de domicilio
- Identificación del representante legal

**Penalidad por Operar Sin Licencia:**
- Clausura del establecimiento
- Multas: $5,000-$50,000 MXN

**⚠️ NOTA:** Si operas 100% remoto (home office), algunos municipios NO requieren licencia. Consultar reglamento municipal.

---

## Obligaciones de Nómina (IMSS, INFONAVIT, SAR)

### 1. IMSS (Instituto Mexicano del Seguro Social)

**¿Qué es?**
Seguridad social obligatoria para TODOS los empleados (incluido dueño si recibe salario).

**Cuándo Registrar:**
- **Dentro de 5 días hábiles** de contratar empleado

**Cómo Registrar:**
- Portal IMSS: https://www.imss.gob.mx/
- IDSE (IMSS Desde Su Empresa)
- Contador/despacho laboral

---

#### **Cuotas IMSS (2026):**

**Distribución Patrón-Trabajador:**

| Ramo | Patrón | Trabajador | Total |
|------|--------|------------|-------|
| **Enfermedades y Maternidad** | 20.4% | 0% | 20.4% |
| **Invalidez y Vida** | 1.75% | 0.625% | 2.375% |
| **Retiro** | 2% | 0% | 2% |
| **Cesantía y Vejez** | 3.15% | 1.125% | 4.275% |
| **Guarderías** | 1% | 0% | 1% |
| **Riesgos de Trabajo** | 0.5-15% (promedio 2.5%) | 0% | 2.5% |
| **TOTAL APROXIMADO** | **~30%** | **~2%** | **~32%** |

**Base de Cotización:**
- Salario Diario Integrado (SDI) = Salario base + prestaciones (aguinaldo, prima vacacional, etc.)

**Ejemplo (Salario mensual $15,000 MXN):**
- SDI: ~$500 MXN/día
- **Cuota mensual patrón:** ~$4,500 MXN (30%)
- **Cuota mensual trabajador:** ~$300 MXN (2%)
- **Total costo patronal:** $15,000 + $4,500 = **$19,500 MXN**

**Pago:**
- **Mensual:** Día 17 del mes siguiente
- Cálculo: Usar SUA (Sistema Único de Autodeterminación) o software nómina

**Penalidad por NO Registrar:**
- Multas: 2-350 veces UMA (Unidad de Medida y Actualización)
- UMA 2026: ~$108 MXN
- **Multa mínima:** $216 MXN
- **Multa máxima:** $37,800 MXN (~$1,900 USD) **POR TRABAJADOR**
- Más: Actualización de cuotas + recargos + multas adicionales

**⚠️ CRÍTICO:** IMSS es IMPLACABLE. No registrar empleados = multas SEVERAS + auditorías.

---

### 2. INFONAVIT (Fondo Nacional de Vivienda)

**¿Qué es?**
Fondo de vivienda para trabajadores.

**Cuota:** 5% del SDI (100% patrón, 0% trabajador)

**Ejemplo (SDI $500 MXN/día):**
- **INFONAVIT mensual:** $500 × 30 días × 5% = **$750 MXN**

**Pago:**
- Junto con IMSS (día 17 del mes siguiente)
- Sistema integrado SUA

---

### 3. SAR (Sistema de Ahorro para el Retiro)

**Componentes:**
- **Retiro:** 2% del SDI (patrón)
- **Cesantía y Vejez:** 3.15% patrón + 1.125% trabajador

**Pago:**
- Junto con IMSS (sistema integrado)

**Total Retiro + Cesantía:**
- Patrón: 5.15%
- Trabajador: 1.125%

---

### 4. ISR Retención en Nómina

**¿Qué es?**
Retención mensual de ISR sobre salarios de empleados.

**Tarifas 2026 (Mensual):**

| Límite Inferior | Límite Superior | Cuota Fija | % Sobre Excedente |
|----------------|----------------|------------|-------------------|
| $0.01 | $746.04 | $0 | 1.92% |
| $746.05 | $6,332.05 | $14.32 | 6.40% |
| $6,332.06 | $11,128.01 | $371.83 | 10.88% |
| $11,128.02 | $12,935.82 | $893.63 | 16.00% |
| $12,935.83 | $15,487.71 | $1,182.88 | 17.92% |
| $15,487.72 | $31,236.49 | $1,640.18 | 21.36% |
| $31,236.50 | $49,233.00 | $5,004.12 | 23.52% |
| $49,233.01 | $93,993.90 | $9,236.89 | 30.00% |
| $93,993.91 | $125,325.20 | $22,665.17 | 32.00% |
| $125,325.21 | En adelante | $32,691.18 | 35.00% |

**Subsidio al Empleo:** Reduce ISR (tabla aparte, aplica en salarios bajos)

**Cálculo Mensual:**
1. Calcular salario mensual gravable
2. Aplicar tabla progresiva
3. Restar subsidio al empleo (si aplica)
4. Retener ISR al trabajador
5. Enterar al SAT (junto con IMSS día 17)

**Ejemplo (Salario $15,000 MXN/mes):**
- Excedente de $12,935.82: $15,000 - $12,935.82 = $2,064.18
- ISR sobre excedente: $2,064.18 × 17.92% = $369.90
- Cuota fija: $1,182.88
- **ISR total:** $369.90 + $1,182.88 = **$1,552.78 MXN**
- Menos subsidio: ~$0 (salario >$12,935)
- **ISR a retener:** **$1,552.78 MXN**

**Entero:**
- Día 17 del mes siguiente (declaración conjunta con IMSS)

---

### 5. CFDI de Nómina (Recibo de Pago Electrónico)

**Obligación:**
- Emitir CFDI de Nómina por CADA pago a empleados

**Información Requerida (además de CFDI normal):**
- Tipo de nómina (ordinaria, extraordinaria, finiquito)
- Percepciones (salario, bonos, comisiones)
- Deducciones (ISR, IMSS, INFONAVIT, préstamos)
- Otros pagos (indemnizaciones, jubilaciones)
- Registro patronal IMSS
- Número de seguridad social del trabajador

**Timing:**
- Antes de entregar pago al trabajador
- O máximo 72 horas después del pago

**Cómo Generar:**
- Software de nómina (ContPAQi Nóminas, Aspel NOI, COI)
- PAC con módulo de nómina
- **Contador/despacho laboral recomendado**

**⚠️ PENALIDAD:** $3,000-$10,000 MXN por cada CFDI de nómina no emitido o incorrecto.

---

## Registro Mercantil (Constitución de Empresa)

### 1. Notario Público

**Obligatorio:** TODAS las sociedades mercantiles (SA de CV, S de RL) requieren escritura pública notariada.

**Costo Notario:**
- **Ciudad de México:** $1,500-$2,500 USD
- **Guadalajara/Monterrey:** $1,200-$2,000 USD
- **Ciudades pequeñas:** $800-$1,500 USD

**Incluye:**
- Acta Constitutiva (escritura pública)
- Inscripción en Registro Público de Comercio
- RFC inicial (algunos notarios)

**Documentos Requeridos:**
- Identificación oficial de socios (INE/Pasaporte)
- CURP de socios
- Comprobante de domicilio (socio y empresa)
- Capital social inicial (depósito bancario o declaración)

**Tiempo:** 2-4 semanas (depende de carga notarial + Registro Público)

---

### 2. Registro Público de Comercio

**¿Qué es?**
Registro estatal de actas constitutivas y poderes notariales.

**Costo:** $100-$300 USD (incluido en honorarios notario)

**Tiempo:** 5-15 días hábiles (notario lo tramita)

**Documento Resultante:**
- Acta Constitutiva inscrita con número de registro
- Personalidad jurídica de la empresa

---

### 3. SA de CV vs. S de RL

#### **SA de CV (Sociedad Anónima de Capital Variable)**

**Características:**
- Socios: Mínimo 2, máximo ilimitado
- Capital: Variable (puedes aumentar/disminuir sin modificar acta)
- Acciones: Representadas por títulos (nominativos)
- Órganos: Asamblea de Accionistas + Consejo de Administración (o Administrador Único)
- Responsabilidad: Limitada al capital aportado

**Pros:**
- Más común (90% de empresas mexicanas)
- Fácil transferir acciones
- Mejor para buscar inversión futura

**Cons:**
- Más formalidades (asambleas anuales obligatorias)
- Más costoso (libros de actas, certificados de acciones)

---

#### **S de RL (Sociedad de Responsabilidad Limitada)**

**Características:**
- Socios: Mínimo 2, máximo 50
- Partes sociales (no acciones)
- Órganos: Asamblea de Socios + Gerente(s)
- Responsabilidad: Limitada al capital aportado

**Pros:**
- Más simple (menos formalidades)
- Transferencia de partes sociales más controlada (requiere consentimiento de socios)

**Cons:**
- Menos común
- Dificulta entrada de nuevos socios/inversores

---

**Recomendación para Delaren Consulting:**
- **SA de CV** (estándar, flexible, profesional)

---

## Obligaciones Bancarias

### 1. Cuenta Bancaria Empresarial

**¿Por qué obligatorio?**
- Separación de patrimonio (protección legal)
- Recibir pagos de clientes (CFDI requiere cuenta a nombre de empresa)
- Pagar nómina e impuestos

**Cuándo Abrir:**
✅ **Después de obtener RFC** (banco requiere RFC como requisito)

**Documentos Requeridos:**
- RFC de la empresa (Constancia de Situación Fiscal)
- Acta Constitutiva certificada
- Identificación oficial del representante legal
- Comprobante de domicilio de la empresa
- Poder Notarial (si no eres administrador único)

**Bancos Recomendados para PYMES:**

| Banco | Comisión Mensual | Transferencias SPEI | Pros |
|-------|------------------|---------------------|------|
| **BBVA** | $300-$500 MXN | Ilimitadas | App robusta, buenos servicios digitales |
| **Santander** | $250-$450 MXN | Ilimitadas | Buena atención PYMES |
| **Banorte** | $350-$600 MXN | Ilimitadas | Red amplia, fuerte en norte de México |
| **Inbursa** | $0-$200 MXN | Ilimitadas | Comisiones bajas |
| **Banamex (Citibank)** | $400-$700 MXN | Ilimitadas | Servicios internacionales (USD) |

**Recomendación para Delaren Consulting (Internacional):**
- **Primary:** BBVA (servicios digitales + USD)
- **Secondary:** Wise Business (multi-currency, bajo costo)

**Costo:**
- Comisión mensual: $0-$600 MXN (según banco y plan)
- Chequera: $500-$1,000 MXN
- Transferencias internacionales: $300-$500 MXN por operación

---

### 2. Control de Divisas

**Buenas Noticias:** México NO tiene control de cambios. Puedes:
- Recibir USD/EUR libremente
- Enviar USD/EUR sin restricciones
- Mantener cuentas en moneda extranjera

**Obligación Fiscal:**
- Declarar ingresos en moneda extranjera usando tipo de cambio SAT del día
- Portal SAT publica tipo de cambio diario oficial

---

## Checklist de Cumplimiento Mensual y Anual

### Mensual (Día 17)
- [ ] **ISR Provisional:** Pago provisional mensual (persona moral)
- [ ] **IVA:** Declaración y pago mensual
- [ ] **DIOT:** Declaración informativa de proveedores
- [ ] **IMSS/INFONAVIT:** Pago de cuotas obrero-patronales (SUA)
- [ ] **ISR Nómina:** Retenciones de ISR a trabajadores (si aplicable)
- [ ] **ISN (Estatal):** Impuesto sobre nómina (varía por estado)

### Mensual (Día 25)
- [ ] **Contabilidad Electrónica:** Subir balanza de comprobación XML al SAT

### Mensual (Todo el mes)
- [ ] **CFDI:** Emitir facturas electrónicas dentro de 72h de cada transacción
- [ ] **CFDI Nómina:** Emitir recibos de nómina electrónicos por cada pago

### Trimestral (Solo algunos casos)
- [ ] **Declaración Trimestral:** Solo si estás en Régimen Simplificado de Confianza (RESICO) - No aplica a personas morales regulares

### Anual (31 de Marzo)
- [ ] **ISR Anual:** Declaración anual de persona moral
- [ ] **Determinación de PTU:** 10% de utilidad fiscal a repartir a trabajadores (si aplicable)

### Anual (Febrero)
- [ ] **Constancias de Retenciones:** Entregar a empleados/proveedores (ISR retenido)
- [ ] **Declaración Anual de Sueldos:** Informativa de nómina anual

### Anual (Variable)
- [ ] **REPSE:** Renovación anual (si aplica)
- [ ] **Opinión de Cumplimiento 32D:** Solicitar cuando clientes requieran (deducibilidad)

---

## Costos Anuales de Compliance (Estimados 2026 en USD)

| Ítem | Frecuencia | Costo (USD) |
|------|------------|-------------|
| **Notario (constitución)** | One-time | $1,500-$3,000 |
| **Registro Público de Comercio** | One-time | $100-$300 |
| **RFC / e.firma** | One-time/Renovación 4 años | $0 (gratis) |
| **Contador CPA (Servicios Mensuales)** | Mensual | $300-$800/mo = **$3,600-$9,600/año** |
| **PAC (CFDI Proveedor)** | Mensual | $10-$60/mo = **$120-$720/año** |
| **Software Contable** (ContPAQi, Aspel) | Anual | $600-$1,500 |
| **REPSE Registration** | Anual | $0 + tiempo contador |
| **Cuenta Bancaria Empresarial** | Mensual | $15-$35/mo = **$180-$420/año** |
| **Auditoría Externa (opcional)** | Anual | $1,500-$5,000 |
| **Legal (contracts, laboral)** | As needed | $500-$2,000 |
| **Nómina (Software si >5 empleados)** | Mensual | $50-$150/mo = **$600-$1,800/año** |
| **IMSS/INFONAVIT (por empleado)** | Mensual | ~$150-$300/empleado/mo |
| **TOTAL (Sin empleados, Bootstrap)** | **Anual** | **$6,000-$13,000** |
| **TOTAL (Con 5 empleados)** | **Anual** | **$15,000-$30,000** |

**⚠️ CRÍTICO:** Contador NO es opcional en México. Costos de $3,600-$9,600/año son **obligatorios** para compliance.

**Desglose Realista (Consultoría 100% Remota, Sin Empleados):**
- Notario (constitución año 1): **$2,000**
- Contador mensual: **$500 × 12 = $6,000**
- PAC (Facturama): **$10 × 12 = $120**
- Software contable: **$800**
- Cuenta bancaria: **$20 × 12 = $240**
- **TOTAL AÑO 1:** **~$9,200 USD**
- **TOTAL AÑO 2+:** **~$7,200 USD** (sin notario one-time)

---

## Recursos y Herramientas

### SAT (Servicio de Administración Tributaria)
- **Portal SAT:** https://www.sat.gob.mx/
- **RFC Registration:** https://www.sat.gob.mx/tramites/28753/obten-tu-rfc-con-la-clave-unica-de-registro-de-poblacion-curp
- **e.firma Solicitud:** https://www.sat.gob.mx/tramites/28523/solicita-tu-certificado-de-e-firma-portable
- **Citas SAT:** https://citas.sat.gob.mx/
- **Declaraciones (Portal):** https://www.sat.gob.mx/declaracion/
- **Buzón Tributario:** https://www.sat.gob.mx/aplicacion/login/48754/accede-a-buzon-tributario
- **Factura Electrónica (CFDI):** https://www.sat.gob.mx/consultas/92764/factura-electronica
- **Tipo de Cambio Diario:** https://www.sat.gob.mx/personas/tipo-de-cambio

### IMSS
- **Portal IMSS:** https://www.imss.gob.mx/
- **IDSE (Registro Patronal):** http://www.imss.gob.mx/patrones/idse-patron
- **SUA (Sistema Único Autodeterminación):** http://www.imss.gob.mx/patrones/sua-sistema-unico-autodeterminacion

### INFONAVIT
- **Portal INFONAVIT:** https://portalmx.infonavit.org.mx/

### STPS (Secretaría del Trabajo)
- **REPSE:** https://repse.stps.gob.mx/

### Proveedores Autorizados de Certificación (PAC)
- **Facturama:** https://www.facturama.mx/ ($199 MXN/mes)
- **Bind ERP:** https://www.bind.com.mx/ ($299-$599 MXN/mes)
- **Aspel Facture:** https://www.aspel.com.mx/mx/productos/facture ($1,200 MXN/mes)
- **ContPAQi Factura:** https://www.contpaqi.com/factura ($800 MXN/mes)

### Software Contable
- **ContPAQi Contabilidad:** $800-$1,200 USD/año - https://www.contpaqi.com/
- **Aspel COI (Contabilidad):** $600-$900 USD/año - https://www.aspel.com.mx/
- **Aspel NOI (Nómina):** $700-$1,000 USD/año
- **CONTPAQi Nóminas:** $800 USD/año

### Bancos
- **BBVA Business:** https://www.bbva.mx/empresas.html
- **Santander Business:** https://www.santander.com.mx/empresas.html
- **Banorte Business:** https://www.banorte.com/empresas/
- **Wise Business (Internacional):** https://wise.com/mx/business/

### Contadores Certificados (CPA México)
- Buscar "Contador Público Certificado" + tu ciudad
- Verificar certificación: Colegio de Contadores Públicos
- **Costo promedio:** $300-$800 USD/mes (servicios completos)

### Directorio de Notarios
- **CDMX:** https://www.consejerosjuridicos.cdmx.gob.mx/notarias
- **Jalisco:** http://www.colegiodenotariosdejal.org.mx/
- **Nuevo León:** https://www.nl.gob.mx/ (búsqueda notarios)

---

## Penalties y Consecuencias de No Compliance

| Violación | Penalidad |
|-----------|-----------|
| **No presentar ISR anual** | 20-30% del ISR omitido + recargos 1.13%/mes |
| **No presentar IVA mensual** | 0.75-1.00% del IVA omitido/mes + recargos |
| **No emitir CFDI o emitir tarde** | $3,000-$10,000 MXN (~$150-$500 USD) por comprobante |
| **No subir Contabilidad Electrónica** | $1,000-$15,000 MXN (~$50-$750 USD) |
| **No presentar DIOT** | $1,000-$15,000 MXN |
| **No registrar trabajadores en IMSS** | 2-350 veces UMA = $216-$37,800 MXN (~$10-$1,900 USD) **POR TRABAJADOR** |
| **No emitir CFDI Nómina** | $3,000-$10,000 MXN por recibo |
| **Cancelar CFDI incorrectamente** | $1,000-$5,000 MXN |
| **No renovar e.firma** | Bloqueo de buzón tributario, imposibilidad de facturar |
| **Omisión fiscal grave (>10% ingresos)** | Delito fiscal: 3 meses - 9 años de prisión |

**⚠️ MÁXIMA PENALIDAD (Delito Fiscal):**
- Omitir >$3,000,000 MXN (~$150,000 USD) en impuestos
- Pena: 3-9 años de prisión + multa 100% del impuesto omitido

---

## Consideraciones Especiales para Empresas Extranjeras

### 1. Establecimiento Permanente (EP)

**¿Qué es?**
Cualquier lugar de negocios en México donde realizas actividades empresariales.

**Triggers de EP:**
- Oficina física en México
- Empleados en México
- Agente dependiente en México (vende en tu nombre)
- Obra de construcción >6 meses

**Consecuencia:**
- Si tienes EP: **Debes pagar impuestos mexicanos** sobre ingresos atribuibles al EP

**Tratado USA-México:**
- Evita doble tributación
- Define EP más estrictamente
- Servicios profesionales: NO crean EP si <183 días/año en México

**Recomendación:**
- Si Delaren LLC (USA) factura a clientes mexicanos DESDE USA (100% remoto): **NO hay EP**
- Si contratas empleados o rentas oficina en México: **SÍ hay EP** → Requiere constitución de empresa mexicana o sucursal

---

### 2. Precios de Transferencia (Transfer Pricing)

**¿Qué es?**
Obligación de documentar que transacciones entre partes relacionadas (ej: Delaren USA y Delaren México) se hacen a precios de mercado (arm's length).

**Cuándo Aplica:**
- Si Delaren USA (matriz) y Delaren México (subsidiaria) hacen transacciones:
  - Servicios entre ellas
  - Regalías, intereses
  - Préstamos

**Obligaciones:**
1. **Estudio de Precios de Transferencia:** Análisis económico demostrando precios de mercado
   - **Costo:** $3,000-$10,000 USD (consultor especializado)
   - **Frequency:** Anual

2. **Declaración Informativa:**
   - **Maestra:** Estructura del grupo corporativo
   - **Local:** Transacciones con partes relacionadas en México
   - **País por País:** Si ingresos consolidados >$12,000 millones MXN (~$600M USD)

**Penalidad por No Cumplir:**
- Multas: $150,000-$300,000 MXN (~$7,500-$15,000 USD)
- Ajuste fiscal por SAT (puede incrementar ISR adeudado)

**⚠️ RECOMENDACIÓN:** Si Delaren México es solo para facturar a clientes locales (NO transacciones con matriz USA), **Transfer Pricing NO aplica**.

---

### 3. Retención en Fuente (Withholding Tax)

**Si Empresa Mexicana Paga a Empresa Extranjera (ej: Delaren México → Proveedor USA):**

| Tipo de Pago | Tasa de Retención |
|--------------|-------------------|
| **Servicios técnicos y asistencia técnica** | 25% |
| **Regalías (uso de marca, software)** | 25% |
| **Intereses** | 10% |
| **Dividendos** | 10% |
| **Servicios digitales (Netflix, SaaS)** | 16% IVA (no retención ISR si es B2B) |

**Ejemplo:**
- Delaren México paga $10,000 USD a consultor USA por servicios técnicos
- **Retención ISR:** $10,000 × 25% = **$2,500 USD**
- Pago neto a consultor: $7,500 USD
- Delaren México entrega $2,500 al SAT

**Tratado USA-México:**
- Puede reducir tasas (ej: regalías 10% en vez de 25%)
- Requiere Certificado de Residencia Fiscal del proveedor USA (IRS Form 6166)

**Obligación:**
- Emitir Constancia de Retención al proveedor extranjero (CFDI de Retenciones)

---

## Próximos Pasos (Action Items)

### Mes 1 (Enero 2026)

#### Si aún NO has constituido empresa:
- [ ] Contratar abogado/contador mexicano (research 3 opciones, $1,500-$3,000 USD)
- [ ] Decidir estructura: SA de CV vs. S de RL (recomendación: SA de CV)
- [ ] Preparar documentos para notario:
  - Identificaciones oficiales de socios
  - CURP de socios
  - Comprobante de domicilio (empresa y socios)
- [ ] Agendar cita con notario público
- [ ] Definir capital social inicial (mínimo $3,000 MXN recomendado, pero puede ser $1 MXN legal)

#### Si ya constituiste:
- [ ] Verificar RFC activo (Constancia de Situación Fiscal)
- [ ] Agendar cita SAT para e.firma (https://citas.sat.gob.mx/)
- [ ] Contratar contador mensual ($300-$800 USD/mes)
- [ ] Contratar PAC (Facturama $199 MXN/mes recomendado)
- [ ] Abrir cuenta bancaria empresarial (BBVA o Banorte)

### Mes 2 (Febrero 2026)
- [ ] Obtener e.firma presencial en SAT
- [ ] Setup software contable con contador (ContPAQi o Aspel)
- [ ] Emitir primer CFDI de prueba
- [ ] Registrar en REPSE (si aplica a tus servicios)
- [ ] Primera declaración ISR/IVA mensual (día 17)

### Mes 3 (Marzo 2026)
- [ ] Presentar contabilidad electrónica (balanza, día 25)
- [ ] Validar proceso mensual con contador (ISR, IVA, DIOT)
- [ ] Si contrataste empleados: Registrar en IMSS (dentro de 5 días)
- [ ] Preparar para declaración anual 2025 (si aplicable, deadline 31 marzo)

### Mes 4-12 (Operación Continua)
- [ ] Ciclo mensual día 17: ISR, IVA, DIOT
- [ ] Ciclo mensual día 25: Contabilidad electrónica
- [ ] Emitir CFDI dentro de 72h de cada transacción
- [ ] Revisar trimestral con contador (cumplimiento, optimización fiscal)

---

**Última Actualización:** 2 de enero, 2026
**Próxima Revisión:** 31 de marzo, 2026 (Post declaración anual)
**Jurisdicción:** México (Federal + Estatal)
**Disclaimer:** Este documento es informativo. México tiene uno de los sistemas fiscales MÁS COMPLEJOS del mundo. Consulta OBLIGATORIAMENTE con contador público certificado mexicano para compliance específico a tu caso. NO intentes cumplir solo (DIY) - el riesgo de penalidades es EXTREMADAMENTE ALTO.

---

**🚨 RECORDATORIO FINAL:**
En México, **NO es opcional** contratar contador. El sistema CFDI + Contabilidad Electrónica + múltiples declaraciones mensuales hace **IMPOSIBLE** el cumplimiento DIY. Presupuesto mínimo anual: **$6,000-$9,000 USD** en servicios contables profesionales.
