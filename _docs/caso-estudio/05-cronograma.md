# Caso de Estudio FerreMax — Cronograma del Proyecto (Semana 5)

> **Documento del caso de estudio ficticio.**  
> Este archivo forma parte del caso FerreMax S.A.S. utilizado en la Cadena de Formación.  
> Construye sobre: [01-contexto-cliente.md](01-contexto-cliente.md) · [02-requisitos.md](02-requisitos.md) · [03-alcance.md](03-alcance.md) · [04-estimacion-tecnicas.md](04-estimacion-tecnicas.md)

---

## 1. Punto de partida — Esfuerzo total (viene de S04)

El equipo de consultores completó la estimación de esfuerzo en la Semana 4 usando Planning Poker y técnica Delphi combinada:

| Módulo | Identificador | Esfuerzo estimado (días-persona) |
|--------|--------------|----------------------------------|
| Base de datos y arquitectura | M0 | 10 |
| Autenticación y control de acceso | M1 | 31 |
| Gestión de inventario | M2 | 67 |
| Gestión de clientes | M3 | 12 |
| Ventas y facturación | M4 | 48 |
| Reportes y análisis | M5 | 20 |
| Configuración y documentación | M6 | 16 |
| **TOTAL** | | **194 días-persona** |

---

## 2. Parámetros del equipo

| Parámetro | Valor | Justificación |
|-----------|-------|---------------|
| Desarrolladores | 2 (Dev A y Dev B) | Único equipo disponible según propuesta de la consultora |
| Factor de capacidad | 80% (0.80) | Equipo dedicado, con pausas y reuniones periódicas estimadas |
| Días hábiles por semana | 5 | Semana laboral estándar Colombia |
| Festivos Colombia | ~18 días/año | Se distribuyen en el buffer |

---

## 3. Cálculo de duración

### 3.1 Duración base

$$\text{Duración base} = \frac{194}{2 \times 0{,}80} = \frac{194}{1{,}60} = 121{,}25 \approx 122 \text{ días hábiles} \approx 24 \text{ semanas}$$

### 3.2 Con buffer de imprevistos (15%)

$$\text{Duración con buffer} = 122 \times 1{,}15 = 140{,}3 \approx 140 \text{ días hábiles}$$

### 3.3 Con optimización por paralelismo

Al trabajar en paralelo en módulos sin dependencia (Dev A y Dev B en módulos distintos simultáneamente), la duración efectiva se reduce de 24 semanas secuenciales a **15 semanas de calendario**:

| Escenario | Duración |
|-----------|---------|
| Secuencial (un módulo a la vez) | ~24 semanas |
| Con paralelismo (Dev A + Dev B en paralelo) | **15 semanas** |
| Diferencia por paralelismo | 9 semanas de ahorro |

---

## 4. Dependencias entre módulos

| Módulo | Depende de | Tipo |
|--------|-----------|------|
| M0 — BD + Arquitectura | Ninguno | — |
| M1 — Autenticación | M0 | FS (Finish-to-Start) |
| M2 — Inventario | M1 | FS |
| M3 — Clientes | M1 | FS (puede ir en paralelo con M2) |
| M4 — Ventas | M2 + M3 | FS (espera que ambos estén listos) |
| M5 — Reportes | M4 | FS |
| M6 — Config. y Docs | M1 (parcial) | FS parcial (puede continuar en paralelo con otros módulos) |
| Pruebas de integración | M4 + M5 + M6 | FS |
| Despliegue + Capacitación | Pruebas | FS |

---

## 5. Asignación del equipo

| Módulo | Dev A | Dev B | Observaciones |
|--------|-------|-------|--------------|
| M0 — BD + Arquitectura | ✓ | ✓ | Ambos, semana 1 |
| M1 — Autenticación | ✓ | | Dev A lidera; Dev B inicia M2 |
| M2 — Inventario | | ✓ | Dev B dedicado durante S2–S9 |
| M3 — Clientes | ✓ | | Dev A al terminar autenticación |
| M4 — Ventas | ✓ | ✓ | Ambos en paralelo para reducir tiempo |
| M5 — Reportes | ✓ | | Dev A en S11–S12 |
| M6 — Config. y Docs | | ✓ | Dev B en S11–S12 |
| Pruebas de integración | ✓ | ✓ | S13–S14 |
| Despliegue + Caps | ✓ | ✓ | S15 |

---

## 6. Cronograma — Gantt por semanas (15 semanas)

```
Módulo / Actividad             | S1 | S2 | S3 | S4 | S5 | S6 | S7 | S8 | S9 |S10 |S11 |S12 |S13 |S14 |S15 |
-------------------------------|----|----|----|----|----|----|----|----|----|----|----|----|----|----|-----|
M0 BD + Arquitectura (A+B)     | ██ |    |    |    |    |    |    |    |    |    |    |    |    |    |    |
M1 Autenticación (Dev A) ⚑    |    | ██ | ██ | ██ | ██ |    |    |    |    |    |    |    |    |    |    |
M2 Inventario (Dev B) ⚑       |    | ██ | ██ | ██ | ██ | ██ | ██ | ██ | ██ |    |    |    |    |    |    |
M3 Clientes (Dev A)            |    |    |    |    |    | ██ |    |    |    |    |    |    |    |    |    |
M4 Ventas (A+B) ⚑             |    |    |    |    |    |    |    | ██ | ██ | ██ |    |    |    |    |    |
M5 Reportes (Dev A)            |    |    |    |    |    |    |    |    |    |    | ██ | ██ |    |    |    |
M6 Config. y Docs (Dev B)      |    |    |    |    |    |    |    |    |    |    | ██ | ██ |    |    |    |
Pruebas integración (A+B) ⚑   |    |    |    |    |    |    |    |    |    |    |    |    | ██ | ██ |    |
Despliegue + Caps (A+B) ⚑     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | ██ |
```

`⚑` = Ruta crítica | `██` = Módulo activo en esa semana

---

## 7. Hitos del proyecto

| # | Hito | Semana | Criterio de aceptación |
|---|------|--------|----------------------|
| **H1** | Autenticación y BD lista en staging | S5 | Carlos Mendoza puede iniciar sesión con su perfil; los 3 roles (gerente, vendedor, almacenista) están configurados y diferenciados |
| **H2** | Inventario y Clientes aprobados en demo | S9 | El gerente puede registrar productos, hacer ajustes de stock y registrar clientes; demo aprobada por Carlos Mendoza |
| **H3** | Sistema completo en ambiente de pruebas | S12 | Los 7 módulos están integrados y desplegados en staging; el flujo login → venta → reporte funciona de extremo a extremo sin errores críticos |
| **H4** | Entrega final en producción | S15 | Sistema accesible desde sede Kennedy y Fontibón; mínimo 2 sesiones de capacitación completadas; manual de usuario entregado |

---

## 8. Ruta crítica

```
M0 BD (S1) → M1 Autenticación (S2–S5) → M2 Inventario (S2–S9) → M4 Ventas (S8–S10) → Pruebas (S13–S14) → Entrega (S15)
```

**Módulo cuello de botella:** M2 — Inventario (67 días-persona, la tarea individual más larga del proyecto).

**Razonamiento:** El módulo de inventario requiere 67 días-persona, más del doble del segundo módulo más grande (Ventas con 48). Está en la ruta crítica porque Ventas depende de que el inventario esté listo. Si Inventario se retrasa 2 semanas, la entrega final se posterga 2 semanas.

**Módulos con holgura (NO están en la ruta crítica):**
- M3 — Clientes: ~2 semanas de holgura (no bloquea directamente a Ventas por sí solo si M2 está retrasado)
- M5 — Reportes: ~2 semanas de holgura
- M6 — Config. y Docs: ~3 semanas de holgura

---

## 9. Supuestos del cronograma

| ID | Supuesto | Impacto si no se cumple |
|----|---------|------------------------|
| SC-01 | Carlos Mendoza estará disponible para demos en H1, H2 y H3 con máximo 3 días de anticipación para coordinar | Hito se retrasa → puede postergar inicio de la fase siguiente hasta 1 semana |
| SC-02 | El servidor de staging (AWS EC2 t2.micro o equivalente) estará disponible desde la semana 1 | No puede probarse la integración → fases 3 y 4 se retrasan |
| SC-03 | Los datos de inventario actuales serán entregados por FerreMax en formato Excel durante la semana 2 | La carga inicial de datos toma más tiempo → M2 aumenta ~5 días de esfuerzo |
| SC-04 | Los 2 desarrolladores no tendrán asignaciones adicionales que reduzcan su capacidad por debajo del 80% | Duración se extendería proporcionalmente al porcentaje de reducción |
| SC-05 | No habrá cambios de alcance después de aprobado el documento de Alcance (S03) | Cualquier cambio mayor requiere renegociar el cronograma y el presupuesto |

---

## 10. Resumen ejecutivo del cronograma

Este es el texto que aparecería en la sección de cronograma de la propuesta técnica de FerreMax:

---

*El proyecto se desarrollará en 4 fases durante un período de **15 semanas (aproximadamente 3.5 meses)** calendario, con un equipo de 2 desarrolladores full-stack a tiempo completo:*

| Fase | Semanas | Actividades | Entregable al cliente |
|------|---------|------------|----------------------|
| **Fase 1: Infraestructura** | S1–S5 | BD, arquitectura y sistema de autenticación | Demo: login con 3 roles configurados |
| **Fase 2: Módulos funcionales** | S2–S10 | Inventario, clientes y ventas | Demo: ciclo completo de venta ficticia |
| **Fase 3: Integración y reportes** | S10–S12 | Reportes, configuración, documentación | Sistema completo integrado en staging |
| **Fase 4: Pruebas y entrega** | S13–S15 | Pruebas de aceptación, despliegue, capacitación | Sistema en producción + manual de usuario |

*Fecha estimada de entrega: **15 semanas a partir de la firma del contrato**.*  
*Condición: Sujeto al cumplimiento de los supuestos SC-01 a SC-05 documentados anteriormente.*

---

*Cadena de Formación · Tecnólogo ADSO · Caso de Estudio FerreMax — Documento S05*
