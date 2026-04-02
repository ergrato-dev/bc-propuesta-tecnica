# ✍️ Redacción Técnica para Propuestas de Ingeniería de Software

> **Referencia**: Cadena de Formación · Semana 7 · Teoría 02

---

## 🎯 Objetivos de esta lectura

- Aplicar las reglas básicas de redacción técnica profesional
- Identificar y corregir los errores de lenguaje más frecuentes en propuestas de aprendices
- Redactar el resumen ejecutivo de una propuesta técnica

---

## 1. ¿Qué es la redacción técnica?

La **redacción técnica** es la escritura orientada a transmitir información precisa, sin ambigüedades, de forma profesional. En el contexto de propuestas TI colombianas, sigue estas características:

| Característica | Descripción |
|---------------|-------------|
| **Impersonal** | Se prefiere la voz activa impersonal: "El sistema registrará..." (no "nosotros haremos...") |
| **Precisa** | Usa términos exactos: "módulo de autenticación con JWT" (no "la parte del login") |
| **Concisa** | Dice lo necesario sin relleno: "El proyecto durará 15 semanas" (no "se estima que el proyecto podría llegar a tener una duración aproximada de alrededor de 15 semanas") |
| **Estructurada** | Párrafos cortos (3–5 oraciones), títulos claros, tablas para datos comparativos |
| **Verificable** | Cada afirmación puede respaldarse: "Según la encuesta Stack Overflow 2024, la tarifa promedio de un desarrollador junior en Colombia es de $28,000–$40,000/hora" |

---

## 2. Reglas de oro para documentos de ingeniería

### Regla 1 — Introduce antes de presentar datos

❌ **Incorrecto** (tabla sin contexto):

```
## Cronograma

| Semana | Actividad |
|--------|-----------|
| 1      | Inicio    |
```

✅ **Correcto** (párrafo introductorio antes de la tabla):

```
## Cronograma

El proyecto se ejecutará en 15 semanas calendario distribuidas en 5 fases.
La siguiente tabla resume los hitos principales del proyecto.

| Semana | Actividad |
|--------|-----------|
| 1      | Inicio    |
```

---

### Regla 2 — Nada de lenguaje coloquial

| ❌ Lenguaje coloquial | ✅ Lenguaje técnico-formal |
|----------------------|--------------------------|
| "vamos a hacer un sistema" | "Se desarrollará un sistema web" |
| "básicamente es un CRUD" | "El módulo gestiona operaciones de creación, consulta, actualización y eliminación de registros" |
| "no es tan difícil hacerlo" | "El módulo tiene complejidad baja-media según la estimación de esfuerzo" |
| "el cliente quiere que..." | "El cliente ha manifestado el requerimiento de..." |
| "tipo Facebook pero para ferreterías" | "Plataforma web de gestión empresarial orientada al sector ferretero" |
| "la parte del login" | "El módulo de autenticación y control de acceso" |

---

### Regla 3 — Define el acrónimo la primera vez que lo usas

❌ "El sistema usará JWT para la autenticación y PostgreSQL como DBMS."

✅ "El sistema usará JWT (JSON Web Token) para la autenticación y PostgreSQL como DBMS (Sistema Gestor de Bases de Datos)."

> A partir de la segunda mención, puedes usar solo la sigla.

---

### Regla 4 — Usa números concretos, no rangos en afirmaciones clave

❌ "El proyecto costará entre $80 y $120 millones."

✅ "El costo total del proyecto asciende a $99,165,000 COP, sujeto a los supuestos descritos en la Sección 10."

---

### Regla 5 — Numera tus secciones y subsecciones

Facilita las referencias cruzadas en el mismo documento y en conversaciones con el cliente.

```
1. Información general
2. Resumen ejecutivo
3. Antecedentes y análisis del problema
   3.1 Descripción de la situación actual
   3.2 Problemática identificada
4. Propuesta de solución
```

---

## 3. Cómo escribir el resumen ejecutivo

El resumen ejecutivo es **la sección más importante del documento**. Sigue esta estructura:

```
Párrafo 1 — El problema del cliente (2–3 oraciones)
Párrafo 2 — La solución propuesta (2–3 oraciones)
Párrafo 3 — Cómo se va a ejecutar: método y duración (1–2 oraciones)
Párrafo 4 — Costo y condiciones de pago principales (1–2 oraciones)
```

**Extensión**: 200 a 350 palabras · Máximo 1 página

---

### Ejemplo de resumen ejecutivo — FerreMax

> **Caso de estudio** · El siguiente resumen corresponde a la propuesta técnica para FerreMax S.A.S.

---

*FerreMax S.A.S. opera actualmente tres puntos de venta en la ciudad de Cali sin un sistema unificado que permita controlar el inventario, registrar las ventas y gestionar la cartera de clientes. Esta situación genera inconsistencias en el stock entre sucursales, pérdidas por ventas sin facturación y dificultades para identificar los productos de mayor rotación.*

*La presente propuesta plantea el desarrollo de un sistema web de gestión integrada que centralizará el inventario, las ventas y la información de clientes y proveedores de las tres sucursales en tiempo real. La solución estará construida sobre tecnologías de código abierto (Python, FastAPI, PostgreSQL, React), lo que elimina costos de licenciamiento y asegura una base tecnológica de largo plazo.*

*El proyecto se ejecutará en 15 semanas mediante una metodología iterativa con entregas por módulo, lo que permitirá a FerreMax verificar el avance y hacer ajustes de forma oportuna. El equipo está compuesto por dos desarrolladores con experiencia en el stack tecnológico propuesto.*

*El costo total del proyecto asciende a $99,165,000 COP, con una condición de pago escalonada: 30% al inicio, 40% al alcanzar los hitos intermedios y 30% en la entrega final. La presente propuesta tiene una validez de 30 días calendario a partir de la fecha de emisión.*

---

> 📊 **Análisis del ejemplo**:
> - Párrafo 1: problema concreto de FerreMax (stock, ventas, cartera)
> - Párrafo 2: solución (sistema web, módulos, tecnología open source)
> - Párrafo 3: cómo y cuánto tiempo (15 semanas, iterativo, equipo)
> - Párrafo 4: precio exacto + condiciones

---

## 4. Errores frecuentes en propuestas de aprendices

| Error | Descripción | Cómo evitarlo |
|-------|-------------|---------------|
| **Secciones vacías** | Secciones con "Por completar" o "N/A" | Nunca entregar con secciones incompletas |
| **Datos contradictorios** | El cronograma dice 12 semanas pero los costos reflejan 20 semanas | Revisar coherencia entre S05, S06 y S07 antes de entregar |
| **Resumen muy técnico** | El resumen ejecutivo habla de APIs, endpoints y migraciones de base de datos | Escribir el resumen para el gerente, no para el desarrollador |
| **Tablas sin contexto** | Una tabla con 20 filas sin introducción ni conclusión | Siempre: párrafo introductorio + tabla + párrafo de conclusión |
| **Alcance ambiguo** | "El sistema incluirá reportes" sin especificar cuáles ni cuántos | Todo lo que entra en el alcance debe ser específico y verificable |
| **Lenguaje futuro incierto** | "Se podría implementar un módulo de facturación electrónica" | Usa el futuro afirmativo: "El módulo de facturación electrónica registrará..." |

---

## 5. Tono correcto para cada sección

| Sección | Tono recomendado | Por qué |
|---------|-----------------|---------|
| Resumen ejecutivo | Persuasivo + claro + no técnico | El directivo decide si sigue leyendo |
| Análisis del problema | Diagnóstico + objetivo + basado en hechos | Muestra que entiendes el negocio del cliente |
| Solución técnica | Técnico + seguro + concreto | El equipo técnico evalúa la idoneidad de la solución |
| Alcance | Preciso + directo + sin ambigüedades | Evita discusiones futuras sobre "¿eso quedó incluido?" |
| Cronograma | Formal + comprometido | El directivo evaluará si los plazos son razonables |
| Costos | Formal + justificado + transparente | El directivo necesita entender qué incluye el precio |
| Condiciones | Legal-formal + claro | Base de la negociación contractual posterior |

---

## ✅ Checklist de esta lectura

- [ ] Identifico al menos 3 errores de redacción coloquial en propuestas
- [ ] Sé la estructura de 4 párrafos del resumen ejecutivo
- [ ] Aplico la regla de introducir cada tabla con un párrafo
- [ ] Uso lenguaje técnico formal en las secciones de mi propuesta

---

*Cadena de Formación · Tecnólogo ADSO · Semana 7 de 9*
