# Técnicas de Estimación: Analogía y Delphi

## 🎯 Objetivos

- Comprender en qué consiste la técnica de estimación por analogía
- Comprender en qué consiste la técnica Delphi (o juicio de expertos)
- Identificar cuándo conviene usar cada técnica
- Reconocer las fortalezas y limitaciones de cada una

---

## 1. Recordatorio: ¿Qué buscamos con las técnicas?

En la clase anterior vimos que estimar es una actividad esencial pero difícil. También vimos que existen diferentes tipos de técnicas: algunas basadas en la experiencia y el juicio (cualitativas/heurísticas) y otras basadas en cálculos matemáticos (cuantitativas).

En esta sesión profundizamos en **dos técnicas cualitativas** ampliamente usadas en la industria TI colombiana:

| Técnica | Base del estimado |
|---------|-------------------|
| **Analogía** | Comparar con proyectos anteriores similares |
| **Delphi** | Consenso de varios expertos, sin influencia mutua |

Ambas son ideales cuando el equipo tiene experiencia pero **no tiene datos históricos detallados** o cuando el proyecto es nuevo y no se puede usar fórmulas.

---

## 2. Técnica de Analogía

### ¿Qué es?

La estimación por **analogía** consiste en comparar el proyecto nuevo con uno o más proyectos **previos, parecidos y ya terminados**, y usar ese histórico como base para el nuevo estimado.

> **Idea clave:** "Hicimos algo parecido antes. ¿Cuánto tardamos? ¿En qué se parece y en qué se diferencia este nuevo proyecto?"

### ¿Cómo se aplica? — Paso a paso

**Paso 1: Identifica el proyecto de referencia**

Busca un proyecto terminado que sea similar en:
- Tipo de sistema (web, móvil, escritorio)
- Tamaño y complejidad aproximados
- Tecnologías usadas
- Equipo de desarrollo

**Paso 2: Documenta qué sabes del proyecto referencia**

| Dato | Proyecto referencia |
|------|---------------------|
| Nombre del proyecto | Sistema de nómina — Empresa textilera Medellín |
| Año de ejecución | 2022 |
| Duración real | 4 meses |
| Equipo | 2 desarrolladores full-stack |
| Módulos principales | Empleados, Liquidación, Reportes |
| Esfuerzo total | ~320 horas |

**Paso 3: Compara con el proyecto nuevo**

Lista las **similitudes** y las **diferencias**:

| Aspecto | Proyecto referencia | Proyecto nuevo | Impacto |
|---------|---------------------|----------------|---------|
| Tipo de sistema | Web interno | Web interno | 🟩 Igual |
| Módulos | 3 módulos principales | 5 módulos | 🔴 Mayor (más trabajo) |
| Integración con hardware | No | Sí (lectores de código) | 🔴 Mayor (nuevo riesgo) |
| Equipo disponible | 2 developers | 2 developers | 🟩 Igual |
| Tecnología | PHP + MySQL | Django + PostgreSQL | 🟡 Diferente (curva de aprendizaje) |

**Paso 4: Aplica factores de ajuste**

Con base en las diferencias, ajusta el estimado hacia arriba o hacia abajo:

```
Estimado base (del proyecto referencia): 4 meses

Ajustes:
  + 2 módulos adicionales:      + 1.5 meses
  + Integración con hardware:   + 0.5 meses
  + Curva de aprendizaje Django: + 0.5 meses

Estimado ajustado: 4 + 1.5 + 0.5 + 0.5 = 6.5 meses
```

> 💡 Los factores de ajuste son subjetivos — por eso se documenta el razonamiento. El estimado tiene una incertidumbre alta cuando hay pocas analogías disponibles.

**Paso 5: Documenta tus supuestos**

Siempre registra:
- ¿Por qué elegiste ese proyecto de referencia?
- ¿Cuáles son las diferencias más importantes?
- ¿Por qué aplicaste esos factores de ajuste?

Sin supuestos documentados, el estimado no tiene valor para el cliente ni para el equipo.

---

### Fortalezas de la técnica de Analogía

✅ Rápida de aplicar cuando hay experiencia previa  
✅ Entendible para el cliente ("lo comparamos con un proyecto que ya hicimos")  
✅ Considera la realidad histórica del equipo, no solo teoría  
✅ Útil en etapas tempranas con información limitada  

### Limitaciones de la técnica de Analogía

❌ Depende de tener proyectos referencia disponibles y documentados  
❌ Si el proyecto nuevo es muy diferente, la analogía pierde valor  
❌ Los factores de ajuste son subjetivos y pueden ser optimistas  
❌ No es útil para estimar componentes técnicos muy nuevos (IA, blockchain) donde no hay referencia  

---

## 3. Técnica Delphi (Juicio de Expertos)

### ¿Qué es?

La técnica **Delphi** es un proceso estructurado para llegar a un estimado por **consenso entre varios expertos**, de manera que cada persona exprese su opinión **de forma independiente** (sin ver la de los otros), reduciendo el efecto de la jerarquía o del "el que habla más fuerte gana".

> **Origen:** La técnica Delphi fue desarrollada por la RAND Corporation en los años 50, originalmente para predicciones militares. En desarrollo de software, la adaptación más conocida es el **Wideband Delphi** (Barry Boehm, 1981).

### ¿Por qué no basta con preguntar en reunión?

En una reunión normal de estimación, ocurren sesgos:

| Problema | Descripción |
|----------|-------------|
| **Efecto de ancla** | El primero que habla "ancla" la expectativa del grupo |
| **Influencia jerárquica** | Los juniors no contradicen al líder técnico |
| **Conformidad social** | Se acepta la primera respuesta para no alargar la reunión |
| **Silencio del experto** | El más introvertido tiene la mejor experiencia pero no habla |

Delphi resuelve esto al forzar la estimación **individual y anónima** antes de la discusión.

---

### ¿Cómo se aplica? — Paso a paso

**Paso 1: Define el alcance a estimar**

Antes de reunir a los expertos, el moderador prepara:
- La lista de funcionalidades o módulos a estimar
- El contexto del proyecto (requisitos conocidos, restricciones)
- La unidad de medida (horas, días, puntos)

**Paso 2: Selecciona los expertos**

Se recomienda entre **3 y 7 personas** con experiencia en:
- Desarrollo técnico (backend, frontend)
- Dominio del negocio (si aplica)
- Gestión de proyectos o análisis

**Paso 3: Primera ronda — estimación individual y anónima**

Cada experto estima **por su cuenta** sin ver el estimado de los demás. Las estimaciones se recolectan por escrito (papel, formulario digital, etc.).

Ejemplo — Primera Ronda para el módulo "Inventario":

| Experto | Estimado (días) |
|---------|----------------|
| Experto A | 18 |
| Experto B | 12 |
| Experto C | 25 |
| Experto D | 15 |

**Paso 4: Análisis de la primera ronda**

El moderador calcula:
- Promedio: (18 + 12 + 25 + 15) / 4 = **17.5 días**
- Rango: 12 – 25 días
- Desviación: hay diferencia significativa → se necesita discusión

**Paso 5: Discusión de diferencias**

Los expertos con los valores más altos y más bajos **explican su razonamiento** (sin presión para cambiar su voto). Se discuten los supuestos de cada uno.

Experto B: "Estimé 12 porque asumo que el inventario no tiene integración con hardware."  
Experto C: "Estimé 25 porque consideré la integración con lectores de código de barras."

→ El grupo acuerda que **sí hay integración** → el supuesto de C es más realista.

**Paso 6: Segunda ronda — estimación revisada**

Cada experto revisa su estimado teniendo en cuenta la nueva información:

| Experto | Segunda estimación |
|---------|--------------------|
| Experto A | 20 |
| Experto B | 18 |
| Experto C | 22 |
| Experto D | 19 |

Nuevo promedio: **19.75 días** (convergencia lograda — rango ahora es 18–22)

**Paso 7: Consolidación**

Cuando el rango es aceptable (generalmente ±20% del promedio), se adopta el promedio o el valor de consenso como estimado final. Si persiste desacuerdo, se repite una ronda más.

---

### Fortalezas de la técnica Delphi

✅ Elimina sesgos de jerarquía y conformidad social  
✅ Captura la experiencia de múltiples expertos  
✅ La discusión explícita de supuestos enriquece el estimado  
✅ Genera mayor compromiso del equipo con el estimado propio  

### Limitaciones de la técnica Delphi

❌ Requiere tiempo: varias rondas + moderación activa  
❌ Depende de la calidad y disponibilidad de expertos  
❌ Puede no converger fácilmente en equipos con visiones muy distintas  
❌ No es útil si el equipo es de una sola persona  

---

## 4. ¿Cuándo usar cada técnica?

| Criterio | Analogía | Delphi |
|----------|----------|--------|
| Tienes proyectos previos similares | ✅ Ideal | 🟡 También útil |
| El proyecto es completamente nuevo | ❌ Difícil | ✅ Mejor opción |
| Necesitas rapidez | ✅ Más rápido | ❌ Toma más tiempo |
| Tienes un equipo de 3+ personas | 🟡 Opcional | ✅ Ideal |
| Trabajas solo | ✅ Funciona | ❌ No aplica |
| Quieres consenso del equipo | 🟡 Parcial | ✅ Diseñado para esto |
| Primera vez que hacen este tipo de proyecto | ❌ Sin referencia | ✅ Usa el juicio colectivo |

> 💡 **En la práctica real:** Los equipos de software colombianos frecuentemente combinan ambas — una persona hace una estimación por analogía inicial y luego se valida con el equipo mediante Delphi informal.

---

## 5. Ejemplo integrado — FerreMax S.A.S.

**Contexto:** El equipo de 3 consultores (Ana, Luis, Camila) va a estimar el módulo de **Inventario** del sistema FerreMax usando analogía + Delphi.

**Paso 1: Analogía inicial (la hace Ana)**
- Proyecto referencia: Sistema de inventario para papelería, desarrollado en 2023
- Duración real: 3 meses, equipo de 2 personas
- Módulo inventario solo: ~45 días
- Diferencias con FerreMax: integración con lectores de código (+10%), dos sedes (+15%)
- Estimado ajustado por analogía: 45 × 1.25 = **~56 días**

**Paso 2: Primera ronda Delphi**

| Experto | Estimado | Supuesto |
|---------|----------|---------|
| Ana | 56 días | Basado en analogía con papelería |
| Luis | 40 días | No consideró integración hardware |
| Camila | 65 días | Consideró sincronización entre sedes como compleja |

**Paso 3: Discusión**
- Luis aclara que sí hay lectores barcode → revisa su estimado
- Camila detalla que la sincronización en tiempo real es el mayor riesgo

**Paso 4: Segunda ronda**

| Experto | Segundo estimado |
|---------|-----------------|
| Ana | 58 días |
| Luis | 55 días |
| Camila | 60 días |

**Resultado:** Promedio = **57.7 días** → se adopta **58 días** para el módulo de Inventario.

---

## 6. Conexión con la Propuesta Técnica

Los estimados obtenidos con estas técnicas alimentan directamente la propuesta técnica:

- **Sección de alcance**: "El módulo de inventario se estima en 58 días hábiles"
- **Sección de presupuesto**: días × tarifa diaria del equipo
- **Sección de riesgos**: los supuestos documentados se convierten en riesgos si no se cumplen
- **Cronograma (Semana 5)**: los días estimados se distribuyen en un Gantt

> ⚠️ **Importante:** En esta semana estimamos en **días de trabajo** (o tallas, que veremos la próxima clase). La conversión a horas-persona y costos se hace en la **Semana 5**.

---

## ✅ Checklist de verificación

Antes de pasar a la siguiente clase, verifica que puedes:

- [ ] Explicar con tus propias palabras qué es la técnica de analogía
- [ ] Enumerar los 5 pasos de la técnica de analogía
- [ ] Explicar por qué la estimación en reunión sin estructura tiene sesgos
- [ ] Explicar los 7 pasos de la técnica Delphi
- [ ] Identificar al menos 2 fortalezas y 2 limitaciones de cada técnica
- [ ] Elegir cuál técnica conviene en un escenario dado

---

## 📚 Recursos adicionales

- Wideband Delphi — Barry Boehm (1981): técnica original adaptada para software
- PMBok 7ª edición, sección "Estimación por analogía"
- *Agile Estimating and Planning* — Mike Cohn (Cap. 4: Técnicas de estimación)
