# T-Shirt Sizing y Planning Poker

## 🎯 Objetivos

- Comprender la técnica T-shirt sizing (tallas de camiseta) y saber aplicarla
- Comprender la técnica Planning Poker y poder facilitar una sesión
- Conocer la escala de Fibonacci y por qué se usa en estimación ágil
- Saber cuándo y cómo combinar estas técnicas con analogía y Delphi

---

## 1. ¿Por qué necesitamos más técnicas?

En la clase anterior vimos **analogía** y **Delphi**: técnicas que se basan en la experiencia previa y el juicio de expertos. Ambas son poderosas, pero tienen un límite: producen resultados en días o meses (unidades de tiempo absolutas), lo que puede generar discusiones prematuras sobre el calendario antes de llegar a un acuerdo sobre la complejidad.

Las técnicas **T-shirt sizing** y **Planning Poker** resuelven ese problema al separar la estimación de la complejidad relativa de la conversión a tiempo. La lógica es:

> **Primero acordamos qué tan complejo es. Luego convertimos eso a tiempo.**

Esto hace que las conversaciones sean más productivas y los estimados más confiables.

---

## 2. T-Shirt Sizing (Tallas de Camiseta)

### ¿Qué es?

T-shirt sizing es una técnica que asigna **tallas de camiseta** (XS, S, M, L, XL) a cada funcionalidad o módulo para indicar su **complejidad relativa**. En lugar de decir "este módulo toma 45 días", decimos "este módulo es M (mediano)".

> **Analogía directa:** Es como cuando en una tienda dices "necesito una camiseta M" — no estás midiendo en centímetros, estás usando una categoría relativa que todos entienden.

### La escala de tallas

| Talla | Complejidad | Conversión sugerida | Ejemplo típico |
|-------|-------------|---------------------|----------------|
| **XS** | Mínima | 1–2 días | Ajuste de texto, cambio de color de botón |
| **S** | Pequeña | 3–5 días | Formulario simple, listado básico |
| **M** | Mediana | 6–10 días | Módulo CRUD completo con validaciones |
| **L** | Grande | 11–20 días | Módulo con lógica de negocio compleja |
| **XL** | Muy grande | 21–35 días | Integración con sistema externo, reportes avanzados |

> ⚠️ **Importante:** La conversión en días es una guía para el equipo, **no una fecha de entrega**. Varía según el tamaño del equipo, la tecnología elegida y la experiencia de quien desarrolla.

---

### ¿Cómo se aplica? — Paso a paso

**Paso 1: Prepara la lista de funcionalidades**

Usa el WBS de la Semana 3. Cada componente del WBS se convierte en un ítem a estimar.

Ejemplo con FerreMax:

```
Módulo 1: Autenticación
  1.1 Inicio de sesión
  1.2 Cierre de sesión
  1.3 Gestión de roles y permisos

Módulo 2: Inventario
  2.1 Registro de productos
  2.2 Actualización de stock
  2.3 Alertas de stock mínimo
  ...
```

**Paso 2: Define un ítem de referencia**

Elige una funcionalidad que todos conozcan bien y asígnale una talla "M". Esta es tu **ancla** de comparación.

Ejemplo: "El formulario de inicio de sesión (usuario + contraseña + validación) es una M."

**Paso 3: Compara cada funcionalidad contra esa referencia**

Para cada ítem, pregunta: ¿Es más simple, igual o más complejo que la referencia M?

- Más simple → S o XS
- Igual → M
- Más complejo → L o XL

**Paso 4: Asigna tallas y documenta el razonamiento**

| ID | Funcionalidad | Talla | Razón |
|----|--------------|-------|-------|
| 1.1 | Inicio de sesión | M | Referencia base |
| 1.2 | Cierre de sesión | XS | Destruir sesión + redirigir |
| 1.3 | Gestión de roles | L | Múltiples permisos por módulo + interfaz de administración |
| 2.1 | Registro de productos | M | Formulario + validaciones + barcode |
| 2.2 | Actualización de stock | S | Solo modifica cantidad existente |
| 2.3 | Alertas de stock mínimo | S | Regla de negocio simple + notificación |

**Paso 5: Convierte tallas a días (estimado total)**

Suma los días de cada módulo:

| Módulo | Tallas | Días estimados |
|--------|--------|----------------|
| Autenticación | M + XS + L | 7 + 1 + 15 = 23 días |
| Inventario | M + S + S + … | … |

---

### Fortalezas del T-shirt Sizing

✅ Muy rápido: se puede estimar todo un proyecto en 1–2 horas  
✅ Accesible: no requiere conocimiento técnico profundo  
✅ Útil para conversaciones con el cliente  
✅ Evita la falsa precisión de "este módulo toma exactamente 47 días"  
✅ Facilita priorización: los ítems XL son candidatos a subdividirse  

### Limitaciones del T-shirt Sizing

❌ La conversión a días tiene incertidumbre alta  
❌ Dos personas pueden entender diferente lo que es "M"  
❌ No sirve para compromisos contractuales sin ajuste posterior  
❌ El ítem de referencia influye en todo el estimado — elegirlo mal distorsiona todo  

---

## 3. Planning Poker

### ¿Qué es?

**Planning Poker** es una técnica de estimación en equipo que combina el principio Delphi (estimación independiente antes de revelar) con las **cartas de la secuencia de Fibonacci** para asignar puntos a cada funcionalidad o historia de usuario.

> **Origen:** La técnica fue descrita por James Grenning en 2002 y popularizada por Mike Cohn en su libro *Agile Estimating and Planning* (2005). Es la técnica de estimación más usada en equipos que trabajan con Scrum.

### La secuencia de Fibonacci y por qué se usa

Las cartas de Planning Poker usan la secuencia: **1, 2, 3, 5, 8, 13, 21, ?**

¿Por qué Fibonacci y no números normales (1, 2, 3, 4, 5…)?

| Propiedad | Explicación |
|-----------|-------------|
| **Incertidumbre creciente** | Cuanto más grande es la tarea, más incertidumbre hay. Fibonacci refleja esto: la diferencia entre 5 y 8 (3 puntos) tiene menos precisión posible que entre 1 y 2 (1 punto). |
| **Evita falsa precisión** | No puedes elegir 6 ni 7, solo 5 u 8. Esto fuerza tomar una posición clara. |
| **Estimación relativa** | Los puntos no son días. Un 8 es "más complejo que un 5", no "8 días". |

La carta **?** significa: "No tengo suficiente información para estimar esto."

---

### ¿Cómo se aplica? — Paso a paso

**Roles en una sesión de Planning Poker:**

| Rol | Responsabilidad |
|-----|----------------|
| **Moderador** | Lee cada historia, facilita la discusión, no vota |
| **Equipo técnico** | Estima y vota (3–7 personas) |
| **Product Owner / Cliente** | Aclara dudas sobre el negocio, no vota funciones técnicas |

---

**Paso 1: Preparación (antes de la reunión)**

- Lista de historias de usuario o funcionalidades a estimar
- Cada participante tiene su mazo de cartas (físico o digital)
- Herramientas gratuitas: [PlanningPoker.com](https://planningpoker.com), [Scrumpoker-online.org](https://www.scrumpoker-online.org/es/)

**Paso 2: Lectura de la historia**

El moderador lee la historia en voz alta. Ejemplo:

> *"Como administrador de FerreMax, quiero poder registrar un nuevo producto con nombre, descripción, precio de costo, precio de venta, cantidad inicial y código de barras, para tener el inventario actualizado desde el primer día."*

El Product Owner responde preguntas de clarificación.

**Paso 3: Estimación individual (simultánea)**

Cada miembro del equipo elige su carta **en secreto** y la coloca boca abajo. Cuando el moderador dice "¡Ya!", todos revelan su carta al mismo tiempo.

**¡Simultaneidad es clave!** Si alguien revela antes, ancla la estimación de los demás.

**Ejemplo de revelación:**

```
Ana:    [5]
Luis:   [13]
Camila: [8]
David:  [8]
```

**Paso 4: Análisis y discusión**

Si hay consenso (o diferencia de 1 carta), se acepta el valor más frecuente.

Si hay diferencias significativas (como en el ejemplo: 5 vs 13), los **valores extremos** explican su razonamiento:

- Ana (5): "Asumí que el código de barras era solo texto libre, no una integración con lector físico."
- Luis (13): "Incluí la integración con el lector de barras y la sincronización entre sedes."

La discusión enriquece el entendimiento del equipo.

**Paso 5: Segunda votación**

Con los nuevos supuestos claros, el equipo vota de nuevo:

```
Ana:    [8]
Luis:   [13]
Camila: [8]
David:  [13]
```

Hay dos valores: 8 y 13. El moderador facilita acuerdo → se adopta **13** al confirmar que la integración hardware está en el alcance.

**Paso 6: Registro**

| Historia de usuario | Estimado (Story Points) | Supuestos |
|---------------------|------------------------|-----------|
| Registro de producto | **13** | Incluye integración con lector de barras y sincronización entre sedes |

---

### Fortalezas del Planning Poker

✅ Elimina el efecto de ancla y la influencia jerárquica  
✅ Genera discusiones valiosas que clarifican el alcance  
✅ Todo el equipo se compromete con el estimado propio  
✅ Identifica ítems con incertidumbre alta (los que generan desacuerdo)  
✅ Disponible en herramientas gratuitas en línea  

### Limitaciones del Planning Poker

❌ Requiere al menos 3 personas para ser efectivo  
❌ Puede tardar mucho si hay muchas historias o mucho desacuerdo  
❌ Los puntos no son horas: requiere una calibración del equipo para las primeras conversiones  
❌ No funciona bien con equipos sin experiencia técnica en el proyecto  

---

## 4. Story Points vs. Días — ¿Cuál es la diferencia?

Esta es una de las preguntas más frecuentes al empezar con Planning Poker:

| Aspecto | Días | Story Points |
|---------|------|-------------|
| Unidad | Tiempo real | Unidad relativa de complejidad |
| Representa | Duración real | Esfuerzo + complejidad + incertidumbre |
| Cambia si hay más personas | Sí: más personas = menos días | No: el 8 sigue siendo 8 |
| Facilita comparaciones | Entre proyectos | Dentro del mismo equipo |
| Conversión a tiempo | Directo | Requiere calibración (velocidad del equipo) |

> 💡 **Para este bootcamp:** En la Semana 4 estimamos en tallas (T-shirt) o puntos (Planning Poker). La **conversión a tiempo en días** la hacemos en la **Semana 5**.

---

## 5. ¿Cuándo usar cada técnica?

| Técnica | Mejor cuando… |
|---------|--------------|
| **Analogía** | Tienes proyectos anteriores como referencia y trabajas solo o con datos históricos |
| **Delphi** | Tienes 3+ expertos disponibles y quieres consenso sin sesgos de jerarquía |
| **T-shirt sizing** | Necesitas una primera estimación rápida del proyecto completo |
| **Planning Poker** | Trabajas en equipo con metodología ágil y tienes historias de usuario definidas |

En la práctica, muchos equipos colombianos usan:
1. **T-shirt sizing** para la propuesta técnica inicial al cliente
2. **Planning Poker** durante la ejecución del proyecto en sprints

---

## 6. Herramientas gratuitas para Planning Poker

| Herramienta | URL | Características |
|-------------|-----|----------------|
| Planning Poker (Atlassian) | planningpoker.com | Online, sin registro requerido |
| Scrumpoker Online | scrumpoker-online.org/es/ | En español, exporta resultados |
| PokerPlanner | pokerplanner.io | Integra con Jira |
| Miro (free tier) | miro.com | Tablero visual + cartas personalizables |
| Cartas físicas | Imprimibles | Busca "planning poker cards PDF gratuito" |

---

## ✅ Checklist de verificación

Antes de pasar a la siguiente clase, verifica que puedes:

- [ ] Explicar la escala de tallas de T-shirt sizing (XS a XL) y su conversión sugerida
- [ ] Describir los 5 pasos para aplicar T-shirt sizing
- [ ] Explicar por qué se usa la secuencia de Fibonacci en Planning Poker
- [ ] Describir los 6 pasos de una sesión de Planning Poker
- [ ] Distinguir entre "Story Points" y "días de trabajo"
- [ ] Identificar cuándo conviene T-shirt sizing vs Planning Poker
- [ ] Nombrar al menos 1 herramienta gratuita para facilitar Planning Poker en línea

---

## 📚 Recursos adicionales

- *Agile Estimating and Planning* — Mike Cohn: el libro de referencia de Planning Poker
- "Planning Poker — Cómo estimar en equipo" — Mountain Goat Software (en inglés, con traducción automática)
- Calculadora de Planning Poker en español: scrumpoker-online.org/es/
