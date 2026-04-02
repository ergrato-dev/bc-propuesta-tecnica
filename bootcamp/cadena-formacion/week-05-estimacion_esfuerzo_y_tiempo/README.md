# Semana 5 — ¿Cuánto Tiempo Tomará?

> **Versión**: Cadena de Formación · Tecnólogo ADSO · Semana 5 de 9

Tienes los estimados de esfuerzo de la Semana 4 (días de trabajo por módulo). Ahora viene una pregunta diferente: ¿cuándo estará listo? Esta semana aprendes a convertir días de esfuerzo en una duración real de proyecto, a construir un cronograma básico y a comunicarle al cliente una fecha realista.

---

## 🎯 Objetivos de Aprendizaje

Al finalizar esta semana serás capaz de:

1. Distinguir con precisión entre **esfuerzo** (días-persona) y **duración** de calendario
2. Calcular la **capacidad real** del equipo aplicando factores de dedicación y disponibilidad
3. Convertir los estimados de la Semana 4 a **duración de proyecto** usando el tamaño del equipo
4. Construir un **cronograma básico** con hitos, dependencias y diagrama de Gantt
5. Identificar la **ruta crítica** de tu proyecto (los módulos que no pueden retrasarse)
6. Integrar el cronograma como sección de tu propuesta técnica

---

## 📚 Requisitos Previos

- Haber completado el entregable de la Semana 4 (tabla de estimación con tallas y días de esfuerzo)
- Conocer la diferencia entre Story Points, esfuerzo y días de trabajo (Semana 4, teoría 01)
- Tener clara la lista de módulos y subcomponentes de tu WBS (Semana 3)

---

## 🗂️ Estructura de la Semana

```
week-05-estimacion_esfuerzo_y_tiempo/
├── 0-assets/           ← 3 diagramas SVG (tema oscuro)
├── 1-teoria/           ← 4 archivos de teoría
├── 2-practicas/        ← Taller guiado sobre FerreMax
├── 3-proyecto/         ← Entregable aplicado a tu proyecto real
├── 4-recursos/         ← Ebooks, videos, webs
├── 5-glosario/         ← Términos clave de la semana
├── README.md           ← (este archivo)
└── rubrica-evaluacion.md
```

---

## 📝 Contenidos

| # | Archivo | Tema | Tiempo |
|---|---------|------|--------|
| 1 | `1-teoria/01-de-esfuerzo-a-duracion.md` | Esfuerzo vs. duración — la confusión más común | 30 min |
| 2 | `1-teoria/02-velocidad-y-capacidad.md` | Capacidad real del equipo — factor de dedicación | 30 min |
| 3 | `1-teoria/03-cronograma-basico-gantt.md` | Cronograma básico: hitos, dependencias, Gantt | 40 min |
| 4 | `1-teoria/04-caso-ferremax-cronograma.md` | FerreMax: de 194 días de esfuerzo al cronograma completo | 20 min |
| 5 | `2-practicas/01-taller-cronograma-ferremax/` | Taller guiado: construir el Gantt de FerreMax | 2.5 h |
| 6 | `3-proyecto/starter/entregable-s05-cronograma.md` | **Entregable:** cronograma de tu proyecto real | 1.5 h |

---

## ⏱️ Distribución del Tiempo (6 horas)

| Actividad | Tiempo |
|-----------|--------|
| Teoría (archivos 1–4) | 2 h |
| Taller guiado FerreMax | 2.5 h |
| Entregable proyecto propio | 1.5 h |
| **Total** | **6 h** |

---

## 📌 Entregable

**Archivo:** `3-proyecto/starter/entregable-s05-cronograma.md`

El aprendiz toma su tabla de estimación de la Semana 4 y produce:
- Cálculo de la duración del proyecto (esfuerzo ÷ capacidad del equipo)
- Lista de hitos del proyecto (mínimo 4)
- Tabla de dependencias entre módulos
- Representación del cronograma (Gantt en texto o enlace a herramienta)
- Sección "Supuestos del cronograma"

Este entregable es la **sección de cronograma** de la propuesta técnica final.

---

## 🎓 Conceptos Clave

| Concepto | Definición breve |
|----------|-----------------|
| **Esfuerzo** | Días-persona necesarios para completar el trabajo |
| **Duración** | Días de calendario entre inicio y fin del proyecto |
| **Capacidad** | Porcentaje real de tiempo productivo del equipo |
| **Hito** | Punto de control temporal con un entregable verificable |
| **Dependencia** | Restricción de orden: una tarea no puede iniciar hasta que otra termina |
| **Ruta crítica** | Cadena de tareas cuyo retraso impacta directamente la fecha de entrega |
| **Diagrama de Gantt** | Representación visual del cronograma con barras de tiempo |
| **Sprint** | Período fijo de trabajo (1–4 semanas) en metodologías ágiles |
| **Buffer** | Tiempo adicional de reserva para absorber imprevistos |

---

## ✅ Checklist de Verificación

Antes de continuar a la Semana 6, verifica:

- [ ] Puedo explicar la diferencia entre esfuerzo (días-persona) y duración (días de calendario)
- [ ] Sé calcular la duración del proyecto dado el esfuerzo y el tamaño del equipo
- [ ] Apliqué el factor de capacidad real (no asumo 8h productivas por día)
- [ ] Mi cronograma tiene al menos 4 hitos con fechas o semanas aproximadas
- [ ] Identifiqué las dependencias entre módulos de mi proyecto
- [ ] Identifiqué cuál es la ruta crítica de mi proyecto
- [ ] El entregable S05 está vinculado con los estimados del entregable S04

---

## 🔗 Navegación

| | |
|---|---|
| ← Semana anterior | [Semana 4 — Técnicas de Estimación](../week-04-tecnicas_de_estimacion/README.md) |
| → Semana siguiente | [Semana 6 — Estimación de Costos](../week-06-estimacion_de_costos/README.md) |

---

## 💡 Consejos para esta Semana

- **No confundas esfuerzo con duración:** 100 días-persona con un equipo de 2 = ~50 días de calendario, no 100.
- **El factor de capacidad es real:** Un desarrollador no produce 8 horas útiles al día — reuniones, pausas, revisiones consumen entre el 20% y el 40% del tiempo.
- **Las dependencias mandan:** Puedes tener mucha gente, pero si el módulo B depende del módulo A, no puedes hacerlos en paralelo.
- **El Gantt no es una promesa:** Es un plan con supuestos. Cambia cuando cambian los supuestos — y eso está bien, siempre que lo comuniques al cliente.
- **Herramienta recomendada:** Para crear el Gantt, usa ProjectLibre (gratuito, offline) o el tablero de Google Sheets con la plantilla de Gantt disponible en Google Workspace.

---

*Cadena de Formación · Tecnólogo ADSO · Semana 5 de 9*
