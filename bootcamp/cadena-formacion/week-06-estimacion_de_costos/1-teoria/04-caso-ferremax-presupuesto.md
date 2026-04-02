# FerreMax: Presupuesto Completo del Proyecto

## 🎯 Objetivos de esta clase

- Ver cómo se construye el presupuesto de FerreMax a partir de los datos de S04 y S05
- Entender cada línea del presupuesto con su justificación
- Obtener el total de la cotización que se presentaría a Carlos Mendoza

---

## 1. Punto de partida — Insumos de semanas anteriores

**De la Semana 4** (Estimación de esfuerzo):

| Módulo | Esfuerzo (días-persona) |
|--------|------------------------|
| M0 BD + Arquitectura | 10 |
| M1 Autenticación | 31 |
| M2 Inventario | 67 |
| M3 Clientes | 12 |
| M4 Ventas | 48 |
| M5 Reportes | 20 |
| M6 Config. y Docs | 16 |
| **Total** | **194 días-persona** |

**De la Semana 5** (Cronograma):
- Duración: **15 semanas** de calendario
- Equipo: **2 desarrolladores** a tiempo completo (Dev A semi-senior, Dev B junior)
- Factor de capacidad: 80%

---

## 2. Distribución del esfuerzo entre el equipo

Basados en la asignación del cronograma S05:

| Dev | Módulos asignados | Esfuerzo total (días-persona) |
|-----|------------------|-------------------------------|
| Dev A (semi-senior) | M0(5) + M1(31) + M3(12) + M4(24) + M5(20) | **92 días** |
| Dev B (junior) | M0(5) + M2(67) + M4(24) + M6(16) | **112 días** |
| **Total** | | **204 días** |

> *Nota*: El total suma 204 y no 194 porque en M0 y M4 los dos devs trabajan en paralelo — el esfuerzo individual de cada módulo completo (M0=10 días, M4=48 días) se divide entre los dos. Lo relevante para el costo es cuántos días factura cada persona.

---

## 3. Sección A — Recurso Humano

$$\text{Costo RH} = \text{Días-persona} \times 8 \text{ horas/día} \times \text{Tarifa/hora}$$

| Rol | Perfil | Días | Horas/día | Tarifa/h (COP) | Subtotal (COP) |
|-----|--------|------|-----------|---------------|----------------|
| Dev A | Semi-senior Full-Stack | 92 | 8 | $55,000 | $40,480,000 |
| Dev B | Junior Full-Stack | 112 | 8 | $38,000 | $34,048,000 |
| **Subtotal Recurso Humano** | | **204** | | | **$74,528,000** |

**Cálculos detallados:**
- Dev A: 92 × 8 × $55,000 = $40,480,000
- Dev B: 112 × 8 × $38,000 = $34,048,000
- **Total RH: $74,528,000**

**Justificación de tarifas:**
- Dev A ($55,000/h): Desarrollador semi-senior con 3 años de experiencia en Python/Django y React. Tarifa acorde al mercado 2025 para consultores en Bogotá (fuente: Computrabajo, Torre.co).
- Dev B ($38,000/h): Desarrollador junior recién egresado con manejo de Python básico y conocimiento de SQL. Tarifa de entrada de mercado para egresados de programas técnicos.

---

## 4. Sección B — Infraestructura y Servicios

El sistema de FerreMax es un monolito web con base de datos PostgreSQL. No requiere infraestructura compleja.

| Ítem | Especificación | Cantidad | Costo unitario (COP) | Subtotal (COP) |
|------|---------------|----------|---------------------|----------------|
| Servidor VPS (staging) | AWS EC2 t3.micro | 4 meses | $90,000/mes | $360,000 |
| Servidor VPS (producción) | AWS EC2 t3.small | 1 mes | $160,000/mes | $160,000 |
| Servicio de base de datos | PostgreSQL en el mismo servidor | — | $0 | $0 |
| Almacenamiento de backups | AWS S3 — 20 GB | 4 meses | $8,000/mes | $32,000 |
| Dominio web | ferremax-sistema.com.co | 1 año | $45,000 | $45,000 |
| Certificado SSL | Let's Encrypt (gratuito) | — | $0 | $0 |
| **Subtotal Infraestructura** | | | | **$597,000** |

> *Nota*: Los costos de AWS están calculados en COP asumiendo tasa de cambio de $4,200 por USD (referencia 2025). Pueden variar según la tasa del día.

---

## 5. Sección C — Licencias y Software

FerreMax usa exclusivamente tecnologías open source:

| Herramienta | Tecnología | Licencia | Costo (COP) |
|-------------|-----------|---------|-------------|
| Lenguaje backend | Python 3.12 | Open Source (PSF) | $0 |
| Framework web | Django 5.x o FastAPI | Open Source (BSD/MIT) | $0 |
| Base de datos | PostgreSQL 16 | Open Source (PostgreSQL License) | $0 |
| Frontend | React 18 o Vue.js 3 | Open Source (MIT) | $0 |
| Control de versiones | Git + GitHub Free | Gratuito | $0 |
| Gestión de proyecto | GitHub Projects | Gratuito | $0 |
| **Subtotal Licencias** | | | **$0** |

---

## 6. Cálculo de la Contingencia

La contingencia se aplica sobre el subtotal de costos directos (A + B + C):

```
Subtotal costos directos = $74,528,000 + $597,000 + $0 = $75,125,000
Contingencia al 10%      = $75,125,000 × 0.10 = $7,512,500
```

**Justificación del 10%**: El proyecto tiene un alcance bien definido (ver S03), tecnología familiar para el equipo, y los módulos están estimados con técnicas combinadas (Delphi + Planning Poker). El nivel de incertidumbre es bajo-medio → 10% es apropiado.

---

## 7. Presupuesto consolidado (costo interno)

| Sección | Concepto | Subtotal (COP) |
|---------|---------|----------------|
| A | Recurso Humano | $74,528,000 |
| B | Infraestructura y Servicios | $597,000 |
| C | Licencias y Software | $0 |
| D | Contingencia (10%) | $7,512,500 |
| **SUBTOTAL COSTO TOTAL** | | **$82,637,500** |

---

## 8. Margen de ganancia y cotización al cliente

La consultora que presenta la propuesta a Carlos Mendoza aplica un margen del **20%** sobre el costo total:

```
Subtotal costos     = $82,637,500
Margen 20%          = $82,637,500 × 0.20 = $16,527,500
TOTAL COTIZACIÓN    = $82,637,500 + $16,527,500 = $99,165,000
```

**Cotización final redondeada: $99,200,000 COP**

> El redondeo al alza es una práctica habitual en propuestas técnicas profesionales. Da margen para pequeños ajustes y hace la cifra más presentable.

---

## 9. Resumen ejecutivo — tabla para la propuesta técnica

Esta es la tabla que verá Carlos Mendoza en la propuesta:

| Concepto | Descripción | Valor (COP) |
|----------|-------------|-------------|
| Desarrollo del sistema | 2 desarrolladores, 15 semanas, 6 módulos funcionales | $74,528,000 |
| Infraestructura | Servidores cloud, dominio, almacenamiento de backups | $597,000 |
| Gestión y contingencia | Reserva para imprevistos (10%) | $7,512,500 |
| **Subtotal** | | **$82,637,500** |
| Servicios profesionales | Margen de gestión del proyecto (20%) | $16,527,500 |
| **TOTAL DE LA PROPUESTA** | | **$99,165,000** |

**Condiciones:**
- Forma de pago: 30% al firmar el contrato, 40% al H2 (Semana 9), 30% a la entrega final (Semana 15)
- Validez de la cotización: 30 días calendario desde la fecha de presentación
- IVA: No incluido. Si aplica régimen de IVA, se calculará sobre el total según normativa DIAN vigente.

---

## 10. Análisis: ¿Es un precio razonable para FerreMax?

**Comparativa de referencia:**

| Referencia | Costo aprox. |
|-----------|-------------|
| Sistema de punto de venta comercial (SaaS) en Colombia | $1,500,000–$3,500,000/año (suscripción) |
| Desarrollo a medida similar en agencia de software Bogotá | $80,000,000–$130,000,000 |
| **Propuesta FerreMax (esta propuesta)** | **$99,165,000** |

**Conclusión**: El precio está dentro del rango del mercado para un sistema similar desarrollado a medida. Es más costoso que adoptar un SaaS existente, pero FerreMax obtiene un sistema 100% adaptado a sus procesos y sin depender de suscripciones continuas.

---

## ✅ Checklist de verificación

Después de esta clase, deberías poder:

- [ ] Calcular el costo de RH de FerreMax para Dev A y Dev B usando la fórmula días × horas × tarifa
- [ ] Identificar los ítems de infraestructura del presupuesto de FerreMax
- [ ] Calcular la contingencia del 10% sobre el subtotal correcto
- [ ] Calcular la cotización final con margen del 20%
- [ ] Explicar por qué el precio de $99,165,000 es razonable para el mercado TI colombiano
