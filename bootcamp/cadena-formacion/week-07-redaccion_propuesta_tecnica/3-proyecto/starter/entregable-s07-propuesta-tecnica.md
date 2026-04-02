# PROPUESTA TÉCNICA — [Nombre de tu Proyecto]

<!-- 📝 Instrucciones de la portada:
     Reemplaza cada campo [entre corchetes] con los datos reales de tu proyecto.
     La portada identifica el documento: no debe quedar con campos vacíos. -->

| Campo | Valor |
|-------|-------|
| Nombre del documento | Propuesta Técnica |
| Nombre del proyecto | [Nombre del sistema que desarrollarás] |
| Versión | v1.0 |
| Fecha de emisión | [Fecha de hoy] |
| Válida hasta | [30 días después de hoy] |
| Cliente | [Nombre de la empresa o persona cliente] |
| Contacto cliente | [Nombre y cargo de la persona con quien negociarás] |
| Aprendiz | [Tu nombre completo] |
| Ficha SENA | [Número de tu ficha] |
| Instructor | [Nombre del instructor] |

---

## Control de Cambios

| Versión | Fecha | Descripción | Autor |
|---------|-------|-------------|-------|
| v0.1 | [Fecha] | Borrador inicial | [Tu nombre] |
| v1.0 | [Fecha] | Primera versión para entrega | [Tu nombre] |

---

## 1. Información General

<!-- 📝 Escribe 1 párrafo breve (3–5 oraciones) que presente el documento:
     quién lo elaboró, para quién va dirigido y cuál es su propósito.
     Ejemplo: "Este documento contiene la propuesta técnica elaborada por [tu nombre]
     en respuesta a la necesidad de [cliente] de contar con [descripción breve del sistema]." -->

[Tu párrafo de información general aquí]

---

## 2. Resumen Ejecutivo

<!-- 📝 Escribe 4 párrafos siguiendo exactamente esta estructura:
     Párrafo 1 → El problema del cliente: sitúa al lector en la situación actual
     Párrafo 2 → La solución que propones: qué vas a construir, con qué tecnologías
     Párrafo 3 → Cómo y cuánto tiempo: metodología simplificada + número de semanas + equipo
     Párrafo 4 → Precio total en COP + condiciones de pago más importantes
     Extensión: 200 a 350 palabras en total. Sin tecnicismos ni siglas sin definir.
     IMPORTANTE: El directivo del cliente debe poder entenderlo sin saber programación. -->

[Párrafo 1: El problema del cliente]

[Párrafo 2: La solución propuesta]

[Párrafo 3: Cómo y cuánto tiempo]

[Párrafo 4: Precio y condiciones]

---

## 3. Antecedentes y Análisis del Problema

### 3.1 Descripción de la organización cliente

<!-- 📝 Describe quién es el cliente: sector, tamaño, ciudad, años de operación, número de empleados.
     No más de 2–3 párrafos. Si es tu proyecto de formación, puedes usar un cliente ficticio real
     o una PYME conocida de tu entorno.
     Ejemplo: "[Cliente] es una empresa del sector [X] con [Y] años de operación en [ciudad]..." -->

[Tu descripción del cliente]

### 3.2 Situación actual

<!-- 📝 Describe cómo funciona actualmente el proceso que tu sistema va a mejorar.
     Usa la tabla de herramientas actuales: columna proceso, herramienta actual, problema que genera.
     No inventes; usa lo que levantaste en S02 (entrevista con el cliente). -->

En la actualidad, [nombre del cliente] gestiona sus operaciones con las siguientes herramientas:

| Proceso | Herramienta actual | Limitación identificada |
|---------|-------------------|------------------------|
| [Proceso 1] | [Herramienta] | [Problema concreto] |
| [Proceso 2] | [Herramienta] | [Problema concreto] |
| [Proceso 3] | [Herramienta] | [Problema concreto] |
| [Proceso 4] | [Herramienta] | [Problema concreto] |

### 3.3 Problemática identificada

<!-- 📝 Lista los problemas concretos con el formato P01, P02, P03, P04.
     Cada problema debe tener: código, nombre corto en negrita, descripción de 2–3 oraciones.
     Mínimo 3 problemas. Idealmente 4–5. Los problemas deben justificar el sistema que propones. -->

- **P01 — [Nombre del problema]**: [Descripción detallada del problema y su impacto en el negocio]
- **P02 — [Nombre del problema]**: [Descripción detallada]
- **P03 — [Nombre del problema]**: [Descripción detallada]
- **P04 — [Nombre del problema]**: [Descripción detallada — si aplica]

---

## 4. Propuesta de Solución Técnica

### 4.1 Descripción general de la solución

<!-- 📝 Describe en 2–3 párrafos el sistema que vas a construir en términos de negocio, no técnicos.
     Responde: ¿qué hace el sistema? ¿cómo lo va a usar el cliente? ¿qué cambia para el cliente?
     No uses jerga: "sistema ERP multi-tenant con microservicios" → "sistema web que permite
     gestionar el inventario desde cualquier punto de venta en tiempo real". -->

[Tu descripción general de la solución]

### 4.2 Módulos del sistema

<!-- 📝 Lista los módulos de tu sistema.
     Fuente: tu entregable S02 (lista de requisitos) y S03 (WBS).
     Por cada módulo: código (M1, M2...), nombre, descripción de 1 oración, usuarios que lo usan.
     Mínimo 4 módulos. -->

| Módulo | Descripción funcional | Usuarios que lo usan |
|--------|----------------------|---------------------|
| M1 — [Nombre] | [Descripción] | [Usuarios] |
| M2 — [Nombre] | [Descripción] | [Usuarios] |
| M3 — [Nombre] | [Descripción] | [Usuarios] |
| M4 — [Nombre] | [Descripción] | [Usuarios] |
| M5 — [Nombre] | [Descripción si aplica] | [Usuarios] |

### 4.3 Stack tecnológico propuesto

<!-- 📝 Lista las tecnologías que usarás.
     Para cada una: capa (backend, BD, frontend, infraestructura), tecnología y justificación clara.
     Justificación = por qué es adecuada para este proyecto específico (no copiar de la teoría). -->

| Capa | Tecnología | Justificación para tu proyecto |
|------|-----------|-------------------------------|
| Backend | [Tecnología] | [Justificación] |
| Base de datos | [Tecnología] | [Justificación] |
| Frontend | [Tecnología] | [Justificación] |
| Infraestructura | [Tecnología] | [Justificación] |

### 4.4 Arquitectura general

<!-- 📝 Describe en 3–5 oraciones cómo se conectan los componentes.
     No necesitas un diagrama complejo — una descripción textual clara es suficiente para S07.
     Incluye: tipo de arquitectura (cliente-servidor, monolítica, etc.), cómo se comunican
     las capas, dónde está alojado, cómo se gestiona la seguridad. -->

[Tu descripción de la arquitectura]

---

## 5. Alcance del Proyecto

### 5.1 Funcionalidades incluidas en el precio

<!-- 📝 Lista todo lo que sí está incluido en el desarrollo.
     Fuente directa: tu entregable S03 (documento de alcance).
     Sé específico: no "módulo de usuario" sino "módulo de usuario con registro, login,
     gestión de permisos y recuperación de contraseña".
     Incluye también: número de sesiones de inducción, días de garantía, tipo de despliegue. -->

Este contrato incluye el desarrollo e implementación de las siguientes funcionalidades:

- [Funcionalidad 1 específica]
- [Funcionalidad 2 específica]
- [Funcionalidad 3 específica]
- [Módulo N — descripción específica]
- Despliegue en ambiente de producción ([plataforma de hosting])
- [X] sesiones de inducción para el equipo del cliente
- [X] días de garantía de corrección de defectos post-entrega

### 5.2 Fuera del alcance

<!-- 📝 Lista lo que NO está incluido. Esto es tan importante como la lista anterior.
     Los ítems fuera del alcance evitan discusiones futuras con el cliente.
     Mínimo 4 ítems concretos y relevantes para tu tipo de sistema. -->

Las siguientes funcionalidades y servicios **no están incluidos** en el precio de esta propuesta:

- [Ítem fuera del alcance 1]
- [Ítem fuera del alcance 2]
- [Ítem fuera del alcance 3]
- [Ítem fuera del alcance 4]
- Soporte técnico mensual posterior al período de garantía (cotizable aparte)

---

## 6. Metodología de Desarrollo

<!-- 📝 Describe el enfoque de trabajo: ¿iterativo? ¿por fases? ¿con entregas parciales?
     Completa la tabla de fases con las semanas de tu cronograma (de S05).
     También describe herramientas de comunicación y control con el cliente. -->

El proyecto se ejecutará mediante una metodología [iterativa / por fases / ágil simplificada] con entregas parciales para validación del cliente.

| Fase | Semanas | Actividades principales | Entregable al cliente |
|------|---------|------------------------|----------------------|
| Fase 1 — Inicio | [S1] | [Actividades] | [Entregable] |
| Fase 2 — [Nombre] | [Sx–Sy] | [Actividades] | [Entregable] |
| Fase 3 — [Nombre] | [Sx–Sy] | [Actividades] | [Entregable] |
| Fase 4 — [Nombre] | [Sx–Sy] | [Actividades] | [Entregable] |
| Fase 5 — Entrega final | [S final] | Despliegue, inducción, entrega código | Sistema en producción + código fuente |

---

## 7. Cronograma

<!-- 📝 Fuente directa: tu entregable S05 (cronograma).
     Presenta la tabla de semanas con las actividades principales y los hitos clave.
     No necesitas copiar el Gantt completo — resume las semanas más importantes.
     Incluye las fechas de inicio y entrega estimadas. -->

El proyecto tiene una duración total de **[X] semanas** a partir de la firma del contrato.

| Semana(s) | Actividad principal | Hito |
|-----------|--------------------|----|
| S1 | [Actividad] | ✓ [Hito si aplica] |
| [Sx–Sy] | [Actividad módulo X] | |
| [S de revisión] | [Revisión con cliente] | ✓ [Aprobación] |
| [S final] | [Entrega y despliegue] | ✓ Entrega final |

**Fecha de inicio estimada**: [fecha]  
**Fecha de entrega estimada**: [fecha]

---

## 8. Estimación de Costos

<!-- 📝 Fuente directa: tu entregable S06 (presupuesto).
     Presenta la tabla ejecutiva de costos (no el presupuesto interno con tarifas).
     Incluye: concepto → valor COP. Y la tabla de condiciones de pago.
     El total debe coincidir EXACTAMENTE con el de tu entregable S06. -->

El costo total del proyecto es el resultado de la estimación detallada realizada en la Semana 6.

| Concepto | Valor (COP) |
|----------|-------------|
| Desarrollo del sistema ([X] módulos) | $[Valor] |
| Infraestructura y servicios | $[Valor] |
| Gestión del proyecto | $[Valor] |
| Reserva técnica y contingencia | $[Valor] |
| **TOTAL PROPUESTA** | **$[Total de S06]** |
| IVA (si aplica) | A convenir |

**Condiciones de pago**:

| Momento | Porcentaje | Valor aproximado |
|---------|------------|-----------------|
| Anticipo (firma del contrato) | 30% | $[30% del total] |
| Entrega hitos intermedios | 40% | $[40% del total] |
| Entrega final | 30% | $[30% del total] |
| **Total** | **100%** | **$[Total]** |

---

## 9. Equipo del Proyecto

<!-- 📝 Lista los perfiles del equipo con rol, experiencia y dedicación.
     Para un proyecto de formación individual: puedes listar tus propias habilidades
     o presentar el equipo como "1 desarrollador junior con perfil full-stack".
     Incluye: nombre del perfil, rol, tecnologías que domina, % de dedicación. -->

| Perfil | Rol en el proyecto | Tecnologías | Dedicación |
|--------|--------------------|-------------|------------|
| [Perfil 1] | [Rol] | [Tecnologías] | [%] |
| [Perfil 2 si aplica] | [Rol] | [Tecnologías] | [%] |

[Párrafo breve describiendo la experiencia del equipo relevante para este proyecto]

---

## 10. Supuestos, Condiciones y Firma

### 10.1 Supuestos del proyecto

<!-- 📝 Lista los supuestos de tu proyecto.
     Fuente: usa los supuestos de tu entregable S06 + agrega supuestos técnicos y de negocio.
     Mínimo 4 supuestos. Cada uno debe ser específico para tu proyecto (no genérico). -->

| ID | Supuesto |
|----|----------|
| SP-01 | [Supuesto específico de tu proyecto — cliente proporciona X] |
| SP-02 | [Supuesto de infraestructura o tecnología] |
| SP-03 | [Supuesto de tiempos de respuesta del cliente] |
| SP-04 | [Supuesto sobre el alcance — qué no cambia sin adenda] |
| SP-05 | [Supuesto adicional relevante para tu contexto] |

### 10.2 Condiciones comerciales

- **Validez de la propuesta**: 30 días calendario desde la fecha de emisión.
- **Cambios de alcance**: Cualquier funcionalidad fuera de la Sección 5.1 requiere adenda escrita y puede implicar ajuste de precio y cronograma.
- **Propiedad del código**: Al realizar el pago total, el cliente recibirá el código fuente con licencia de uso perpetuo.
- **Confidencialidad**: Ambas partes acuerdan mantener la confidencialidad de la información compartida durante el proyecto.

### 10.3 Firma de aceptación

```
ACEPTACIÓN DE LA PROPUESTA TÉCNICA

Cliente
Nombre completo:  ______________________________
Cargo:            ______________________________
Empresa:          ______________________________
Fecha:            ______________________________
Firma:            ______________________________

Proveedor / Aprendiz
Nombre completo:  ______________________________
Ficha SENA:       ______________________________
Fecha:            ______________________________
Firma:            ______________________________
```

---

*Cadena de Formación · Tecnólogo ADSO · Semana 7 de 9*
