# Cumplimiento Fiscal México - Guía Completa 2026

**Delaren Consulting LLC - Operaciones en México**
**Tipo de Negocio:** Consultoría y servicios profesionales (100% remoto)
**Última Actualización:** 3 de enero, 2026

---

## Resumen Ejecutivo

Esta guía cubre todos los requisitos fiscales mexicanos para operar un negocio de consultoría. Aunque Delaren Consulting LLC es una entidad de Wyoming (USA), si prestas servicios desde México o a clientes mexicanos, pueden aplicar obligaciones fiscales mexicanas.

**NOTA CRÍTICA:** La complejidad del sistema fiscal mexicano (especialmente CFDI 4.0 y contabilidad electrónica) hace **obligatorio** contratar un contador certificado. No es recomendable DIY.

### Costos Estimados de Compliance Anual (México)
- **Contador (mensual):** $400-$800 USD/mes = **$4,800-$9,600/año**
- **PAC (facturación electrónica):** $50-$200 USD/mes = **$600-$2,400/año**
- **Notario (incorporación one-time):** $1,500-$3,000 USD
- **Software contable:** $50-$150 USD/mes = **$600-$1,800/año**
- **REPSE (si aplica):** $100-$300 USD one-time
- **TOTAL ANUAL:** **$6,000-$14,000 USD**

**Comparación con Wyoming LLC:** México es **6-14x más costoso** en compliance que Wyoming ($700-$1,000/año).

---

## 1. RFC (Registro Federal de Contribuyentes)

### ¿Qué es?
El RFC es el identificador fiscal único en México, equivalente al EIN en USA. Formato de 13 caracteres para personas morales (empresas) o 13 caracteres para personas físicas con actividad empresarial.

**Formato:**
- **Persona Moral:** ABC123456XYZ (ejemplo: DEL150723GH4)
- **Persona Física:** AAAA######XXX (basado en nombre y fecha de nacimiento)

### ¿Quién necesita RFC?
- Todas las personas físicas con actividad empresarial
- Todas las personas morales (SA de CV, S de RL, etc.)
- Extranjeros con establecimiento permanente en México
- Residentes fiscales mexicanos (viven >183 días/año en México)

### Documentos Requeridos (Persona Física con Actividad Empresarial)
- CURP (Clave Única de Registro de Población)
- Acta de nacimiento
- Comprobante de domicilio (recibo luz/agua/teléfono no mayor a 3 meses)
- Identificación oficial (INE/pasaporte)
- Comprobante de correo electrónico

### Documentos Requeridos (Persona Moral - SA de CV)
- Acta constitutiva protocolizada ante notario
- Poder notarial del representante legal
- CURP y RFC del representante legal
- Comprobante de domicilio fiscal
- Cédula de identificación fiscal (si ya existe)

### Proceso de Registro

#### Opción A: En línea (solo renovaciones o personas físicas simples)
- Portal: https://www.sat.gob.mx/tramites/16703/obten-tu-rfc-con-la-clave-unica-de-registro-de-poblacion-(curp)
- Tiempo: 20-30 minutos
- Requiere: CURP, e.firma (si ya la tienes)

#### Opción B: Presencial en oficina del SAT (recomendado para personas morales)
- Agendar cita: https://citas.sat.gob.mx/
- Llevar documentos originales y copias
- Tiempo: 1-2 horas en oficina
- Emisión inmediata de Cédula de Identificación Fiscal

### Costo
**$0 pesos** (trámite gratuito)

### Deadline
- Personas morales: Dentro del **primer mes** de inicio de operaciones
- Personas físicas: Antes de emitir primera factura

### Penalidades por No Inscripción
- Multa de $3,000 a $10,000 pesos
- Imposibilidad de emitir facturas (CFDIs)
- Imposibilidad de deducir gastos
- Operación ilegal del negocio

### Recursos Oficiales
- Portal SAT RFC: https://www.sat.gob.mx/tramites/operacion/28753/obten-tu-rfc-con-la-clave-unica-de-registro-de-poblacion-curp
- Citas SAT: https://citas.sat.gob.mx/

---

## 2. e.firma / FIEL (Firma Electrónica Avanzada)

### ¿Qué es?
La e.firma (antes conocida como FIEL) es la firma electrónica avanzada del SAT, equivalente digital de una firma autógrafa. Es **obligatoria** para prácticamente todos los trámites fiscales electrónicos.

### Usos de la e.firma
- Presentar declaraciones fiscales (ISR, IVA, DIOT)
- Firmar facturas electrónicas (CFDIs)
- Consultar información en el portal del SAT
- Subir contabilidad electrónica
- Trámites en línea con el SAT

### Componentes
1. **Certificado digital (.cer)** - Clave pública
2. **Clave privada (.key)** - Archivo encriptado
3. **Contraseña** - Para usar la clave privada

### Proceso de Obtención

#### Paso 1: Generar solicitud
- Software: Certifica del SAT (Windows/Mac/Linux)
- Descarga: https://www.sat.gob.mx/aplicacion/42150/genera-y-descarga-tu-certificado-de-e-firma-portable
- Genera archivo .req (solicitud de certificado)

#### Paso 2: Agendar cita presencial
- Portal: https://citas.sat.gob.mx/
- Tipo de trámite: "Obtención de e.firma"
- **IMPORTANTE:** Debes acudir físicamente a oficina del SAT
- Llevar USB con archivo .req generado

#### Paso 3: Recoger certificado
- Acudir a cita con documentos originales:
  - Identificación oficial (INE/pasaporte)
  - RFC
  - Comprobante de domicilio
  - USB con .req
- SAT emite certificado .cer y clave privada .key en tu USB
- Tiempo en oficina: 30-60 minutos

### Documentos Requeridos (Persona Física)
- Identificación oficial vigente (INE/pasaporte)
- RFC
- Comprobante de domicilio (no mayor a 3 meses)
- Correo electrónico

### Documentos Requeridos (Persona Moral - Representante Legal)
- Identificación oficial del representante legal
- RFC de la empresa
- Poder notarial que acredite representación legal
- Acta constitutiva
- Comprobante de domicilio fiscal

### Vigencia y Renovación
- **Vigencia:** 4 años
- **Renovación:** Se debe renovar **antes** de la fecha de vencimiento
- **Proceso:** Mismo que obtención inicial (cita presencial)
- **Consecuencia de expiración:** No puedes presentar declaraciones ni emitir facturas

### Costo
**$0 pesos** (trámite gratuito)

### Deadline
- Obtener **antes** de presentar primera declaración fiscal
- Idealmente dentro del primer mes de obtener RFC

### Penalidades
- Sin e.firma vigente: Imposible cumplir obligaciones fiscales electrónicas
- Multa por declaraciones no presentadas: $1,400-$17,000 pesos por declaración

### Seguridad
- **NUNCA** compartir archivos .key o contraseña
- Hacer backup seguro (USB encriptado, password manager)
- Si se pierde/roba: Revocar certificado inmediatamente en SAT

### Recursos Oficiales
- Solicitar e.firma: https://www.sat.gob.mx/tramites/28523/solicita-tu-certificado-de-e-firma-portable
- Renovar e.firma: https://www.sat.gob.mx/tramites/92784/renueva-tu-certificado-de-e-firma
- Citas: https://citas.sat.gob.mx/

---

## 3. ISR (Impuesto Sobre la Renta)

### ¿Qué es?
El ISR es el impuesto sobre la renta (corporate income tax) que grava las ganancias de personas físicas y morales.

### Tasa Impositiva

#### Personas Morales (SA de CV, S de RL)
- **Tasa fija:** 30% sobre utilidad fiscal
- No hay tasas progresivas, siempre 30% flat

#### Personas Físicas con Actividad Empresarial (PFAE)
- **Tasa progresiva:** 1.92% - 35% según nivel de ingresos
- Tabla anual 2026:

| Ingresos Anuales (MXN) | Tasa Marginal |
|------------------------|---------------|
| $0 - $8,952 | 1.92% |
| $8,952 - $75,984 | 6.40% |
| $75,984 - $133,536 | 10.88% |
| $133,536 - $155,229 | 16.00% |
| $155,229 - $185,852 | 17.92% |
| $185,852 - $374,837 | 21.36% |
| $374,837 - $590,795 | 23.52% |
| $590,795 - $1,127,926 | 30.00% |
| $1,127,926 - $1,503,902 | 32.00% |
| $1,503,902 - $4,511,705 | 34.00% |
| Más de $4,511,705 | 35.00% |

### Ejercicio Fiscal
- **Año calendario:** 1 de enero - 31 de diciembre
- No hay opción de fiscal year diferente

### Declaración Anual

#### Personas Morales
- **Deadline:** 31 de marzo del año siguiente
- **Formato:** Declaración Anual de Personas Morales (vía portal SAT)
- **Requiere:** Estados financieros auditados (si ingresos >$100M MXN), contabilidad electrónica al día

#### Personas Físicas
- **Deadline:** 30 de abril del año siguiente
- **Formato:** Declaración Anual de Personas Físicas (vía portal SAT)

### Pagos Provisionales (Mensuales)

#### Personas Morales
- **Frecuencia:** Mensual
- **Deadline:** Día **17 del mes siguiente**
  - Ejemplo: ISR de enero se paga antes del 17 de febrero
- **Cálculo:** (Ingresos acumulados - Deducciones acumuladas) × 30% - Pagos provisionales anteriores
- **Plataforma:** Portal SAT con e.firma

#### Personas Físicas (Actividad Empresarial)
- **Frecuencia:** Mensual
- **Deadline:** Día **17 del mes siguiente**
- **Cálculo:** Similar a personas morales, pero con tasa progresiva

### Deducciones Permitidas (Personas Morales)
- Gastos estrictamente indispensables para la actividad
- Salarios y honorarios (con CFDI y retenciones)
- Arrendamiento de oficina
- Servicios profesionales (contabilidad, legal)
- Software y herramientas de trabajo
- Viáticos y gastos de viaje (con límites)
- Depreciación de activos fijos
- Intereses por préstamos empresariales

### Deducciones NO Permitidas
- Gastos personales
- Multas y recargos fiscales
- ISR propio
- Pagos sin CFDI
- Pagos en efectivo >$2,000 pesos

### Cómo Presentar Declaraciones
1. Acceder al portal SAT: https://www.sat.gob.mx/
2. Login con RFC + e.firma o Contraseña
3. Ir a "Declaraciones" > "Presentar Declaración"
4. Seleccionar tipo de declaración (ISR mensual/anual)
5. Capturar ingresos, deducciones, retenciones
6. Calcular impuesto
7. Generar línea de captura para pago
8. Pagar en banco o portal bancario (mismo día)
9. Enviar declaración con e.firma

### Software Recomendado
- **ContPAQi:** $150-$300 USD/mes (software mexicano #1)
- **Aspel COI/NOI:** $100-$200 USD/mes
- **SAT Declaraciones:** Gratis pero muy básico
- **Tu contador:** Probablemente tiene su propio sistema

### Penalidades

| Infracción | Multa |
|------------|-------|
| No presentar declaración anual | $1,400 - $34,500 pesos |
| Presentar declaración extemporánea | $1,400 - $17,000 pesos |
| No presentar pago provisional mensual | $1,400 - $17,000 pesos |
| Datos incorrectos/omisiones | $1,400 - $34,500 pesos |
| No pagar ISR adeudado | Recargos 1.47% mensual + actualización inflacionaria |

### Recursos Oficiales
- Declaración Anual PM: https://www.sat.gob.mx/aplicacion/operacion/31274/presenta-tu-declaracion-anual-de-personas-morales
- Pagos Provisionales: https://www.sat.gob.mx/declaracion/74087/presenta-tu-declaracion-de-pagos-provisionales-de-personas-morales-del-regimen-general
- Calculadora ISR: https://www.sat.gob.mx/aplicacion/login/43824/calcula-tu-impuesto-sobre-la-renta

---

## 4. IVA (Impuesto al Valor Agregado)

### ¿Qué es?
El IVA es el impuesto al consumo (sales tax / VAT) que se cobra sobre la venta de bienes y servicios en México.

### Tasas de IVA

#### Tasa General
- **16%** en todo el país (excepto frontera)
- Aplica a la mayoría de servicios de consultoría

#### Tasa Fronteriza
- **8%** en zona fronteriza (100 km de la frontera norte)
- Aplica a bienes y servicios en esa región

#### Tasa 0% (Exentos)
- Exportación de bienes y servicios
- Alimentos básicos (leche, huevos, pan, tortillas)
- Medicinas de patente
- Libros, periódicos, revistas

#### Actividades sin IVA (No objeto)
- Venta de terrenos
- Intereses bancarios
- Seguros de vida

### IVA en Servicios de Consultoría

#### Servicios a Clientes Mexicanos (dentro de México)
- **Tasa:** 16%
- **Facturación:** Debes cobrar IVA al cliente y trasladarlo
- **Ejemplo:** Servicio $10,000 MXN + $1,600 IVA = **$11,600 MXN total**

#### Servicios a Clientes Extranjeros (exportación de servicios)
- **Tasa:** 0% (tasa 0%, no exento)
- **Requisitos para tasa 0%:**
  - Cliente reside en el extranjero
  - Servicio se aprovecha en el extranjero (no dentro de México)
  - Factura con domicilio fiscal extranjero
  - Contrato que evidencie uso en el extranjero
- **Beneficio:** No cobras IVA, pero sí puedes acreditar IVA de gastos

### IVA Acreditable (Recuperable)

**Concepto:** El IVA que pagas en tus gastos empresariales se puede recuperar (acreditar) contra el IVA que cobras a tus clientes.

**Ejemplo:**
```
IVA Cobrado (trasladado a clientes): $5,000 MXN
IVA Pagado (en gastos del negocio):   $2,000 MXN
--------------------------------------------
IVA a Pagar al SAT:                   $3,000 MXN
```

**Si IVA acreditable > IVA cobrado:**
- Tienes **saldo a favor**
- Opciones:
  1. Compensarlo contra IVA de meses siguientes
  2. Solicitar devolución al SAT (proceso 40-60 días)

### Declaración Mensual de IVA

#### Deadline
- **Día 17 del mes siguiente**
- Ejemplo: IVA de enero se declara y paga antes del **17 de febrero**

#### Proceso
1. Calcular IVA trasladado (cobrado a clientes)
2. Calcular IVA acreditable (pagado en gastos)
3. Diferencia = IVA a pagar (o saldo a favor)
4. Presentar declaración en portal SAT
5. Pagar vía portal bancario (mismo día)

#### Plataforma
- Portal SAT: https://www.sat.gob.mx/declaracion/
- Requiere: RFC + e.firma o Contraseña

### Facturación con IVA (CFDI)

**Obligatorio:**
- Todas las facturas (CFDIs) deben separar:
  - Subtotal (antes de IVA)
  - IVA trasladado (16% o 0%)
  - Total (Subtotal + IVA)

**Ejemplo CFDI:**
```
Servicio de Consultoría: $10,000.00 MXN
IVA 16%:                  $1,600.00 MXN
Total:                   $11,600.00 MXN
```

### Retención de IVA (2/3 del IVA)

**Cuando aplica:**
- Servicios profesionales prestados a **personas morales** (empresas)
- El cliente debe retener **2/3 del IVA** y enterarlo al SAT

**Ejemplo:**
```
Servicio:               $10,000 MXN
IVA 16%:                 $1,600 MXN
Retención IVA (2/3):     $1,067 MXN  (cliente retiene)
IVA a recibir (1/3):       $533 MXN  (tú recibes)
Total a cobrar:        $10,533 MXN
```

**CFDI de Retención:**
- El cliente debe emitirte un CFDI de Retenciones (tipo "Retenciones e Información de Pagos")
- Tú acreditas ese IVA retenido en tu declaración mensual

### Penalidades IVA

| Infracción | Multa |
|------------|-------|
| No presentar declaración mensual | $1,400 - $17,000 pesos |
| Presentar declaración extemporánea | $1,400 - $17,000 pesos + recargos 1.47% mensual |
| No pagar IVA adeudado | Recargos 1.47% mensual + actualización inflacionaria |
| No emitir CFDI con IVA correcto | $1,400 - $20,000 pesos por factura |

### Casos Especiales

#### Régimen de Pequeños Contribuyentes (RESICO - Régimen Simplificado de Confianza)
- Para personas físicas con ingresos <$3.5M MXN/año
- **Tasa reducida de IVA:** Algunos sectores pueden tener tratamiento preferencial
- **Declaración:** Bimestral en lugar de mensual

#### Exportación de Servicios (Tasa 0%)
- **Documentación requerida:**
  - Contrato internacional
  - Comprobante de pago desde el extranjero
  - Factura (CFDI) con "Exportación" marcada
  - Evidencia de que servicio se aprovecha fuera de México

### Recursos Oficiales
- Declaración IVA Mensual: https://www.sat.gob.mx/declaracion/74696/presenta-tu-declaracion-mensual-definitiva-de-iva
- Guía IVA: https://www.sat.gob.mx/consultas/92764/conoce-el-impuesto-al-valor-agregado
- Exportación de Servicios: https://www.sat.gob.mx/consultas/61073/exportacion-de-servicios

---

## 5. CFDI 4.0 (Comprobante Fiscal Digital por Internet)

### ¿Qué es el CFDI?
El CFDI es la **factura electrónica obligatoria** en México. Desde 2014, todas las facturas deben ser digitales, timbradas por un PAC, y cumplir con formato XML establecido por el SAT.

**Versión actual:** CFDI 4.0 (vigente desde 1 de enero de 2022)

### ¿Por qué es obligatorio?
- **Deducibilidad:** Sin CFDI, el gasto NO es deducible para ISR ni acreditable para IVA
- **Rastreabilidad:** SAT recibe copia de cada factura en tiempo real
- **Cumplimiento:** Es requisito legal para cualquier transacción de negocio a negocio (B2B)

### Tipos de CFDI

#### 1. CFDI de Ingreso
- **Uso:** Venta de bienes o servicios (factura normal)
- **Emitido por:** Proveedor/vendedor
- **Emitido a:** Cliente
- **Ejemplo:** Tu factura a un cliente por consultoría

#### 2. CFDI de Egreso (Nota de Crédito)
- **Uso:** Devoluciones, descuentos, cancelaciones
- **Emitido por:** Quien emitió el CFDI original
- **Referencia:** CFDI de Ingreso original (UUID)
- **Ejemplo:** Cancelar factura por servicio no prestado

#### 3. CFDI de Traslado
- **Uso:** Movimiento de mercancías sin transferencia de propiedad
- **Emitido por:** Quien transporta
- **Ejemplo:** No aplica para servicios de consultoría

#### 4. CFDI de Nómina
- **Uso:** Pago de salarios a empleados
- **Emitido por:** Empleador (tú, si tienes empleados)
- **Emitido a:** Cada empleado (mensual o por periodo)
- **Incluye:** Sueldo bruto, deducciones (ISR, IMSS), sueldo neto

#### 5. CFDI de Retenciones e Información de Pagos
- **Uso:** Retenciones de ISR/IVA a proveedores
- **Emitido por:** Cliente (persona moral) que retiene
- **Emitido a:** Proveedor (tú, si te retienen)
- **Ejemplo:** Cliente retuvo 10% ISR + 10.67% IVA de tu factura

#### 6. CFDI de Pago (Complemento de Pago)
- **Uso:** Acreditar que se pagó un CFDI previo
- **Emitido por:** Quien recibe el pago
- **Emitido a:** Quien pagó
- **Ejemplo:** Cliente pagó tu factura a crédito 30 días después

### PAC (Proveedor Autorizado de Certificación)

**¿Qué es?**
Los PAC son empresas autorizadas por el SAT para "timbrar" (validar y certificar) los CFDIs. Sin timbrado del PAC, la factura NO es válida.

**Proceso:**
1. Tú generas el CFDI en tu sistema (XML con datos de factura)
2. Envías XML al PAC
3. PAC valida estructura, datos, RFC, e.firma
4. PAC "timbra" el CFDI (agrega sello digital SAT + UUID único)
5. PAC regresa XML timbrado + PDF
6. Tú envías XML + PDF al cliente

**Proveedores PAC Populares:**

| PAC | Costo Mensual (USD) | Características |
|-----|---------------------|-----------------|
| **Facturama** | $50-$100 | API moderna, dashboard web, planes flexibles |
| **Bind ERP** | $100-$200 | Sistema completo (contabilidad + facturación) |
| **Aspel Facture** | $80-$150 | Software desktop + timbrado, popular en PyMEs |
| **Buzón Fiscal (SAT)** | $0 | Solo para consulta, NO para emitir |
| **Facturando.mx** | $30-$80 | Económico, bueno para freelancers |
| **SICOFI** | $50-$120 | Integración con contabilidad |

**Costos típicos:**
- **Timbres ilimitados:** $50-$200 USD/mes (más común)
- **Por timbrado:** $1-$3 MXN por CFDI (menos eficiente si emites >50/mes)

**Recomendación:** Facturama o Bind ERP (buena relación costo/funcionalidad)

### Datos Obligatorios en CFDI 4.0

#### Datos del Emisor (tú)
- RFC
- Nombre o razón social
- Régimen fiscal (ej: 612 - Personas Físicas con Actividades Empresariales)
- Código postal del domicilio fiscal

#### Datos del Receptor (cliente)
- RFC (o RFC genérico XAXX010101000 para público general)
- Nombre o razón social
- Código postal
- Régimen fiscal del receptor
- **Uso de CFDI** (clave SAT):
  - G03: Gastos en general
  - D04: Donaciones
  - P01: Por definir
  - S01: Sin efectos fiscales (honorarios)

#### Datos del Comprobante
- Folio (número consecutivo, opcional pero recomendado)
- Fecha y hora de emisión
- Forma de pago (01-Efectivo, 03-Transferencia, 99-Por definir)
- Método de pago (PUE-Pago en una sola exhibición, PPD-Pago en parcialidades)
- Moneda (MXN, USD, EUR)
- Tipo de cambio (si no es MXN)

#### Datos del Concepto (servicio/producto)
- Clave de producto/servicio SAT (ej: 80141600 - Servicios de consultoría empresarial)
- Cantidad
- Unidad de medida (E48 - Servicio, H87 - Pieza)
- Descripción del servicio
- Valor unitario
- Importe (cantidad × valor unitario)
- IVA trasladado (16%, 0%, o exento)

### Plazos para Emisión de CFDI

**Regla general:** El CFDI debe emitirse **al momento de la transacción** o máximo **72 horas después** de recibir el pago.

**Excepciones:**
- **Pago en parcialidades (PPD):** Emites CFDI al dar el servicio, luego Complemento de Pago cuando te paguen
- **Servicios continuos (retainers):** CFDI mensual al final del periodo

**IMPORTANTE:** Si emites CFDI con fecha anterior a más de 72 horas, el SAT puede rechazarlo.

### Cancelación de CFDI

#### Proceso (CFDI 4.0)
1. Solicitas cancelación en tu PAC/sistema
2. Se envía solicitud de cancelación al receptor (cliente)
3. **Cliente debe aceptar la cancelación** (tiene 72 horas para responder)
4. Si acepta: CFDI se cancela
5. Si no responde en 72 horas: Se cancela automáticamente
6. Si rechaza: No se puede cancelar (debes emitir CFDI de Egreso - nota de crédito)

#### Motivos de Cancelación (Clave SAT)
- 01: Comprobante emitido con errores con relación
- 02: Comprobante emitido con errores sin relación
- 03: No se llevó a cabo la operación
- 04: Operación nominativa relacionada con una factura global

#### Consecuencias Fiscales
- CFDI cancelado NO genera ingreso para ISR ni IVA
- Si ya declaraste ese ingreso: Debes presentar declaración complementaria

### Validación de CFDI

**Siempre valida CFDIs recibidos de proveedores:**
1. Portal SAT: https://www.sat.gob.mx/aplicacion/login/53027/verifica-el-estatus-de-un-cfdi
2. Ingresar UUID (folio fiscal) del CFDI
3. Verificar que esté "Vigente" (no cancelado)

**Datos a verificar:**
- RFC emisor correcto
- Monto correcto
- Fecha dentro del periodo fiscal
- Estado: Vigente (no cancelado)

### Almacenamiento y Conservación

**Obligatorio conservar:**
- XML timbrado (versión legal, tiene validez fiscal)
- PDF (versión para lectura humana, NO tiene validez fiscal por sí solo)

**Plazo:** **5 años** desde la fecha de emisión

**Dónde guardar:**
- Sistema del PAC (backup automático)
- Tu servidor/nube (Google Drive, Dropbox con encriptación)
- Buzón Fiscal del SAT (automático, consulta gratuita)

### Software de Facturación

#### Opción A: PAC con Sistema Integrado (recomendado)
- **Facturama:** Dashboard web + API + mobile app
- **Bind ERP:** Facturación + contabilidad + inventarios
- **Aspel Facture:** Software desktop (instalación local)

#### Opción B: Software de Contabilidad con Facturación
- **ContPAQi:** Sistema MX #1, incluye facturación + contabilidad
- **SICOFI:** Contabilidad + facturación + nómina
- **QuickBooks México:** Versión localizada con CFDI

#### Opción C: API para Desarrolladores
- **Facturama API:** Integración a tu sistema custom
- **Bind API:** Para empresas con desarrollo propio
- **Facturando.mx API:** Económica para startups

**Recomendación para Delaren Consulting:**
- **Año 1 (pocos clientes):** Facturama básico ($50/mes) + Contador hace contabilidad
- **Año 2+ (scaling):** Bind ERP ($150/mes) para integrar todo

### Penalidades CFDI

| Infracción | Multa |
|------------|-------|
| No emitir CFDI cuando es obligatorio | $1,410 - $87,890 pesos |
| Emitir CFDI con datos incorrectos | $1,410 - $20,000 pesos |
| No cancelar CFDI erróneo | $1,410 - $20,000 pesos |
| No proporcionar CFDI al cliente | $1,410 - $87,890 pesos |

### Recursos Oficiales
- Portal CFDI SAT: https://www.sat.gob.mx/consultas/92764/factura-electronica
- Validar CFDI: https://verificacfdi.facturaelectronica.sat.gob.mx/
- Catálogo de claves SAT: http://omawww.sat.gob.mx/tramitesyservicios/Paginas/catalogos_emision_cfdi_2022.htm
- Lista de PAC autorizados: https://www.sat.gob.mx/consultas/92764/lista-de-proveedores-de-certificacion-de-cfdi

---

## 6. DIOT (Declaración Informativa de Operaciones con Terceros)

### ¿Qué es?
El DIOT es un reporte mensual informativo que detalla **todas las compras y gastos** que hiciste a tus proveedores durante el mes.

**Propósito:** El SAT cruza información:
- Tú reportas que le compraste $X a Proveedor ABC
- SAT verifica que Proveedor ABC reportó ingreso de $X en su declaración de IVA

### ¿Quién debe presentar DIOT?
- **Personas morales** (empresas)
- **Personas físicas con actividad empresarial** que apliquen IVA acreditable
- **NO aplica:** Si no tienes IVA acreditable (ej: régimen de pequeños contribuyentes sin IVA)

### Información a Reportar

Por cada proveedor del mes:
- RFC del proveedor
- Nombre/razón social
- Tipo de tercero (04 - Proveedor Nacional, 05 - Proveedor Extranjero)
- Tipo de operación (03 - Servicios, 06 - Arrendamiento, etc.)
- Monto del IVA acreditable (16%, 0%, exento)
- Monto del IVA retenido
- Monto pagado sin IVA (importación, extranjeros)

### Operaciones que SE Reportan
- Compras de servicios profesionales (contabilidad, legal, desarrollo)
- Arrendamiento de oficina
- Compras de software/herramientas
- Viáticos y gastos deducibles
- Cualquier gasto con IVA acreditable

### Operaciones que NO SE Reportan
- Gastos sin IVA (salarios, IMSS, intereses)
- Importaciones (se reportan por separado)
- Tus ventas (solo compras se reportan en DIOT)

### Deadline
- **Día 17 del mes siguiente**
- Ejemplo: DIOT de enero se presenta antes del **17 de febrero**

### Proceso de Presentación

#### Paso 1: Generar archivo DIOT
- **Software:** Tu sistema contable (ContPAQi, Aspel, Bind) genera archivo .txt
- **Formato:** Layout específico del SAT (A-29)
- **Contenido:** Lista de proveedores con totales de compras

#### Paso 2: Subir al SAT
1. Portal SAT: https://www.sat.gob.mx/declaracion/
2. Login con RFC + e.firma
3. Declaraciones > Informativas > DIOT
4. Subir archivo .txt generado
5. Validar (el SAT revisa errores de formato)
6. Enviar

#### Paso 3: Recibir acuse
- SAT genera acuse de recibo
- Guardar acuse por 5 años

### Casos Especiales

#### Sin operaciones en el mes
- **NO** estás obligado a presentar DIOT "en ceros"
- Solo presentas si hubo compras

#### Proveedores extranjeros
- Reportar como tipo de tercero "05 - Proveedor Extranjero"
- No hay IVA acreditable (IVA es impuesto nacional)
- Puede haber retención de ISR si aplica

### Software Recomendado
- **ContPAQi:** Genera DIOT automáticamente
- **Aspel NOI:** Módulo DIOT incluido
- **Bind ERP:** Generación automática desde contabilidad
- **Excel + Validador SAT:** Menos recomendado (propenso a errores)

### Penalidades DIOT

| Infracción | Multa |
|------------|-------|
| No presentar DIOT | $1,410 - $35,250 pesos |
| Presentar DIOT extemporánea | $1,410 - $35,250 pesos |
| Datos incorrectos u omisiones | $1,410 - $35,250 pesos |

### Recursos Oficiales
- Guía DIOT: https://www.sat.gob.mx/declaracion/74957/presenta-tu-declaracion-informativa-de-operaciones-con-terceros--diot-
- Layout A-29 (formato): http://omawww.sat.gob.mx/fichas_tematicas/declaraciones_informativas/Documents/diot_anexo_a29.pdf

---

## 7. Contabilidad Electrónica

### ¿Qué es?
La Contabilidad Electrónica es la obligación de llevar tu contabilidad en formato digital XML y enviar mensualmente:
1. **Catálogo de Cuentas** (chart of accounts)
2. **Balanza de Comprobación** (trial balance)

al portal del SAT.

**Vigente desde:** 2015 (Personas Morales), 2016 (Personas Físicas)

### ¿Quién debe llevar Contabilidad Electrónica?
- **Personas Morales** (SA de CV, S de RL): SÍ, obligatorio
- **Personas Físicas con Actividad Empresarial**: SÍ, obligatorio (con excepciones)
- **Régimen Simplificado de Confianza (RESICO)**: NO obligados si ingresos <$3.5M MXN/año

### Componentes de la Contabilidad Electrónica

#### 1. Catálogo de Cuentas (Chart of Accounts)

**¿Qué es?**
Lista de todas las cuentas contables que usas para clasificar ingresos, gastos, activos, pasivos.

**Estructura:**
- Debe basarse en el **Código Agrupador SAT** (catálogo estandarizado)
- Ejemplo:
  - 100.00.00 - Activo
    - 101.00.00 - Activo Circulante
      - 101.01.00 - Caja y Bancos
        - 101.01.01 - Banco Santander Cuenta 1234

**Deadline de envío:**
- **Primera vez:** Dentro del **primer mes** de inicio de operaciones
- **Actualizaciones:** Cuando agregues/modifiques cuentas (envío en la Balanza del mes)

**Formato:**
- XML con estructura SAT (layout específico)
- Tu software contable lo genera automáticamente

#### 2. Balanza de Comprobación (Trial Balance)

**¿Qué es?**
Reporte mensual de **todos los movimientos contables** del mes, mostrando saldos iniciales, movimientos, y saldos finales de cada cuenta.

**Contenido:**
- Todas las pólizas contables del mes
- Saldo inicial de cada cuenta
- Cargos (débitos) del mes
- Abonos (créditos) del mes
- Saldo final de cada cuenta

**Deadline de envío:**
- **Día 25 del mes siguiente** (antes del día 17 era para declaraciones de impuestos)
- Ejemplo: Balanza de enero se envía antes del **25 de febrero**

**Formato:**
- XML con estructura SAT (layout específico)

#### 3. Pólizas del Periodo (opcional, solo si el SAT lo solicita)

**¿Qué es?**
Detalle completo de cada transacción contable (póliza de ingresos, egresos, diario).

**Envío:**
- **NO se envían mensualmente de forma automática**
- Solo si el SAT te audita y solicita en forma oficial

### Proceso de Envío

#### Paso 1: Registro contable mensual
- Tu contador registra todas las operaciones del mes
- Clasifica ingresos/gastos en cuentas del Catálogo
- Genera pólizas contables (con soporte de CFDIs)

#### Paso 2: Generación de XML
- Software contable genera:
  - Catálogo de Cuentas XML (si es primera vez o hay cambios)
  - Balanza de Comprobación XML

#### Paso 3: Envío al SAT
1. Portal SAT: https://www.sat.gob.mx/aplicacion/login/51825/envia-tu-contabilidad-electronica
2. Login con RFC + e.firma
3. Subir archivo XML de Balanza
4. Validar (SAT revisa errores de formato/estructura)
5. Enviar

#### Paso 4: Acuse
- SAT genera acuse de recibo con folio
- Guardar acuse por 5 años

### Reglas de Registro Contable

#### Todas las pólizas deben tener:
- Número de póliza consecutivo
- Fecha de la operación
- Cuenta(s) contable(s) afectada(s)
- Descripción de la operación
- **UUID del CFDI relacionado** (obligatorio si la operación tiene factura)

**CRÍTICO:** Cada gasto/ingreso debe estar respaldado por un CFDI. Sin CFDI, no es deducible.

### Software de Contabilidad Electrónica

| Software | Costo Mensual (USD) | Características |
|----------|---------------------|-----------------|
| **ContPAQi** | $150-$300 | #1 en México, genera todo automáticamente |
| **Aspel NOI** | $100-$200 | Muy popular en PyMEs, instalación local |
| **Bind ERP** | $150-$250 | Nube, incluye facturación + contabilidad |
| **SICOFI** | $80-$150 | Bueno para consultores, incluye nómina |
| **SAT Mis Cuentas** | $0 | Herramienta básica del SAT (no recomendada) |

**RECOMENDACIÓN:** **NO** intentes hacer contabilidad electrónica tú mismo. Contrata contador certificado.

### Penalidades Contabilidad Electrónica

| Infracción | Multa |
|------------|-------|
| No enviar Catálogo de Cuentas | $1,410 - $35,250 pesos |
| No enviar Balanza de Comprobación | $1,410 - $35,250 pesos |
| Enviar Balanza extemporánea | $1,410 - $17,630 pesos |
| Datos incorrectos en contabilidad | $1,410 - $35,250 pesos |
| No conservar contabilidad por 5 años | $1,410 - $35,250 pesos |

### Recursos Oficiales
- Contabilidad Electrónica: https://www.sat.gob.mx/aplicacion/login/51825/envia-tu-contabilidad-electronica
- Catálogo de Cuentas SAT: http://omawww.sat.gob.mx/fichas_tematicas/contabilidad_electronica/Documents/catalogo_cuentas.pdf
- Layout Balanza XML: http://omawww.sat.gob.mx/fichas_tematicas/contabilidad_electronica/Paginas/documentos_tecnicos.aspx

---

## 8. REPSE (Registro de Prestadoras de Servicios Especializados)

### ¿Qué es?
El REPSE es un registro obligatorio ante la Secretaría del Trabajo y Previsión Social (STPS) para empresas que prestan "servicios especializados" a otras empresas.

**Objetivo:** Combatir subcontratación ilegal (outsourcing) y garantizar derechos laborales.

### ¿Cuándo Aplica REPSE?

#### Servicios Especializados (SÍ aplica)
- Consultoría empresarial
- Desarrollo de software
- Marketing digital
- Contabilidad y auditoría
- Servicios legales
- Recursos humanos
- Diseño gráfico
- Cualquier servicio B2B no relacionado con la actividad principal del cliente

#### Servicios NO Especializados (NO aplica)
- Venta de productos
- Servicios al consumidor final (B2C)
- Servicios ocasionales sin relación laboral

**Para Delaren Consulting:** **SÍ aplica** si prestas servicios de consultoría/desarrollo/marketing a empresas mexicanas.

### Requisitos para Obtener REPSE

#### Persona Moral (SA de CV, S de RL)
- Acta constitutiva protocolizada
- RFC
- e.firma vigente
- Comprobante de domicilio fiscal
- Cumplimiento de obligaciones fiscales (opinión de cumplimiento SAT)
- Cumplimiento de obligaciones IMSS (opinión de cumplimiento IMSS)

#### Persona Física con Actividad Empresarial
- RFC
- e.firma vigente
- Comprobante de domicilio
- Opinión de cumplimiento SAT
- Opinión de cumplimiento IMSS (si tienes empleados)

### Proceso de Registro REPSE

#### Paso 1: Obtener opinión de cumplimiento
1. **SAT:** Solicitar en portal SAT (32D - opinión cumplimiento)
2. **IMSS:** Solicitar en portal IMSS (si tienes empleados)
   - Si no tienes empleados: Declarar "sin trabajadores"

#### Paso 2: Registro en REPSE
1. Portal: https://repse.stps.gob.mx/
2. Login con e.firma
3. Llenar solicitud de registro
4. Adjuntar documentos:
   - Acta constitutiva (PDF)
   - Opinión cumplimiento SAT (PDF)
   - Opinión cumplimiento IMSS o escrito de no trabajadores (PDF)
5. Enviar solicitud

#### Paso 3: Revisión STPS
- STPS revisa documentos (10-15 días hábiles)
- Si aprueba: Emite **Folio REPSE** (número de registro único)
- Si rechaza: Corregir y reenviar

#### Paso 4: Obtener constancia
- Descargar **Constancia de Registro REPSE** (PDF con folio)
- Válida por **3 años**

### Renovación
- **Cada 3 años** antes del vencimiento
- Proceso similar a registro inicial
- Renovar opiniones de cumplimiento SAT/IMSS

### Costo
- **$0 pesos** (trámite gratuito ante STPS)
- Costo indirecto: Tiempo del contador para preparar documentos ($100-$300 USD)

### Deadline
- **Antes** de prestar primer servicio especializado
- Si ya estás prestando servicios: Regularizar **inmediatamente**

### Consecuencias de NO tener REPSE

#### Para ti (proveedor)
- Multa de **$250-$5,000 veces UMA** ($27,000-$540,000 pesos aprox)
- Clausura del negocio
- Impedimento para contratar con empresas formales

#### Para tu cliente
- No puede deducir tus facturas si no tienes REPSE vigente
- Multa de **250-5,000 veces UMA** por contratar sin validar REPSE

**Por eso:** Clientes corporativos serios **siempre** piden tu Folio REPSE antes de contratarte.

### Uso del Folio REPSE

#### En CFDIs (Facturas)
- **Obligatorio** incluir Folio REPSE en facturas de servicios especializados
- Campo específico en CFDI 4.0: "REPSE" (dentro del complemento de servicios)

#### En Contratos
- Incluir Folio REPSE en contrato de servicios
- Cliente lo necesita para validar que eres proveedor legal

### Validación de REPSE

**Clientes pueden validar tu REPSE:**
1. Portal REPSE: https://repse.stps.gob.mx/
2. Consulta Pública > Validar Registro
3. Ingresar tu RFC o Folio REPSE
4. Ver estatus (Vigente/Vencido/Cancelado)

### Excepciones (NO requieren REPSE)

- **Servicios ocasionales:** Una sola vez, sin continuidad
- **Freelancers sin estructura empresarial:** Discutible, pero STPS recomienda tramitarlo igual
- **Servicios B2C:** No son "especializados" según la ley

### Recursos Oficiales
- Portal REPSE: https://repse.stps.gob.mx/
- Guía de Registro: https://www.gob.mx/stps/acciones-y-programas/registro-de-prestadoras-de-servicios-especializados-u-obras-especializadas-repse
- Consulta Pública REPSE: https://repse.stps.gob.mx/ConsultaPublica

---

## 9. Obligaciones Estatales y Municipales

### Impuesto Sobre Nómina (Estatal)

#### ¿Qué es?
Impuesto estatal sobre los salarios pagados a empleados. **Solo aplica si tienes empleados en nómina.**

#### Tasa por Estado (ejemplos 2026)
| Estado | Tasa |
|--------|------|
| Ciudad de México | 3% |
| Estado de México | 3% |
| Jalisco (Guadalajara) | 2.5% |
| Nuevo León (Monterrey) | 3% |
| Querétaro | 2.5% |
| Guanajuato | 2% |
| Puebla | 3% |

#### Cálculo
```
Nómina Mensual Total: $50,000 MXN
Tasa (CDMX): 3%
Impuesto Sobre Nómina: $50,000 × 0.03 = $1,500 MXN
```

#### Deadline
- **Mensual:** Día 17 del mes siguiente (varía por estado)
- **Anual:** Declaración informativa anual

#### Exenciones
- Si NO tienes empleados: **No aplica**
- Algunos estados exentan primer año o primeros X empleados

#### Plataforma de Pago
- Portal de finanzas del estado (cada estado tiene su propio sistema)
- Ejemplo CDMX: https://oficinavirtual.cdmx.gob.mx/

### Licencia Municipal de Funcionamiento

#### ¿Qué es?
Permiso municipal para operar un negocio en una ubicación física.

#### ¿Cuándo aplica?
- **SÍ aplica:** Si tienes oficina física, local, o estableci miento
- **NO aplica:** Si trabajas 100% remoto desde tu domicilio particular (uso residencial)

#### Costo
- Varía por municipio: $500-$5,000 pesos
- Depende de giro, tamaño, ubicación

#### Proceso
1. Solicitud ante municipio
2. Inspección de protección civil (si aplica)
3. Pago de derechos
4. Emisión de licencia

#### Para Delaren Consulting (100% remoto)
- **NO necesario** si no tienes oficina física ni recibes clientes en domicilio
- Si eventualmente rentas oficina: Tramitar licencia en ese momento

---

## 10. Obligaciones Laborales (IMSS, INFONAVIT, SAR)

**IMPORTANTE:** Solo aplica **si tienes empleados**. Si eres solo tú (owner) o solo contratas freelancers por honorarios, NO aplica.

### IMSS (Instituto Mexicano del Seguro Social)

#### ¿Qué es?
Seguro social obligatorio para empleados que cubre:
- Seguro de enfermedades y maternidad
- Seguro de riesgos de trabajo
- Seguro de invalidez y vida
- Seguro de retiro, cesantía y vejez
- Seguro de guarderías y prestaciones sociales

#### ¿Cuándo aplica?
- **SÍ aplica:** Si contratas empleados con relación laboral (nómina)
- **NO aplica:** Si contratas por honorarios (freelancers con factura)

#### Registro
- **Deadline:** Dentro de **5 días hábiles** de la fecha de contratación del empleado
- **Cómo:** Portal IMSS Digital o IMSS desde su empresa (IDSE)
- **Plataforma:** https://www.imss.gob.mx/imssdigital

#### Cuotas IMSS (Porcentaje sobre Salario Base de Cotización)

**Aportación Patronal (Empleador):**
- **Enfermedad y Maternidad:** ~20.40%
- **Riesgos de Trabajo:** 0.5% - 15% (según actividad)
- **Invalidez y Vida:** 1.75%
- **Retiro:** 2%
- **Cesantía y Vejez:** 3.15%
- **Guarderías:** 1%
- **INFONAVIT:** 5%

**TOTAL Aprox:** **25-30%** del salario bruto del empleado

**Aportación Obrera (Empleado):**
- **Enfermedad y Maternidad:** ~0.40%
- **Invalidez y Vida:** 0.625%
- **Cesantía y Vejez:** 1.125%

**TOTAL Aprox:** **2-3%** del salario bruto (retenido de nómina)

#### Ejemplo Práctico
```
Salario Mensual Empleado: $15,000 MXN
Aportación Patronal (28%): $4,200 MXN
Aportación Obrera (2.5%):    $375 MXN (retenida de nómina)
Costo total para employer: $15,000 + $4,200 = $19,200 MXN
Empleado recibe (antes ISR): $15,000 - $375 = $14,625 MXN
```

#### Pago de Cuotas
- **Bimestral:** Cada 2 meses (17 del mes siguiente al bimestre)
- **Plataforma:** SUA (Sistema Único de Autodeterminación) o portal IMSS

#### Penalidades IMSS
- No registrar empleado: **2 a 350 veces UMA** ($216-$37,800 pesos) **POR EMPLEADO**
- No pagar cuotas: Recargos + multas + posible demanda laboral
- **GRAVE:** El IMSS es muy estricto, auditorías frecuentes

### INFONAVIT (Instituto del Fondo Nacional de la Vivienda para los Trabajadores)

#### ¿Qué es?
Fondo de vivienda para empleados, permite créditos hipotecarios.

#### Aportación
- **5%** del salario base de cotización
- **100% patronal** (empleador paga, empleado no aporta)

#### Registro y Pago
- Se hace junto con IMSS (mismo proceso)
- Pago bimestral vía SUA

### SAR (Sistema de Ahorro para el Retiro)

#### ¿Qué es?
Cuenta individual de retiro para empleados (similar a 401k USA).

#### Aportación
- **Retiro:** 2% (patronal)
- **Cesantía y Vejez:** 3.15% (patronal) + 1.125% (obrero)
- **TOTAL:** ~6.3% aprox.

#### Administración
- AFORE (Administradora de Fondos para el Retiro) elegida por empleado
- Aportaciones se pagan vía SUA junto con IMSS

### CFDI de Nómina (Facturación de Salarios)

#### Obligatorio
- **Desde 2014:** Todos los salarios deben emitirse como **CFDI de Nómina**
- Incluye: Salario bruto, deducciones (ISR, IMSS obrero), salario neto

#### Contenido CFDI de Nómina
- Datos del empleado (RFC, CURP, número IMSS)
- Percepciones (sueldo, bonos, horas extra)
- Deducciones (ISR retenido, IMSS obrero)
- Neto a pagar

#### Emisión
- **Frecuencia:** Por cada periodo de pago (semanal, quincenal, mensual)
- **PAC:** Mismo PAC que tus facturas de servicios
- **Software:** ContPAQi Nóminas, Aspel NOI, Bind (módulo nómina)

### ISR sobre Salarios (Retención)

#### Tasa Progresiva (misma que personas físicas)
- 1.92% a 35% según tabla anual
- Empleador **retiene** ISR de cada nómina
- Empleador **entera** (paga) ISR al SAT mensualmente

#### Pago
- **Mensual:** Día 17 del mes siguiente
- **Declaración:** Vía portal SAT (Declaración de retenciones)

#### Anual
- Cálculo anual del ISR (diciembre/enero)
- Si reteniste de más: Devolución al empleado
- Si reteniste de menos: Empleado paga diferencia en su declaración anual

### Alternativa: Contratar por Honorarios (Freelancers)

**Ventajas:**
- **NO** pagas IMSS, INFONAVIT, SAR (el freelancer paga sus propios impuestos)
- **NO** emites CFDI de Nómina (freelancer te emite factura de honorarios)
- Costo: Solo honorarios + IVA (si aplica)

**Desventajas:**
- Freelancer no tiene prestaciones (vacaciones, aguinaldo, IMSS)
- Relación más inestable
- SAT puede reclasificar como empleado si hay subordinación/horario fijo

**Recomendación para Delaren Consulting (Primer año):**
- Contratar por **honorarios** (freelancers) para evitar carga IMSS
- Si scaling y necesitas empleados fijos: Contratar nómina en Año 2+

---

## 11. Constitución de Empresa en México

### Tipos de Entidades

#### Persona Física con Actividad Empresarial (PFAE)
**Estructura:**
- Tú como persona física eres el negocio
- Responsabilidad ilimitada (tus bienes personales en riesgo)

**Ventajas:**
- Fácil de registrar (solo RFC + e.firma)
- Costos bajos ($0 constitución)
- Menos complejidad contable

**Desventajas:**
- Responsabilidad ilimitada
- Menos credibilidad con clientes enterprise
- Impuestos progresivos (hasta 35%)

**Recomendado para:**
- Freelancers, consultores independientes
- Ingresos <$1M MXN/año

#### Sociedad Anónima de Capital Variable (SA de CV)
**Estructura:**
- Sociedad de accionistas
- Responsabilidad limitada al capital aportado
- Requiere mínimo 2 accionistas (pueden ser familiares)
- Capital mínimo: $50,000 pesos (25% exhibido al constituir)

**Ventajas:**
- Responsabilidad limitada (asset protection)
- Credibilidad corporativa
- Facilita inversión externa

**Desventajas:**
- Costo alto de constitución ($1,500-$3,000 USD notario)
- Más complejidad contable y legal
- Obligaciones corporativas (asamblea de accionistas, libros corporativos)

**Recomendado para:**
- Negocios con múltiples socios
- Empresas que buscan inversión
- Ingresos >$2M MXN/año

#### Sociedad de Responsabilidad Limitada (S de RL)
**Estructura:**
- Sociedad de socios (no accionistas)
- Responsabilidad limitada al capital aportado
- Mínimo 2 socios, máximo 50
- No hay capital mínimo legal

**Ventajas:**
- Responsabilidad limitada
- Menos formalidades que SA de CV (no requiere asamblea formal)
- Flexible para pequeños negocios

**Desventajas:**
- Difícil transferir participación (requiere consentimiento socios)
- Menos atractiva para inversionistas
- Costo notario similar a SA de CV

**Recomendado para:**
- Pequeños negocios con 2-5 socios
- Operación familiar
- Ingresos $500k-$2M MXN/año

### Proceso de Constitución (SA de CV / S de RL)

#### Paso 1: Permiso de uso de denominación social
- Solicitar ante Secretaría de Economía
- Verificar que el nombre de tu empresa no esté registrado
- Portal: https://www.gob.mx/se/
- Costo: ~$500 pesos
- Tiempo: 1-2 días

#### Paso 2: Elaboración de Estatutos Sociales
- Contratar notario público
- Redactar acta constitutiva (estatutos):
  - Nombre de la sociedad
  - Objeto social (actividad del negocio)
  - Domicilio fiscal
  - Capital social
  - Socios/accionistas y porcentajes
  - Administración (consejo, director, etc.)
- Notario revisa y prepara acta

#### Paso 3: Protocolización ante Notario
- Firma del acta constitutiva ante notario público
- Todos los socios/accionistas deben estar presentes (o dar poder)
- Notario protocoliza (inscribe en su libro de actas)

#### Paso 4: Inscripción en Registro Público de Comercio
- Notario tramita inscripción (usualmente incluido en su fee)
- Registro Público valida y registra
- Tiempo: 5-10 días

#### Paso 5: Obtención de RFC
- Con acta constitutiva protocolizada, registrar RFC ante SAT
- Proceso descrito en sección 1 (RFC)

#### Paso 6: Obtención de e.firma
- Proceso descrito en sección 2 (e.firma)

### Costos de Constitución (2026)

| Ítem | Costo (USD) |
|------|-------------|
| **Permiso denominación social** | $25-$50 |
| **Notario Público** | $1,500-$3,000 |
| **Registro Público de Comercio** | Incluido en notario |
| **RFC** | $0 |
| **e.firma** | $0 |
| **TOTAL** | **$1,525-$3,050** |

**Tiempo total:** 15-30 días desde inicio hasta tener RFC y e.firma

### Notario Público

**Rol:**
- Fedatario público que da fe pública a acta constitutiva
- Obligatorio por ley mexicana (no puedes constituir sin notario)

**Cómo elegir notario:**
- Buscar "notario público [tu ciudad]"
- Pedir recomendaciones a tu contador/abogado
- Comparar fees (varía mucho por zona/notario)

**Documentos que notario entrega:**
- Acta constitutiva protocolizada (escritura pública)
- Inscripción en Registro Público de Comercio
- Copias certificadas (necesarias para RFC, bancos)

### Alternativa: Operar como Persona Física desde LLC Wyoming

**Escenario:**
- Tienes Delaren Consulting LLC (Wyoming)
- Operas desde México como persona física freelancer
- Emites facturas como Persona Física con Actividad Empresarial (no como LLC)

**Ventajas:**
- Evitas costos de constitución en México ($1,500-$3,000)
- Evitas complejidad de entidad mexicana
- Mantienes flexibilidad

**Desventajas:**
- No puedes emitir facturas a nombre de LLC desde México (SAT requiere RFC mexicano)
- Clientes mexicanos necesitan factura mexicana (CFDI)

**Recomendación:**
- **Año 1:** Operar como Persona Física Mexicana + tener LLC Wyoming para clientes USA
- **Año 2+:** Evaluar si vale la pena constituir SA de CV en México (si >60% clientes son mexicanos)

---

## 12. Costos de Compliance Anual (Resumen 2026)

### Escenario A: Persona Física con Actividad Empresarial (PFAE)

| Ítem | Frecuencia | Costo (USD/año) |
|------|------------|-----------------|
| **Contador (mensual)** | 12 meses | $4,800-$9,600 |
| **PAC (facturación)** | 12 meses | $600-$2,400 |
| **Software contable** | 12 meses | $600-$1,800 |
| **REPSE (si aplica)** | One-time/renovación 3 años | $100-$300 |
| **e.firma renovación** | Cada 4 años | $0 |
| **TOTAL ANUAL** | - | **$6,100-$14,100** |

**Promedio:** $10,000 USD/año

### Escenario B: Sociedad Anónima (SA de CV)

| Ítem | Frecuencia | Costo (USD/año) |
|------|------------|-----------------|
| **Constitución notario** | One-time | $1,500-$3,000 |
| **Contador (mensual)** | 12 meses | $6,000-$12,000 |
| **PAC (facturación)** | 12 meses | $600-$2,400 |
| **Software contable** | 12 meses | $600-$1,800 |
| **Auditoría anual** (si ingresos >$100M MXN) | Anual | $2,000-$5,000 |
| **REPSE** | Renovación 3 años | $100-$300 |
| **Asamblea anual** | Anual | $200-$500 |
| **TOTAL AÑO 1** | - | **$10,000-$25,000** |
| **TOTAL AÑOS SUBSECUENTES** | - | **$9,500-$22,000** |

**Promedio:** $15,000-$20,000 USD/año

### Comparación con Wyoming LLC

| Concepto | Wyoming LLC | México PFAE | México SA de CV |
|----------|-------------|-------------|-----------------|
| **Constitución** | $0-$500 | $0 | $1,500-$3,000 |
| **Compliance Anual** | $700-$1,000 | $6,100-$14,100 | $9,500-$22,000 |
| **Contador** | $500-$1,500 | $4,800-$9,600 | $6,000-$12,000 |
| **Complejidad** | Baja | Alta | Muy Alta |
| **Recomendado si...** | Clientes USA | Clientes MX, ingresos <$1M | Clientes MX, ingresos >$2M |

### Recomendación Estratégica para Delaren Consulting

**Año 1 (2026):**
- **Wyoming LLC:** Para clientes USA/internacionales (mantener)
- **Persona Física México:** Para clientes mexicanos (RFC + e.firma)
- **Costo total:** ~$7,000-$11,000 USD/año (ambas estructuras)

**Año 2 (2027):**
- Si >60% ingresos son de México y >$50k/año: Evaluar constituir SA de CV
- Si >60% ingresos son de USA: Mantener solo Wyoming LLC

---

## 13. Penalidades (Resumen Consolidado)

### Penalidades Graves (Enforcement Alto)

| Infracción | Multa | Severidad |
|------------|-------|-----------|
| **No registrar empleados en IMSS** | $216-$37,800 pesos **POR EMPLEADO** | 🔴 MUY GRAVE |
| **No emitir CFDI** | $1,410-$87,890 pesos | 🔴 MUY GRAVE |
| **No presentar declaración ISR anual** | $1,400-$34,500 pesos + recargos | 🔴 GRAVE |
| **No tener REPSE (si aplica)** | $27,000-$540,000 pesos + clausura | 🔴 GRAVE |
| **No presentar contabilidad electrónica** | $1,410-$35,250 pesos | 🟡 GRAVE |

### Penalidades Moderadas

| Infracción | Multa | Severidad |
|------------|-------|-----------|
| **Declaración extemporánea ISR/IVA** | $1,400-$17,000 pesos | 🟡 MODERADA |
| **No presentar DIOT** | $1,410-$35,250 pesos | 🟡 MODERADA |
| **Datos incorrectos en CFDI** | $1,410-$20,000 pesos | 🟡 MODERADA |
| **No renovar e.firma** | Imposibilidad de cumplir obligaciones | 🟡 MODERADA |

### Recargos y Actualizaciones

**Recargos por mora (no pagar impuestos a tiempo):**
- **Tasa:** 1.47% mensual (aprox. 18% anual)
- **Actualización:** + inflación mensual (INPC)

**Ejemplo:**
```
ISR adeudado: $10,000 pesos
Retraso: 3 meses
Recargos (1.47% × 3): $441 pesos
Actualización inflación (aprox 1% × 3): $300 pesos
TOTAL a pagar: $10,741 pesos
```

### Consecuencias No Monetarias

- **Opinión negativa de cumplimiento SAT:** No puedes participar en licitaciones públicas
- **Embargo de cuentas bancarias:** SAT puede congelar cuentas si no pagas
- **Cancelación de sellos digitales:** No puedes emitir CFDIs (paraliza negocio)
- **Demandas laborales:** Si no registraste empleados en IMSS, empleado puede demandar

---

## 14. Consideraciones para Entidades Extranjeras

### Establecimiento Permanente (EP)

#### ¿Qué es?
Un Establecimiento Permanente es cualquier lugar fijo de negocios en México donde una entidad extranjera realiza actividades empresariales.

#### ¿Cuándo aplica?
- Tienes oficina física en México
- Tienes empleados en México
- Prestas servicios en México de forma continua (>183 días/año)
- Tienes agente dependiente en México

#### Consecuencias de EP
- **Obligación de tributar ISR en México** (30% sobre utilidades atribuibles al EP)
- Debe registrarse ante SAT como EP de entidad extranjera
- Presentar declaraciones en México

#### Cómo evitar EP (si operas desde México como owner extranjero)
- **No** tener oficina física registrada a nombre de entidad extranjera
- **No** tener empleados contratados por entidad extranjera en México
- Operar como Persona Física Mexicana (no a nombre de LLC extranjera)

**Para Delaren Consulting LLC:**
- Si operas 100% remoto desde México como owner: **Potencial EP**
- **Solución:** Emitir facturas como Persona Física Mexicana (tú), no como LLC Wyoming

### Precios de Transferencia

#### ¿Qué es?
Regulación que obliga a empresas relacionadas (matriz-subsidiaria, misma propiedad) a transaccionar a precios de mercado.

#### ¿Cuándo aplica?
- Transacciones entre partes relacionadas (mismo dueño)
- Ingresos >$13M MXN/año (aprox $700k USD)
- Operaciones internacionales

#### Obligación
- **Estudio de Precios de Transferencia:** Documento que justifica que precios son "arm's length" (mercado)
- **Costo:** $3,000-$10,000 USD (elaborado por contador/abogado especializado)

**Para Delaren Consulting LLC (primer año):**
- **NO aplica** si ingresos <$700k USD
- Si escalas a >$700k: Contratar especialista en transfer pricing

### Retenciones sobre Pagos al Extranjero

#### Si Delaren LLC (Wyoming) factura a cliente mexicano

**Servicios de consultoría:**
- Cliente mexicano debe retener **25% ISR** sobre pago
- Cliente entera esa retención al SAT mexicano
- LLC puede acreditar esa retención en USA (Foreign Tax Credit) si aplica

**Regalías/Royalties:**
- Retención **25% ISR**

**Intereses:**
- Retención **10% ISR** (o según tratado fiscal)

**Solución:** Emitir facturas como Persona Física Mexicana para evitar retención

### Tratado para Evitar Doble Tributación (México-USA)

**Beneficios:**
- Reduce o elimina retenciones sobre ciertos tipos de ingresos
- Permite acreditar impuestos pagados en México contra impuestos USA (y viceversa)

**Requisitos:**
- Certificado de residencia fiscal (Form 6166 en USA)
- Registro ante SAT mexicano como beneficiario de tratado

**Para Delaren Consulting:**
- Si operas como LLC y facturas a clientes mexicanos: Evaluar tratado
- **Más simple:** Operar como Persona Física Mexicana directamente

---

## 15. Recursos Oficiales Consolidados

### SAT (Servicio de Administración Tributaria)

| Recurso | URL |
|---------|-----|
| **Portal Principal SAT** | https://www.sat.gob.mx/ |
| **RFC - Obtener** | https://www.sat.gob.mx/tramites/operacion/28753/obten-tu-rfc-con-la-clave-unica-de-registro-de-poblacion-curp |
| **e.firma - Solicitar** | https://www.sat.gob.mx/tramites/28523/solicita-tu-certificado-de-e-firma-portable |
| **Citas SAT** | https://citas.sat.gob.mx/ |
| **Declaraciones (ISR, IVA, DIOT)** | https://www.sat.gob.mx/declaracion/ |
| **Validar CFDI** | https://verificacfdi.facturaelectronica.sat.gob.mx/ |
| **Contabilidad Electrónica** | https://www.sat.gob.mx/aplicacion/login/51825/envia-tu-contabilidad-electronica |
| **Buzón Fiscal** | https://www.sat.gob.mx/aplicacion/login/43824/buzontributario |
| **Opinión de Cumplimiento** | https://www.sat.gob.mx/aplicacion/login/53027/mi-portal |

### IMSS (Instituto Mexicano del Seguro Social)

| Recurso | URL |
|---------|-----|
| **Portal Principal IMSS** | https://www.imss.gob.mx/ |
| **IMSS Digital** | https://www.imss.gob.mx/imssdigital |
| **IDSE (Registro empleados)** | http://www.imss.gob.mx/patrones/registro-patronal |
| **Opinión de Cumplimiento IMSS** | https://serviciosdigitales.imss.gob.mx/gestionAsegurados-web-externo/emiteConstanciaCumplimiento |

### STPS (Secretaría del Trabajo y Previsión Social)

| Recurso | URL |
|---------|-----|
| **Portal REPSE** | https://repse.stps.gob.mx/ |
| **Consulta Pública REPSE** | https://repse.stps.gob.mx/ConsultaPublica |

### Otros

| Recurso | URL |
|---------|-----|
| **Secretaría de Economía (Denominación Social)** | https://www.gob.mx/se/ |
| **INFONAVIT** | https://www.infonavit.org.mx/ |
| **FinCEN (BOI - si necesitas también para LLC Wyoming)** | https://boiefiling.fincen.gov/ |

---

## 16. Checklist de Cumplimiento Mensual (México)

### Primera Quincena del Mes

#### Día 1-10
- [ ] Conciliar cuentas bancarias del mes anterior
- [ ] Recibir todos los CFDIs de gastos del mes anterior
- [ ] Validar que todos los CFDIs recibidos estén vigentes (no cancelados)

#### Día 10-15
- [ ] Contador: Registrar todas las pólizas contables del mes anterior
- [ ] Preparar DIOT con lista de proveedores del mes

### Segunda Quincena del Mes

#### Día 17 (DEADLINE CRÍTICO)
- [ ] **Presentar y pagar Declaración ISR mensual** (pago provisional)
- [ ] **Presentar y pagar Declaración IVA mensual**
- [ ] **Presentar DIOT** (Declaración Informativa Operaciones con Terceros)
- [ ] Si tienes empleados: **Pagar Impuesto Sobre Nómina estatal**
- [ ] Si es mes de pago bimestral: **Pagar cuotas IMSS/INFONAVIT**

#### Día 20-25
- [ ] Generar Balanza de Comprobación del mes anterior
- [ ] Revisar que contabilidad esté al día

#### Día 25 (DEADLINE)
- [ ] **Enviar Contabilidad Electrónica al SAT** (Balanza de Comprobación XML)

#### Día 26-Fin de Mes
- [ ] Revisar flujo de caja del mes
- [ ] Proyectar impuestos del mes siguiente
- [ ] Emitir CFDIs a clientes con pagos recibidos

---

## 17. Checklist de Cumplimiento Anual (México)

### Enero-Marzo

#### Enero
- [ ] Cierre contable del año anterior (diciembre)
- [ ] Cálculo anual de ISR empleados (si aplica)
- [ ] Emitir CFDIs de Nómina con ajuste anual
- [ ] Preparar documentos para declaración anual

#### Febrero
- [ ] Contador: Elaborar estados financieros del año anterior
- [ ] Revisar deducciones del año (viáticos, gastos deducibles)
- [ ] Solicitar opinión de cumplimiento SAT (si necesitas para REPSE o licitaciones)

#### Marzo
- [ ] **Día 31 de Marzo: DEADLINE Declaración Anual ISR (Personas Morales)**

### Abril

- [ ] **Día 30 de Abril: DEADLINE Declaración Anual ISR (Personas Físicas)**
- [ ] Si aplica: Declaración informativa de préstamos, donativos, premios

### Trimestral/Bimestral (si aplica)

- [ ] Pago de cuotas IMSS (bimestral: día 17 del mes siguiente al bimestre)

### Eventos Específicos

- [ ] **Cada 3 años:** Renovar REPSE (antes del vencimiento)
- [ ] **Cada 4 años:** Renovar e.firma (antes del vencimiento)
- [ ] **Cuando cambies de domicilio:** Actualizar en RFC (30 días)
- [ ] **Cuando contrates empleado:** Registrar en IMSS (5 días hábiles)

---

## 18. Recomendaciones Estratégicas para Delaren Consulting

### Fase 1: Arranque (Mes 1-3, Enero-Marzo 2026)

**Prioridad 1 (CRÍTICO):**
1. [ ] Obtener RFC como Persona Física con Actividad Empresarial
2. [ ] Agendar cita para e.firma (SAT)
3. [ ] Contratar contador certificado (entrevistar 3 opciones)
4. [ ] Contratar PAC (Facturama recomendado, $50/mes)

**Prioridad 2 (IMPORTANTE):**
5. [ ] Registrar REPSE (si vas a prestar servicios a empresas)
6. [ ] Setup sistema contable básico (software que recomiende contador)
7. [ ] Crear templates de CFDI (configurar en PAC)

**Costo Mes 1-3:**
- Contador (setup + 3 meses): $1,500-$2,500 USD
- PAC (3 meses): $150-$300 USD
- REPSE: $100-$300 USD
- **TOTAL:** $1,750-$3,100 USD

### Fase 2: Operación Normal (Mes 4-12)

**Rutina Mensual:**
1. [ ] Emitir CFDIs a clientes (dentro de 72 horas de recibir pago)
2. [ ] Recibir CFDIs de proveedores (validar vigencia)
3. [ ] Día 17: Pagar ISR + IVA + DIOT (contador prepara, tú firmas con e.firma)
4. [ ] Día 25: Enviar contabilidad electrónica (contador lo hace)
5. [ ] Conciliar cuentas bancarias con contador

**Costo Mensual Recurrente:**
- Contador: $400-$800 USD/mes
- PAC: $50-$100 USD/mes
- Software contable: $50-$150 USD/mes
- **TOTAL:** $500-$1,050 USD/mes = **$6,000-$12,600/año**

### Fase 3: Escalamiento (Año 2, 2027)

**Si ingresos >$1M MXN/año (~$55k USD):**
1. [ ] Evaluar constituir SA de CV para:
   - Asset protection
   - Credibilidad corporativa
   - Optimización fiscal

**Si ingresos >$2M MXN/año (~$110k USD):**
2. [ ] Contratar empleados vs. freelancers (evaluar costo IMSS)
3. [ ] Implementar sistema ERP completo (Bind/ContPAQi)

**Si >60% clientes son USA:**
4. [ ] Mantener solo Wyoming LLC, minimizar operación México

---

## 19. Errores Comunes a Evitar

### Error #1: No contratar contador desde el inicio
**Consecuencia:** Multas, declaraciones incorrectas, pérdida de deducciones
**Solución:** Contratar contador certificado **antes** de emitir primera factura

### Error #2: Emitir CFDIs sin entender IVA
**Consecuencia:** Cobrar IVA incorrecto, problemas con SAT
**Solución:** Confirmar con contador si servicio lleva 16%, 0%, o exento

### Error #3: No validar CFDIs recibidos
**Consecuencia:** Deducir gastos con facturas canceladas (SAT rechaza)
**Solución:** Validar UUID de cada CFDI en portal SAT antes de registrar gasto

### Error #4: No registrar empleados en IMSS
**Consecuencia:** Multa de $216-$37,800 pesos **POR EMPLEADO** + demanda laboral
**Solución:** Registrar en IMSS dentro de 5 días de contratación, o contratar por honorarios

### Error #5: No renovar e.firma a tiempo
**Consecuencia:** No puedes presentar declaraciones ni emitir facturas
**Solución:** Calendar reminder 60 días antes de vencimiento (cada 4 años)

### Error #6: Operar sin REPSE
**Consecuencia:** Multa $27k-$540k pesos + cliente no puede deducir tus facturas
**Solución:** Tramitar REPSE **antes** de prestar primer servicio a empresa

### Error #7: Pagar impuestos tarde (después del día 17)
**Consecuencia:** Recargos 1.47% mensual + actualización inflacionaria
**Solución:** Calendar reminder día 15 de cada mes (2 días antes del deadline)

### Error #8: No conservar XML de CFDIs
**Consecuencia:** En auditoría SAT, sin XML no puedes probar gasto
**Solución:** Backup automático de XML en 2 lugares (PAC + tu nube)

### Error #9: Mezclar finanzas personales y del negocio
**Consecuencia:** Pierdas deducciones, SAT puede rechazar gastos
**Solución:** Cuenta bancaria separada 100% para negocio

### Error #10: No presentar contabilidad electrónica (día 25)
**Consecuencia:** Multa $1,410-$35,250 pesos
**Solución:** Contador debe tener proceso automático para enviar balanza día 20-25

---

## 20. Conclusión y Siguientes Pasos

### Complejidad del Sistema Fiscal Mexicano

El cumplimiento fiscal en México es **significativamente más complejo** que en USA (Wyoming LLC):

| Aspecto | México | Wyoming LLC |
|---------|--------|-------------|
| **Facturación** | CFDI 4.0 obligatorio (XML, PAC, timbrado) | Invoice simple (PDF) |
| **Impuestos** | ISR + IVA mensual + anual | Solo federal anual (pass-through) |
| **Contabilidad** | Electrónica XML mensual obligatoria | Básica (QuickBooks suficiente) |
| **Empleados** | IMSS + INFONAVIT + SAR + CFDI Nómina | W-2 simple |
| **Costo Compliance** | $6,000-$14,000/año | $700-$1,000/año |
| **Contador** | OBLIGATORIO | Opcional (DIY posible) |

### Recomendación Final para Delaren Consulting LLC

**Estructura Dual Año 1 (2026):**

1. **Wyoming LLC** (mantener):
   - Clientes USA/internacionales
   - Asset protection
   - Credibilidad internacional

2. **Persona Física Mexicana** (registrar):
   - Clientes mexicanos
   - Cumplimiento fiscal local
   - Evitar Establecimiento Permanente

**Flujo de Facturación:**
- Cliente en USA → Factura desde Wyoming LLC (invoice normal)
- Cliente en México → Factura desde tu RFC mexicano (CFDI 4.0)

**Costo Total Año 1:**
- Wyoming LLC: $700-$1,000
- México PFAE: $6,100-$14,100
- **TOTAL: $6,800-$15,100/año**

### Action Items Inmediatos (Enero 2026)

**Semana 1:**
- [ ] Entrevistar 3 contadores (pedir referencias, comparar fees)
- [ ] Elegir contador y firmar contrato

**Semana 2:**
- [ ] Tramitar RFC (con ayuda de contador)
- [ ] Agendar cita e.firma en SAT

**Semana 3:**
- [ ] Contratar PAC (Facturama recomendado)
- [ ] Asistir a cita e.firma SAT

**Semana 4:**
- [ ] Tramitar REPSE (si aplica)
- [ ] Setup sistema contable con contador
- [ ] Emitir primer CFDI de prueba

**Mes 2-3:**
- [ ] Primera declaración mensual (ISR + IVA + DIOT) día 17
- [ ] Primer envío contabilidad electrónica día 25
- [ ] Optimizar proceso con contador

### Contacto y Soporte

**Este documento es informativo, no constituye asesoría fiscal/legal.**

Para tu situación específica:
- **Contratar:** Contador Público Certificado (CPC) con experiencia en SAT
- **Consultar:** Abogado fiscal si constitución de SA de CV o casos complejos

---

**Última Actualización:** 3 de enero, 2026
**Próxima Revisión:** 31 de marzo, 2026 (Post-Tax Season)
**Elaborado por:** Claude (Anthropic) para Delaren Consulting LLC
**Disclaimer:** Esta guía es informativa y educativa. Consulta con contador certificado y abogado para decisiones fiscales y legales específicas a tu situación.

---

## Referencias y Fuentes

**Nota sobre limitaciones:** Este documento fue elaborado sin acceso a web en tiempo real (enero 2026). Toda la información proviene de conocimiento entrenado hasta enero 2025. **IMPORTANTE:** Verifica toda información con fuentes oficiales actualizadas:

### Fuentes Oficiales Recomendadas (Verificar en 2026)
1. **SAT.gob.mx** - Portal oficial del Servicio de Administración Tributaria
2. **IMSS.gob.mx** - Portal oficial del Instituto Mexicano del Seguro Social
3. **REPSE.stps.gob.mx** - Portal oficial de REPSE
4. **Ley del ISR** - Diario Oficial de la Federación
5. **Ley del IVA** - Diario Oficial de la Federación
6. **Código Fiscal de la Federación** - DOF

### Tasas, Montos y Deadlines
Toda información de tasas impositivas (ISR 30%, IVA 16%), plazos (día 17, día 25), multas, y costos son aproximados y pueden haber cambiado en 2026. **Confirmar con SAT y contador antes de tomar decisiones.**

### Tablas ISR Personas Físicas
La tabla de ISR progresivo (1.92%-35%) presentada corresponde a ejercicio 2025. SAT actualiza anualmente. Verificar tabla vigente en 2026 en:
https://www.sat.gob.mx/consultas/58972/calcula-tu-impuesto-anual

