# Caso FerreMax — Definición del Alcance del Sistema

> Este archivo documenta cómo se define el alcance del sistema para FerreMax S.A.S., con base en los requisitos levantados en la Semana 2. Es el documento de referencia del caso de estudio para esta semana.

---

## 1. Contexto: Lo que Carlos Mendoza Pidió

En la reunión de levantamiento de requisitos (Semana 2), Carlos Mendoza, gerente de FerreMax S.A.S., planteó una lista extensa de necesidades. Algunas eran claras y urgentes; otras eran "buenos deseos" para el futuro. Como consultores, nuestra tarea fue priorizar y definir qué entra en esta primera versión del sistema.

**Recordatorio del cliente:**
- **Empresa**: FerreMax S.A.S. — ferretería con 2 sedes (Kennedy y Fontibón, Bogotá)
- **Problema principal**: El inventario está en Excel, las ventas se llevan en papel y hay errores frecuentes de stock
- **Objetivo**: Un sistema que centralice el inventario y las ventas de ambas sedes

**Requisitos funcionales levantados en S02** (referencia):

| ID | Requisito Funcional | Prioridad |
|----|---------------------|-----------|
| RF-001 | Registrar y gestionar productos (nombre, código, categoría, precio, stock) | Alta |
| RF-002 | Registrar entradas de inventario (compras a proveedor) | Alta |
| RF-003 | Registrar salidas de inventario (ventas o ajustes) | Alta |
| RF-004 | Consultar stock actual de cualquier producto | Alta |
| RF-005 | Generar alerta cuando un producto esté por debajo del stock mínimo | Alta |
| RF-006 | Registrar y gestionar clientes (nombre, cédula, teléfono, correo) | Media |
| RF-007 | Registrar ventas con detalle de productos vendidos | Alta |
| RF-008 | Calcular el total de una venta automáticamente | Alta |
| RF-009 | Consultar el historial de ventas por fecha y por cliente | Media |
| RF-010 | Generar reporte de ventas del día | Media |
| RF-011 | Gestionar usuarios del sistema con distintos roles (administrador, vendedor) | Alta |
| RF-012 | Permitir que el administrador cree, edite e inactive usuarios | Alta |
| RF-013 | Exportar reportes de inventario o ventas a PDF o Excel | Baja |

**Requisitos no funcionales (RNF) de S02:**

| ID | Requisito No Funcional | Categoría |
|----|----------------------|-----------|
| RNF-001 | El sistema debe funcionar en navegadores web modernos sin instalación | Accesibilidad |
| RNF-002 | El tiempo de respuesta de las consultas no debe superar 3 segundos | Rendimiento |
| RNF-003 | Solo usuarios autenticados pueden acceder al sistema | Seguridad |
| RNF-004 | Las contraseñas deben almacenarse cifradas | Seguridad |
| RNF-005 | El sistema debe ser usable sin capacitación técnica especializada | Usabilidad |
| RNF-006 | El sistema debe estar disponible en horario laboral (lunes-sábado, 7am-8pm) | Disponibilidad |
| RNF-007 | Los datos deben respaldarse automáticamente una vez al día | Confiabilidad |
| RNF-008 | El sistema debe poder adaptarse a una tercera sede en el futuro | Escalabilidad |

---

## 2. Declaración de Alcance — Versión 1

### 2.1. In Scope (Dentro del Alcance — Versión 1)

Después de analizar los requisitos y el presupuesto disponible, el alcance de la primera versión del sistema incluye:

| # | Módulo / Funcionalidad | Requisitos que cubre |
|---|----------------------|---------------------|
| 1 | **Módulo de Autenticación**: Acceso al sistema con usuario y contraseña; roles administrador y vendedor | RF-011, RF-012, RNF-003, RNF-004 |
| 2 | **Módulo de Inventario**: CRUD de productos (registrar, editar, consultar, inactivar), control de stock, alertas de bajo stock | RF-001, RF-002, RF-003, RF-004, RF-005 |
| 3 | **Módulo de Clientes**: CRUD de clientes (registrar, editar, consultar, inactivar) | RF-006 |
| 4 | **Módulo de Ventas**: Registro de ventas con detalle de productos, cálculo automático de total | RF-007, RF-008 |
| 5 | **Módulo de Reportes básicos**: Reporte de ventas del día, historial de ventas por período, reporte de inventario actual | RF-009, RF-010 |
| 6 | **Infraestructura**: Sistema web accesible desde navegador, disponible en horario laboral, respaldo diario de datos | RNF-001, RNF-002, RNF-006, RNF-007 |

### 2.2. Out of Scope (Fuera del Alcance — Versión 1)

Las siguientes funcionalidades **no hacen parte** de la primera versión del sistema. Podrán considerarse para una fase 2, sujeto a nueva negociación y presupuesto:

| # | Funcionalidad excluida | Motivo |
|---|----------------------|--------|
| 1 | Exportación de reportes a PDF/Excel (RF-013) | Baja prioridad — la consulta en pantalla cubre la necesidad inmediata; se puede agregar en fase 2 |
| 2 | Integración con plataformas de pago en línea (PSE, Wompi) | No fue solicitado como urgente; agrega complejidad y costo |
| 3 | Aplicación móvil o app para Android/iOS | Carlos trabaja desde PC; el sistema web responde en móvil pero no hay app nativa |
| 4 | Módulo de contabilidad (estados financieros, libro diario) | Requiere software contable especializado; fuera del alcance técnico del proyecto |
| 5 | Sistema de facturación electrónica DIAN | Requiere certificado digital, firma electrónica y cumplimento de normativa tributaria — posible fase 3 |
| 6 | Gestión de proveedores y órdenes de compra | No fue priorizado por Carlos para la primera versión |

> **Nota al cliente**: *"Las funcionalidades listadas como 'fuera del alcance' no serán entregadas en la versión 1 del sistema. Si en el futuro desea incluir alguna de ellas, se debe abrir una nueva negociación con el equipo de desarrollo."*

---

## 3. Lista de Entregables del Proyecto FerreMax

| # | Entregable | Tipo | Verificable cuando... |
|---|-----------|------|----------------------|
| E-001 | Código fuente en repositorio GitHub | Software | El repositorio es público o compartido, con README y commits organizados |
| E-002 | Base de datos diseñada e implementada | Software | La BD tiene todas las tablas (productos, clientes, ventas, usuarios) con sus relaciones |
| E-003 | Módulo de autenticación funcional | Software | Un usuario puede iniciar sesión con su rol y ver solo lo que le corresponde |
| E-004 | Módulo de inventario funcional | Software | Se pueden registrar, editar, consultar e inactivar productos; el stock se actualiza con cada movimiento |
| E-005 | Módulo de clientes funcional | Software | Se pueden registrar, editar y consultar clientes |
| E-006 | Módulo de ventas funcional | Software | Se puede registrar una venta, el sistema calcula el total y descuenta del stock |
| E-007 | Módulo de reportes funcional | Software | Se puede ver el historial de ventas por fecha y consultar el inventario actual |
| E-008 | Documento de requisitos (S02) | Documentación | Firmado por el cliente, con todos los RF y RNF listados |
| E-009 | Propuesta técnica completa | Documentación | Documento de 8 secciones según estructura del bootcamp |
| E-010 | Manual de usuario básico | Documentación | El manual explica cómo usar cada módulo con capturas de pantalla |

---

## 4. WBS del Sistema FerreMax (2 niveles)

```
Sistema de Gestión FerreMax S.A.S.
│
├── 1. Autenticación y Usuarios
│   ├── 1.1 Pantalla de login con validación
│   ├── 1.2 Gestión de usuarios (crear, editar, inactivar) — solo administrador
│   └── 1.3 Control de acceso por rol
│
├── 2. Gestión de Inventario
│   ├── 2.1 CRUD de productos (crear, editar, ver, inactivar)
│   ├── 2.2 Registro de entradas de inventario
│   ├── 2.3 Registro de salidas de inventario
│   ├── 2.4 Consulta de stock actual
│   └── 2.5 Alertas de bajo stock configurables
│
├── 3. Gestión de Clientes
│   ├── 3.1 CRUD de clientes (crear, editar, ver, inactivar)
│   └── 3.2 Búsqueda de clientes por nombre o cédula
│
├── 4. Módulo de Ventas
│   ├── 4.1 Formulario de nueva venta (seleccionar cliente, agregar productos)
│   ├── 4.2 Cálculo automático de subtotal, IVA y total
│   └── 4.3 Registro de venta (actualiza inventario automáticamente)
│
├── 5. Reportes
│   ├── 5.1 Reporte de ventas del día
│   ├── 5.2 Historial de ventas por período (filtro por fecha)
│   └── 5.3 Reporte de inventario actual
│
└── 6. Documentación del Proyecto
    ├── 6.1 Propuesta técnica completa
    ├── 6.2 Diagrama de base de datos (ERD)
    └── 6.3 Manual de usuario básico
```

---

## 5. Análisis de Factibilidad — FerreMax

### 5.1. Factibilidad Técnica

| Criterio | Evaluación | Resultado |
|----------|-----------|-----------|
| Tecnología | Python + FastAPI (backend), HTML/CSS/JS (frontend) o Django — open source | ✅ Viable |
| Habilidades | El equipo de desarrollo conoce Python y bases de datos relacionales (PostgreSQL/SQLite) | ✅ Viable |
| Infraestructura | Hosting compartido desde $15.000 COP/mes (Railway, Render, o servidor SENA) | ✅ Viable |
| Complejidad | CRUD + autenticación + reportes básicos — complejidad media-baja para el nivel del equipo | ✅ Viable |
| Tiempo | ~16 semanas de desarrollo disponibles para los 5 módulos propuestos | ✅ Realista |

**Conclusión técnica**: El proyecto es técnicamente viable con las herramientas y habilidades disponibles.

### 5.2. Factibilidad Operativa

| Criterio | Evaluación | Resultado |
|----------|-----------|-----------|
| Disposición del cliente | Carlos solicitó activamente el sistema; está motivado para cambiar los procesos actuales | ✅ Alta |
| Nivel técnico de usuarios | Los empleados manejan PC básico y Excel — curva de aprendizaje moderada | ✅ Manejable |
| Equipos disponibles | Kennedy tiene 3 computadores; Fontibón tiene 2 — suficiente para el sistema web | ✅ Suficiente |
| Conectividad | Ambas sedes tienen internet de negocio con fibra óptica | ✅ Adecuada |
| Plan de implementación | Se lanzará primero en Kennedy, luego en Fontibón con capacitación de 1 día | ✅ Planificable |

**Conclusión operativa**: El sistema es operativamente viable. Se requiere una jornada de capacitación al personal de cada sede.

### 5.3. Factibilidad Económica Básica

**Estimación de costo (orden de magnitud):**

| Componente | Estimación |
|-----------|-----------|
| Desarrollo (desarrollo + diseño + pruebas) | A definir en Semana 5 |
| Hosting por 12 meses | ~$180.000 – $360.000 COP/año |
| **Total estimado** | A definir con mayor precisión en S05 |

**Beneficios esperados para FerreMax:**

| Beneficio | Impacto estimado |
|----------|-----------------|
| Reducción de errores en inventario | Menos mermas y sobrantes — ahorro progresivo |
| Ahorro de tiempo en registro | Empleados invierten menos tiempo en papelería y Excel |
| Mejor visibilidad del negocio | Carlos puede tomar decisiones con datos reales |
| Escalabilidad | El sistema puede crecer a nuevas sedes sin rediseño |

**Conclusión económica**: Los beneficios operativos justifican la inversión. La relación costo-beneficio es positiva para una PYME del sector ferretero en Bogotá.

### 5.4. Conclusión General de Factibilidad

| Tipo | Resultado |
|------|-----------|
| Técnica | ✅ Viable |
| Operativa | ✅ Viable con capacitación |
| Económica | ✅ Viable — beneficios superan costos estimados |
| **Recomendación** | **Proceder con el desarrollo del sistema** |

---

## 6. Restricciones y Supuestos del Proyecto

### Restricciones

| ID | Restricción | Impacto |
|----|------------|---------|
| R-001 | El proyecto debe completarse en el trimestre académico en curso | Limita el alcance a los módulos propuestos |
| R-002 | El presupuesto del cliente es limitado (PYME en crecimiento) | Los costos de tecnología deben mantenerse bajos — preferir open source |
| R-003 | Un solo desarrollador disponible (aprendiz) | El alcance fue calibrado para ser desarrollado por una persona |
| R-004 | El sistema debe funcionar sin instalación en los equipos del cliente | Se elige arquitectura web (no app de escritorio) |
| R-005 | Cumplir con la Ley 1581 de Protección de Datos en el manejo de información de clientes | Se requiere política de privacidad básica |

### Supuestos

| ID | Supuesto | Consecuencia si cambia |
|----|----------|----------------------|
| S-001 | Carlos Mendoza tendrá disponibilidad para revisiones cada 2 semanas | Si no hay disponibilidad, el proyecto puede atrasarse por falta de validación |
| S-002 | La empresa dispondrá de hosting o servicio en la nube para el despliegue | Si no, habrá un costo adicional no contemplado |
| S-003 | Los datos del inventario actual (en Excel) se migrarán manualmente — no hay importación automática | Si hay miles de productos, la migración puede tomar más tiempo de lo previsto |
| S-004 | Los usuarios finales tienen conocimiento básico de uso de computador y navegador web | Si no tienen este conocimiento, se requiere capacitación adicional |
| S-005 | No hay cambios regulatorios durante el desarrollo que afecten el alcance | Cambios en normativa tributaria (facturación electrónica) podrían requerir ajustes |

---

*Este documento es el caso de referencia para la Semana 3 de Cadena de Formación.*
*Ver también: [`docs/caso-estudio/03-alcance-wbs.md`](../../../../docs/caso-estudio/03-alcance-wbs.md)*
