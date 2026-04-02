# Taller 01 — Del Esfuerzo al Cronograma: FerreMax

## 🎯 Objetivo del taller

En este taller vas a tomar los resultados de estimación de la Semana 4 y convertirlos en un cronograma real con fechas, Gantt y hitos. Trabajarás sobre el caso FerreMax, el mismo que hemos venido usando.

**Duración estimada:** 2.5 horas

---

## 📋 Contexto rápido

**Proyecto:** FerreMax S.A.S. — Sistema de gestión de inventario, clientes y ventas  
**Equipo:** 2 desarrolladores full-stack  
**Total de esfuerzo (S04):** 194 días-persona  
**Factor de capacidad a usar:** 80% (0.80)

Ya sabes cuánto *esfuerzo* requiere cada módulo. Ahora vas a convertir eso en tiempo real de calendario.

---

## Paso 1: Calcula la duración base del proyecto

**Instrucción:** Usa la fórmula que aprendiste en la Teoría 01 para calcular cuántos días de calendario toma el proyecto si el equipo trabaja en secuencia (uno detrás del otro, sin paralelismo).

**Fórmula:**
$$\text{Duración base} = \frac{\text{Esfuerzo total}}{\text{Personas} \times \text{Factor de capacidad}}$$

**Ejemplo resuelto:**

| Variable | Valor |
|----------|-------|
| Esfuerzo total | 194 días-persona |
| Personas | 2 |
| Factor de capacidad | 0.80 |
| **Duración base** | **194 ÷ (2 × 0.80) = ?** |

**Tu turno:** Completa el cálculo aquí:

```
Duración base = 194 ÷ (_____ × _____) = _______ días
```

Ahora agrega el buffer del 15% para imprevistos:

```
Con buffer = _______ × 1.15 = _______ días ≈ _______ semanas
```

---

## Paso 2: Establece las dependencias entre módulos

**Instrucción:** Lee la tabla de módulos e indica cuáles pueden desarrollarse en *paralelo* y cuáles deben esperar a que otro termine primero.

**Referencia — Módulos de FerreMax:**

| ID | Módulo | Esfuerzo (días-persona) |
|----|--------|------------------------|
| M0 | BD + Arquitectura base | 10 (5+5) |
| M1 | Autenticación | 31 |
| M2 | Inventario | 67 |
| M3 | Clientes | 12 |
| M4 | Ventas | 48 |
| M5 | Reportes | 20 |
| M6 | Config. y Documentación | 16 |

**Ejemplo resuelto:**

| Módulo | ¿Depende de? | ¿Puede ir en paralelo con? |
|--------|-------------|---------------------------|
| M0 — BD + Arquitectura | Ninguno (es el primero) | Nada (bloquea a todos) |
| M1 — Autenticación | M0 | No — M0 debe estar listo |

**Tu turno:** Completa la tabla para los módulos restantes:

| Módulo | ¿Depende de? | ¿Puede ir en paralelo con? |
|--------|-------------|---------------------------|
| M2 — Inventario | <!-- Completar: ¿qué debe estar listo antes? --> | <!-- ¿Algún módulo puede desarrollarse al mismo tiempo? --> |
| M3 — Clientes | <!-- Completar --> | <!-- Completar --> |
| M4 — Ventas | <!-- Completar --> | <!-- Completar --> |
| M5 — Reportes | <!-- Completar --> | <!-- Completar --> |
| M6 — Config. y Docs | <!-- Completar --> | <!-- Completar --> |

> 💡 **Pista:** Para un sistema web con login, todos los módulos funcionales dependen de que la autenticación esté lista. Las ventas dependen de que existan productos (inventario) y clientes registrados.

---

## Paso 3: Asigna módulos al equipo

**Instrucción:** Con Dev A y Dev B disponibles, decide quién trabaja en qué módulo. Recuerda: dos devs pueden trabajar en paralelo en módulos *sin dependencia entre sí*.

**Ejemplo resuelto:**

| Módulo | Asignado a | Semana inicio | Semana fin |
|--------|-----------|--------------|-----------|
| M0 — BD + Arquitectura | Dev A + Dev B | S1 | S1 |
| M1 — Autenticación | Dev A | S2 | S5 |

**Tu turno:** Completa la asignación:

| Módulo | Asignado a | Semana inicio | Semana fin |
|--------|-----------|--------------|-----------|
| M2 — Inventario | <!-- Dev A / Dev B / Ambos --> | <!-- S? --> | <!-- S? --> |
| M3 — Clientes | <!-- Dev A / Dev B / Ambos --> | <!-- S? --> | <!-- S? --> |
| M4 — Ventas | <!-- Dev A / Dev B / Ambos --> | <!-- S? --> | <!-- S? --> |
| M5 — Reportes | <!-- Dev A / Dev B / Ambos --> | <!-- S? --> | <!-- S? --> |
| M6 — Config. y Docs | <!-- Dev A / Dev B / Ambos --> | <!-- S? --> | <!-- S? --> |
| Pruebas integración | Ambos | <!-- S? --> | <!-- S? --> |
| Despliegue | Ambos | <!-- S? --> | <!-- S? --> |

---

## Paso 4: Construye el Gantt

**Instrucción:** Completa el diagrama de Gantt llenando `██` en las semanas en que cada módulo está activo. Usa la tabla del Paso 3 como referencia.

```
Módulo / Actividad         | S1 | S2 | S3 | S4 | S5 | S6 | S7 | S8 | S9 |S10 |S11 |S12 |S13 |S14 |S15 |
---------------------------|----|----|----|----|----|----|----|----|----|----|----|----|----|----|-----|
BD + Arquitectura (A+B)    | ██ |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
Autenticación (Dev A)      |    | ██ | ██ | ██ | ██ |    |    |    |    |    |    |    |    |    |    |
Inventario (Dev B)         |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
  ← Completar: ¿S? a S?   |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
Clientes (Dev A)           |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
  ← Completar              |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
Ventas (Dev A + Dev B)     |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
  ← Completar              |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
Reportes (Dev A)           |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
  ← Completar              |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
Config y Docs (Dev B)      |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
  ← Completar              |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
Pruebas integración (A+B)  |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
  ← Completar              |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
Despliegue + Caps (A+B)    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
  ← Completar              |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
```

---

## Paso 5: Define los hitos del proyecto

**Instrucción:** Define 3 hitos para el proyecto FerreMax. Un hito es un punto de control que marca el fin de una fase importante.

**Ejemplo resuelto:**

| Hito | Nombre | Semana | Criterio de aceptación |
|------|--------|--------|----------------------|
| H1 | Autenticación y BD listos en staging | S5 | Carlos Mendoza puede iniciar sesión; los 3 roles están configurados |

**Tu turno:** Define los hitos H2 y H3:

| Hito | Nombre | Semana | Criterio de aceptación |
|------|--------|--------|----------------------|
| H2 | <!-- Nombre del hito --> | <!-- S? --> | <!-- ¿Qué debe cumplirse para aprobarlo? --> |
| H3 | <!-- Nombre del hito --> | <!-- S? --> | <!-- ¿Qué debe cumplirse? Ej: "todo el sistema en pruebas" --> |
| H4 | Entrega final | S15 | Sistema en producción + 2 sesiones de capacitación completadas |

---

## Paso 6: Identifica la ruta crítica

**Instrucción:** Escribe la secuencia de módulos que forman la ruta crítica (la cadena más larga de dependencias).

**Ejemplo de respuesta (incompleto):**
```
BD + Arquitectura (S1) → Autenticación (S2-S5) → _______ → _______ → Despliegue (S?)
```

Completa la ruta crítica:

```
BD (S1) → _________ (S2-S5) → _________ (S?-S?) → _________ (S?-S?) → Pruebas (S?-S?) → Despliegue (S?)
```

**Responde:** ¿Por qué el módulo de _________ es el cuello de botella del proyecto?

```
Respuesta: _______________________________________________
```

---

## 🏁 Revisión final

Al terminar el taller verifica:

- [ ] Calculé la duración base y la duración con buffer
- [ ] Identifiqué correctamente qué módulos dependen de cuáles
- [ ] Asigné módulos al equipo aprovechando el trabajo en paralelo
- [ ] Construí el Gantt con todas las semanas completas
- [ ] Definí los 4 hitos con criterios de aceptación claros
- [ ] Identifiqué la ruta crítica y expliqué por qué ese módulo es el cuello de botella

---

> 📄 Continúa con **`plantilla-cronograma-ferremax.md`** para consolidar el cronograma completo en formato de propuesta técnica.
