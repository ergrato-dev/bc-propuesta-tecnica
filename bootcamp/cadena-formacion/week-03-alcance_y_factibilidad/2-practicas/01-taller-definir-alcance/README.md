# Taller 01 — Definir el Alcance de un Proyecto de Software

> **Tipo de actividad**: Práctica guiada sobre el caso de estudio FerreMax
> **Tiempo estimado**: 2 horas
> **Materiales**: Este README + `plantilla-alcance-ferremax.md`

---

## 🎯 Objetivos del Taller

Al completar este taller, el aprendiz será capaz de:

1. Redactar una declaración de alcance (in scope y out of scope) a partir de una lista de requisitos
2. Construir una lista de entregables del proyecto
3. Elaborar un WBS básico de 2 niveles para un sistema de software
4. Evaluar la factibilidad técnica y operativa con criterios concretos

---

## 🗂️ Archivos del Taller

| Archivo | Descripción |
|---------|-------------|
| `README.md` | Instrucciones del taller (este archivo) |
| `plantilla-alcance-ferremax.md` | Plantilla parcialmente resuelta — tú completas las secciones indicadas |

---

## 📋 Contexto del Caso

Eres un consultor junior que acaba de terminar el levantamiento de requisitos con Carlos Mendoza, gerente de FerreMax S.A.S. (ferretería, 2 sedes en Bogotá, ~25 empleados).

La sesión de Semana 2 produjo una lista de 13 requisitos funcionales y 8 no funcionales. Ahora tu tarea es:

1. Decidir cuáles entran en la versión 1 del sistema y cuáles quedan para una fase 2
2. Documentar el alcance en formato propuesta técnica
3. Construir el WBS del sistema
4. Evaluar si el proyecto es factible

**Lee los requisitos de referencia en [`1-teoria/04-caso-ferremax-alcance.md`](../../1-teoria/04-caso-ferremax-alcance.md) antes de continuar.**

---

## 📝 Instrucciones Paso a Paso

### Paso 1: Clasificar los Requisitos (20 min)

Abre la `plantilla-alcance-ferremax.md` y ve a la **Sección 1 — Clasificación de Requisitos**.

Recibirás una tabla con todos los requisitos de FerreMax. Tu tarea es clasificar cada uno:
- ✅ **Versión 1**: entra en el alcance actual
- ⏳ **Versión 2**: queda para una fase futura
- ❓ **Necesita clarificación**: no hay suficiente información para decidir

**Criterio para clasificar:**
- Prioridad Alta en S02 → candidato para versión 1
- Prioridad Media → analiza si encaja en el tiempo y presupuesto disponibles
- Prioridad Baja → generalmente va a versión 2

**Ejemplo resuelto:**

| ID | Requisito | Decisión | Justificación |
|----|-----------|---------|---------------|
| RF-001 | Registrar y gestionar productos | ✅ Versión 1 | Prioridad Alta — es el núcleo del sistema |
| RF-013 | Exportar reportes a PDF/Excel | ⏳ Versión 2 | Prioridad Baja — la consulta en pantalla cubre la necesidad inmediata |

**Tu turno**: Clasifica los RF-002 al RF-012 en la plantilla.

---

### Paso 2: Redactar el In Scope y Out of Scope (25 min)

Ve a la **Sección 2 — Declaración de Alcance** de la plantilla.

Con base en tu clasificación del Paso 1, redacta:

**2.1. In Scope** — Lista los módulos o funcionalidades que confirmas para la versión 1. Sé específico: no escribas "módulo de inventario" genérico, escribe qué hace ese módulo.

**Ejemplo resuelto:**
```
| 1 | Módulo de Autenticación: acceso con usuario/contraseña; roles administrador y vendedor |
```

**Tu turno**: Completa la lista in scope con los módulos que decidiste incluir.

**2.2. Out of Scope** — Lista lo que explícitamente NO entra, con justificación breve.

**Ejemplo resuelto:**
```
| 1 | Exportación de reportes a PDF | Baja prioridad — consulta en pantalla cubre la necesidad inmediata |
```

**Tu turno**: Completa la lista out of scope con al menos 4 ítems y su justificación.

---

### Paso 3: Lista de Entregables (20 min)

Ve a la **Sección 3 — Lista de Entregables** de la plantilla.

Recuerda: un entregable es un resultado concreto y verificable. Incluye tanto software como documentación.

**Ejemplo resuelto:**
```
| E-001 | Módulo de inventario funcional | Software | El stock de un producto se actualiza al registrar una venta |
```

**Tu turno**: Completa la lista con al menos 6 entregables (4 de software + 2 de documentación).

---

### Paso 4: WBS Básico (30 min)

Ve a la **Sección 4 — WBS Básico** de la plantilla.

Construye el WBS del sistema FerreMax con 2 niveles, usando la estructura de módulos.

**Ejemplo de Nivel 1 y 2 para el módulo de Ventas:**
```
4. Módulo de Ventas
   4.1 Formulario de nueva venta
   4.2 Cálculo automático de total
   4.3 Registro de venta (actualiza inventario)
```

**Tu turno**: Completa el WBS para los módulos 1 (Autenticación), 2 (Inventario) y 3 (Clientes). El módulo de Ventas ya está resuelto como ejemplo.

---

### Paso 5: Análisis de Factibilidad (25 min)

Ve a la **Sección 5 — Factibilidad** de la plantilla.

Evalúa los tres tipos de factibilidad para el proyecto FerreMax:

**5.1. Factibilidad Técnica** — Usa la tabla con los criterios: tecnología, habilidades, infraestructura, complejidad, tiempo.

**Ejemplo resuelto:**
```
| Tecnología | Python/FastAPI — open source, amplia documentación | ✅ Viable |
```

**Tu turno**: Completa los otros 4 criterios de factibilidad técnica.

**5.2. Factibilidad Operativa** — Evalúa: disposición del cliente, nivel técnico, equipos, conectividad.

**5.3. Conclusión** — Con base en las evaluaciones anteriores, escribe un párrafo de 3-4 oraciones con tu conclusión de viabilidad.

---

### Paso 6: Restricciones y Supuestos (opcional — 15 min adicionales)

Si terminaste los pasos 1-5 antes del tiempo estimado, aborda la **Sección 6 — Restricciones y Supuestos**.

Lista al menos 3 restricciones y 3 supuestos del proyecto FerreMax basándote en la información disponible. Usa el formato de tabla de la plantilla.

---

## ✅ Criterios de Calidad del Taller

Antes de entregar al instructor, verifica:

- [ ] Todos los 13 RF están clasificados (versión 1, versión 2 o necesita clarificación)
- [ ] El in scope tiene al menos 5 módulos/funcionalidades claramente descritos
- [ ] El out of scope tiene al menos 4 ítems con justificación
- [ ] La lista de entregables tiene al menos 6 ítems (4 software + 2 docs)
- [ ] El WBS tiene al menos 3 módulos con nivel 2 completo
- [ ] La factibilidad técnica evalúa los 5 criterios propuestos
- [ ] Hay una conclusión de factibilidad redactada en párrafo
- [ ] Las secciones no tienen `<!-- Completar -->` sin responder

---

## 💬 Para Pensar y Reflexionar

Después de completar la plantilla, reflexiona sobre estas preguntas:

1. ¿Hubo algún requisito que dudaste si incluirlo en versión 1 o versión 2? ¿Cuál fue tu criterio final?
2. Si Carlos te dijera "quiero que también incluya la facturación electrónica DIAN" después de firmar el alcance, ¿qué le responderías?
3. ¿Qué pasaría si no documentas el out of scope y al final del proyecto el cliente reclama una funcionalidad que no construiste?

---

*Siguiente: [3-proyecto — Entregable para tu proyecto real →](../../3-proyecto/README.md)*
