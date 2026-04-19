# 🛠️ Taller — Redactar la Propuesta Técnica de FerreMax

> **Referencia**: Cadena de Formación · Semana 7 · Práctica 01  
> **Duración estimada**: 2 horas 30 minutos  
> **Modalidad**: Individual o en parejas con el caso de estudio FerreMax

---

## 🎯 Objetivo del taller

Redactar las secciones principales de la propuesta técnica de FerreMax integrando los datos de las semanas anteriores, siguiendo las guías de redacción técnica de esta semana.

---

## 📋 Materiales necesarios

Antes de comenzar, ten a la mano:

- `1-teoria/03-secciones-obligatorias.md` — Referencia de qué va en cada sección
- `1-teoria/04-caso-ferremax-propuesta.md` — Borrador guía completo del caso
- `docs/caso-estudio/01-contexto-cliente.md` — Contexto base de FerreMax
- `docs/caso-estudio/05-cronograma.md` — Cronograma de S05 (15 semanas)
- `docs/caso-estudio/06-presupuesto.md` — Presupuesto de S06 ($99,165,000)
- Archivo de trabajo: `plantilla-propuesta-ferremax.md` ← **edita este archivo**

---

## Paso 1 — Portada (10 min)

Antes de redactar, necesitas identificar los datos básicos del documento.

**Ejemplo resuelto** — Los siguientes datos ya están definidos en el caso FerreMax:

| Campo | Valor |
|-------|-------|
| Nombre del documento | Propuesta Técnica |
| Nombre del proyecto | Sistema de Gestión Integrada FerreMax |
| Cliente | FerreMax S.A.S. |
| Contacto cliente | Carlos Ramírez — Gerente General |

**Tu turno**: Abre `plantilla-propuesta-ferremax.md` y completa los campos marcados con `<!-- Completar -->` en la portada.

> 📌 Campos a completar: versión, fecha de emisión, válida hasta, nombre de los miembros del equipo proveedor.

---

## Paso 2 — Resumen ejecutivo (30 min)

El resumen ejecutivo es la sección más importante. Recuerda la estructura de 4 párrafos:

**Estructura a seguir:**

```
Párrafo 1 → El problema de FerreMax (datos concretos: 3 sucursales, sin sistema, inconsistencias de stock)
Párrafo 2 → La solución (sistema web, módulos, tecnología open source)
Párrafo 3 → Cómo y cuánto tiempo (metodología iterativa, 15 semanas, 2 desarrolladores)
Párrafo 4 → Precio y condiciones principales ($99,165,000 COP, 30/40/30)
```

**Ejemplo resuelto** (párrafo 1):

> "FerreMax S.A.S. opera actualmente tres puntos de venta en Cali sin un sistema unificado que permita controlar el inventario, registrar las ventas y gestionar la cartera de clientes. Esta situación genera inconsistencias en el stock entre sucursales, dificultades para la facturación y ausencia de información consolidada para la toma de decisiones gerenciales."

**Tu turno**: Escribe los párrafos 2, 3 y 4 en la sección de resumen ejecutivo de la plantilla.

> ⚠️ Verificación: ¿Tu resumen tiene entre 200 y 350 palabras? ¿Puede entenderlo el gerente de FerreMax sin saber programación?

---

## Paso 3 — Análisis del problema (25 min)

En este paso debes redactar las tres subsecciones del análisis del problema.

**Ejemplo resuelto** — Problema P01 (ya dado en la teoría):

> "**P01 — Inconsistencia de stock entre sucursales**: El mismo producto puede aparecer con stock disponible en la sucursal A mientras registra agotado en la sucursal B, sin cruce de información en tiempo real. Esto genera ventas fallidas y compras duplicadas."

**Tu turno**: Completa la tabla de herramientas actuales de FerreMax con los datos faltantes (marcados con `<!-- Completar -->`):

| Proceso | Herramienta actual | Limitación |
|---------|-------------------|------------|
| Control de inventario | Archivos Excel por WhatsApp | <!-- Completar → ¿qué problema genera? --> |
| Registro de ventas | Facturas talonario en papel | <!-- Completar → ¿qué problema genera? --> |
| Reportes gerenciales | Construidos manualmente cada semana | <!-- Completar → ¿cuánto tiempo pierde el gerente? --> |

> 💡 Tip: Los datos de este problema están en `docs/caso-estudio/01-contexto-cliente.md`.

---

## Paso 4 — Propuesta de solución (30 min)

Esta sección describe qué se va a construir.

**Ejemplo resuelto** — Descripción general de la solución (párrafo 1, ya dado en la teoría):

> "Se propone el desarrollo de un sistema web de acceso multi-sucursal denominado FerreMax GI (Gestión Integrada), que centralizará el inventario, las ventas y la gestión de clientes y proveedores de los tres puntos de venta en una única plataforma de acceso web."

**Tu turno**: Completa la tabla de stack tecnológico con la justificación para cada tecnología:

| Capa | Tecnología | Tu justificación (¿por qué esta tecnología para FerreMax?) |
|------|-----------|-------------------------------------------------------------|
| Backend | Python 3.12 + FastAPI | <!-- Completar min. 10 palabras --> |
| Base de datos | PostgreSQL 16 | <!-- Completar min. 10 palabras --> |
| Frontend | React 18 + Vite | <!-- Completar min. 10 palabras --> |
| Infraestructura | AWS EC2 + S3 | <!-- Completar min. 10 palabras --> |

> 💡 Tip: Consulta la sección 4.3 de la teoría 04 para ver las justificaciones completas. Redacta con tus propias palabras.

---

## Paso 5 — Alcance: en el alcance y fuera del alcance (20 min)

Esta sección viene directamente del documento de alcance de la Semana 3.

**Ejemplo resuelto** — Primera funcionalidad fuera del alcance:

> "Integración con facturación electrónica DIAN: No está incluida en el alcance por requerir un servicio habilitador de facturación electrónica adicional y certificaciones ante la DIAN que están fuera del tiempo estimado."

**Tu turno**: Agrega 2 ítems más a la lista de funcionalidades fuera del alcance en la plantilla. Deben ser funcionalidades reales para el tipo de sistema de FerreMax, pero que no están en los módulos M1–M6.

---

## Paso 6 — Cronograma y costos (15 min)

En este paso integras los datos de S05 y S06 en la propuesta.

**Verificación de coherencia** (responde en tu plantilla):

| Pregunta | Dato en S05/S06 | Dato en tu propuesta | ¿Coinciden? |
|----------|----------------|---------------------|-------------|
| ¿Cuántas semanas dura el proyecto? | 15 semanas | `___` semanas | Sí / No |
| ¿Cuántos desarrolladores? | 2 (Dev A + Dev B) | `___` | Sí / No |
| ¿Cuál es el costo total? | $99,165,000 COP | $`___` COP | Sí / No |
| ¿Cuál es el anticipo? | 30% = $29,749,500 | $`___` | Sí / No |

> ⚠️ Si algún dato no coincide, corrígelo en la plantilla antes de continuar. La coherencia numérica es un criterio de evaluación.

---

## Paso 7 — Supuestos y firma (10 min)

Los supuestos son las condiciones que se asumen como verdaderas. Si cambian, el precio puede cambiar.

**Ejemplo resuelto** — Supuesto SP-01 (ya dado):

> "FerreMax proporcionará acceso a la red interna y al dominio web en los primeros 5 días hábiles del proyecto."

**Tu turno**: Escribe un supuesto adicional (SP-06) que no esté en la lista de la plantilla. El supuesto debe ser específico para el proyecto FerreMax y realista.

```
SP-06: ___________________________________________________________
```

---

## ✅ Checklist final del taller

Antes de dar por terminado el taller, verifica:

- [ ] La portada tiene versión, fecha y datos del cliente y proveedor
- [ ] El resumen ejecutivo tiene los 4 párrafos y no supera 350 palabras
- [ ] El análisis del problema tiene la tabla de herramientas actuales completa
- [ ] La propuesta de solución tiene la tabla de stack con justificaciones
- [ ] La sección de alcance tiene al menos 3 ítems fuera del alcance
- [ ] Los números de cronograma y costos coinciden con S05 y S06
- [ ] Agregaste un supuesto SP-06 propio

---

*Cadena de Formación · Tecnólogo ADSO · Semana 7 de 9*
