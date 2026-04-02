# 📖 03 — Cómo Conducir una Entrevista con el Cliente

> Teoría · Semana 2 · Cadena de Formación
> Aplica al caso de estudio: **FerreMax S.A.S.**

---

## 🎯 Objetivos

- Preparar una entrevista de levantamiento de requisitos paso a paso
- Conducir la entrevista con estructura y sin improvisación
- Documentar los resultados en un acta de reunión formal
- Saber qué hacer cuando el cliente no sabe qué quiere

---

## 1. Antes de la Entrevista: La Preparación

Una entrevista mal preparada es tiempo perdido — del cliente y del consultor. Antes de sentarte frente al cliente, debes tener claro:

### 1.1 ¿Qué ya sabes?

Revisa el entregable de la semana anterior (contexto del proyecto) y anota:
- ¿Qué problemas ya identificaste?
- ¿Qué preguntas quedaron sin responder?
- ¿Qué stakeholders están involucrados?

**Ejemplo FerreMax:** Del análisis de la semana 1, ya sabemos que Carlos no respondió: si el sistema requiere facturación DIAN, si hay software contable, cómo migrarán datos de Excel y quién lo administrará.

### 1.2 Prepara un guion de entrevista

Un guion es una lista ordenada de bloques temáticos con preguntas preparadas. No es un cuestionario rígido — es una guía para no olvidar nada.

**Estructura de un buen guion:**

```
BLOQUE 1: Calentamiento (2-3 min)
  → Saludo, presentación, propósito de la reunión

BLOQUE 2: Contexto actual (10-15 min)
  → Preguntas abiertas sobre cómo funciona hoy el negocio

BLOQUE 3: Problemas y necesidades (15-20 min)
  → Qué duele, qué falla, qué quieren mejorar

BLOQUE 4: Preguntas específicas (10-15 min)
  → Aclarar dudas concretas que quedaron de la reunión anterior

BLOQUE 5: Validación y cierre (5-10 min)
  → Confirmar lo entendido, acordar próximos pasos
```

### 1.3 Prepara el material

- Bloc de notas o laptop para tomar apuntes
- Grabadora (solo si el cliente autoriza)
- Plantilla de acta de reunión en blanco
- Copia del contexto del proyecto (entregable S01) para referenciar

---

## 2. Durante la Entrevista

### 2.1 Apertura

Empieza estableciendo confianza y dejando claro el propósito:

> "Buenos días Carlos, gracias por su tiempo. El objetivo de hoy es entender mejor las necesidades del sistema para que podamos definir exactamente qué vamos a construir. ¿Le parece bien si tomamos notas durante la reunión?"

Tres reglas de la apertura:
1. **Sé puntual.** El tiempo del cliente vale.
2. **Pide permiso para grabar o tomar notas.**
3. **Explica qué vas a hacer con la información.**

---

### 2.2 Preguntas durante la entrevista

**Empieza con preguntas abiertas:**

> "¿Cuénteme cómo es el día a día cuando un vendedor registra una venta?"
> "¿Cuál es el mayor problema que tiene el inventario hoy?"
> "¿Qué mejoraría primero si pudiera cambiar algo del proceso actual?"

**Profundiza cuando necesites más detalle:**

> "Mencionó que los precios difieren entre sedes. ¿Puede explicarme por qué son diferentes?"
> "Cuando dice 'tiempo real', ¿con cuánto retraso estaría bien? ¿5 minutos? ¿1 minuto?"

**Usa preguntas hipotéticas para encontrar requisitos implícitos:**

> "Si un vendedor olvida registrar una venta, ¿qué pasa hoy? ¿Qué debería pasar con el sistema?"
> "¿Qué pasa si dos vendedores intentan vender el último producto al mismo tiempo desde sedes distintas?"

**Confirma antes de seguir:**

> "Entiendo que el sistema debe mostrar el inventario en tiempo real para las dos sedes y que solo el gerente puede modificar precios. ¿Es correcto?"

---

### 2.3 Cuando el cliente dice "no sé"

Es normal. Algunos clientes no saben qué quieren hasta que ven opciones. Estrategias:

| Situación | Respuesta recomendada |
|-----------|----------------------|
| "No sé cómo quiero que se vea" | Muestra ejemplos de pantallas similares y pregunta qué le gusta |
| "No sé si necesito eso" | Cuéntale el costo de NO tenerlo: "Si no se hace X, entonces Y podría pasar..." |
| "Eso es problema del programador" | Explica que necesitas su opinión para que el sistema sea útil para su negocio |
| "Lo que sea, tú sabes más que yo" | Regresa al problema: "¿Qué problema estamos resolviendo con esto?" |

---

### 2.4 Señales de alerta durante la entrevista

Presta atención a estas situaciones que generan problemas después:

| Señal | Riesgo | Cómo manejarlo |
|-------|--------|----------------|
| "También quisiera que el sistema hiciera X, Y y Z" (lista interminable) | Alcance sin límite (scope creep) | Anota todo, pero deja claro que después definirán qué entra en la primera versión |
| "Lo necesito para la próxima semana" | Expectativas de tiempo irreales | Registra la expectativa, no la confirmes en el momento |
| "Ya sé cómo hacerlo — sería solo con esta tecnología..." | El cliente diseña la solución | Escucha, pero redirige: "Cuéntame el problema y yo propongo la solución técnica" |
| Contradicción entre dos stakeholders | Conflicto de requisitos | Dokumenta ambas versiones, aclara quién tiene autoridad para decidir |

---

## 3. Después de la Entrevista: El Acta

El acta de reunión es el documento que formaliza lo que se habló y acordó. Debe elaborarse **máximo 24 horas después** de la reunión para que los detalles estén frescos.

### 3.1 Estructura del Acta de Reunión

```markdown
# Acta de Reunión

**Proyecto:** [Nombre del proyecto]
**Fecha:** [DD/MM/AAAA]
**Hora inicio:** [HH:MM]    **Hora fin:** [HH:MM]
**Lugar / Modalidad:** [Presencial en... / Google Meet]

## Participantes

| Nombre | Cargo | Empresa | Firma |
|--------|-------|---------|-------|
|        |       |         |       |

## 1. Objetivo de la Reunión

[Una oración describiendo el propósito]

## 2. Temas Tratados

[Lista de los temas discutidos, con un resumen de cada uno]

## 3. Requisitos Identificados

[Lista de requisitos que surgieron — pueden ser preliminares]

## 4. Acuerdos y Compromisos

| # | Acuerdo / Compromiso | Responsable | Fecha límite |
|---|---------------------|-------------|--------------|
|   |                     |             |              |

## 5. Preguntas Pendientes

[Preguntas que surgieron pero no se pudieron responder en la reunión]

## 6. Próxima Reunión

**Fecha propuesta:** [DD/MM/AAAA]
**Objetivo:** [Qué se revisará en la siguiente reunión]
```

---

### 3.2 Validación del Acta

Después de elaborar el acta:

1. **Compártela con el cliente** (por correo o WhatsApp si es informal)
2. **Pide confirmación** de que el acta refleja correctamente lo hablado
3. **Si el cliente no responde en 48 horas**, el acta se considera aceptada
4. **Guarda la confirmación** — es evidencia del levantamiento

> 🔒 **Por qué es importante:** Si en el futuro el cliente dice "yo no pedí eso", el acta firmada (o confirmada por correo) es tu respaldo. Este hábito te salvará de muchos malentendidos profesionales.

---

## 4. Ejemplo Aplicado a FerreMax

**Contexto:** El consultor preparó la segunda reunión con Carlos Mendoza para resolver las preguntas que quedaron de la semana 1.

**Guion preparado para la segunda reunión:**

```
BLOQUE 1: Calentamiento (3 min)
  → "Buenos días Carlos. La semana pasada identificamos los problemas 
     principales. Hoy quiero profundizar en algunas preguntas específicas."

BLOQUE 2: Preguntas pendientes de la semana 1 (20 min)
  → ¿Necesitan facturación electrónica DIAN?
  → ¿Tienen software contable actualmente?
  → ¿Cómo quiere migrar los datos de los Excel actuales?
  → ¿Quién administrará el sistema una vez entregado?
  → ¿Tendrán proveedores con acceso al sistema?

BLOQUE 3: Módulos y funcionalidades (15 min)
  → ¿Qué módulos son más urgentes?
  → ¿Quién puede modificar precios?
  → ¿Cómo quiere ver el inventario en su celular?
  → ¿Qué reportes son indispensables desde el primer día?

BLOQUE 4: Validación y cierre (5 min)
  → Resumir lo hablado
  → Acordar próximos pasos
```

---

## ✅ Checklist de Verificación

- [ ] Tengo preparado un guion de entrevista con bloques temáticos para mi proyecto
- [ ] Sé distinguir entre preguntas abiertas y cerradas
- [ ] Entiendo para qué sirve el acta de reunión y cómo llenarla
- [ ] Sé qué hacer cuando el cliente no sabe qué quiere

---

*Cadena de Formación · Tecnólogo ADSO · Semana 2 de 9*
