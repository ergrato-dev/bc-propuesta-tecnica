# Velocidad y Capacidad Real del Equipo

## 🎯 Objetivos

- Comprender qué es la velocidad de un equipo de desarrollo
- Calcular la capacidad real del equipo para un sprint o período
- Aplicar estos conceptos a la planificación del cronograma

---

## 1. ¿Qué es la velocidad del equipo?

En metodologías ágiles, la **velocidad** (velocity) es la cantidad de trabajo que un equipo completa en un período fijo llamado **sprint**.

> **Definición:** Velocidad = número de Story Points (o días de esfuerzo) completados por el equipo en un sprint.

La velocidad no se establece de antemano — **se mide** después de completar varios sprints. Los primeros 2–3 sprints de un proyecto sirven para calibrar la velocidad real del equipo.

**Ejemplo:**

| Sprint | Story Points planeados | Story Points completados | Velocidad real |
|--------|----------------------|--------------------------|----------------|
| Sprint 1 | 30 | 22 | 22 |
| Sprint 2 | 25 | 26 | 26 |
| Sprint 3 | 28 | 25 | 25 |
| **Promedio** | | | **24.3** |

Con una velocidad promedio de 24 puntos/sprint, el equipo puede planificar cuántos sprints necesita para completar el backlog.

---

## 2. ¿Por qué necesitamos conocer la velocidad?

La velocidad convierte los Story Points en tiempo real del proyecto:

$$\text{Sprints necesarios} = \frac{\text{Total Story Points del proyecto}}{\text{Velocidad promedio del equipo}}$$

**Ejemplo:**
- Total del proyecto FerreMax: ~194 días-persona ≈ 194 puntos simplificados
- Velocidad del equipo: 24 puntos/sprint (sprints de 2 semanas)
- Sprints necesarios: 194 ÷ 24 ≈ **8–9 sprints** (~4–4.5 meses)

> 💡 **Para proyectos nuevos:** Al inicio no se tiene velocidad histórica. Se usa la técnica de **velocidad estimada inicial** basada en la capacidad del equipo (siguiente sección).

---

## 3. Capacidad del equipo

Mientras que la **velocidad** es un dato histórico medido, la **capacidad** es el máximo teórico que el equipo podría completar en un período dado.

$$\text{Capacidad (puntos/sprint)} = \text{Personas} \times \text{Días del sprint} \times \text{Factor de capacidad}$$

**Ejemplo — FerreMax, sprint de 2 semanas (10 días hábiles):**

```
Equipo:               2 desarrolladores
Días del sprint:      10 días hábiles
Factor de capacidad:  80%

Capacidad = 2 × 10 × 0.80 = 16 días-persona efectivos

Si 1 día-persona = 1 punto (simplificado):
→ Capacidad = 16 puntos/sprint
```

> **Primera velocidad estimada:** Se usa la capacidad × 0.7 para el primer sprint (el equipo necesita tiempo de arranque):
> 16 × 0.70 = **~11 puntos** en el primer sprint.

---

## 4. Factores que reducen la capacidad

La capacidad real nunca es 100% de la teórica. Los factores que la reducen:

### 4.1 Disponibilidad por eventos planeados

| Evento | Impacto en la capacidad |
|--------|------------------------|
| Vacaciones, festivos | −días exactos de la persona |
| Evaluaciones SENA / parciales | −medio día a día completo |
| Capacitaciones internas | −horas de la capacitación |
| Reuniones de proyecto (diseño, revisión) | −1 a 2h/semana |
| Presentaciones al cliente | −medio día por reunión |

### 4.2 Deuda técnica y trabajo no planeado

Todo proyecto acumula **deuda técnica**: código que funciona pero que necesita ser mejorado, bugs que aparecen durante el desarrollo, cambios de requisitos del cliente.

La industria reserva entre el **10% y el 20%** del sprint para trabajo no planeado.

**Cálculo realista para FerreMax:**

```
Capacidad teórica (2 devs × 10 días × 80%):   16 días
Menos: reuniones semanales (2h × 2 semanas):   − 0.5 días
Menos: trabajo no planeado (15%):              − 2.4 días
Menos: festivos del período (1 día):           − 1.0 día

Capacidad real de este sprint:                ≈ 12 días-persona
```

### 4.3 Rol de cada persona

No todas las personas del equipo tienen el mismo peso en puntos:

| Perfil | Puntos/día (referencia) |
|--------|------------------------|
| Desarrollador senior | 1.2× puntos/día |
| Desarrollador mid-level | 1.0× puntos/día |
| Desarrollador junior | 0.7× puntos/día |
| Aprendiz SENA (trabajando) | 0.6–0.8× puntos/día |

> Para simplificar en la propuesta técnica: si el equipo es heterogéneo, usa el promedio del equipo.

---

## 5. Tabla de capacidad por sprint — FerreMax

Esta es la tabla que alimentará el cronograma en la teoría 03:

| Sprint | Período | Equipo | Festivos/eventos | Capacidad real (días) |
|--------|---------|--------|-----------------|----------------------|
| 1 | Semana 1–2 | 2 devs | Arranque del proyecto | ~10 días |
| 2 | Semana 3–4 | 2 devs | Ninguno | ~12 días |
| 3 | Semana 5–6 | 2 devs | Ninguno | ~12 días |
| 4 | Semana 7–8 | 2 devs | 1 festivo (Semana Santa) | ~10 días |
| 5 | Semana 9–10 | 2 devs | Ninguno | ~12 días |
| 6 | Semana 11–12 | 2 devs | Ninguno | ~12 días |
| 7 | Semana 13–14 | 2 devs | Revisión intermedia cliente | ~10 días |
| 8 | Semana 15–16 | 2 devs | Ninguno | ~12 días |
| 9 | Semana 17–18 | 2 devs | Pruebas de aceptación | ~8 días |
| 10 | Semana 19–20 | 2 devs | Despliegue + capacitación | ~6 días |

**Total capacidad: ~104 días de esfuerzo real** — equivalente a los 194 días totales divididos entre 2 personas ajustados por capacidad.

---

## 6. Velocidad inicial para proyectos nuevos — Cálculo paso a paso

Cuando no hay velocidad histórica, el proceso es:

**Paso 1:** Calcula la capacidad teórica del primer sprint.

**Paso 2:** Aplica factor de inicio (70% de la capacidad para Sprint 1, por curva de aprendizaje del proyecto).

**Paso 3:** Revisa después del Sprint 1 real y ajusta para los siguientes sprints.

**Fórmula:**

$$V_{inicial} = \text{Capacidad} \times 0.70$$

Esta velocidad inicial se usa para estimar el Sprint 1. A partir del Sprint 2, se usa la velocidad real medida.

---

## 7. ¿Y si no usamos sprints?

No todos los proyectos de software usan sprints. Muchos proyectos colombianos para PYMES siguen un enfoque de **fases secuenciales** (waterfall o cascada):

| Fase | Descripción | Duración típica |
|------|-------------|----------------|
| Análisis y diseño | Requisitos, arquitectura, WBS | 2–4 semanas |
| Desarrollo | Codificación módulo a módulo | Según estimados S04 |
| Pruebas | QA, pruebas de usuario | 1–3 semanas |
| Despliegue | Instalación, configuración, migración | 1–2 semanas |
| Capacitación | Entrenamiento a usuarios | 1 semana |

En este enfoque, la **capacidad** se calcula igual que antes, pero en lugar de sprints se habla de semanas de trabajo por fase.

Para la propuesta técnica de FerreMax se usa un enfoque **híbrido**: fases con sprints internos, lo cual es común en proyectos para PYMES colombianas donde el cliente no tiene experiencia con metodologías ágiles.

---

## ✅ Checklist de verificación

Antes de pasar a la siguiente clase, verifica que puedes:

- [ ] Definir velocidad del equipo y explicar cómo se mide
- [ ] Calcular la capacidad teórica de un sprint dado el equipo y factor de capacidad
- [ ] Listar al menos 3 factores que reducen la capacidad real de un sprint
- [ ] Explicar cómo calcular la velocidad inicial para un proyecto nuevo
- [ ] Calcular cuántos sprints necesita un proyecto dado el total de puntos y la velocidad

---

## 📚 Recursos adicionales

- *Scrum: The Art of Doing Twice the Work in Half the Time* — Jeff Sutherland
- Mountain Goat Software: "Velocity — frequently asked questions" (mountaingoatsoftware.com)
- Atlassian: "Velocity charts in Jira — how to read them" (atlassian.com/es)
