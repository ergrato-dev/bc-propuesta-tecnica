# Plantilla: Estimación de Módulos — FerreMax S.A.S.

**Aprendiz(ces):**  
**Ficha:**  
**Fecha:**  
**Instructor:**  

---

## 📋 Datos del proyecto

| Campo | Valor |
|-------|-------|
| Proyecto | FerreMax — Sistema de Gestión v1.0 |
| Cliente | Carlos Mendoza — FerreMax S.A.S., Bogotá |
| Semana de estimación | Semana 4 — Técnicas de Estimación |
| Técnicas aplicadas | T-shirt Sizing + Planning Poker |

---

## Paso 2: T-Shirt Sizing — Módulos A, B y D

### Referencia (ancla)

> **A.1 Inicio y cierre de sesión = M** (mediano)  
> *Formulario login + validación JWT + redirección por rol → 8 días de esfuerzo*

---

### Módulo A — Autenticación

<!-- 📝 Para cada ítem:
     1. Compara con A.1 (la referencia M = 8 días)
     2. Asigna talla: XS / S / M / L / XL
     3. Elige días dentro del rango de esa talla
     4. Escribe una frase de razonamiento (por qué esa talla)
     Escala: XS=1-2d | S=3-5d | M=6-10d | L=11-20d | XL=21-35d -->

| ID | Funcionalidad | Talla | Días | Razonamiento |
|----|--------------|-------|------|-------------|
| A.1 | Inicio y cierre de sesión | **M** | **8** | *Referencia base — login + JWT + redirect por rol* |
| A.2 | Gestión de usuarios (CRUD) | <!-- XS / S / M / L / XL --> | <!-- días --> | <!-- Razonamiento --> |
| A.3 | Asignación de roles | <!-- XS / S / M / L / XL --> | <!-- días --> | <!-- Razonamiento --> |

**Subtotal Módulo A:** _____ días

---

### Módulo B — Inventario

<!-- 📝 Recuerda que B.4 (Sincronización entre sedes) es un ítem complejo.
     ¿Qué talla asignarías considerando que debe funcionar en tiempo real entre dos sedes?
     Documenta bien el supuesto. -->

| ID | Funcionalidad | Talla | Días | Razonamiento |
|----|--------------|-------|------|-------------|
| B.1 | Registro y edición de productos | <!-- XS / S / M / L / XL --> | <!-- días --> | <!-- Razonamiento --> |
| B.2 | Control de stock (entradas y salidas) | <!-- XS / S / M / L / XL --> | <!-- días --> | <!-- Razonamiento --> |
| B.3 | Alertas de stock mínimo | <!-- XS / S / M / L / XL --> | <!-- días --> | <!-- Razonamiento --> |
| B.4 | Sincronización entre sedes | <!-- XS / S / M / L / XL --> | <!-- días --> | <!-- Razonamiento + supuesto clave --> |

**Subtotal Módulo B:** _____ días

**Supuesto para B.4:**
<!-- 📝 Documenta el supuesto principal de este ítem. Ejemplo:
     "Se asume que la latencia de sincronización aceptable es de X segundos." -->

> _

---

### Módulo D — Reportes

| ID | Funcionalidad | Talla | Días | Razonamiento |
|----|--------------|-------|------|-------------|
| D.1 | Reporte de ventas por período | <!-- XS / S / M / L / XL --> | <!-- días --> | <!-- Razonamiento --> |
| D.2 | Reporte de stock actual | <!-- XS / S / M / L / XL --> | <!-- días --> | <!-- Razonamiento --> |

**Subtotal Módulo D:** _____ días

---

## Paso 3: Planning Poker — Módulo C (Ventas)

### Ítems C.1 y C.2 — T-Shirt Sizing

| ID | Funcionalidad | Talla | Días | Razonamiento |
|----|--------------|-------|------|-------------|
| C.1 | Registro de ventas (punto de venta) | <!-- XS / S / M / L / XL --> | <!-- días --> | <!-- Razonamiento --> |
| C.2 | Historial de ventas con búsqueda | <!-- XS / S / M / L / XL --> | <!-- días --> | <!-- Razonamiento --> |

---

### Ítem C.3 — Factura Electrónica (Planning Poker)

**Historia a estimar:**
> *"El sistema debe generar facturas electrónicas válidas ante la DIAN. Debe integrarse con un PAC usando su API y funcionar en ambiente de producción."*

**Escala Fibonacci:** 1 · 2 · 3 · 5 · 8 · 13 · 21 · ?

#### Ronda 1 — Estimación individual

<!-- 📝 Si trabajas en grupo: cada persona elige su carta en secreto y la revela al mismo tiempo.
     Si trabajas solo: anota tu estimado "optimista" y tu estimado "pesimista".
     Escala Fibonacci: 1 / 2 / 3 / 5 / 8 / 13 / 21 / ? -->

| Participante / Perspectiva | Carta elegida | Supuesto detrás del número |
|---------------------------|--------------|---------------------------|
| <!-- Nombre o "Perspectiva optimista" --> | <!-- número Fibonacci --> | <!-- Qué asume esta estimación --> |
| <!-- Nombre o "Perspectiva pesimista" --> | <!-- número Fibonacci --> | <!-- Qué asume esta estimación --> |
| <!-- Nombre (si hay más) --> | <!-- número Fibonacci --> | <!-- Qué asume esta estimación --> |

**¿Hay diferencias significativas (2+ posiciones en la escala)?**  
<!-- Sí / No -->  
Si sí: ¿Cuál es la razón de la diferencia?  
> _

---

#### Discusión de diferencias

<!-- 📝 Describe brevemente qué descubrieron en la discusión.
     ¿Qué supuestos eran diferentes? ¿Qué aclararon? -->

> _

---

#### Ronda 2 — Estimación revisada

<!-- 📝 Con los nuevos supuestos claros, cada participante revisa su estimado. -->

| Participante / Perspectiva | Carta revisada |
|---------------------------|---------------|
| <!-- Nombre o "Perspectiva optimista" --> | <!-- número revisado --> |
| <!-- Nombre o "Perspectiva pesimista" --> | <!-- número revisado --> |
| <!-- Nombre (si hay más) --> | <!-- número revisado --> |

**Estimado de consenso (C.3):** _____ puntos → _____ días

**Supuesto clave de C.3:**
> _

---

### Subtotal Módulo C

| ID | Funcionalidad | Talla / Puntos | Días |
|----|--------------|----------------|------|
| C.1 | Registro de ventas | | |
| C.2 | Historial de ventas | | |
| C.3 | Factura electrónica | | |

**Subtotal Módulo C:** _____ días

---

## Paso 4: Tabla de Consolidación Final

<!-- 📝 Transfiere los valores de los pasos anteriores a esta tabla.
     Verifica que las sumas sean correctas. -->

| Módulo | Subcomponentes | Total días |
|--------|---------------|-----------|
| **A — Autenticación** | A.1 + A.2 + A.3 | _____ días |
| **B — Inventario** | B.1 + B.2 + B.3 + B.4 | _____ días |
| **C — Ventas** | C.1 + C.2 + C.3 | _____ días |
| **D — Reportes** | D.1 + D.2 | _____ días |
| | | |
| **TOTAL ESFUERZO** | | **_____ días** |

> 📌 Este es el **esfuerzo total estimado** (días de trabajo de un desarrollador).  
> No es la duración del proyecto en el calendario — eso lo calcularemos en la Semana 5.

---

## Paso 5: Preguntas de Reflexión

<!-- 📝 Responde con honestidad. No hay una única respuesta correcta.
     Se evalúa el razonamiento, no el número exacto. Mínimo 3 líneas por pregunta. -->

**Pregunta 1:** ¿Cuál fue el ítem más difícil de estimar? ¿Por qué?

> _

---

**Pregunta 2:** ¿Qué pasaría con el estimado si resulta que la sincronización entre sedes (B.4) necesita funcionar en tiempo real estricto (menos de 1 segundo)? ¿Cambiaría la talla? ¿En cuánto?

> _

---

**Pregunta 3:** Si el cliente te pregunta "¿por qué la factura electrónica tarda tanto?", ¿qué le responderías en términos no técnicos?

> _
