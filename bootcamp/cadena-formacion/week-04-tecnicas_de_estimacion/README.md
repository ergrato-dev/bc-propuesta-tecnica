# 📚 Semana 04 — Estimar sin Adivinar: Técnicas de Estimación

> **Versión**: Cadena de Formación · Técnico en Programación → Tecnólogo ADSO

---

## 🎯 Objetivos de Aprendizaje

Al finalizar esta semana, el aprendiz será capaz de:

1. Explicar por qué estimar es necesario y cuáles son sus limitaciones
2. Aplicar al menos 3 técnicas de estimación cualitativa: analogía, Delphi, T-shirt sizing
3. Facilitar una sesión de Planning Poker para estimar con el equipo
4. Seleccionar la técnica de estimación más adecuada según el contexto del proyecto
5. Documentar las estimaciones con los supuestos que las sustentan
6. Usar las estimaciones como insumo para la sección de planificación de la propuesta técnica

---

## 📋 Requisitos Previos

- Haber completado la Semana 3 (alcance y WBS del proyecto)
- Tener el entregable `entregable-s03-alcance.md` con el WBS de tu proyecto — es el insumo de esta semana
- Conocer los módulos y entregables de tu proyecto real

---

## 🗂️ Estructura de la Semana

```
week-04-tecnicas_de_estimacion/
├── README.md                                    ← Estás aquí
├── rubrica-evaluacion.md                        ← Criterios de evaluación
├── 0-assets/                                    ← Diagramas y visualizaciones
├── 1-teoria/
│   ├── 01-por-que-estimar.md                    ← Qué es estimar, por qué es difícil y por qué es necesario
│   ├── 02-tecnicas-cualitativas.md              ← Analogía, Delphi y comparación de técnicas
│   ├── 03-tshirt-y-planning-poker.md            ← T-shirt sizing y Planning Poker paso a paso
│   └── 04-caso-ferremax-estimacion.md           ← FerreMax: aplicar las 3 técnicas al sistema
├── 2-practicas/
│   └── 01-taller-estimar-ferremax/              ← Taller guiado con FerreMax
├── 3-proyecto/
│   ├── README.md                                ← Instrucciones del entregable
│   └── starter/                                 ← Plantilla para tu proyecto real
├── 4-recursos/
│   ├── ebooks-free/
│   ├── videografia/
│   └── webgrafia/
└── 5-glosario/
    └── README.md                                ← Términos clave de la semana
```

---

## 📝 Contenidos

| # | Archivo | Tipo | Tiempo |
|---|---------|------|--------|
| 1 | `1-teoria/01-por-que-estimar.md` | Teoría | 20 min |
| 2 | `1-teoria/02-tecnicas-cualitativas.md` | Teoría | 25 min |
| 3 | `1-teoria/03-tshirt-y-planning-poker.md` | Teoría | 25 min |
| 4 | `1-teoria/04-caso-ferremax-estimacion.md` | Caso de estudio | 20 min |
| 5 | `2-practicas/01-taller-estimar-ferremax/` | Práctica guiada | 120 min |
| 6 | `3-proyecto/` | Entregable real | 90 min |
| — | `5-glosario/README.md` | Referencia | A demanda |

---

## ⏱️ Distribución del Tiempo (6 horas)

```
📖 Teoría          ████████░░░░░░░░░░░░   1h 30min  (~25%)
💻 Prácticas       ████████████░░░░░░░░   2h 00min  (~33%)
🚀 Proyecto real   ████████░░░░░░░░░░░░   1h 30min  (~25%)
📚 Glosario/Rec.   ████░░░░░░░░░░░░░░░░   1h 00min  (~17%)
```

---

## 📌 Entregable de la Semana

**Documento:** `Estimación Preliminar del Proyecto` (Sección 4a de tu propuesta técnica)

El aprendiz completa la plantilla `3-proyecto/starter/entregable-s04-estimacion.md` con la información de su **proyecto real aprobado**, cubriendo:

- Selección y justificación de la técnica de estimación usada
- Tabla de estimación de los módulos del WBS (S03) con tallas o puntos
- Supuestos que sustentan las estimaciones
- Conversión de estimaciones a días/semanas de trabajo (insumo para S05)

> 📁 Este documento es la **parte inicial de la Sección 4 de la propuesta técnica**.
> La estimación en horas y el cronograma detallado se desarrollan en la Semana 5.

---

## 🎓 Conceptos Clave

| Término | Definición breve |
|---------|-----------------|
| **Estimación** | Cálculo aproximado del esfuerzo, tiempo o costo necesario para completar un trabajo |
| **Esfuerzo** | Cantidad de trabajo (en horas o días) que requiere una tarea, independiente del tiempo calendario |
| **Velocidad** | En métodos ágiles: cuántos puntos de historia puede completar el equipo por iteración |
| **Analogía** | Estimar comparando con proyectos similares ya realizados |
| **Delphi** | Técnica de estimación por consenso de expertos, en múltiples rondas |
| **T-shirt sizing** | Asignar tallas (XS, S, M, L, XL) a las tareas según su complejidad relativa |
| **Planning Poker** | Técnica ágil de estimación grupal con cartas de secuencia Fibonacci |
| **Story Points** | Unidad relativa de medida del esfuerzo en metodologías ágiles |
| **Sesgo de optimismo** | Tendencia humana a subestimar el tiempo y esfuerzo necesarios |
| **Buffer** | Margen de tiempo agregado a la estimación para cubrir imprevistos |
| **Estimación de 3 puntos** | Técnica que usa tres valores: optimista, más probable y pesimista |

---

## ✅ Checklist de Verificación

Antes de entregar, verifica que tu documento cumple con:

- [ ] Se seleccionó una técnica de estimación y se justificó la elección
- [ ] Cada módulo del WBS (S03) tiene una estimación con su talla o valor
- [ ] Se documentaron al menos 3 supuestos que sustentan las estimaciones
- [ ] Los totales por módulo están calculados correctamente
- [ ] Hay una conversión de tallas/puntos a días estimados de trabajo
- [ ] El documento tiene información del proyecto real, no del caso FerreMax
- [ ] Lenguaje formal, sin secciones vacías ni `<!-- Completar -->` sin responder

---

## 🔗 Navegación

| ← Anterior | → Siguiente |
|-----------|-------------|
| [← Semana 03 — Alcance y Factibilidad](../week-03-alcance_y_factibilidad/README.md) | [Semana 05 — Estimación de Esfuerzo y Tiempo →](../week-05-estimacion_esfuerzo_y_tiempo/README.md) |

---

## 💡 Consejos para esta Semana

- **Estimar no es adivinar, pero tampoco es exacto.** El objetivo es llegar a un rango razonable, no a un número perfecto.
- **Todas las técnicas de esta semana son relativas** — comparan tareas entre sí, no calculan horas absolutas. Eso está bien: la conversión a horas viene en S05.
- **Los supuestos son tan importantes como los números.** Si el cliente pregunta "¿por qué tanto?", la respuesta está en los supuestos.
- **El error de estimación es normal.** Lo importante es documentar por qué estimaste lo que estimaste, para aprender de la diferencia entre estimado y real.
- **En el caso FerreMax de esta semana** verás cómo el mismo sistema puede estimarse con tres técnicas diferentes — y cómo los resultados no son idénticos, pero convergen a un rango similar.

---

*Cadena de Formación · Tecnólogo ADSO · Semana 4 de 9*
