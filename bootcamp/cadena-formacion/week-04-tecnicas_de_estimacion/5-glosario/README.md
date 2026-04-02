# Glosario — Semana 4: Técnicas de Estimación

Términos clave de esta semana, ordenados alfabéticamente.  
⭐ = término especialmente importante para la propuesta técnica.

---

## A

**Analogía (estimación por)**  
Técnica que estima el esfuerzo de un proyecto nuevo comparándolo con uno o más proyectos anteriores similares. Se identifican similitudes y diferencias, y se aplican factores de ajuste para llegar al nuevo estimado. Requiere proyectos de referencia documentados.

**Ancla de referencia**  
En T-shirt sizing, el ítem que se escoge como punto de comparación neutro y se asigna la talla M. Todos los demás ítems se comparan contra esta ancla. Una mala elección de ancla distorsiona todos los demás estimados.

---

## B

**Backlog**  
Lista priorizada de historias de usuario, funcionalidades o tareas pendientes de un proyecto ágil. En Planning Poker, el backlog es la lista de ítems que el equipo debe estimar.

---

## C

**Cono de la incertidumbre** ⭐  
Modelo visual que muestra cómo la incertidumbre de un estimado disminuye a medida que el proyecto avanza. Al inicio puede haber un error de ×4 o ÷4; al final del proyecto, el error se reduce a ±10%. Desarrollado por Barry Boehm.

**Consenso**  
Acuerdo del grupo sobre un valor de estimación. En Planning Poker, el consenso se logra cuando todos los participantes votan el mismo número o números muy cercanos.

**Convergencia (Delphi)**  
Proceso por el cual las estimaciones individuales de los expertos se acercan entre sí a medida que se realizan más rondas de votación y se discuten los supuestos. El objetivo de Delphi es lograr convergencia sin presión social.

---

## D

**Delphi (técnica)** ⭐  
Método de estimación por consenso de expertos en el que cada participante vota de forma independiente y anónima, se discuten las diferencias, y se realizan rondas sucesivas hasta llegar a un acuerdo. Elimina sesgos de jerarquía y conformidad social.

**Duración**  
Tiempo de calendario que transcurre entre el inicio y el fin de una actividad o proyecto. Diferente del esfuerzo: una tarea puede requerir 20 horas de esfuerzo pero durar 5 días de calendario si el desarrollador trabaja 4 horas diarias en ella.

---

## E

**Esfuerzo** ⭐  
Cantidad de trabajo necesario para completar una tarea, medido en horas-persona o días-persona. No equivale a la duración. Ejemplo: "El módulo de inventario requiere 200 horas de esfuerzo" (≠ 200 días de calendario).

**Estimación** ⭐  
Proceso de aproximar el tamaño, el esfuerzo, el costo o la duración de un trabajo. Toda estimación tiene incertidumbre asociada que debe declararse.

---

## F

**Factor de ajuste**  
Porcentaje o multiplicador que se aplica al estimado base (proyecto de referencia) para reflejar diferencias con el proyecto nuevo. Por ejemplo: "+20% por integración con hardware adicional".

**Fibonacci (secuencia de)** ⭐  
Sucesión matemática donde cada número es la suma de los dos anteriores: 1, 1, 2, 3, 5, 8, 13, 21, 34... En Planning Poker se usa la versión simplificada: 1, 2, 3, 5, 8, 13, 21. Refleja que la incertidumbre crece de forma no lineal.

---

## H

**Historia de usuario**  
Descripción breve de una funcionalidad desde la perspectiva del usuario. Formato estándar: "Como [tipo de usuario], quiero [acción], para [beneficio]". Es la unidad básica de estimación en Planning Poker.

---

## I

**Incertidumbre**  
Falta de conocimiento exacto sobre cómo se desarrollará el proyecto. En estimación, la incertidumbre justifica los rangos de estimado (mínimo–probable–máximo) en lugar de un único número exacto.

---

## J

**Juicio de expertos**  
Uso de la experiencia y conocimiento de una o más personas calificadas para apoyar una decisión o estimado. Técnica Delphi es la forma estructurada del juicio de expertos.

---

## M

**Moderador (Planning Poker)**  
Persona que facilita la sesión de Planning Poker. Lee las historias, gestiona el tiempo de debate y garantiza que las revelaciones sean simultáneas. Generalmente no vota.

---

## P

**Planning Poker** ⭐  
Técnica de estimación ágil en la que los miembros del equipo usan cartas con la secuencia de Fibonacci para votar simultáneamente sobre la complejidad relativa de cada historia. Las diferencias generan discusión que enriquece el entendimiento del trabajo.

**Punto de historia (Story Point)**  
Unidad de medida relativa usada en Planning Poker para representar la complejidad, el esfuerzo y la incertidumbre de una historia de usuario. No equivale a horas ni días — es relativo al equipo y al proyecto.

**Proyecto de referencia**  
En estimación por analogía, el proyecto anterior que se usa como base de comparación. Debe ser un proyecto terminado, documentado y lo más similar posible al proyecto nuevo.

---

## R

**Rango de estimado**  
En lugar de un único número, un estimado con rango indica un mínimo y un máximo posible. Ejemplo: "El módulo de inventario tomará entre 40 y 70 días". Más honesto que un número exacto espurio.

---

## S

**Sesgo de optimismo**  
Tendencia cognitiva a subestimar el tiempo y el esfuerzo necesarios para completar un proyecto. Es uno de los principales errores en estimación de software. Se combate documentando supuestos y usando técnicas estructuradas.

**Story Points** → ver *Punto de historia*

**Supuesto** ⭐  
Condición que se asume verdadera para que un estimado sea válido. Si el supuesto resulta falso, el estimado cambia. Documentar supuestos es obligatorio en toda propuesta técnica seria.

---

## T

**T-shirt sizing** ⭐  
Técnica de estimación que asigna tallas de camiseta (XS, S, M, L, XL) a cada funcionalidad según su complejidad relativa. Más rápido que Planning Poker y útil para estimar el proyecto completo en etapas tempranas.

**Talla (de camiseta)**  
Categoría de complejidad en T-shirt sizing: XS (1-2 días), S (3-5 días), M (6-10 días), L (11-20 días), XL (21-35 días). Solo son orientativas; la conversión exacta se ajusta según el equipo.

---

## V

**Velocidad (velocity)**  
Cantidad de Story Points que un equipo completa en un sprint (período fijo de trabajo, normalmente 2 semanas). Se usa para predecir cuándo se completará el proyecto. Se calcula después de varios sprints, no al inicio.

---

## W

**Wideband Delphi**  
Adaptación de la técnica Delphi para desarrollo de software, propuesta por Barry Boehm en 1981. Incluye reuniones de moderación, estimaciones anónimas y discusión de diferencias en ciclos iterativos.
