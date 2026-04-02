# De Esfuerzo a Duración: ¿No es lo mismo?

## 🎯 Objetivos

- Comprender la diferencia fundamental entre esfuerzo y duración
- Aplicar la fórmula de conversión de esfuerzo a duración
- Identificar los factores que afectan la duración real de un proyecto

---

## 1. El error más frecuente en estimación

Imagina que estimas que el módulo de inventario de FerreMax requiere **59 días de esfuerzo**. El cliente pregunta:

> *"¿Entonces en 59 días está listo?"*

La respuesta correcta es: **no necesariamente**. Esta confusión es el error más frecuente al presentar estimados, y puede generar compromisos que no se pueden cumplir.

El problema es que **esfuerzo** y **duración** son dos cosas distintas.

---

## 2. Definiciones precisas

### Esfuerzo (Effort)

> Cantidad total de trabajo necesario para completar una tarea, medido en **horas-persona** o **días-persona**.

Representa cuánto trabajo hay que hacer, independientemente de cuántas personas lo hacen o cuándo lo hacen.

**Ejemplo:** Construir una pared requiere 40 horas de trabajo de albañil (esfuerzo = 40 horas-persona).

### Duración (Duration)

> Tiempo de calendario que transcurre entre el inicio y el final de una actividad o proyecto, medido en **días, semanas o meses de calendario**.

Representa cuánto **tiempo real pasa**, teniendo en cuenta el equipo disponible.

**Ejemplo:**
- 1 albañil trabajando → 40 horas ÷ 8h/día = **5 días de calendario**
- 2 albañiles trabajando en paralelo → 40 horas ÷ 2 personas ÷ 8h/día = **2.5 días de calendario**

### La fórmula básica

$$\text{Duración} = \frac{\text{Esfuerzo (horas-persona)}}{\text{Personas en el equipo} \times \text{Horas productivas por día}}$$

---

## 3. El problema de las "horas productivas"

En la fórmula anterior hay un término crítico: **horas productivas por día**.

Un desarrollador no trabaja 8 horas efectivas al día. Existe una diferencia entre su tiempo disponible y su tiempo productivo:

| Actividad que consume tiempo | Horas típicas/día |
|------------------------------|:------------------:|
| Jornada laboral declarada | 8 h |
| Reuniones de equipo (daily, planificación) | −0.5 h |
| Revisión de código (code review) | −0.5 h |
| Interrupte s (mensajes, preguntas) | −0.5 h |
| Configuración, ambientes, deployments | −0.5 h |
| **Horas productivas reales estimadas** | **≈ 6 h** |

Esto nos da una **factor de productividad del 75%** (6h ÷ 8h = 0.75). En la práctica, muchos equipos usan entre 60% y 80% dependiendo del contexto.

> 💡 **En el SENA y proyectos de práctica:** Los aprendices enfrentan interrupciones adicionales (clases, evaluaciones, trabajo en dos proyectos al tiempo). Un factor del 60% es realista: 8h × 60% = ~4.8h productivas por día.

---

## 4. Fórmula completa con factor de capacidad

$$\text{Duración (días)} = \frac{\text{Esfuerzo (días-persona)}}{\text{Personas en el equipo} \times \text{Factor de capacidad}}$$

Donde:
- **Personas en el equipo** = desarrolladores asignados al proyecto
- **Factor de capacidad** = porcentaje del tiempo disponible que se dedicará a este proyecto

**Ejemplo FerreMax:**

```
Esfuerzo total (S04):    194 días-persona
Equipo:                  2 desarrolladores
Factor de capacidad:     80% (proyecto principal, pocas interrupciones)

Duración =  194 ÷ (2 × 0.80)
         =  194 ÷ 1.60
         =  121 días de calendario
         ≈  5.5 meses de trabajo
```

---

## 5. Casos de uso del factor de capacidad

| Escenario | Factor recomendado |
|-----------|--------------------|
| Equipo dedicado 100% a este proyecto | 80–85% |
| Equipo trabaja en 2 proyectos simultáneos | 45–55% |
| Aprendices SENA con clases + proyecto | 50–65% |
| Proyecto de práctica a tiempo parcial | 40–50% |
| Equipo senior con buen soporte técnico | 85–90% |

> ⚠️ **Nunca uses 100%:** Ningún equipo es 100% productivo 100% del tiempo. Un factor del 100% te lleva directamente al sesgo de optimismo que estudiamos en la Semana 4.

---

## 6. El efecto del tamaño del equipo

Agregar más personas a un proyecto **no siempre lo hace más rápido**. La **Ley de Brooks** (Fred Brooks, 1975) dice:

> *"Agregar personas a un proyecto de software tardío lo hace más tardío."*

¿Por qué? Porque cada persona nueva:
- Necesita tiempo de inducción (onboarding)
- Genera comunicación adicional entre el equipo
- Puede generar conflictos de integración en el código

La relación entre personas y duración no es perfectamente lineal. Para proyectos pequeños (<6 meses), la penalización de comunicación es manejable:

| Equipo | Canales de comunicación |
|--------|------------------------|
| 2 personas | 1 canal |
| 3 personas | 3 canales |
| 4 personas | 6 canales |
| 5 personas | 10 canales |

Fórmula: $\text{Canales} = \frac{n \times (n-1)}{2}$

Para FerreMax (equipo de 2 y luego de 3), la complejidad de comunicación es manejable.

---

## 7. Tipos de tiempo en un proyecto

Además del tiempo de desarrollo, un proyecto real incluye otras actividades que consumen tiempo:

| Tipo de tiempo | Descripción | Estimado típico |
|---------------|-------------|----------------|
| **Tiempo de desarrollo** | Código, pruebas unitarias | 70–75% del total |
| **Tiempo de revisiones** | Code review, feedback del cliente | 10–15% del total |
| **Tiempo de correcciones** | Bugs reportados en revisión | 5–10% del total |
| **Tiempo de despliegue** | Configurar servidores, CI/CD | 5–8% del total |
| **Buffer de contingencia** | Imprevistos, enfermedades | 10–15% adicional |

Para FerreMax, el equipo agrega un **15% de buffer**:

```
Duración base de desarrollo:   121 días
Buffer (15%):                +  18 días
Duración total del proyecto:   139 días ≈ 6.5 meses
```

---

## 8. Comparativa: esfuerzo vs. duración en FerreMax

| Módulo | Esfuerzo (días-persona) | Duración estimada (2 devs, 80%) |
|--------|------------------------|--------------------------------|
| Autenticación | 31 | ~19 días |
| Inventario | 67 | ~42 días |
| Clientes | 12 | ~8 días |
| Ventas | 48 | ~30 días |
| Reportes | 20 | ~13 días |
| Config. y docs | 16 | ~10 días |
| **TOTAL** | **194** | **~122 días base** |

> Los módulos no se ejecutan todos en paralelo — algunos tienen dependencias. La asignación real de plazos se hace en el cronograma (Semana 5, teoría 03).

---

## ✅ Checklist de verificación

Antes de pasar a la siguiente clase, verifica que puedes:

- [ ] Explicar con un ejemplo propio qué es esfuerzo y qué es duración
- [ ] Aplicar la fórmula de conversión con equipo y factor de capacidad
- [ ] Justificar por qué el factor de capacidad es siempre menor al 100%
- [ ] Distinguir los tipos de tiempo que consume un proyecto (desarrollo, revisión, correcciones, despliegue)
- [ ] Calcular la duración de FerreMax con los datos dados

---

## 📚 Recursos adicionales

- *The Mythical Man-Month* — Fred Brooks (1975): el libro más citado sobre por qué agregar personas no siempre funciona
- PMBok 7ª edición, sección "Duración de actividades": metodología formal de conversión
- Atlassian: "Velocity vs. capacity — what's the difference?" (en inglés, con traducción automática)
