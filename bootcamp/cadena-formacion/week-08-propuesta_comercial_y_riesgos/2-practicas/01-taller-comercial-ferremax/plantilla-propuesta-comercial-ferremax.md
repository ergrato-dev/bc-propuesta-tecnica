# PROPUESTA COMERCIAL Y RIESGOS — FerreMax GI
## Plantilla del Taller — Semana 8

> **Instrucciones generales:** Completa todas las secciones marcadas con `<!-- Completar -->`. No elimines las instrucciones de los comentarios — solo rellena los espacios indicados.

---

## §8 Tabla de Costos

La inversión total para el desarrollo completo del sistema **FerreMax GI** asciende a **$99,165,000 COP**, con el siguiente desglose:

| Categoría | Descripción del servicio | Valor COP |
|---|---|---|
| Desarrollo de software | Ingeniería, programación y pruebas de los 6 módulos (15 semanas) | $74,528,000 |
| Gestión de proyecto | Coordinación técnica, reuniones de avance, documentación | $8,120,000 |
| Infraestructura en la nube | <!-- Completar: AWS EC2 + RDS, ¿cuántos meses? --> | <!-- Completar: $X,XXX,000 --> |
| Licencias de software | Herramientas de código abierto (Python, React, PostgreSQL) | $0 |
| Contingencia (10%) | <!-- Completar: ¿qué cubre la contingencia? --> | <!-- Completar: $X,XXX,XXX --> |
| Utilidad del proveedor (15%) | <!-- Completar: ¿sobre qué base se calcula la utilidad? --> | <!-- Completar: $X,XXX,XXX --> |
| **TOTAL DEL PROYECTO** | | **$99,165,000 COP** |

> *Todos los valores incluyen IVA. Los precios son válidos hasta el 15 de diciembre de 2024.*

---

## §9 Condiciones Comerciales

### 9.1 Condiciones de Pago

El pago se realizará en tres cuotas vinculadas a hitos verificables del proyecto:

| Cuota | Porcentaje | Valor COP | Hito que activa el pago |
|---|---|---|---|
| Anticipo | 30% | $29,749,500 | Al firmar el contrato |
| Segundo pago | 40% | <!-- Completar: $XX,XXX,000 --> | <!-- Completar: ¿qué hito activa este pago? (semana y módulos) --> |
| Pago final | 30% | <!-- Completar: $XX,XXX,500 --> | <!-- Completar: ¿qué hito activa este pago? (semana y entregable) --> |
| **Total** | **100%** | **$99,165,000** | |

<!-- Completar: Redacta en una oración la cláusula de suspensión por mora.
     Ejemplo: "El retraso en el pago de cualquier cuota superior a ___ días hábiles habilitará al proveedor para..."
     
     Escribe aquí tu cláusula:
-->

**Cláusula de suspensión:** 

### 9.2 Garantía Post-Entrega

<!-- Completar: Redacta el párrafo de garantía para FerreMax GI.
     Recuerda incluir:
     - Número de días de garantía (pista: proyecto mediano = 30 días)
     - Qué SÍ cubre (solo bugs de programación)
     - Al menos 3 exclusiones específicas para este proyecto
     
     Usa el ejemplo de 1-teoria/02-tabla-costos-y-condiciones.md §5 como referencia.
-->

**Garantía:** 

**Exclusiones de la garantía:**
- 
- 
- 

### 9.3 Propiedad Intelectual

<!-- Completar: Redacta la cláusula de propiedad intelectual para FerreMax GI.
     Debe indicar:
     - A quién pertenece el código mientras no se pague el total (al proveedor)
     - Cuándo se transfiere (al completar el pago del 100%)
     - A quién se transfiere (FerreMax S.A.S.)
-->

**Propiedad intelectual:** 

### 9.4 Validez de la Oferta

Esta propuesta tiene validez hasta el **15 de diciembre de 2024** (30 días desde la fecha de emisión: 15 de noviembre de 2024).

---

## §12 Matriz de Riesgos

### Escala de Calificación

| Nivel | Probabilidad (P) | Impacto (I) | Nivel de riesgo (P×I) |
|---|---|---|---|
| 1 | Muy baja (~10%) | Muy bajo | 1–3: Bajo 🟢 |
| 2 | Baja (~25%) | Bajo | 4–7: Medio 🟡 |
| 3 | Media (~50%) | Moderado | 8–12: Alto 🟠 |
| 4 | Alta (~75%) | Alto | 13–25: Crítico 🔴 |
| 5 | Muy alta (~90%) | Muy alto | |

---

### Tabla de Riesgos Identificados

| ID | Descripción del riesgo | Categoría | P | I | P×I | Nivel | Estrategia | Acción concreta |
|---|---|---|---|---|---|---|---|---|
| R01 | El cliente solicita cambios en el alcance sin seguir el proceso formal | Gestión | 4 | 4 | 16 | 🔴 Crítico | Mitigar | Cláusula de control de cambios en el contrato (SP-05). Toda solicitud fuera del alcance §5 genera adenda de oferta firmada antes de ejecutarse. Revisión de alcance en cada reunión semanal con acta. |
| R02 | Un miembro del equipo abandona el proyecto antes de finalizar | Recursos | 2 | 5 | 10 | 🟠 Alto | Mitigar | Documentar el código semana a semana. Pair programming en módulos críticos. GitHub accesible para el cliente como observador. |
| R03 | El cliente no está disponible para validar entregables en el plazo acordado | Comunicación | 3 | 3 | 9 | 🟠 Alto | Mitigar | Designar representante técnico del cliente con ≥2h/semana disponibles. Plazo de aprobación: 3 días hábiles. Sin respuesta = aprobado tácitamente. Acta de reunión documenta cada validación. |
| R04 | Los datos en Excel del cliente tienen errores que complican la migración | Técnico | 3 | 4 | 12 | 🔴 Crítico | Mitigar | Auditoría de datos en Semana 1 con informe de calidad. Si errores >20%, se cotiza limpieza de datos como servicio adicional. |
| R05 | Falla en la infraestructura cloud (AWS) durante producción | Técnico | 2 | 3 | 6 | 🟡 Medio | Transferir | Responsabilidad de disponibilidad transferida a AWS (SLA 99.9%). Se configuran backups automáticos diarios. |
| R06 | El cliente incumple alguna cuota de pago acordada | Financiero | 2 | 5 | 10 | 🟠 Alto | Mitigar | Cláusula de suspensión ante mora >15 días hábiles. Notificación escrita previa a la suspensión. Reanudación tras regularización, sin penalización por el retraso. |
| R07 | <!-- Completar: describe el riesgo como evento incierto --> | <!-- Completar: categoría --> | <!-- P: 1-5 --> | <!-- I: 1-5 --> | <!-- P×I --> | <!-- Nivel --> | <!-- Estrategia --> | <!-- Completar: acción concreta y específica (no solo "monitorear") --> |
| R08 | <!-- Completar --> | <!-- Completar --> | <!-- --> | <!-- --> | <!-- --> | <!-- --> | <!-- --> | <!-- Completar --> |
| R09 | <!-- Completar --> | <!-- Completar --> | <!-- --> | <!-- --> | <!-- --> | <!-- --> | <!-- --> | <!-- Completar --> |
| R10 | <!-- Completar --> | <!-- Completar --> | <!-- --> | <!-- --> | <!-- --> | <!-- --> | <!-- --> | <!-- Completar --> |

---

### Top 3 Riesgos Críticos

<!-- Completar: Identifica los 3 riesgos con mayor puntaje P×I de la tabla anterior.
     Indica quién es responsable de gestionar cada uno.
     
     | Posición | ID | Descripción del riesgo | Nivel (P×I) | Responsable |
     |---|---|---|---|---|
     | 1 | | | | |
     | 2 | | | | |
     | 3 | | | | |
-->

| Posición | ID | Descripción del riesgo | Nivel (P×I) | Responsable |
|---|---|---|---|---|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |

---

## §13 Firma de Aceptación

Al firmar este documento, el cliente y el proveedor aceptan los términos técnicos, comerciales y las condiciones aquí establecidas.

| Rol | Nombre y cargo | Firma | Fecha |
|---|---|---|---|
| **Cliente** | <!-- Completar: nombre y cargo del gerente FerreMax --> | _________________________ | ___/___/___ |
| **Proveedor** | <!-- Completar: equipo + ficha SENA --> | _________________________ | ___/___/___ |

---

> 📋 **Checklist de verificación antes de entregar:**
> - [ ] Total de la tabla de costos = $99,165,000 COP
> - [ ] Tres cuotas suman exactamente $99,165,000 COP
> - [ ] Garantía incluye número de días y mínimo 3 exclusiones
> - [ ] R07 a R10 tienen categoría, P, I, nivel y acción concreta
> - [ ] Los niveles de riesgo están calculados correctamente (P×I)
> - [ ] El Top 3 identifica los riesgos de mayor puntaje
> - [ ] Campos de firma completados con datos de FerreMax

*Cadena de Formación · Tecnólogo ADSO · Semana 8 de 9 · Taller — Caso FerreMax*
