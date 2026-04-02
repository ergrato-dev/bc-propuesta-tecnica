# Documento de Alcance — FerreMax S.A.S.

> **Propósito**: Documento maestro del caso de estudio para la Semana 3 del bootcamp.
> Describe el alcance definido del sistema FerreMax después del levantamiento de requisitos (S02).

---

**Proyecto**: Sistema de Gestión FerreMax S.A.S.
**Versión del sistema**: 1.0
**Consultor**: Equipo de consultoría (simulado)
**Fecha de elaboración**: Semana 3 — Marzo 2025
**Estado**: Aprobado (referencia del caso de estudio)

---

## 1. Resumen Ejecutivo

FerreMax S.A.S. es una ferretería con dos sedes en Bogotá (Kennedy y Fontibón) que lleva su inventario en Excel y registra las ventas en papel. Esto genera pérdidas por errores de stock, demoras en el servicio y falta de información para tomar decisiones.

Se propone desarrollar un **sistema web de gestión de inventario y ventas** que centralice la información de ambas sedes, mejore el control del stock y facilite el seguimiento de las ventas. La primera versión del sistema cubrirá los módulos esenciales con tecnología open source de bajo costo de mantenimiento.

---

## 2. Declaración de Alcance

### 2.1. In Scope — Versión 1

| # | Módulo / Funcionalidad | Descripción |
|---|----------------------|-------------|
| 1 | **Autenticación y Control de Acceso** | Login con usuario y contraseña. Dos roles: administrador (acceso total) y vendedor (solo inventario y ventas). El administrador puede crear, editar e inactivar usuarios. |
| 2 | **Gestión de Inventario** | CRUD completo de productos (código, nombre, categoría, precio, stock mínimo). Registro de entradas (compras a proveedor) y salidas (ajustes). Consulta de stock en tiempo real. Alerta visual cuando el stock cae por debajo del mínimo configurado. |
| 3 | **Gestión de Clientes** | CRUD de clientes (nombre, número de cédula, teléfono, correo electrónico). Búsqueda por nombre o cédula. |
| 4 | **Módulo de Ventas** | Registro de ventas con selección de cliente y de productos. Cálculo automático de subtotal y total. El registro de la venta descuenta automáticamente el stock del producto. |
| 5 | **Reportes Básicos** | Reporte de ventas del día visualizable en pantalla. Historial de ventas filtrable por rango de fechas. Reporte de inventario actual con estado de stock. |
| 6 | **Infraestructura** | Sistema web accesible desde cualquier navegador moderno sin instalación. Disponible en horario laboral (lunes a sábado, 7am–8pm). Respaldo automático de datos una vez al día. |

### 2.2. Out of Scope — Versión 1

Las siguientes funcionalidades **no hacen parte** de la versión 1 del sistema. Podrán considerarse para una fase posterior del proyecto, sujeto a nueva negociación y presupuesto:

| # | Funcionalidad excluida | Motivo de exclusión |
|---|----------------------|---------------------|
| 1 | Exportación de reportes a PDF o Excel | Prioridad baja — consulta en pantalla cubre la necesidad inmediata de Carlos |
| 2 | Aplicación móvil nativa (Android/iOS) | Carlos opera desde PC; el sistema web es responsivo en móvil. App nativa implica costo y tiempo adicional |
| 3 | Facturación electrónica DIAN | Requiere certificado digital, firma electrónica y cumplimiento de normativa tributaria — complejidad y costo fuera del alcance del proyecto |
| 4 | Integración con pasarelas de pago en línea (PSE, Wompi, Nequi) | No fue solicitado como necesidad inmediata; implica integración de terceros costosa |
| 5 | Módulo de contabilidad y estados financieros | Requiere conocimientos contables especializados y potencial integración con software SIIGO u otros |
| 6 | Gestión de proveedores y órdenes de compra | No fue identificado como requisito prioritario en la sesión de levantamiento |

---

## 3. Lista de Entregables

| Código | Entregable | Tipo | Verificable cuando... |
|--------|-----------|------|----------------------|
| E-001 | Código fuente en repositorio GitHub | Software | El repositorio es accesible, tiene README, estructura de carpetas organizada y commits con mensajes descriptivos |
| E-002 | Base de datos implementada | Software | La BD contiene las tablas de usuarios, productos, clientes, ventas y movimientos de inventario con sus relaciones |
| E-003 | Sistema de autenticación funcional | Software | Un administrador y un vendedor pueden iniciar sesión con sus respectivos accesos diferenciados |
| E-004 | Módulo de inventario funcional | Software | Se pueden registrar productos, consultar el stock actual y el sistema genera alertas cuando el stock cae al mínimo |
| E-005 | Módulo de clientes funcional | Software | Se pueden registrar, editar, buscar y visualizar clientes |
| E-006 | Módulo de ventas funcional | Software | Se puede registrar una venta completa con cálculo automático del total y actualización del stock |
| E-007 | Módulo de reportes funcional | Software | Se puede visualizar el reporte de ventas del día y el inventario actual |
| E-008 | Documento de alcance (este documento) | Documentación | Documento completo con in scope, out of scope, WBS, factibilidad, restricciones y supuestos |
| E-009 | Propuesta técnica completa (S01–S08) | Documentación | Documento final con todas las secciones del bootcamp integradas |
| E-010 | Manual de usuario básico | Documentación | El manual explica cómo usar cada módulo con capturas de pantalla y pasos numerados |

---

## 4. WBS — Estructura de Desglose del Trabajo

```
1.0  Sistema de Gestión FerreMax S.A.S.
│
├── 1.1  Autenticación y Usuarios
│   ├── 1.1.1  Pantalla de login con validación de credenciales
│   ├── 1.1.2  Gestión de usuarios (crear, editar, inactivar) — solo administrador
│   └── 1.1.3  Control de acceso diferenciado por rol
│
├── 1.2  Gestión de Inventario
│   ├── 1.2.1  CRUD de productos (código, nombre, categoría, precio, stock mínimo)
│   ├── 1.2.2  Registro de entradas de inventario (compras a proveedor)
│   ├── 1.2.3  Registro de salidas de inventario (ajustes manuales)
│   ├── 1.2.4  Consulta de stock actual en tiempo real
│   └── 1.2.5  Alertas de bajo stock configurables por producto
│
├── 1.3  Gestión de Clientes
│   ├── 1.3.1  CRUD de clientes (nombre, cédula, teléfono, correo)
│   └── 1.3.2  Búsqueda de clientes por nombre o cédula
│
├── 1.4  Módulo de Ventas
│   ├── 1.4.1  Formulario de nueva venta (selección de cliente y productos)
│   ├── 1.4.2  Cálculo automático de subtotal y total de la venta
│   └── 1.4.3  Registro de venta con actualización automática del stock
│
├── 1.5  Reportes
│   ├── 1.5.1  Reporte de ventas del día
│   ├── 1.5.2  Historial de ventas por rango de fechas
│   └── 1.5.3  Reporte de inventario actual con estado de stock
│
└── 1.6  Documentación del Proyecto
    ├── 1.6.1  Propuesta técnica completa (9 secciones bootcamp)
    ├── 1.6.2  Diagrama entidad-relación (ERD) de la base de datos
    └── 1.6.3  Manual de usuario básico
```

---

## 5. Análisis de Factibilidad

### 5.1. Factibilidad Técnica

| Criterio | Evaluación | Resultado |
|----------|-----------|-----------|
| Tecnología disponible | Python/FastAPI (backend), HTML/CSS/JS vanilla o Jinja2 (frontend), PostgreSQL o SQLite — todo open source | ✅ Viable |
| Habilidades del equipo | El aprendiz conoce Python y bases de datos relacionales; CRUD y autenticación están dentro del alcance del programa ADSO | ✅ Viable |
| Infraestructura | Hosting en Railway o Render (~$0–15 USD/mes); alternativa en servidor del SENA para ambiente de pruebas | ✅ Viable |
| Complejidad técnica | CRUD + autenticación + reportes básicos — complejidad media-baja para el nivel del equipo de desarrollo | ✅ Viable |
| Tiempo disponible | ~16 semanas de desarrollo; 5 módulos con complejidad baja-media cada uno — planificación realista | ✅ Viable |

**Conclusión técnica**: El proyecto es técnicamente viable con las herramientas y habilidades del equipo. El stack tecnológico seleccionado (Python, web, base de datos relacional) corresponde directamente a las competencias desarrolladas en el programa ADSO.

### 5.2. Factibilidad Operativa

| Criterio | Evaluación | Resultado |
|----------|-----------|-----------|
| Disposición del cliente | Carlos Mendoza solicitó activamente el sistema; está motivado para cambiar los procesos actuales con Excel y papel | ✅ Alta |
| Nivel técnico de usuarios | Los empleados de ambas sedes manejan computador básico y algunos usan Excel — curva de aprendizaje moderada, manejable con capacitación de 1 día | ✅ Manejable |
| Equipos disponibles | Sede Kennedy: 3 computadores; Sede Fontibón: 2 computadores — suficiente para acceso simultáneo del equipo | ✅ Suficiente |
| Conectividad a internet | Ambas sedes tienen servicio de internet de negocio con fibra óptica | ✅ Adecuada |
| Plan de implementación | Lanzamiento primero en Kennedy, luego en Fontibón con capacitación de 1 día por sede | ✅ Planificable |

**Conclusión operativa**: El sistema es operativamente viable. Se requiere una jornada de capacitación al personal de cada sede antes de la puesta en producción.

### 5.3. Factibilidad Económica

**Beneficios esperados para FerreMax:**

| Beneficio | Impacto estimado |
|----------|-----------------|
| Reducción de errores en inventario | Menor número de mermas por productos no registrados o mal contados |
| Ahorro de tiempo en registro de ventas | Cada venta se registra en ~2 min vs ~8 min en papel → ahorro diario significativo |
| Control de stock en tiempo real | Carlos puede verificar el inventario desde cualquier computador sin depender de un archivo Excel actualizado manualmente |
| Toma de decisiones con datos | Reportes de ventas del día y del período permiten planificar compras a proveedores |
| Escalabilidad | El sistema puede extenderse a una tercera sede sin rediseño |

**Conclusión económica**: Los beneficios operativos y la reducción de errores justifican la inversión. El costo de desarrollo, siendo un proyecto de aprendizaje, es significativamente menor al costo comercial del mercado. La PYME obtiene un sistema personalizado a un costo accesible.

### 5.4. Conclusión General

| Tipo | Resultado |
|------|-----------|
| Técnica | ✅ Viable |
| Operativa | ✅ Viable con capacitación |
| Económica | ✅ Viable — beneficios superan costos |
| **Recomendación** | **Proceder con el desarrollo del sistema versión 1** |

---

## 6. Restricciones del Proyecto

| ID | Restricción | Tipo | Impacto |
|----|------------|------|---------|
| R-001 | El proyecto debe estar terminado dentro del trimestre académico (16 semanas) | Tiempo | Limita el alcance a los 5 módulos propuestos |
| R-002 | La tecnología usada debe ser open source o de costo mínimo (PYME en crecimiento) | Presupuesto | Se selecciona stack Python + PostgreSQL/SQLite sin licencias |
| R-003 | Un solo desarrollador disponible (aprendiz del programa ADSO) | Recursos | La complejidad del sistema fue calibrada para 1 persona |
| R-004 | El sistema debe ser web — no puede requerir instalación en los equipos del cliente | Tecnología | Se elige arquitectura cliente-servidor HTTP (no aplicación de escritorio) |
| R-005 | El tratamiento de datos de clientes debe cumplir con la Ley 1581 de Protección de Datos de Colombia | Regulación | Se requiere política de privacidad básica y medidas de seguridad en contraseñas |

---

## 7. Supuestos del Proyecto

| ID | Supuesto | Consecuencia si cambia |
|----|----------|----------------------|
| S-001 | Carlos Mendoza estará disponible para revisiones y aprobaciones cada dos semanas | Si no hay disponibilidad, el proyecto puede atrasarse por falta de validación del cliente |
| S-002 | La empresa dispondrá de servicio de hosting o se usará el servidor de prácticas del SENA para el despliegue final | Si no hay hosting disponible, habrá que buscar alternativa de último momento |
| S-003 | Los datos del inventario actual (en Excel) se migrarán manualmente por el personal de FerreMax | Si hay miles de referencias, la migración puede tomar más tiempo del previsto |
| S-004 | Los usuarios finales tienen conocimiento básico de uso de computador y navegador web | Si no lo tienen, se requiere capacitación más intensiva que la planificada (1 día) |
| S-005 | No hay cambios regulatorios significativos durante el desarrollo que afecten los módulos | Un cambio en la normativa de facturación electrónica DIAN podría requerir ajustes no contemplados |

---

*Documento maestro del caso de estudio — Semana 03 · Cadena de Formación · Tecnólogo ADSO*
*Ver también: [1-teoria/04-caso-ferremax-alcance.md](../../bootcamp/cadena-formacion/week-03-alcance_y_factibilidad/1-teoria/04-caso-ferremax-alcance.md)*
