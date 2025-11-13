# Dashboard Visual en Google Sheets — Guía de Configuración

**Objetivo:** Crear un dashboard visual en Google Sheets que actualices semanalmente para monitorear KPIs críticos

**Tiempo de setup:** 60-90 minutos
**Actualización semanal:** 10-15 minutos

---

## Paso 1: Crear Nuevo Google Sheet

1. Ve a https://sheets.google.com
2. Crear nuevo → Hoja de cálculo en blanco
3. Renombrar: "Dashboard Financiero - Plan 90 Días"
4. Crear 5 pestañas (hojas):
   - `Dashboard` (principal - vista visual)
   - `FlujoCaja` (datos semanales)
   - `AR` (cuentas por cobrar)
   - `CRM` (leads y pipeline)
   - `Datos` (configuración y cálculos)

---

## Paso 2: Importar Datos Base

### Hoja "FlujoCaja"
1. Importar `finance/flujo_caja_semanal.csv`:
   - Archivo → Importar → Subir → flujo_caja_semanal.csv
   - Ubicación: Reemplazar hoja actual
   - Separador: Detectar automáticamente
2. Resultado: Columnas desde semana hasta comentarios

### Hoja "AR"
1. Importar `finance/ar_tracking.csv`:
   - Mismo proceso que FlujoCaja
2. Resultado: Columnas de facturas y cuentas por cobrar

### Hoja "CRM"
1. Importar `ops/crm_simple.csv`:
   - Mismo proceso
2. Resultado: Leads, clientes, etapas

---

## Paso 3: Configurar Hoja "Dashboard" (Vista Principal)

### Layout del Dashboard

```
┌─────────────────────────────────────────────────────────────────┐
│  DASHBOARD FINANCIERO - PLAN 90 DÍAS                            │
│  Última actualización: [Fecha]                                  │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  📊 MÉTRICAS FINANCIERAS              🎯 METAS                  │
│  ┌──────────────────────────┐        ┌─────────────────────┐   │
│  │ Ingresos Mes   $25,950   │        │ Día 30  $33,950     │   │
│  │ Margen Neto    $950      │        │ Día 60  $40,950     │   │
│  │ Fondo Emerg.   $0        │        │ Día 90  $45,950     │   │
│  │ % s/Equilibrio 132%      │        └─────────────────────┘   │
│  └──────────────────────────┘                                   │
│                                                                  │
│  💳 DEUDA                              📈 COMERCIAL             │
│  ┌──────────────────────────┐        ┌─────────────────────┐   │
│  │ Deuda Total    $160,000  │        │ Clientes    4       │   │
│  │ Nu Card        $85,200   │        │ Retainers   0       │   │
│  │ Pago Mensual   $12,000   │        │ Pipeline    $0      │   │
│  └──────────────────────────┘        └─────────────────────┘   │
│                                                                  │
│  🚨 ALERTAS                                                      │
│  ┌──────────────────────────────────────────────────────────┐  │
│  │ ⚠️  Margen < $1,000 MXN (CRÍTICO)                         │  │
│  │ ⚠️  Pipeline < $40,000 (URGENTE: Prospectar)             │  │
│  │ ⚠️  Fondo emergencia = $0 (Acumular $3K en 30 días)      │  │
│  └──────────────────────────────────────────────────────────┘  │
│                                                                  │
│  📊 GRÁFICOS                                                     │
│  ┌──────────────────────────────────────────────────────────┐  │
│  │ [Gráfico: Ingresos vs Meta por Mes]                       │  │
│  │ [Gráfico: Evolución Deuda Nu Card]                        │  │
│  │ [Gráfico: Crecimiento Pipeline]                           │  │
│  └──────────────────────────────────────────────────────────┘  │
└─────────────────────────────────────────────────────────────────┘
```

### Configuración Paso a Paso

#### Sección 1: Header (Fila 1-3)

**Celda A1:**
- Escribir: "DASHBOARD FINANCIERO - PLAN 90 DÍAS"
- Formato: Fuente 18pt, Negrita, Color azul oscuro
- Merge A1:F1 (unir celdas)

**Celda A2:**
- Escribir: "Última actualización:"
- Celda B2: Fórmula `=TEXT(TODAY(),"DD/MM/YYYY")`

**Celda A3:**
- Escribir: "Semana:"
- Celda B3: Fórmula `=WEEKNUM(TODAY())`

---

#### Sección 2: Métricas Financieras (Filas 5-12)

**Configurar en celdas A5:C12:**

| Celda | Contenido | Fórmula / Valor | Formato |
|-------|-----------|-----------------|---------|
| A5 | 📊 MÉTRICAS FINANCIERAS | | Negrita, 14pt |
| A6 | Ingresos Mensuales | | |
| B6 | | `=SUM(FlujoCaja!D:D)` | Moneda MXN |
| C6 | Meta: $33,950 | | Gris claro |
| A7 | Margen Neto Mensual | | |
| B7 | | `=B6-Datos!B2` | Moneda MXN |
| C7 | Meta: $8,650 | | Gris claro |
| A8 | Fondo Emergencia | | |
| B8 | | `=SUM(FlujoCaja!J:J)` | Moneda MXN |
| C8 | Meta: $6,298 (30d) | | Gris claro |
| A9 | Punto de Equilibrio | | |
| B9 | $19,650 | | Moneda MXN |
| A10 | % Sobre Equilibrio | | |
| B10 | | `=(B6/B9)*100` | Porcentaje |

**Formato Condicional en B7 (Margen Neto):**
- Regla: Si valor < 1000 → Fondo ROJO, Texto BLANCO, Negrita
- Regla: Si valor >= 1000 y < 5000 → Fondo AMARILLO
- Regla: Si valor >= 5000 → Fondo VERDE CLARO

---

#### Sección 3: Deuda (Filas 5-10, Columnas E:G)

**Configurar en celdas E5:G10:**

| Celda | Contenido | Fórmula / Valor | Formato |
|-------|-----------|-----------------|---------|
| E5 | 💳 DEUDA | | Negrita, 14pt |
| E6 | Deuda Total | | |
| F6 | | `=Datos!B10` | Moneda MXN |
| G6 | Meta: $140,000 (90d) | | Gris claro |
| E7 | Saldo Nu Card | | |
| F7 | | `=Datos!B11` | Moneda MXN |
| G7 | Tasa: 99.9% | | Rojo |
| E8 | Pago Mensual | | |
| F8 | $12,000 | | Moneda MXN |
| E9 | Reducción vs Inicio | | |
| F9 | | `=Datos!B10-160000` | Moneda MXN |

**Formato Condicional en F9 (Reducción):**
- Regla: Si valor < 0 → Texto VERDE (negativo es bueno, significa que bajó)
- Regla: Si valor > 0 → Texto ROJO (aumentó la deuda)

---

#### Sección 4: Comercial (Filas 12-18, Columnas E:G)

**Configurar en celdas E12:G18:**

| Celda | Contenido | Fórmula / Valor | Formato |
|-------|-----------|-----------------|---------|
| E12 | 📈 COMERCIAL | | Negrita, 14pt |
| E13 | Clientes Activos | | |
| F13 | | `=COUNTIF(CRM!M:M,"Cliente Activo")` | Número |
| G13 | Meta: 7 (90d) | | Gris claro |
| E14 | Clientes México | | |
| F14 | | `=COUNTIFS(CRM!M:M,"Cliente Activo",CRM!I:I,"Mexico")` | Número |
| E15 | Retainers Activos | | |
| F15 | | `=COUNTIFS(CRM!M:M,"Cliente Activo",CRM!Q:Q,"Retainer*")` | Número |
| G15 | Meta: 2-3 (90d) | | Gris claro |
| E16 | Pipeline Value | | |
| F16 | | `=SUMIF(CRM!M:M,"Prospecto",CRM!P:P)+SUMIF(CRM!M:M,"Reunión*",CRM!P:P)+SUMIF(CRM!M:M,"Propuesta*",CRM!P:P)` | Moneda MXN |
| G16 | Meta: $80,000 (90d) | | Gris claro |

**Formato Condicional en F16 (Pipeline):**
- Regla: Si valor < 40000 → Fondo ROJO (alerta)
- Regla: Si valor >= 40000 y < 60000 → Fondo AMARILLO
- Regla: Si valor >= 60000 → Fondo VERDE CLARO

---

#### Sección 5: Alertas (Filas 20-27)

**Configurar en celdas A20:G27:**

| Celda | Contenido | Fórmula | Formato |
|-------|-----------|---------|---------|
| A20 | 🚨 ALERTAS | | Negrita, Rojo, 14pt |
| A21 | Margen < $1,000 | | |
| B21 | | `=IF(B7<1000,"⚠️ SÍ","✅ NO")` | Condicional |
| A22 | Pipeline < $40K | | |
| B22 | | `=IF(F16<40000,"⚠️ SÍ","✅ NO")` | Condicional |
| A23 | Fondo < $5K | | |
| B23 | | `=IF(B8<5000,"⚠️ SÍ","✅ NO")` | Condicional |
| A24 | Leads Activos < 5 | | |
| B24 | | `=IF(COUNTIF(CRM!M:M,"Prospecto")<5,"⚠️ SÍ","✅ NO")` | Condicional |
| A25 | AR > 30 días vencido | | |
| B25 | | `=IF(COUNTIF(AR!N:N,">30")>0,"⚠️ SÍ","✅ NO")` | Condicional |

**Formato Condicional en columna B (Alertas):**
- Regla: Si contiene "⚠️ SÍ" → Fondo ROJO, Texto BLANCO, Negrita
- Regla: Si contiene "✅ NO" → Fondo VERDE CLARO

---

## Paso 4: Crear Gráficos

### Gráfico 1: Ingresos vs Meta (Evolución Mensual)

**Ubicación:** Celdas A30:D45

**Datos:**
| Mes | Ingresos Reales | Meta | Diferencia |
|-----|-----------------|------|------------|
| Mes 1 | =B6 | 33950 | =B30-C30 |
| Mes 2 | [Actualizar] | 40950 | |
| Mes 3 | [Actualizar] | 45950 | |

**Crear gráfico:**
1. Seleccionar A29:C32
2. Insertar → Gráfico
3. Tipo: Gráfico de columnas agrupadas
4. Título: "Ingresos vs Meta - Evolución 90 Días"
5. Eje Y: Ingresos (MXN)
6. Series:
   - Serie 1 (Ingresos Reales): Color azul
   - Serie 2 (Meta): Color verde claro

---

### Gráfico 2: Evolución Deuda Nu Card

**Ubicación:** Celdas F30:I45

**Datos:**
| Mes | Saldo Nu Card | Reducción vs Inicial |
|-----|---------------|----------------------|
| Inicio | 85200 | 0 |
| Mes 1 | [Actualizar] | =[Saldo]-85200 |
| Mes 2 | [Actualizar] | |
| Mes 3 | [Actualizar] | |

**Crear gráfico:**
1. Seleccionar F29:G33
2. Insertar → Gráfico
3. Tipo: Gráfico de líneas
4. Título: "Reducción Deuda Nu Card"
5. Serie: Color rojo degradando a verde

---

### Gráfico 3: Crecimiento de Pipeline

**Ubicación:** Celdas A48:D60

**Datos:**
| Semana | Pipeline Value | Leads Activos | Propuestas |
|--------|----------------|---------------|------------|
| Sem 46 | 0 | 3 | 0 |
| Sem 47 | [Actualizar] | [Act.] | [Act.] |
| ... | | | |

**Crear gráfico:**
1. Tipo: Gráfico de área apilada
2. Título: "Evolución de Pipeline (Semanal)"
3. Series: Pipeline en azul, Leads en verde

---

## Paso 5: Hoja "Datos" (Configuración)

Esta hoja contiene valores de referencia que NO cambias frecuentemente.

### Configurar en Datos!A1:B20:

| A | B |
|---|---|
| **CONFIGURACIÓN** | |
| Gastos Personales Mensuales | 6000 |
| Gastos Contadores Mensuales | 1300 |
| Gastos Herramientas Mensuales | 350 |
| Total Gastos Fijos Mensuales | =SUM(B2:B4)+12000 |
| Punto de Equilibrio | 19650 |
| | |
| **DEUDA (Actualizar Mensual)** | |
| Deuda Total | 160000 |
| Saldo Nu Card | 85200 |
| Saldo TDC #2 | 25000 |
| Saldo TDC #3 | 20000 |
| Saldo TDC #4 | 15000 |
| Deuda Hermana | 30000 |
| | |
| **METAS** | |
| Meta Ingresos Mes 1 | 33950 |
| Meta Ingresos Mes 2 | 40950 |
| Meta Ingresos Mes 3 | 45950 |

---

## Paso 6: Rutina de Actualización Semanal

### Cada Lunes 9:00am:

#### 1. Actualizar Hoja "FlujoCaja" (5 min)
- Agregar nueva fila con datos de la semana pasada:
  - Semana
  - Fechas
  - Ingresos cobrados (suma de lo que entró)
  - Gastos pagados (personales + deuda + contadores + herramientas)
  - Flujo neto
  - AR pendiente
  - Fondo emergencia acumulado
  - Comentarios

#### 2. Actualizar Hoja "AR" (3 min)
- Marcar facturas cobradas (cambiar estado a "Cobrado", agregar fecha_cobro_real)
- Agregar nuevas facturas emitidas esta semana
- Actualizar días_pendientes para facturas aún abiertas

#### 3. Actualizar Hoja "CRM" (5 min)
- Actualizar etapas de leads que avanzaron
- Agregar leads nuevos contactados
- Actualizar fechas de último_seguimiento y prox_seguimiento
- Cambiar prob_cierre si hubo avances

#### 4. Actualizar Hoja "Datos" (2 min, solo si cambia algo)
- Si cobrastes un anticipo grande, actualizar deuda si pagaste extra
- Si CONDUSEF resolvió, actualizar saldo Nu Card y tasa

#### 5. Revisar Dashboard (2 min)
- Ver alertas (si hay rojas, tomar acción inmediata)
- Verificar que métricas se ven correctas
- Si algo se ve raro, revisar fórmulas

**Total:** 15-20 minutos cada lunes

---

## Paso 7: Compartir y Backup

### Compartir con Contador
1. Compartir → Agregar correo de tu contador
2. Permisos: "Puede ver" (solo lectura)
3. Enviar notificación

### Backup Semanal
1. Archivo → Descargar → Microsoft Excel (.xlsx)
2. Guardar en carpeta local: `backups/dashboard_semana_XX.xlsx`

---

## Fórmulas Útiles para Copiar/Pegar

### Suma de Ingresos Mensuales
```
=SUM(FlujoCaja!D:D)
```

### Contar Clientes Activos en México
```
=COUNTIFS(CRM!M:M,"Cliente Activo",CRM!I:I,"Mexico")
```

### Calcular Pipeline Value
```
=SUMIF(CRM!M:M,"Prospecto",CRM!P:P)+SUMIF(CRM!M:M,"Reunión*",CRM!P:P)+SUMIF(CRM!M:M,"Propuesta*",CRM!P:P)
```

### Alertas (Margen < $1K)
```
=IF(B7<1000,"⚠️ SÍ - CRÍTICO: Generar ingresos urgente","✅ NO")
```

### DSO (Days Sales Outstanding) Promedio
```
=AVERAGE(AR!N:N)
```

### Tasa de Conversión (Propuestas → Cierres)
```
=COUNTIF(CRM!M:M,"Cliente Activo")/COUNTIF(CRM!M:M,"Propuesta*")*100
```

---

## Formato Condicional - Reglas Completas

### Para Márgenes/Ingresos (Verde/Amarillo/Rojo)
```
Regla 1: Si valor < 1000 → Rojo
Regla 2: Si valor >= 1000 y < 5000 → Amarillo
Regla 3: Si valor >= 5000 → Verde claro
```

### Para Alertas (Texto con emojis)
```
Regla 1: Si celda contiene "⚠️" → Fondo rojo, texto blanco
Regla 2: Si celda contiene "✅" → Fondo verde claro
```

### Para Pipeline
```
Regla 1: Si < $40,000 → Rojo (urgente prospectar)
Regla 2: Si >= $40,000 y < $60,000 → Amarillo (mantener)
Regla 3: Si >= $60,000 → Verde (saludable)
```

---

## Accesos Rápidos y Atajos

### Atajos de Teclado Útiles
- `Ctrl + ;` → Insertar fecha actual
- `Ctrl + Shift + ;` → Insertar hora actual
- `Ctrl + D` → Copiar celda de arriba
- `Ctrl + '` → Copiar fórmula de arriba
- `Alt + =` → Auto-suma

### Validación de Datos (para evitar errores)
**En hoja CRM, columna M (Etapa):**
1. Seleccionar columna M
2. Datos → Validación de datos
3. Criterio: Lista de elementos
4. Opciones: `Prospecto,Reunión Agendada,Propuesta Enviada,Negociación,Cliente Activo,Perdido`

---

## Solución de Problemas Comunes

### "Las fórmulas no calculan"
- Verificar que los nombres de las hojas sean exactos (FlujoCaja, no Flujo Caja)
- Verificar que las columnas referenciadas existan
- Probar con `Ctrl + Shift + F9` (recalcular todo)

### "Los gráficos no actualizan"
- Click derecho en gráfico → Actualizar
- O: Editar gráfico → Cambiar rango de datos

### "Formato condicional no funciona"
- Verificar que las reglas estén en orden correcto (más específica primero)
- Verificar que el rango sea el correcto
- Probar eliminando y recreando la regla

---

## Exportar/Imprimir Dashboard

### Para Imprimir (A4 o Carta)
1. Archivo → Imprimir
2. Configuración:
   - Orientación: Horizontal
   - Escala: Ajustar a 1 página de ancho
   - Márgenes: Estrechos
   - Encabezado/Pie: Ninguno
3. Imprimir PDF para guardar snapshot semanal

---

## Próximos Pasos

1. [ ] Crear Google Sheet siguiendo esta guía (60-90 min)
2. [ ] Importar datos de CSVs
3. [ ] Configurar fórmulas y formato condicional
4. [ ] Crear 3 gráficos
5. [ ] Probar actualización semanal (este lunes)
6. [ ] Compartir con contador (solo lectura)
7. [ ] Establecer rutina de lunes 9am

---

**Última actualización:** 13 noviembre 2025
**Tiempo de setup:** 60-90 minutos (una sola vez)
**Mantenimiento:** 15 minutos/semana

**Link a tu Dashboard:** _______________________________________________
_(Pegar aquí el link cuando lo crees)_
