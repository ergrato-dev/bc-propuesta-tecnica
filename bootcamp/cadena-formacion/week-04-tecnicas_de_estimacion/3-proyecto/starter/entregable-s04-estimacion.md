# Entregable S04 — Estimación del Sistema

**Nombre del proyecto:**  
**Aprendiz:**  
**Ficha:**  
**Instructor:**  
**Fecha:**  
**Semana:** 4 de 9 — Técnicas de Estimación

---

## 1. Resumen del Proyecto

<!-- 📝 Copia el nombre y la descripción breve de tu proyecto (de tu entregable S01 o S02).
     En 2-3 líneas: ¿qué hace el sistema? ¿para quién? -->

**Nombre del sistema:**  
**Cliente / usuario principal:**  
**Descripción en una línea:**  

---

## 2. WBS Base para la Estimación

<!-- 📝 Lista los módulos y subcomponentes de tu WBS (entregable S03).
     Si tu WBS tiene más de 3 niveles, usa solo los niveles 1 y 2 aquí.
     Si no tienes WBS todavía, lista las funcionalidades principales que conozcas.
     Formato: usa viñetas con sangría para los subcomponentes. -->

<!-- Ejemplo:
- Módulo 1: Autenticación
  - 1.1 Inicio de sesión
  - 1.2 Cierre de sesión
  - 1.3 Gestión de roles
- Módulo 2: Gestión de productos
  - 2.1 Registro de productos
  ...
-->

- Módulo 1:
  -
  -
- Módulo 2:
  -
  -
- Módulo 3:
  -
  -

<!-- Agrega más módulos según necesites. -->

---

## 3. T-Shirt Sizing — Todos los Módulos

<!-- 📝 Aplica T-shirt sizing a CADA subcomponente de tu WBS.
     
     Pasos:
     1. Define tu ítem de referencia "M" (escríbelo debajo de la tabla)
     2. Compara cada ítem con esa referencia
     3. Asigna talla: XS / S / M / L / XL
     4. Elige un número de días dentro del rango
     5. Escribe mínimo una frase de razonamiento por ítem
     
     Escala de conversión:
     XS = 1–2 días | S = 3–5 días | M = 6–10 días | L = 11–20 días | XL = 21–35 días -->

**Mi ítem de referencia M es:**
<!-- Ejemplo: "El formulario de registro de usuarios con validaciones = M" -->  
>

---

| ID | Funcionalidad | Talla | Días | Razonamiento |
|----|--------------|-------|------|-------------|
| | | | | |
| | | | | |
| | | | | |
| | | | | |
| | | | | |
| | | | | |
| | | | | |
| | | | | |

<!-- Agrega más filas según la cantidad de ítems en tu WBS. -->

---

## 4. Segunda Técnica — Módulo más complejo

<!-- 📝 Identifica el módulo o subcomponente que más incertidumbre te genera.
     Aplica UNA de las dos técnicas: Analogía O Planning Poker.
     
     Elige Analogía si:
     - Tienes experiencia con un proyecto similar
     - Puedes comparar tu módulo con algo que ya desarrollaste
     
     Elige Planning Poker si:
     - Tienes al menos 1 compañero/a para hacer la sesión
     - El ítem es técnicamente nuevo para ti -->

**Módulo seleccionado para segunda técnica:**  
**Técnica elegida:** [  ] Analogía   [  ] Planning Poker  

---

### Opción A — Analogía

<!-- 📝 Completa esta sección SOLO si elegiste Analogía -->

**Proyecto de referencia:**  
<!-- Nombra el proyecto similar que usas como base. Puede ser: algo que desarrollaste en el SENA,
     un proyecto de práctica, un sistema que conoces de cerca. -->

| Campo | Proyecto referencia | Mi proyecto |
|-------|---------------------|-------------|
| Nombre del proyecto | | |
| Tipo de sistema | | |
| Módulo comparable | | |
| Duración real del módulo referencia | | — |

**Diferencias encontradas:**

| Aspecto | Proyecto referencia | Mi proyecto | Impacto (+/−%) |
|---------|---------------------|-------------|----------------|
| | | | |
| | | | |

**Cálculo:**

```
Base (proyecto referencia):   _____ días
Ajustes:
  +/- ______________:         _____ días
  +/- ______________:         _____ días

Estimado ajustado:            _____ días
```

**Supuesto principal de esta analogía:**
> _

---

### Opción B — Planning Poker

<!-- 📝 Completa esta sección SOLO si elegiste Planning Poker -->

**Historia / funcionalidad a estimar:**
> _

**Escala Fibonacci:** 1 · 2 · 3 · 5 · 8 · 13 · 21 · ?

#### Ronda 1

| Participante | Carta elegida | Supuesto |
|-------------|--------------|---------|
| | | |
| | | |

**¿Hubo diferencias? ¿Qué las explica?**
> _

#### Ronda 2 (si hubo diferencias)

| Participante | Carta revisada |
|-------------|---------------|
| | |
| | |

**Estimado de consenso:** _____ puntos → _____ días  
**Supuesto principal:**
> _

---

## 5. Tabla de Estimación Consolidada

<!-- 📝 Transfiere los valores de las secciones 3 y 4 a esta tabla resumen.
     Verifica que las sumas sean correctas.
     Si aplicaste la segunda técnica a un módulo, usa ese valor (no el de T-shirt sizing) para ese módulo. -->

| Módulo | Total días (T-shirt) | Ajuste 2da técnica | Total final |
|--------|---------------------|-------------------|------------|
| Módulo 1: | | — | |
| Módulo 2: | | | |
| Módulo 3: | | — | |
| | | | |
| **TOTAL ESFUERZO** | | | **_____ días** |

> 📌 Este total representa el **esfuerzo estimado** de desarrollo (días de trabajo de un desarrollador).  
> En la Semana 5 convertiremos esto en duración real del proyecto.

---

## 6. Supuestos Documentados

<!-- 📝 Lista TODOS los supuestos importantes de tu estimación.
     Un supuesto es una condición que asumes verdadera para que el estimado sea válido.
     Si el supuesto cambia, el estimado cambia también.
     Incluye mínimo 4 supuestos. -->

<!-- Ejemplo:
     "S-001: Se asume que el cliente ya tiene un proveedor de hosting contratado."
     "S-002: Se asume que la integración con la DIAN usa Alegra como PAC." -->

| ID | Supuesto | Módulo afectado | Si no se cumple… |
|----|----------|----------------|-----------------|
| S-001 | | | |
| S-002 | | | |
| S-003 | | | |
| S-004 | | | |

---

## 7. Reflexión Personal

<!-- 📝 Responde estas preguntas con al menos 2 oraciones cada una.
     No hay respuesta incorrecta; se evalúa tu proceso de razonamiento. -->

**¿Cuál fue el módulo más difícil de estimar? ¿Por qué?**

> _

**¿Qué información adicional sobre tu proyecto te ayudaría a hacer una estimación más precisa?**

> _

**¿Cómo presentarías este estimado a tu cliente para que confíe en él?**

> _
