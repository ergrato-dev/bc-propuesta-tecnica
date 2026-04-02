# Por Qué Estimar — Y Por Qué Es Tan Difícil

## 🎯 Objetivos

- Comprender qué es la estimación en el contexto de un proyecto de software
- Entender por qué la estimación es necesaria aunque sea imprecisa
- Reconocer el sesgo de optimismo y cómo afecta a los proyectos
- Diferenciar esfuerzo, duración y costo

---

## 1. ¿Qué es Estimar?

**Estimar** es calcular de forma aproximada el esfuerzo, tiempo o costo necesarios para completar un trabajo, antes de que ese trabajo ocurra.

La palabra clave es **aproximado**. Una estimación no es una promesa, no es una predicción exacta y no es un compromiso inamovible. Es una hipótesis razonada basada en la información disponible en este momento.

> "Toda estimación es incorrecta. La pregunta es: ¿qué tan incorrecta está dentro de los límites aceptables?"
> — Paráfrasis de principio de gestión de proyectos

---

## 2. ¿Por Qué Necesitamos Estimar?

Antes de construir un proyecto, el cliente necesita saber:

- **¿Cuánto va a costar?** → Para tomar la decisión de invertir o no
- **¿Cuánto tiempo tomará?** → Para planificar su negocio, contratar personal, lanzar al mercado
- **¿Vale la pena?** → Para comparar con otras opciones

Sin estimaciones, no es posible tomar ninguna de esas decisiones. El cliente no puede aprobar un proyecto si no sabe siquiera en qué rango de costo y tiempo está.

**Ejemplo concreto:**
Carlos de FerreMax no puede decirle a su contador "esto puede costar entre $3.000.000 y $60.000.000 COP, no sé". Necesita un número razonable para presupuestar. La estimación sirve para reducir esa incertidumbre a un rango manejable.

---

## 3. El Problema del Software: Todo es Invisible

Estimar software es diferente a estimar construir una pared o fabricar una mesa. Los materiales del software son intangibles: líneas de código, lógica, decisiones de diseño. No hay una forma directa de "ver cuánto falta".

### La analogía del iceberg

Lo que el cliente ve es la pantalla funcional — el 10% visible. Lo que el desarrollador sabe que hay debajo: validaciones, manejo de errores, seguridad, base de datos, pruebas, despliegue — el 90% invisible.

![Comparación de técnicas de estimación](../0-assets/01-por-que-es-difícil-estimar.svg)

### Por qué las estimaciones iniciales suelen ser bajas

Los estudios de gestión de proyectos muestran consistentemente que:
- Los proyectos de software se entregan en promedio con **retrasos del 40–80%** frente al plan inicial
- El costo real supera el estimado en promedio entre un **50% y 100%**
- Solo el **16%** de los proyectos de software se completan en tiempo y costo original (Chaos Report, Standish Group)

Estos números no son para desanimar — son para que entiendas que **la estimación perfecta no existe**, y que tu objetivo es llegar a un rango razonable con supuestos documentados.

---

## 4. El Sesgo de Optimismo

El **sesgo de optimismo** es la tendencia humana natural a creer que las cosas serán más fáciles, rápidas y baratas de lo que realmente resultan ser.

En software, el sesgo de optimismo se manifiesta así:

| Pensamiento optimista | Realidad frecuente |
|----------------------|-------------------|
| "El login lo hago en 2 horas" | El login con roles, cifrado y sesiones toma 1–2 días |
| "La base de datos es sencilla" | El diseño, normalización y migración de datos toman tiempo |
| "Las pruebas las hago al final" | Las pruebas y corrección de bugs consumen hasta el 30% del proyecto |
| "No habrá cambios de requisitos" | El cliente siempre pide ajustes durante el desarrollo |
| "Ya sé esa tecnología" | Siempre hay algo nuevo que aprender en cada proyecto |

### ¿Cómo contrarrestarlo?

1. **Usar técnicas estructuradas** — en lugar de "¿cuánto crees que tarda?", aplicar metodología
2. **Descomponer en partes pequeñas** — es más fácil estimar una pantalla que un sistema completo
3. **Agregar un buffer** — un margen del 20–30% para imprevistos es estándar en el sector
4. **Documentar supuestos** — "estimé X asumiendo Y; si Y cambia, el tiempo cambia"
5. **Revisar con experiencias pasadas** — ¿cuánto tomó algo similar antes?

---

## 5. Esfuerzo vs. Duración vs. Costo

Antes de estimar, es importante distinguir tres conceptos que se confunden constantemente:

| Concepto | Definición | Ejemplo |
|----------|-----------|---------|
| **Esfuerzo** | Cantidad total de trabajo (horas-persona) | "Este módulo requiere 40 horas de trabajo" |
| **Duración** | Tiempo calendario desde el inicio hasta el fin | "Tardará 2 semanas (10 días hábiles)" |
| **Costo** | Valor en dinero del esfuerzo + recursos | "40 horas × $35.000/hora = $1.400.000 COP" |

La relación entre ellos depende de cuántas personas trabajan y cuántas horas por día:

```
Duración = Esfuerzo ÷ (Personas × Horas por día)
Costo    = Esfuerzo × Tarifa por hora
```

**Ejemplo:**
- Esfuerzo estimado del módulo de inventario: 40 horas
- 1 persona trabajando 4 horas diarias (aprendiz con otros compromisos)
- Duración calendario: 40 ÷ (1 × 4) = **10 días hábiles = 2 semanas**
- Costo (tarifa aprendiz junior ~$25.000/hora): 40 × $25.000 = **$1.000.000 COP**

---

## 6. El Cono de la Incertidumbre

La precisión de una estimación mejora a medida que avanza el proyecto y se conoce más:

```
Inicio del proyecto                           Fin del proyecto
        |                                            |
        ▼                                            ▼
  [Muy incierto]                             [Alta certeza]
   ×4 o ÷4                                    ×1.1 o ÷1.1

  "Puede costar                             "Costará entre
   entre $5M y $80M"     →→→→→→→           $18M y $22M"
```

En la Semana 4 estás al inicio del cono — las estimaciones son amplias. A medida que defines mejor los requisitos y el alcance (S02, S03), el cono se estrecha. En S05 y S06 llegarás a estimaciones más precisas.

---

## 7. Tipos de Técnicas de Estimación

Hay muchas técnicas de estimación. En este bootcamp usaremos las más accesibles para proyectos de aprendizaje:

| Categoría | Técnica | Cuándo usarla |
|-----------|---------|---------------|
| **Cualitativa** | Analogía | Tengo proyectos similares como referencia |
| **Cualitativa** | Delphi | Necesito consenso de varias personas |
| **Relativa** | T-shirt sizing | Quiero una visión rápida de la complejidad relativa |
| **Relativa** | Planning Poker | Tengo equipo y quiero estimación colaborativa |
| **Cuantitativa** | Story Points + velocidad | Metodología ágil con histórico de sprints |

Las técnicas cualitativas y relativas se ven en esta semana (S04). Las cuantitativas y la conversión a horas/días se profundizan en S05.

---

## ✅ Checklist de Comprensión

- [ ] ¿Qué diferencia hay entre esfuerzo y duración?
- [ ] ¿Por qué los proyectos de software tienden a demorarse más de lo estimado?
- [ ] ¿Qué es el sesgo de optimismo y cómo afecta las estimaciones?
- [ ] ¿Qué es el cono de la incertidumbre?
- [ ] ¿En qué momento del proyecto las estimaciones son más precisas?

---

*Siguiente: [02 — Técnicas Cualitativas de Estimación →](./02-tecnicas-cualitativas.md)*
