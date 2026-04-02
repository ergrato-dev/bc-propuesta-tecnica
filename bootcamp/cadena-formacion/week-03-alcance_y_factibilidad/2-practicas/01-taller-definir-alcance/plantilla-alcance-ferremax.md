# Plantilla — Alcance del Sistema FerreMax S.A.S.

> **Instrucciones**: Este es el documento de trabajo del taller. Completa todas las secciones marcadas con `<!-- Completar -->`. Basa tus respuestas en el caso de estudio FerreMax y en los requisitos levantados en la Semana 2.
>
> Cuando termines, NO deben quedar secciones con `<!-- Completar -->` sin responder.

---

**Proyecto**: Sistema de Gestión FerreMax S.A.S.
**Cliente**: Carlos Mendoza — Ferretería FerreMax
**Consultor**: ___________________________
**Fecha**: ___________________________
**Versión**: 1.0 (Versión 1 del sistema)

---

## Sección 1 — Clasificación de Requisitos

<!-- 📝 Instrucción: Clasifica cada requisito en una de estas categorías:
     ✅ Versión 1 — incluye en el alcance actual
     ⏳ Versión 2 — deja para una fase futura
     ❓ Clarificación — falta información para decidir
     
     Justifica brevemente tu decisión (1 frase). -->

| ID | Requisito Funcional | Prioridad S02 | Decisión | Justificación |
|----|---------------------|--------------|---------|---------------|
| RF-001 | Registrar y gestionar productos (nombre, código, categoría, precio, stock) | Alta | ✅ Versión 1 | Núcleo del sistema — sin esto no hay inventario |
| RF-002 | Registrar entradas de inventario (compras a proveedor) | Alta | <!-- Completar: ✅ / ⏳ / ❓ --> | <!-- Completar: 1 frase de justificación --> |
| RF-003 | Registrar salidas de inventario (ventas o ajustes) | Alta | <!-- Completar --> | <!-- Completar --> |
| RF-004 | Consultar stock actual de cualquier producto | Alta | <!-- Completar --> | <!-- Completar --> |
| RF-005 | Generar alerta cuando un producto esté bajo el stock mínimo | Alta | <!-- Completar --> | <!-- Completar --> |
| RF-006 | Registrar y gestionar clientes (nombre, cédula, teléfono, correo) | Media | <!-- Completar --> | <!-- Completar --> |
| RF-007 | Registrar ventas con detalle de productos vendidos | Alta | <!-- Completar --> | <!-- Completar --> |
| RF-008 | Calcular el total de una venta automáticamente | Alta | <!-- Completar --> | <!-- Completar --> |
| RF-009 | Consultar historial de ventas por fecha y por cliente | Media | <!-- Completar --> | <!-- Completar --> |
| RF-010 | Generar reporte de ventas del día | Media | <!-- Completar --> | <!-- Completar --> |
| RF-011 | Gestionar usuarios con distintos roles (administrador, vendedor) | Alta | <!-- Completar --> | <!-- Completar --> |
| RF-012 | El administrador puede crear, editar e inactivar usuarios | Alta | <!-- Completar --> | <!-- Completar --> |
| RF-013 | Exportar reportes de inventario o ventas a PDF o Excel | Baja | ⏳ Versión 2 | Baja prioridad — consulta en pantalla cubre la necesidad inmediata |

---

## Sección 2 — Declaración de Alcance

### 2.1. In Scope — Versión 1

<!-- 📝 Instrucción: Lista los módulos o funcionalidades que SÍ entrarán en la versión 1.
     Sé específico: describe qué hace cada módulo, no solo su nombre.
     Ejemplo: "Módulo de Autenticación: acceso con usuario/contraseña; roles administrador y vendedor"
     Incluye al menos 5 módulos. -->

| # | Módulo / Funcionalidad | Requisitos que cubre |
|---|----------------------|---------------------|
| 1 | Módulo de Autenticación: acceso al sistema con usuario y contraseña; roles administrador y vendedor | RF-011, RF-012 |
| 2 | <!-- Completar: describe el módulo de inventario --> | <!-- RF que cubre --> |
| 3 | <!-- Completar: describe el módulo de clientes --> | <!-- RF que cubre --> |
| 4 | <!-- Completar: describe el módulo de ventas --> | <!-- RF que cubre --> |
| 5 | <!-- Completar: describe el módulo de reportes --> | <!-- RF que cubre --> |

### 2.2. Out of Scope — Versión 1

<!-- 📝 Instrucción: Lista las funcionalidades que explícitamente NO entrarán en esta versión.
     Justifica brevemente por qué quedan fuera.
     Incluye al menos 4 ítems.
     Ejemplo: "Exportación a PDF | Baja prioridad — la consulta en pantalla es suficiente por ahora" -->

| # | Funcionalidad excluida | Motivo |
|---|----------------------|--------|
| 1 | Exportación de reportes a PDF/Excel (RF-013) | Baja prioridad — la consulta en pantalla cubre la necesidad inmediata |
| 2 | <!-- Completar: funcionalidad --> | <!-- Completar: motivo --> |
| 3 | <!-- Completar: funcionalidad --> | <!-- Completar: motivo --> |
| 4 | <!-- Completar: funcionalidad --> | <!-- Completar: motivo --> |

---

## Sección 3 — Lista de Entregables

<!-- 📝 Instrucción: Lista todos los resultados concretos y verificables que el proyecto producirá.
     Incluye tanto software (módulos funcionales) como documentación.
     Incluye al menos 6 entregables (4 software + 2 documentación).
     Completa la columna "Verificable cuando..." — ¿cómo sabemos que está listo? -->

| # | Entregable | Tipo | Verificable cuando... |
|---|-----------|------|----------------------|
| E-001 | Sistema de autenticación funcional | Software | Un usuario puede iniciar sesión con su rol y ver solo lo que le corresponde |
| E-002 | <!-- Completar: módulo de inventario --> | Software | <!-- Completar: criterio de verificación --> |
| E-003 | <!-- Completar: módulo de clientes --> | Software | <!-- Completar: criterio de verificación --> |
| E-004 | <!-- Completar: módulo de ventas --> | Software | <!-- Completar: criterio de verificación --> |
| E-005 | <!-- Completar: módulo de reportes --> | Software | <!-- Completar: criterio de verificación --> |
| E-006 | <!-- Completar: entregable de documentación --> | Documentación | <!-- Completar: criterio de verificación --> |
| E-007 | <!-- Completar: otro entregable de documentación --> | Documentación | <!-- Completar: criterio de verificación --> |

---

## Sección 4 — WBS Básico (2 niveles)

<!-- 📝 Instrucción: Completa el WBS descomponiendo cada módulo en sus componentes.
     El módulo de Ventas ya está resuelto como ejemplo.
     Completa los módulos: 1-Autenticación, 2-Inventario, 3-Clientes.
     Cada módulo debe tener entre 2 y 5 subcomponentes de nivel 2. -->

```
Sistema de Gestión FerreMax S.A.S.
│
├── 1. Autenticación y Usuarios
│   ├── 1.1 <!-- Completar: subcomponente -->
│   ├── 1.2 <!-- Completar: subcomponente -->
│   └── 1.3 <!-- Completar: subcomponente -->
│
├── 2. Gestión de Inventario
│   ├── 2.1 <!-- Completar: subcomponente -->
│   ├── 2.2 <!-- Completar: subcomponente -->
│   ├── 2.3 <!-- Completar: subcomponente -->
│   └── 2.4 <!-- Completar: subcomponente -->
│
├── 3. Gestión de Clientes
│   ├── 3.1 <!-- Completar: subcomponente -->
│   └── 3.2 <!-- Completar: subcomponente -->
│
├── 4. Módulo de Ventas           ← (resuelto — referencia)
│   ├── 4.1 Formulario de nueva venta (seleccionar cliente, agregar productos)
│   ├── 4.2 Cálculo automático de subtotal y total
│   └── 4.3 Registro de venta (actualiza inventario automáticamente)
│
├── 5. Reportes
│   ├── 5.1 <!-- Completar: subcomponente -->
│   └── 5.2 <!-- Completar: subcomponente -->
│
└── 6. Documentación del Proyecto
    ├── 6.1 Propuesta técnica completa
    └── 6.2 Manual de usuario básico
```

---

## Sección 5 — Análisis de Factibilidad

### 5.1. Factibilidad Técnica

<!-- 📝 Instrucción: Evalúa cada criterio con un análisis breve y un resultado (✅ Viable / ⚠️ Con riesgo / ❌ No viable).
     El primer criterio ya está resuelto como ejemplo. Completa los restantes. -->

| Criterio | Evaluación | Resultado |
|----------|-----------|-----------|
| Tecnología disponible | Python/FastAPI — open source, abundante documentación, compatible con el proyecto | ✅ Viable |
| Habilidades del equipo | <!-- Completar: ¿el equipo conoce las tecnologías necesarias? --> | <!-- ✅ / ⚠️ / ❌ --> |
| Infraestructura / hosting | <!-- Completar: ¿hay servidor o servicio de nube disponible? ¿cuánto cuesta? --> | <!-- ✅ / ⚠️ / ❌ --> |
| Complejidad técnica | <!-- Completar: ¿el sistema tiene partes muy complejas para el nivel del equipo? --> | <!-- ✅ / ⚠️ / ❌ --> |
| Tiempo disponible | <!-- Completar: ¿el tiempo de desarrollo es suficiente para los módulos propuestos? --> | <!-- ✅ / ⚠️ / ❌ --> |

### 5.2. Factibilidad Operativa

<!-- 📝 Instrucción: Evalúa si el cliente y sus empleados pueden adoptar y operar el sistema.
     Completa todos los criterios. -->

| Criterio | Evaluación | Resultado |
|----------|-----------|-----------|
| Disposición del cliente | <!-- Completar: ¿Carlos está motivado para cambiar? ¿hay resistencia? --> | <!-- ✅ / ⚠️ / ❌ --> |
| Nivel técnico de usuarios | <!-- Completar: ¿los empleados pueden usar un sistema web? --> | <!-- ✅ / ⚠️ / ❌ --> |
| Equipos disponibles | <!-- Completar: ¿la empresa tiene computadores suficientes? --> | <!-- ✅ / ⚠️ / ❌ --> |
| Conectividad a internet | <!-- Completar: ¿hay internet en ambas sedes? --> | <!-- ✅ / ⚠️ / ❌ --> |

### 5.3. Conclusión de Factibilidad

<!-- 📝 Instrucción: Escribe un párrafo de 3-4 oraciones con tu conclusión.
     Responde: ¿El proyecto es viable? ¿Con qué condiciones? ¿Qué recomiendas? -->

<!-- Completar: párrafo de conclusión -->

---

## Sección 6 — Restricciones y Supuestos (opcional)

### Restricciones

<!-- 📝 Instrucción: Lista condiciones fijas que limitan el proyecto (no son negociables).
     Ejemplos: plazos, presupuesto máximo, tecnologías obligatorias, regulaciones.
     Incluye al menos 3. -->

| ID | Restricción | Tipo | Impacto en el proyecto |
|----|------------|------|----------------------|
| R-001 | <!-- Completar --> | <!-- Tiempo / Presupuesto / Tecnología / Regulación --> | <!-- Completar --> |
| R-002 | <!-- Completar --> | <!-- Completar --> | <!-- Completar --> |
| R-003 | <!-- Completar --> | <!-- Completar --> | <!-- Completar --> |

### Supuestos

<!-- 📝 Instrucción: Lista condiciones que asumimos como verdaderas para que el proyecto funcione.
     Explica qué pasaría si cada supuesto cambia.
     Incluye al menos 3. -->

| ID | Supuesto | Consecuencia si cambia |
|----|----------|----------------------|
| S-001 | <!-- Completar: condición que asumo como verdadera --> | <!-- Completar: impacto si cambia --> |
| S-002 | <!-- Completar --> | <!-- Completar --> |
| S-003 | <!-- Completar --> | <!-- Completar --> |

---

*Taller 01 · Semana 03 · Cadena de Formación · Tecnólogo ADSO*
