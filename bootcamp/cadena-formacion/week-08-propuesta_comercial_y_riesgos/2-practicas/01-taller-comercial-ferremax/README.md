# 🛠️ Taller — Propuesta Comercial y Riesgos: FerreMax GI

> **Versión**: Cadena de Formación · Semana 8  
> **Tiempo estimado**: 2 horas 20 minutos  
> **Modalidad**: Individual o en parejas  
> **Archivo de trabajo**: `plantilla-propuesta-comercial-ferremax.md`

---

## 📋 Contexto del Caso

El equipo DevSoft ADSO ya entregó la propuesta técnica de FerreMax GI (Semana 7). Ahora el gerente **Andrés Morales** solicita el complemento comercial antes de tomar la decisión de contratar:

> *"El documento técnico quedó muy bien. Ahora necesito ver claro cuánto voy a pagar, cuándo, y qué pasa si algo sale mal con el proyecto."*

Este taller completa el documento con la sección comercial completa y la matriz de riesgos.

---

## 🎯 Pasos del Taller

---

### Paso 1: Construcción de la Tabla de Costos Final (25 min)

**Contexto:**
El presupuesto interno del equipo (Semana 6) resultó en un total de **$99,165,000 COP**. Ahora debes construir la versión para el cliente — sin mostrar tarifas por hora.

**Ejemplo resuelto (2 de 5 categorías):**

| Categoría | Descripción | Valor COP |
|---|---|---|
| Desarrollo de software | Ingeniería, programación y pruebas | $74,528,000 |
| Gestión de proyecto | Coordinación, reuniones, documentación | $8,120,000 |
| ... | ... | ... |

**Tu turno:**
Abre `plantilla-propuesta-comercial-ferremax.md` y completa:
- Las **3 categorías faltantes** de la tabla de costos (infraestructura, contingencia, utilidad)
- Los **montos en COP** de cada categoría (guíate con los datos del presupuesto de S06)
- Verifica que el **total sea $99,165,000 COP**

> 📌 Recuerda: La tabla del cliente NO muestra tarifas por hora ni costos de salario. Solo categorías generales.

---

### Paso 2: Redacción de las Condiciones de Pago (20 min)

**Contexto:**
FerreMax GI usa el esquema 30/40/30. Las condiciones de pago deben especificar no solo los porcentajes, sino también los **montos exactos en COP** y el **hito o momento** que activa cada cuota.

**Ejemplo resuelto (primera cuota):**

| Cuota | Porcentaje | Valor COP | Momento de pago |
|---|---|---|---|
| Anticipo | 30% | $29,749,500 | Al firmar el contrato |
| ... | ... | ... | ... |

**Tu turno:**
Completa en la plantilla:
- La **segunda cuota** (40%)  — calcula el monto y define el hito que la activa
- La **tercera cuota** (30%) — calcula el monto y define el hito que la activa
- Redacta en una oración la cláusula de suspensión por mora

---

### Paso 3: Garantía y Propiedad Intelectual (15 min)

**Contexto:**
FerreMax GI es un sistema mediano con 6 módulos y 15 semanas de desarrollo. Define el período de garantía apropiado y redacta la cláusula de propiedad intelectual.

**Referencia:**
- Proyectos de 4–6 módulos → garantía recomendada: **30 días**
- La propiedad intelectual se transfiere al **pagar el 100%**

**Tu turno:**
Completa en la plantilla:
- El párrafo de **garantía** con el número de días y las exclusiones mínimas (mínimo 3 exclusiones)
- El párrafo de **propiedad intelectual** indicando a quién pertenece el código y cuándo se transfiere

---

### Paso 4: Análisis de Riesgos — Completar 4 Riesgos Propios (45 min)

**Contexto:**
La plantilla ya tiene 6 riesgos documentados (R01 al R06). Tu misión es identificar y documentar **4 riesgos adicionales** (R07 al R10) del proyecto FerreMax GI que no estén ya cubiertos.

**Pistas de riesgos que podrías identificar:**
- ¿Qué pasa si el volumen de datos en Excel es mayor al esperado?
- ¿Qué pasa si el sistema tiene problemas de rendimiento con 3 sucursales?
- ¿Qué pasa si hay un cambio normativo (DIAN)?
- ¿Qué pasa si algún módulo resulta más complejo de lo estimado?

**Ejemplo resuelto (R06 ya dado):**

| ID | Descripción | Categoría | P | I | P×I | Nivel | Estrategia | Acción concreta |
|---|---|---|---|---|---|---|---|---|
| R06 | El cliente incumple alguna cuota de pago | Financiero | 2 | 5 | 10 | 🟠 Alto | Mitigar | Cláusula de suspensión ante mora >15 días hábiles; se notifica por escrito antes de pausar el proyecto |

**Tu turno:**
Completa en la plantilla las filas **R07, R08, R09, R10** con:
- Descripción clara del riesgo como evento
- Categoría (Técnico / Gestión / Comunicación / Financiero / Recursos / Externo)
- Probabilidad (1–5) e impacto (1–5) con justificación
- Nivel calculado (P×I) y clasificación
- Estrategia y acción concreta (no escribas solo "monitorear")

---

### Paso 5: Priorización de Riesgos (15 min)

**Contexto:**
Una vez que tienes la tabla completa (10 riesgos), debes identificar cuáles son los **3 más críticos** y proponer a quién se le asigna la responsabilidad de gestionar cada uno.

**Ejemplo resuelto:**

| Posición | ID | Riesgo | Nivel | Responsable |
|---|---|---|---|---|
| 1 | R01 | Cambios en el alcance | 🔴 Crítico (16) | Dev A + cliente |

**Tu turno:**
Completa en la plantilla la tabla de **"Top 3 Riesgos"** con los 3 riesgos de mayor puntaje P×I de tu tabla completa.

---

### Paso 6: Firma de Aceptación (5 min)

**Contexto:**
El documento cierra con los campos de firma. Completa los datos del documento en la plantilla.

**Tu turno:**
Completa en la plantilla:
- Datos de la firma del cliente (nombre y cargo de Andrés Morales)
- Datos de la firma del proveedor (equipo, ficha SENA)

---

### Paso 7: Verificación de Coherencia (15 min)

Antes de "entregar" el documento al instructor, verifica:

| Verificación | ✅ OK | ❌ Revisar |
|---|---|---|
| Total de la tabla de costos = $99,165,000 COP | | |
| Anticipo (30%) = $29,749,500 COP | | |
| Segundo pago (40%) = $39,666,000 COP | | |
| Tercer pago (30%) = $29,749,500 COP | | |
| Suma de las 3 cuotas = $99,165,000 COP | | |
| La garantía dice exactamente cuántos días y qué excluye | | |
| R07 a R10 tienen estrategia y acción concreta (no solo "monitorear") | | |
| Todos los niveles de riesgo están calculados correctamente (P×I) | | |

---

## 💡 Consejos para el Taller

- La **tabla de costos** no es difícil de calcular si tienes el presupuesto de S06 a la mano. Recuerda que la contingencia es el 10% del desarrollo y la utilidad el 15% del total antes de utilidad.
- Los **riesgos más reales** no son los más obvios (como "se puede romper el servidor"). Los más frecuentes en proyectos reales son de **comunicación** (cliente no disponible) y **gestión** (cambios de alcance).
- Una estrategia de riesgo **siempre incluye un responsable**. No basta con decir qué hacer — hay que saber quién lo hace.

---

## 📁 Archivos de Este Taller

```
01-taller-comercial-ferremax/
├── README.md                               ← Este archivo (instrucciones)
└── plantilla-propuesta-comercial-ferremax.md  ← Plantilla con placeholders
```

---

*Cadena de Formación · Tecnólogo ADSO · Semana 8 de 9*
