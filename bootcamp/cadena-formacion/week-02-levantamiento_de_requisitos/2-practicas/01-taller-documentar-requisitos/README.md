# 🛠️ Taller 01 — Documentar Requisitos desde una Reunión Real

> Práctica guiada · Semana 2 · Cadena de Formación
> Caso de estudio: **FerreMax S.A.S.**

---

## 🎯 Objetivo del Taller

Practicar la extracción y documentación de requisitos a partir de la transcripción de una reunión real con el cliente, usando el formato estándar de la propuesta técnica.

**Al finalizar el taller podrás:**
- Identificar requisitos funcionales y no funcionales dentro de una conversación
- Documentar requisitos con ID, descripción en formato correcto y prioridad
- Detectar requisitos ambiguos o incompletos y proponer preguntas de aclaración
- Completar un acta de reunión con los datos de la sesión

---

## ⏱️ Tiempo estimado: 2 horas

| Actividad | Tiempo |
|-----------|--------|
| Leer `transcripcion-primera-reunion.md` | 15 min |
| Paso 1: Identificar y clasificar requisitos | 35 min |
| Paso 2: Completar el documento de requisitos | 30 min |
| Paso 3: Detectar ambigüedades | 20 min |
| Paso 4: Completar el acta de reunión | 15 min |
| Revisión con el instructor | 5 min |

---

## 📋 Instrucciones Generales

1. Lee primero el documento `transcripcion-primera-reunion.md` completo — es la primera reunión con Carlos Mendoza de FerreMax (diferente a la segunda reunión que se ve en teoría)
2. Luego regresa a este archivo y completa cada paso en orden
3. Escribe tus respuestas **directamente en este archivo**, reemplazando los comentarios `<!-- Completar -->`
4. Usa también la plantilla `plantilla-acta-requisitos.md` para el paso 4

> 💡 **Importante:** La transcripción que leerás es la primera reunión — Carlos habla de manera informal, desordenada, como hablan los clientes reales. Tu trabajo es organizar y formalizar esa información.

---

## 📄 Paso 1: Identificar y Clasificar Requisitos

Lee la transcripción y extrae **todo lo que Carlos y sus empleados piden o mencionan** que el sistema debería hacer o cómo debería funcionar. Clasifica cada uno como RF o RNF.

**Ejemplo resuelto:**

| # | Cita textual (o paráfrasis) de la transcripción | Tipo | Requisito formalizado |
|---|------------------------------------------------|------|-----------------------|
| 1 | "Que cualquier vendedor pueda ver el inventario... desde cualquier sede" | RF | El sistema debe mostrar el inventario actualizado en tiempo real para todas las sedes |

**Tu turno — completa con todos los requisitos que encuentres:**

> 📌 Encontrarás al menos 10. Busca tanto los que Carlos pide explícitamente como los que se dan a entender por el contexto.

| # | Cita textual (o paráfrasis) | Tipo | Requisito formalizado |
|---|----------------------------|------|-----------------------|
| 2 | <!-- Completar: copia o resume lo que dijo en la reunión --> | <!-- RF / RNF --> | <!-- El sistema debe... --> |
| 3 | <!-- Completar --> | <!-- RF / RNF --> | <!-- El sistema debe... --> |
| 4 | <!-- Completar --> | <!-- RF / RNF --> | <!-- El sistema debe... --> |
| 5 | <!-- Completar --> | <!-- RF / RNF --> | <!-- El sistema debe... --> |
| 6 | <!-- Completar --> | <!-- RF / RNF --> | <!-- El sistema debe... --> |
| 7 | <!-- Completar --> | <!-- RF / RNF --> | <!-- El sistema debe... --> |
| 8 | <!-- Completar --> | <!-- RF / RNF --> | <!-- El sistema debe... --> |
| 9 | <!-- Completar --> | <!-- RF / RNF --> | <!-- El sistema debe... --> |
| 10 | <!-- Completar --> | <!-- RF / RNF --> | <!-- El sistema debe... --> |
| 11 | <!-- Completar: si encuentras más, agrégalos --> | <!-- RF / RNF --> | <!-- El sistema debe... --> |

---

## 📋 Paso 2: Completar el Documento de Requisitos

A partir de lo que identificaste en el paso 1, completa las tablas del documento de requisitos de FerreMax con el formato estándar (ID, descripción, prioridad).

**Requisitos Funcionales:**

**Ejemplo resuelto:**

| ID | Descripción | Prioridad |
|----|-------------|-----------|
| RF-001 | El sistema debe mostrar el inventario disponible en tiempo real para todas las sedes | Alta |

**Tu turno — completa con los RF que identificaste:**

| ID | Descripción | Prioridad |
|----|-------------|-----------|
| RF-002 | <!-- El sistema debe... --> | <!-- Alta / Media / Baja --> |
| RF-003 | <!-- El sistema debe... --> | <!-- Alta / Media / Baja --> |
| RF-004 | <!-- El sistema debe... --> | <!-- Alta / Media / Baja --> |
| RF-005 | <!-- El sistema debe... --> | <!-- Alta / Media / Baja --> |
| RF-006 | <!-- El sistema debe... --> | <!-- Alta / Media / Baja --> |

> 💡 **Recuerda:** La prioridad refleja lo que el CLIENTE considera más urgente, no lo que a ti te parezca más interesante de programar.

---

**Requisitos No Funcionales:**

**Ejemplo resuelto:**

| ID | Descripción | Categoría |
|----|-------------|-----------|
| RNF-001 | El sistema debe funcionar en celulares Android desde la versión 8.0 | Compatibilidad |

**Tu turno — completa con los RNF que identificaste:**

| ID | Descripción | Categoría |
|----|-------------|-----------|
| RNF-002 | <!-- Descripción del comportamiento esperado --> | <!-- Rendimiento / Seguridad / Usabilidad / Compatibilidad / Disponibilidad --> |
| RNF-003 | <!-- Completar --> | <!-- Categoría --> |
| RNF-004 | <!-- Completar --> | <!-- Categoría --> |

---

## 🔍 Paso 3: Detectar Ambigüedades

Identifica al menos **3 requisitos** de los que extraíste que tienen algún problema: son ambiguos, incompletos o podrían interpretarse de más de una manera.

Para cada uno, propone una pregunta de aclaración que harías al cliente.

**Ejemplo resuelto:**

| Requisito con problema | Tipo de problema | Pregunta de aclaración al cliente |
|------------------------|------------------|-----------------------------------|
| "El sistema debe ser fácil de usar" | Ambiguo — no es verificable | ¿Qué operación básica debería poder hacer un empleado sin capacitación? ¿En cuántos pasos máximo? |

**Tu turno — identifica 3 más:**

| Requisito con problema | Tipo de problema | Pregunta de aclaración al cliente |
|------------------------|------------------|-----------------------------------|
| <!-- Escribe el requisito problemático --> | <!-- Ambiguo / Incompleto / Contradictorio --> | <!-- ¿...? --> |
| <!-- Completar --> | <!-- Completar --> | <!-- ¿...? --> |
| <!-- Completar --> | <!-- Completar --> | <!-- ¿...? --> |

---

## 📝 Paso 4: Completar el Acta de Reunión

Abre el archivo `plantilla-acta-requisitos.md` y complétala con los datos de la transcripción. Necesitarás:
- Extraer los participantes mencionados
- Resumir los temas principales tratados en la reunión
- Listar los acuerdos informales que hicieron
- Identificar las preguntas que quedaron sin responder

> 📄 Cuando termines, el acta debe estar lista para enviarle por correo al cliente (Carlos Mendoza) para su confirmación.

---

## 💬 Reflexión Final

Responde con 2-3 oraciones cada pregunta:

**1. ¿Qué información de la transcripción fue la más difícil de convertir en un requisito formal? ¿Por qué?**

<!-- Escribe tu respuesta aquí -->

**2. Si pudieras hacer una segunda reunión con Carlos, ¿cuáles serían tus 3 preguntas más importantes?**

<!-- Escribe tus 3 preguntas aquí -->

**3. ¿Qué diferencias notas entre cómo Carlos describe lo que quiere y cómo lo escribiste tú como requisito formal?**

<!-- Escribe tu respuesta aquí -->

---

*Cadena de Formación · Tecnólogo ADSO · Semana 2 de 9*
