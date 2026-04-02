# FerreMax: Del Esfuerzo al Cronograma Completo

## 🎯 Objetivos de esta clase

- Ver cómo se convierte la tabla de estimación de la Semana 4 en un cronograma real
- Construir el Gantt de FerreMax semana a semana
- Identificar la ruta crítica del proyecto FerreMax

---

## 1. Punto de partida — Lo que tenemos de la Semana 4

De la Semana 4, el equipo de consultores tiene:

**Tabla de esfuerzo consolidada:**

| Módulo | Esfuerzo (días-persona) |
|--------|------------------------|
| 1 — Autenticación | 31 |
| 2 — Inventario | 67 |
| 3 — Clientes | 12 |
| 4 — Ventas | 48 |
| 5 — Reportes | 20 |
| 6 — Config. y Documentación | 16 |
| **TOTAL** | **194** |

**Supuesto del equipo:** 2 desarrolladores full-stack a tiempo completo.

---

## 2. Paso 1: Calcular la duración base

Aplicando la fórmula de la Teoría 01:

```
Duración base = Esfuerzo ÷ (Personas × Factor de capacidad)
             = 194 ÷ (2 × 0.80)
             = 194 ÷ 1.60
             = 121 días de calendario ≈ 24 semanas de trabajo
```

Con un **buffer del 15%** para imprevistos y correcciones:

```
121 × 1.15 = 139 días ≈ 28 semanas ≈ 7 meses
```

Pero recordemos que los módulos **no se hacen todos en serie** — hay oportunidades de paralelismo.

---

## 3. Paso 2: Definir dependencias entre módulos

Antes de construir el Gantt, el equipo identifica qué debe hacerse antes de qué:

| Módulo | Depende de | Justificación |
|--------|-----------|---------------|
| Configuración inicial de BD | — | Primer paso de todo sistema |
| Autenticación (Módulo 1) | BD configurada | Necesita tablas de usuarios en la BD |
| Inventario (Módulo 2) | Autenticación | Todas las operaciones de inventario requieren login |
| Clientes (Módulo 3) | Autenticación | Misma razón |
| Ventas (Módulo 4) | Inventario + Clientes | Una venta necesita productos (inventario) y cliente |
| Reportes (Módulo 5) | Ventas + Inventario | Los reportes consolidan datos de ventas e inventario |
| Config. y Docs (Módulo 6) | Módulo 1 (parcial) | La configuración del sistema arranca desde autenticación |

**Flujograma de dependencias:**

```
BD + Arquitectura
       ↓
   Autenticación (M1)
   ↙              ↘
Inventario (M2)  Clientes (M3)
       ↓          ↙
    Ventas (M4)
       ↓
   Reportes (M5)
       ↓
 Pruebas de integración
       ↓
   Despliegue + Capacitación (M6)
```

---

## 4. Paso 3: Asignar módulos al equipo

Con 2 desarrolladores (Dev A y Dev B), el equipo decide la asignación:

| Módulo | Asignado a | Días de esfuerzo |
|--------|-----------|-----------------|
| BD + Arquitectura inicial | Dev A + Dev B (juntos) | 5 días c/u = 10 |
| Autenticación | Dev A | 31 días |
| Inventario | Dev B (con apoyo Dev A en integración barcode) | 67 días |
| Clientes | Dev A (mientras Dev B termina inventario) | 12 días |
| Ventas | Dev A + Dev B | 48 días |
| Reportes | Dev A | 20 días |
| Config. y Docs | Dev B | 16 días |

---

## 5. Paso 4: Convertir esfuerzo a duración por módulo

Con equipo de 2 devs y capacidad del 80%:

| Módulo | Esfuerzo (días-p) | Dev(s) asignados | Duración (semanas) |
|--------|------------------|------------------|--------------------|
| BD + Arquitectura | 10 (5+5) | Dev A + Dev B | ~1 semana (en paralelo) |
| Autenticación | 31 | Dev A | ~4 semanas |
| Inventario | 67 | Dev B | ~8 semanas |
| Clientes | 12 | Dev A | ~1.5 semanas |
| Ventas | 48 | Dev A + Dev B | ~3 semanas (en paralelo) |
| Reportes | 20 | Dev A | ~2.5 semanas |
| Config. y Docs | 16 | Dev B | ~2 semanas |
| Pruebas de integración | (incluido en buffer) | Ambos | ~2 semanas |
| Despliegue + capacitación | (incluido en buffer) | Ambos | ~1 semana |

---

## 6. El Cronograma de FerreMax — Gantt por semanas

```
Módulo / Actividad         | S1 | S2 | S3 | S4 | S5 | S6 | S7 | S8 | S9 |S10 |S11 |S12 |S13 |S14 |S15 |
---------------------------|----|----|----|----|----|----|----|----|----|----|----|----|----|----|-----|
BD + Arquitectura (A+B)    | ██ |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
Autenticación (Dev A)      |    | ██ | ██ | ██ | ██ |    |    |    |    |    |    |    |    |    |    |
● Hito H1: Autenticación   |    |    |    |    | ●  |    |    |    |    |    |    |    |    |    |    |
Inventario — parte 1 (B)   |    | ██ | ██ | ██ | ██ | ██ | ██ | ██ |    |    |    |    |    |    |    |
Clientes (Dev A)           |    |    |    |    |    | ██ |    |    |    |    |    |    |    |    |    |
● Hito H2: Inventario + Clientes |  |    |    |    |    |    |    | ●  |    |    |    |    |    |    |    |
Ventas (Dev A + Dev B)     |    |    |    |    |    |    |    | ██ | ██ | ██ |    |    |    |    |    |
Reportes (Dev A)           |    |    |    |    |    |    |    |    |    |    | ██ | ██ |    |    |    |
Config. y Docs (Dev B)     |    |    |    |    |    |    |    |    |    |    | ██ | ██ |    |    |    |
● Hito H3: Sistema completo|    |    |    |    |    |    |    |    |    |    |    | ●  |    |    |    |
Pruebas integración (A+B)  |    |    |    |    |    |    |    |    |    |    |    |    | ██ | ██ |    |
Despliegue + Capacitación  |    |    |    |    |    |    |    |    |    |    |    |    |    |    | ██ |
● Hito H4: Entrega final   |    |    |    |    |    |    |    |    |    |    |    |    |    |    | ●  |
```

**Duración total del proyecto: 15 semanas ≈ 3.5 meses de calendario**

> ¿Por qué 15 semanas y no 28? Porque la **ejecución en paralelo** (Dev A y Dev B trabajando en módulos distintos simultáneamente) reduce significativamente la duración. El esfuerzo total es 194 días-persona, pero la duración calendarizada es ~60 días hábiles.

---

## 7. Los 4 Hitos de FerreMax

| Hito | Semana | Entregable | Criterio de aceptación |
|------|--------|-----------|------------------------|
| **H1: Autenticación y BD lista** | Semana 5 | Sistema de login funcionando en staging | Carlos Mendoza puede iniciar sesión con su usuario; los 3 roles están configurados |
| **H2: Inventario y Clientes listos** | Semana 8 | Módulos 2 y 3 en staging | El gerente puede registrar productos, hacer control de stock y registrar clientes |
| **H3: Sistema completo integrado** | Semana 12 | Todos los módulos desplegados en staging | Flujo completo: login → inventario → venta → factura → reporte; sin errores críticos |
| **H4: Entrega final** | Semana 15 | Sistema en producción + capacitación completada | Sistema accesible desde sedes Kennedy y Fontibón; 2 sesiones de capacitación completadas |

---

## 8. La Ruta Crítica de FerreMax

La ruta crítica es la cadena más larga de tareas dependientes:

```
BD + Arquitectura (S1)
    → Autenticación (S2–S5)
        → Inventario (S2–S9) ← este es el cuello de botella
            → Ventas (S8–S10)
                → Pruebas (S13–S14)
                    → Despliegue (S15)
```

**La ruta crítica pasa por el Módulo de Inventario** (67 días de esfuerzo, desarrollado por Dev B). Si el módulo de inventario se retrasa, todo el proyecto se retrasa. Por eso:

- El Dev B está 100% asignado al inventario
- El Dev A puede trabajar en paralelo (autenticación, luego clientes, luego ventas)
- Los módulos de reportes y configuración son de la ruta NO crítica — tienen ~2 semanas de holgura

---

## 9. ¿Qué pasa si hay retraso?

Si el Módulo de Inventario se retrasa 2 semanas (por un problema con la integración del lector de barras, supuesto SG-01 de no cumplirse), el cronograma se afecta así:

| Escenario | Impacto |
|-----------|---------|
| Inventario +2 semanas de retraso | Ventas no puede iniciar hasta S11 → Pruebas se trasladan a S15 → Entrega final: S17 |
| Retraso en Reportes (no crítico) | Sin impacto en entrega final (tiene 2 semanas de holgura) |
| Cliente no disponible para H2 | Si la demo se retrasa 1 semana, el siguiente bloque empieza 1 semana más tarde |

---

## 10. Tabla consolidada para la Propuesta Técnica

Esta es la sección "Cronograma" que incluirán en la propuesta técnica de FerreMax:

| Fase | Semanas | Módulos | Hitos |
|------|---------|---------|-------|
| Fase 1: Infraestructura y Autenticación | S1–S5 | BD + Módulo 1 | H1 en S5 |
| Fase 2: Módulos funcionales | S2–S10 | Módulos 2, 3, 4 | H2 en S8 |
| Fase 3: Integración y reportes | S10–S12 | Módulos 5 y 6 | H3 en S12 |
| Fase 4: Pruebas y entrega | S13–S15 | Pruebas + despliegue + caps. | H4 en S15 |

**Fecha estimada de entrega:** 15 semanas desde el inicio del proyecto (aprox. 3.5 meses).  
**Condición:** Esta fecha asume el cumplimiento de todos los supuestos del documento `04-estimacion-tecnicas.md`.

---

## ✅ Checklist de verificación

Después de esta clase, deberías poder:

- [ ] Explicar cómo se pasó de 194 días-persona a 15 semanas de calendario
- [ ] Leer el Gantt de FerreMax y decir qué semana trabaja cada developer en qué
- [ ] Identificar los 4 hitos y sus criterios de aceptación
- [ ] Identificar la ruta crítica y explicar por qué un retraso en inventario afecta todo
- [ ] Explicar qué módulos tienen holgura y por qué
