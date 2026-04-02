# 📚 Semana 06 — Estimación de Costos

> **Versión**: Cadena de Formación · Tecnólogo ADSO · Semana 6 de 9

---

## 🎯 Objetivos de Aprendizaje

Al finalizar esta semana serás capaz de:

- Identificar las categorías de costo de un proyecto de software (recurso humano, infraestructura, licencias, contingencia)
- Consultar y aplicar tarifas reales del mercado TI colombiano
- Construir una hoja de presupuesto estructurada para un proyecto de software
- Calcular el costo total de un proyecto incluyendo margen de ganancia y contingencia
- Integrar el presupuesto como sección de la propuesta técnica

---

## 📚 Requisitos Previos

Para aprovechar esta semana necesitas tener completados los entregables de:

- **Semana 3** — Documento de alcance (define QUÉ se va a construir)
- **Semana 4** — Estimación de esfuerzo (cuántos días-persona por módulo)
- **Semana 5** — Cronograma (cuántas semanas durará el proyecto)

Estos tres documentos son los insumos directos para construir el presupuesto.

---

## 🗂️ Estructura de la Semana

```
week-06-estimacion_de_costos/
├── 0-assets/              ← Diagramas SVG: categorías de costo, estructura presupuesto, tarifas TI
├── 1-teoria/              ← Teoría: categorías, tarifas Colombia, presupuesto, caso FerreMax
├── 2-practicas/           ← Taller guiado: construir presupuesto de FerreMax
├── 3-proyecto/            ← Entregable: presupuesto de tu proyecto real
├── 4-recursos/            ← Ebooks, videos y referencias
├── 5-glosario/            ← Términos clave de costos y presupuesto
├── README.md              ← Este archivo
└── rubrica-evaluacion.md  ← Criterios de evaluación
```

---

## 📝 Contenidos

| # | Archivo | Tema | Tiempo estimado |
|---|---------|------|----------------|
| T01 | `1-teoria/01-categorias-de-costo.md` | Qué tipos de costos tiene un proyecto de software | 25 min |
| T02 | `1-teoria/02-tarifas-mercado-ti-colombia.md` | Cuánto cobra un desarrollador en Colombia (2025) | 20 min |
| T03 | `1-teoria/03-estructura-presupuesto.md` | Cómo estructurar y presentar el presupuesto | 25 min |
| T04 | `1-teoria/04-caso-ferremax-presupuesto.md` | Presupuesto completo de FerreMax paso a paso | 30 min |
| P01 | `2-practicas/01-taller-presupuesto-ferremax/` | Taller guiado: construye el presupuesto de FerreMax | 2.5 h |
| E06 | `3-proyecto/starter/entregable-s06-presupuesto.md` | Presupuesto de tu proyecto real | 1.5 h |

---

## ⏱️ Distribución del Tiempo (6 horas)

| Actividad | Tiempo |
|-----------|--------|
| Lectura de teoría (T01–T04) | 1 h 40 min |
| Taller práctico FerreMax | 2 h 30 min |
| Entregable — presupuesto propio | 1 h 30 min |
| Revisión y ajuste | 20 min |
| **Total** | **6 horas** |

---

## 📌 Entregable

**Archivo**: `3-proyecto/starter/entregable-s06-presupuesto.md`  
**Nombre en la propuesta técnica**: *"Estimación de Costos del Proyecto"*

Debes entregar el presupuesto de tu proyecto real con:
- Tabla de costos por categoría (recurso humano, infraestructura, licencias, contingencia)
- Cálculos visibles (tarifa × horas o días)
- Subtotales por categoría
- Margen de ganancia y total final
- Supuestos del presupuesto

**Relación con semanas anteriores**: Los días-persona de la Semana 4 y el cronograma de la Semana 5 son los insumos directos de esta tabla.

---

## 🎓 Conceptos Clave

| Concepto | Descripción breve |
|----------|------------------|
| **Costo directo** | Gasto directamente asociado al desarrollo (salarios, infraestructura asignada al proyecto) |
| **Costo indirecto** | Gasto compartido entre varios proyectos (arriendo oficina, servicios, contabilidad) |
| **Recurso humano** | Mayor categoría de costo en software: salarios o tarifas de los desarrolladores y roles del equipo |
| **Contingencia** | Reserva del 10–15% para cubrir riesgos e imprevistos no estimados |
| **Margen de ganancia** | Porcentaje que se agrega al costo total para que la consultora/empresa genere utilidad (típico: 15–25%) |
| **Tarifa hora-consultor** | Precio por hora que cobra un desarrollador o consultor independiente en Colombia |
| **Presupuesto vs. cotización** | El presupuesto es interno (calcula el costo real); la cotización es lo que se presenta al cliente (incluye margen) |
| **Costo de infraestructura** | Servidores, hosting, dominio, SSL, licencias de base de datos o servicios cloud |
| **TCO (Total Cost of Ownership)** | Costo total de propiedad: incluye desarrollo + mantenimiento + operación a largo plazo |

---

## ✅ Checklist de Verificación

Antes de entregar tu documento de la semana 6, verifica:

- [ ] Incluiste todas las categorías de costo (no solo el recurso humano)
- [ ] Las tarifas que usaste son razonables para el mercado TI colombiano actual
- [ ] Los días-persona coinciden con tu `entregable-s04-estimacion.md`
- [ ] Calculaste una contingencia del 10–15%
- [ ] Agregaste un margen de ganancia justificado (si aplica)
- [ ] El total es coherente con el cronograma de la Semana 5

---

## 🔗 Navegación

| | Semana |
|--|--------|
| ← Anterior | [Semana 05 — Estimación de Esfuerzo y Tiempo](../week-05-estimacion_esfuerzo_y_tiempo/README.md) |
| → Siguiente | [Semana 07 — Redacción de la Propuesta Técnica](../week-07-redaccion_propuesta_tecnica/README.md) |

---

## 💡 Consejos para esta Semana

- **No subestimes la infraestructura**: El costo del servidor o del servicio en la nube es real y debe aparecer en el presupuesto, aunque sea una línea pequeña comparada con el recurso humano.
- **El 80% del costo de software es recurso humano**: Es normal. No te preocupes si tu tabla tiene una línea gigante de "Desarrollo" y el resto es pequeño.
- **Investiga tarifas reales**: Consulta portales como Computrabajo, LinkedIn Jobs y Freelancer.com.co para entender el mercado actual. Las tarifas cambian cada año.
- **Diferencia costo de cotización**: El presupuesto es lo que te cuesta a ti; la cotización es lo que le cobras al cliente. Aprende a distinguirlos.
- **Usa Google Sheets**: La hoja de presupuesto es más fácil de construir y revisar en una hoja de cálculo. Puedes exportarla como imagen o incrustarla en tu propuesta.

---

*Cadena de Formación · Tecnólogo ADSO · Semana 6 de 9*
