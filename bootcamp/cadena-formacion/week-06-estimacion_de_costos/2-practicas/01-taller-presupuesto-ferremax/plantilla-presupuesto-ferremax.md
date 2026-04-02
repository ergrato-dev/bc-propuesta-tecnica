# Plantilla de Presupuesto — FerreMax S.A.S.

> **Instrucciones**: Esta plantilla consolida el presupuesto del proyecto FerreMax en el formato que incluirías en la propuesta técnica. Completa las celdas marcadas como `<!-- Completar -->` usando los cálculos que hiciste en el taller.

---

## Sección 1: Encabezado del Presupuesto

| Campo | Valor |
|-------|-------|
| **Proyecto** | Sistema de Gestión FerreMax S.A.S. |
| **Cliente** | FerreMax S.A.S. — Carlos Mendoza, Gerente |
| **Elaborado por** | [Nombre del consultor / empresa] |
| **Fecha de elaboración** | [Fecha] |
| **Versión** | 1.0 |
| **Validez de la cotización** | 30 días calendario |
| **Moneda** | Pesos colombianos (COP) |

---

## Sección 2: Presupuesto Detallado

### A. Recurso Humano

<!-- 📝 Instrucción: Esta es la tabla de costos de personal. Completa los subtotales.
     Fórmula: Subtotal = Días × Horas/día × Tarifa/hora -->

| Rol | Perfil | Días | Horas/día | Tarifa/hora (COP) | Subtotal (COP) |
|-----|--------|------|-----------|------------------|----------------|
| Desarrollador A | Semi-senior Full-Stack | 92 | 8 | $55,000 | <!-- 92 × 8 × 55,000 = ? --> |
| Desarrollador B | Junior Full-Stack | <!-- Días Dev B --> | 8 | $38,000 | <!-- Completar --> |
| **SUBTOTAL RECURSO HUMANO** | | | | | <!-- Suma --> |

---

### B. Infraestructura y Servicios

<!-- 📝 Instrucción: Completa los subtotales de cada ítem de infraestructura. -->

| Ítem | Especificación | Cantidad | Costo unitario (COP) | Subtotal (COP) |
|------|---------------|----------|---------------------|----------------|
| Servidor staging | AWS EC2 t3.micro — 4 meses | 4 meses | $90,000/mes | <!-- Completar --> |
| Servidor producción | AWS EC2 t3.small — 1 mes | 1 mes | $160,000/mes | <!-- Completar --> |
| Almacenamiento backups | AWS S3 — 20 GB | 4 meses | $8,000/mes | <!-- Completar --> |
| Dominio web | ferremax-sistema.com.co / 1 año | 1 | $45,000 | $45,000 |
| Certificado SSL | Let's Encrypt — gratuito | — | $0 | $0 |
| **SUBTOTAL INFRAESTRUCTURA** | | | | <!-- Suma --> |

---

### C. Licencias y Software

| Herramienta | Tecnología | Licencia | Costo (COP) |
|-------------|-----------|---------|-------------|
| Lenguaje backend | Python 3.12 | Open Source | $0 |
| Framework web | Django / FastAPI | Open Source | $0 |
| Base de datos | PostgreSQL 16 | Open Source | $0 |
| Frontend | React / Vue.js 3 | Open Source | $0 |
| Control de versiones | Git + GitHub Free | Gratuito | $0 |
| **SUBTOTAL LICENCIAS** | | | **$0** |

---

### D. Contingencia

<!-- 📝 Instrucción: La contingencia es el 10% sobre el subtotal de A + B + C.
     Completa la base de cálculo y el valor. -->

| Concepto | Base de cálculo | % | Valor (COP) |
|----------|----------------|---|-------------|
| Contingencia por riesgos e imprevistos | <!-- Subtotal A + B + C --> | 10% | <!-- Completar --> |

**Justificación**: Proyecto con alcance bien definido (ver S03-Alcance), tecnología conocida por el equipo, y estimaciones validadas con Delphi + Planning Poker. Nivel de incertidumbre bajo-medio → 10% es apropiado.

---

## Sección 3: Consolidado de Costos

<!-- 📝 Instrucción: Consolida las 4 categorías en esta tabla de resumen. -->

| Sección | Categoría | Subtotal (COP) |
|---------|-----------|----------------|
| A | Recurso Humano | <!-- Completar --> |
| B | Infraestructura y Servicios | <!-- Completar --> |
| C | Licencias y Software | $0 |
| D | Contingencia (10%) | <!-- Completar --> |
| **SUBTOTAL COSTOS DEL PROYECTO** | | <!-- Suma A + B + C + D --> |
| Margen de servicios profesionales (20%) | | <!-- Subtotal × 0.20 --> |
| **TOTAL COTIZACIÓN AL CLIENTE** | | <!-- Subtotal + Margen --> |

---

## Sección 4: Tabla Ejecutiva (para la propuesta técnica)

<!-- 📝 Instrucción: Esta es la tabla resumida que verá el cliente en la propuesta técnica.
     No mostramos el detalle de tarifas individuales — solo los grandes grupos. -->

| Concepto | Descripción | Valor (COP) |
|----------|-------------|-------------|
| Desarrollo del sistema | 2 desarrolladores full-stack, 15 semanas, 6 módulos funcionales | <!-- Completar con subtotal RH --> |
| Infraestructura y servicios cloud | Servidores (staging + producción), dominio, backups | <!-- Completar con subtotal Infra --> |
| Gestión y contingencia | Reserva del 10% para imprevistos y gestión del proyecto | <!-- Completar con contingencia --> |
| **Subtotal** | | <!-- Completar --> |
| Servicios profesionales | Margen de gestión (20%) | <!-- Completar --> |
| **TOTAL DE LA PROPUESTA** | | <!-- TOTAL FINAL --> |

---

## Sección 5: Condiciones Comerciales

| Condición | Detalle |
|-----------|---------|
| **Forma de pago** | 30% al firmar el contrato · 40% al H2 (Semana 9) · 30% a la entrega final (Semana 15) |
| **Validez de la cotización** | 30 días calendario desde la fecha de presentación |
| **IVA** | No incluido. Si aplica régimen de IVA, se calcula sobre el total según normativa DIAN |
| **Cambios de alcance** | Cualquier funcionalidad fuera del alcance aprobado en S03 generará una cotización adicional |
| **Garantía** | 30 días de soporte correctivo posterior a la entrega final sin costo adicional |

---

## Sección 6: Supuestos del Presupuesto

<!-- 📝 Instrucción: Agrega al menos UN supuesto adicional relevante a la situación de FerreMax.
     Los supuestos SP-01 a SP-04 están predefinidos. Añade SP-05 basándote en lo que sabes del caso. -->

| ID | Supuesto | Impacto si no se cumple |
|----|---------|------------------------|
| SP-01 | Las tarifas de los desarrolladores son fijas durante el proyecto; no aplican ajustes por inflación | El costo de RH podría aumentar si el proyecto supera 6 meses |
| SP-02 | Las tarifas de infraestructura cloud son estables; variaciones del dólar superiores al 10% se renegocian | El costo de AWS podría variar hasta ±15% |
| SP-03 | No se realizarán cambios de alcance después de firmado el contrato; cambios solicitados generan cotización adicional | Cada módulo adicional suma en promedio $8,000,000–$15,000,000 al presupuesto |
| SP-04 | Los datos actuales de inventario de FerreMax serán entregados en formato Excel estructurado en la Semana 2 | Una migración de datos sin estructura puede agregar 5–8 días-persona al módulo M2 |
| SP-05 | <!-- Agrega tu supuesto adicional aquí --> | <!-- ¿Qué pasa si no se cumple? --> |

---

> ✅ **Cuando termines**, verifica que:
> - El total de la cotización esté entre $85M y $110M COP (rango esperado para este caso)
> - Los subtotales de la Sección 3 coinciden con los cálculos detallados en Secciones 2A, 2B, 2C y 2D
> - Los días-persona (92 + valor Dev B) corresponden a los días del cronograma S05
> - Los supuestos están redactados de forma clara y verificable
