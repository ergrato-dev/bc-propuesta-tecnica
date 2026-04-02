# Plantilla de Cronograma — FerreMax S.A.S.

> **Instrucciones:** Esta plantilla es para consolidar el cronograma del proyecto FerreMax en el formato que incluirías en la propuesta técnica. Completa todas las celdas marcadas como `<!-- Completar -->`. Algunas filas tienen datos de referencia ya calculados en el taller.

---

## Sección A: Datos del Proyecto

| Campo | Valor |
|-------|-------|
| **Proyecto** | Sistema de Gestión FerreMax |
| **Cliente** | FerreMax S.A.S. — Carlos Mendoza |
| **Equipo** | 2 desarrolladores full-stack |
| **Total de esfuerzo** | 194 días-persona |
| **Duración base calculada** | <!-- Completar: 194 ÷ (2 × 0.80) = ? días --> |
| **Duración con buffer (15%)** | <!-- Completar: ? × 1.15 = ? días ≈ ? semanas --> |
| **Fecha de inicio estimada** | Semana 1 (referencia) |
| **Fecha de entrega estimada** | <!-- Completar: Semana ? --> |

---

## Sección B: Tabla de Duración por Módulo

<!-- 📝 Instrucción: Para cada módulo, calcula la duración individual teniendo en cuenta quién está asignado y con qué factor.
     Fórmula: Duración = Esfuerzo ÷ (Personas asignadas × 0.80)
     Redondea al número entero de días o semanas superior. -->

<!-- Ejemplo resuelto:
| M0 — BD + Arquitectura | 10 | Dev A + Dev B | 2 | 80% | 10 ÷ (2 × 0.80) = 6.25 ≈ 1 semana |
-->

| Módulo | Esfuerzo (días-p) | Asignado a | Personas | Factor cap. | Duración estimada |
|--------|------------------|-----------|---------|------------|------------------|
| M0 — BD + Arquitectura | 10 | Dev A + Dev B | 2 | 80% | <!-- Completar: ? semanas --> |
| M1 — Autenticación | 31 | Dev A | 1 | 80% | <!-- Completar: ? semanas --> |
| M2 — Inventario | 67 | Dev B | 1 | 80% | <!-- Completar: ? semanas --> |
| M3 — Clientes | 12 | Dev A | 1 | 80% | <!-- Completar: ? semanas --> |
| M4 — Ventas | 48 | Dev A + Dev B | 2 | 80% | <!-- Completar: ? semanas --> |
| M5 — Reportes | 20 | Dev A | 1 | 80% | <!-- Completar: ? semanas --> |
| M6 — Config. y Docs | 16 | Dev B | 1 | 80% | <!-- Completar: ? semanas --> |
| Pruebas de integración | (buffer incluido) | Ambos | 2 | 80% | 2 semanas (planificadas) |
| Despliegue + Capacitación | (buffer incluido) | Ambos | 2 | 80% | 1 semana (planificada) |

---

## Sección C: Diagrama de Gantt — Vista por semanas

<!-- 📝 Instrucción: Llena `██` en las celdas correspondientes a las semanas en que cada módulo está activo.
     La fila de autenticación ya está completa como referencia. Completa el resto. -->

```
Módulo / Actividad         | S1 | S2 | S3 | S4 | S5 | S6 | S7 | S8 | S9 |S10 |S11 |S12 |S13 |S14 |S15 |
---------------------------|----|----|----|----|----|----|----|----|----|----|----|----|----|----|-----|
M0 BD + Arquitectura (A+B) | ██ |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
M1 Autenticación (Dev A)   |    | ██ | ██ | ██ | ██ |    |    |    |    |    |    |    |    |    |    |
M2 Inventario (Dev B)      |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
                           | ↑ Completar con ██ en las semanas correctas                           |
M3 Clientes (Dev A)        |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
                           | ↑ Completar                                                           |
M4 Ventas (Dev A + Dev B)  |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
                           | ↑ Completar                                                           |
M5 Reportes (Dev A)        |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
                           | ↑ Completar                                                           |
M6 Config. y Docs (Dev B)  |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
                           | ↑ Completar                                                           |
Pruebas integración (A+B)  |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
                           | ↑ Completar                                                           |
Despliegue + Caps (A+B)    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
                           | ↑ Completar                                                           |
```

---

## Sección D: Hitos del Proyecto

<!-- 📝 Instrucción: Define los 4 hitos del proyecto FerreMax. El H1 ya está definido como ejemplo.
     Un criterio de aceptación responde: "¿Qué debe estar funcionando para dar este hito por cumplido?" -->

| # | Hito | Semana | Criterio de aceptación |
|---|------|--------|----------------------|
| H1 | Autenticación y BD lista en staging | S5 | Carlos Mendoza puede iniciar sesión; los 3 roles (gerente, vendedor, almacenista) están configurados y funcionando |
| H2 | <!-- Nombre del hito --> | <!-- S? --> | <!-- ¿Qué debe funcionar para aprobar este hito? --> |
| H3 | <!-- Nombre del hito --> | <!-- S? --> | <!-- Criterio de aceptación claro y verificable --> |
| H4 | Entrega final en producción | <!-- S? --> | Sistema accesible desde ambas sedes (Kennedy y Fontibón); 2 sesiones de capacitación completadas con el personal de FerreMax |

---

## Sección E: Ruta Crítica

<!-- 📝 Instrucción: Escribe la secuencia de módulos que forman la ruta crítica (el camino más largo).
     La ruta crítica comienza siempre en el primer módulo y termina en la entrega final. -->

**Ruta crítica identificada:**

```
M0 BD (S1) → M1 Autenticación (S2–S5) → __________ (S?–S?) → __________ (S?–S?) → Pruebas (S?–S?) → Entrega (S?)
```

**Módulo cuello de botella:** _________________

**Justificación:** 
```
<!-- Explica en 2–3 oraciones por qué ese módulo es el cuello de botella. 
     Pista: Tiene el mayor esfuerzo individual y bloquea al menos 2 módulos más. -->
```

---

## Sección F: Tabla de Resumen para Propuesta Técnica

<!-- 📝 Instrucción: Completa esta tabla resumen. Es la que va directamente en el documento de propuesta técnica. -->

| Fase | Semanas | Actividades principales | Entregable al cliente |
|------|---------|------------------------|----------------------|
| Fase 1: Infraestructura | S1–S5 | BD, arquitectura, autenticación | Demo: sistema de login funcionando |
| Fase 2: Módulos funcionales | <!-- S?–S? --> | <!-- Inventario, Clientes --> | <!-- ¿Qué ve el cliente en esta fase? --> |
| Fase 3: Integración | <!-- S?–S? --> | <!-- Ventas, Reportes, Config --> | <!-- ¿Qué demo o entrega hay? --> |
| Fase 4: Cierre | <!-- S?–S? --> | Pruebas, despliegue, capacitación | Sistema en producción, manual de usuario |

**Duración total:** _______ semanas ≈ _______ meses de calendario

---

> ✅ **Cuando termines**, revisa que:
> - La duración total en la Sección F coincide con el cálculo de la Sección A
> - El Gantt no tiene módulos activos antes de que sus dependencias estén completas
> - Los hitos corresponden a los finales de cada fase
> - La ruta crítica pasa por los módulos con mayor esfuerzo
