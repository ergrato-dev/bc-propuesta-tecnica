# 💼 Propuesta Comercial y Matriz de Riesgos — FerreMax S.A.S.

> **Documento del caso de estudio — Semana 8**
> Ejemplo de referencia para instructores y aprendices. No es el entregable del aprendiz.

---

## Datos del Proyecto

| Campo | Detalle |
|---|---|
| **Cliente** | FerreMax S.A.S. |
| **Proyecto** | Sistema de Gestión de Inventario (FerreMax GI) |
| **Proveedor** | DevSol Colombia S.A.S. |
| **Fecha de emisión** | 15 de noviembre de 2024 |
| **Versión** | 1.0 |

---

## Índice del Documento

Este archivo cubre la **Parte II — Propuesta Comercial** (§8 a §13) del documento integrado.
La Parte I — Propuesta Técnica (§1 a §7) está documentada en [`07-propuesta-tecnica-borrador.md`](./07-propuesta-tecnica-borrador.md).

| Sección | Contenido |
|---|---|
| §8 | Tabla de costos presentada al cliente |
| §9 | Condiciones comerciales (pago, garantía, PI, confidencialidad, validez) |
| §10 | (Reservado — integrado en §3 de la Parte I) |
| §11 | (Integrado en §5 de la Parte I) |
| §12 | Matriz de riesgos del proyecto |
| §13 | Firmas y aceptación |

---

## §8 — Tabla de Costos

La siguiente tabla presenta el valor del proyecto agrupado por categorías de gasto. Los precios incluyen todos los costos del equipo y la infraestructura requerida para entregar el sistema completo.

| Categoría | Descripción | Valor (COP) |
|---|---|---:|
| Desarrollo de software | Diseño, codificación, pruebas y despliegue de los 6 módulos. Incluye 2 desarrolladores al 80% de dedicación durante 15 semanas. | $74,528,000 |
| Gestión del proyecto | Coordinación, reuniones de avance semanales, control de cambios, documentación técnica y entregables de gestión. | $8,120,000 |
| Infraestructura cloud | Servidor AWS EC2 (t3.medium) + base de datos RDS (db.t3.micro) por 6 meses. Incluye configuración inicial y soporte. | $3,600,000 |
| Licencias de software | Herramientas de desarrollo, repositorios y entornos de prueba. Todas las herramientas seleccionadas son de código abierto o licencia gratuita. | $0 |
| Contingencia (10%) | Reserva para imprevistos identificados en el análisis de riesgos (§12). No se factura si no se usa. | $8,624,800 |
| Utilidad empresarial | Margen operativo del proveedor (15% sobre costos directos). | $4,292,200 |
| **TOTAL** | | **$99,165,000** |

> **Nota:** Los valores incluyen todos los impuestos aplicables. El IVA sobre honorarios profesionales puede aplicar según la naturaleza jurídica del contratante; consultar con contador.

---

## §9 — Condiciones Comerciales

### §9.1 — Forma de Pago

El proyecto se factura en tres cuotas asociadas a hitos de entrega verificables:

| Cuota | % | Valor (COP) | Momento de pago | Hito de activación |
|---|---|---:|---|---|
| Anticipo | 30% | $29,749,500 | Firma del contrato | Inicio formal del proyecto |
| Segunda cuota | 40% | $39,666,000 | Semana 8 del proyecto | Aprobación de módulos M1, M2 y M3 en entorno de pruebas |
| Cuota final | 30% | $29,749,500 | Entrega definitiva | Aceptación formal del sistema completo + capacitación realizada |
| **Total** | **100%** | **$99,165,000** | | |

**Cláusula de mora:** El incumplimiento en el pago de cualquier cuota por más de 15 días calendario otorga a DevSol Colombia S.A.S. el derecho de suspender el proyecto sin penalización hasta que el pago sea recibido. El plazo de entrega se extiende automáticamente por el tiempo de suspensión.

### §9.2 — Garantía

DevSol Colombia S.A.S. garantiza el correcto funcionamiento del sistema durante **30 días calendario** contados desde la fecha de entrega definitiva y aceptación formal por parte del cliente.

Durante este período, el proveedor corregirá sin costo adicional cualquier falla de funcionamiento que corresponda a errores en el código desarrollado.

**La garantía no cubre:**
- Modificaciones en los requisitos originales aprobados
- Errores provocados por uso incorrecto del sistema
- Cambios en la infraestructura del cliente realizados sin notificación al proveedor
- Actualizaciones de terceros (sistema operativo, base de datos) aplicadas por el cliente

### §9.3 — Propiedad Intelectual

A partir del pago completo del 100% del valor del contrato, FerreMax S.A.S. adquiere la titularidad total sobre:
- El código fuente del sistema FerreMax GI
- La documentación técnica y manuales de usuario
- Los activos digitales (diagramas, bases de datos, configuraciones) generados para este proyecto

Hasta el momento del pago total, el código fuente permanece en custodia del proveedor. DevSol Colombia S.A.S. se reserva el derecho de reutilizar componentes genéricos no específicos a FerreMax S.A.S. en proyectos futuros.

### §9.4 — Confidencialidad

Ambas partes se comprometen a mantener estricta confidencialidad sobre la información intercambiada durante el proyecto, incluyendo datos comerciales, procesos internos, precios y documentación técnica. Esta obligación se extiende por **2 años** a partir de la fecha de entrega definitiva del proyecto.

### §9.5 — Validez de la Oferta

La presente propuesta técnico-comercial tiene validez de **30 días calendario** contados desde la fecha de emisión (15 de noviembre de 2024). Vencido este plazo (15 de diciembre de 2024) sin formalización del contrato, DevSol Colombia S.A.S. se reserva el derecho de ajustar los valores presentados.

---

## §12 — Matriz de Riesgos del Proyecto

### Escala de valoración

| Nivel | Probabilidad (P) | Descripción |
|---|---|---|
| 1 | Muy baja | Probabilidad < 10% |
| 2 | Baja | Probabilidad 10-25% |
| 3 | Media | Probabilidad 26-50% |
| 4 | Alta | Probabilidad 51-75% |
| 5 | Muy alta | Probabilidad > 75% |

| Nivel | Impacto (I) | Descripción |
|---|---|---|
| 1 | Muy bajo | Retraso < 1 día, impacto imperceptible |
| 2 | Bajo | Retraso < 1 semana |
| 3 | Medio | Retraso 1-2 semanas |
| 4 | Alto | Retraso 2-4 semanas o costo adicional > 10% |
| 5 | Muy alto | Fracaso del módulo o del proyecto |

**Nivel de riesgo = P × I**

| Rango | Nivel | Color |
|---|---|---|
| 1 – 3 | 🟢 Bajo | Monitoreo básico |
| 4 – 7 | 🟡 Medio | Seguimiento semanal |
| 8 – 12 | 🟠 Alto | Plan de respuesta obligatorio |
| 13 – 25 | 🔴 Crítico | Acción preventiva inmediata |

---

### Registro de riesgos

| ID | Descripción del riesgo | Categoría | P | I | P×I | Nivel | Estrategia | Acción concreta | Responsable |
|---|---|---|---|---|---|---|---|---|---|
| R01 | Cambios de alcance sin control de cambios formal | Gestión | 4 | 4 | 16 | 🔴 Crítico | Mitigar | Incluir cláusula contractual de control de cambios. Reunión quincenal de validación de alcance con firma del cliente. | Gerente de proyecto |
| R02 | Rotación del equipo de desarrollo (salida de un desarrollador) | Recursos | 2 | 5 | 10 | 🟠 Alto | Mitigar | Documentar el código fuente semanalmente con estándares de comentarios. Sesión de pair programming cada 2 semanas. | Dev A (líder técnico) |
| R03 | Cliente no disponible para validaciones en los tiempos pactados | Comunicación | 3 | 3 | 9 | 🟠 Alto | Mitigar | Bloquear agenda del cliente para revisiones en el calendario del proyecto. Protocolo de aprobación tácita a 3 días hábiles. | Gerente de proyecto |
| R04 | Datos de inventario en Excel con errores que complican la migración | Técnico | 3 | 4 | 12 | 🔴 Crítico | Mitigar | Auditoría completa de los archivos Excel en la semana 1. Prueba de migración en entorno de desarrollo antes de pasar a producción. | Dev B |
| R05 | Falla de infraestructura cloud (AWS EC2 o RDS) | Técnico | 2 | 3 | 6 | 🟡 Medio | Aceptar | El SLA de AWS garantiza 99.9% de disponibilidad. Se activará backup local si la falla supera 4 horas. Informar al cliente. | Dev A |
| R06 | Incumplimiento en el pago de la segunda o tercera cuota | Financiero | 2 | 5 | 10 | 🟠 Alto | Mitigar | Cláusula de suspensión ante mora >15 días incluida en el contrato. Recordatorio automático 5 días antes del hito de pago. | Gerente de proyecto |
| R07 | Requisitos ambiguos o incompletos al iniciar el desarrollo | Técnico | 3 | 4 | 12 | 🔴 Crítico | Mitigar | Taller de revisión y firma del documento de requisitos en la semana 1. Sin requisito aprobado no se inicia su módulo. | Gerente de proyecto + Dev A |
| R08 | Tiempo de desarrollo subestimado para algún módulo | Gestión | 2 | 4 | 8 | 🟠 Alto | Mitigar | Buffer del 15% incluido en la estimación (semana 5). Reunión de seguimiento semanal con revisión del tablero Kanban. | Dev A |
| R09 | Rendimiento insuficiente del sistema con 3 sucursales simultáneas | Técnico | 2 | 3 | 6 | 🟡 Medio | Mitigar | Pruebas de carga básicas en las semanas 12-13 con scripts de simulación de usuarios concurrentes. | Dev B |
| R10 | Cambios en la normativa DIAN sobre facturación electrónica | Externo / Legal | 1 | 3 | 3 | 🟢 Bajo | Aceptar | Fuera del alcance actual del proyecto (documentado en §5.2 de la propuesta técnica). Será cotizado como módulo adicional si aplica. | Gerente de proyecto |

---

### Resumen de riesgos por nivel

| Nivel | Cantidad | Riesgos |
|---|---|---|
| 🔴 Crítico (13-25) | 3 | R01, R04, R07 |
| 🟠 Alto (8-12) | 4 | R02, R03, R06, R08 |
| 🟡 Medio (4-7) | 2 | R05, R09 |
| 🟢 Bajo (1-3) | 1 | R10 |

### Planes de respuesta detallados — Riesgos críticos y altos prioritarios

#### R01 — Cambios de alcance sin control de cambios formal (Crítico · P×I = 16)

**Situación**: FerreMax es una PYME con un gerente muy activo. Es probable que durante el desarrollo surjan nuevas ideas o modificaciones a los requisitos originales.

**Plan preventivo:**
1. Incluir cláusula explícita de control de cambios en el contrato (§9 adicionado)
2. Preparar formulario de «Solicitud de Cambio» firmado por el gerente general para cualquier modificación
3. Todo cambio aprobado genera addendum al contrato con nuevo valor y plazo
4. Reunión de validación de alcance cada 2 semanas — acta firmada

**Plan de contingencia** (si el riesgo se materializa): Detener el desarrollo del módulo afectado, emitir cotización del cambio en 48 horas, esperar aprobación formal antes de retomar.

---

#### R04 — Datos de inventario en Excel con errores (Crítico · P×I = 12)

**Situación**: FerreMax lleva su inventario en hojas Excel desde hace 6 años. Es altamente probable que los datos tengan inconsistencias (duplicados, campos vacíos, formatos mezclados).

**Plan preventivo:**
1. Semana 1: Dev B realiza auditoría completa de los 3 archivos Excel proporcionados por FerreMax
2. Entregar a FerreMax un reporte de calidad de datos con los problemas encontrados
3. FerreMax tiene 1 semana para limpiar los datos antes del inicio del módulo M4 (migración)
4. Si los datos no están limpios a tiempo, el módulo M4 se posterga sin penalización para el proveedor

**Plan de contingencia**: Desarrollar script de limpieza de datos básico (costo adicional cotizable), incluido como opción en el addendum de cambio.

---

#### R07 — Requisitos ambiguos al iniciar el desarrollo (Crítico · P×I = 12)

**Situación**: El levantamiento de requisitos se realizó en 2 sesiones. Algunos requisitos pueden ser interpretados de formas diferentes por el cliente y el equipo técnico.

**Plan preventivo:**
1. Semana 1 del proyecto (no de la propuesta): taller de revisión de requisitos con Carlos Mendoza y el jefe de bodega
2. Cada requisito se valida con criterios de aceptación específicos: «El sistema hace X cuando Y, y muestra Z»
3. Sin criterio de aceptación aprobado por el cliente → el módulo no se incluye en el sprint
4. Documento de requisitos firmado es el acuerdo de referencia ante cualquier disputa

---

#### R06 — Incumplimiento de pagos (Alto · P×I = 10)

**Plan preventivo:**
1. Contrato revisado por abogado con cláusula de mora (suspensión a los 15 días de vencimiento)
2. Recordatorio automático de pago 5 días hábiles antes del hito
3. No se entrega el código fuente ni las credenciales de producción hasta confirmar el 100% del pago final

---

## §13 — Aceptación y Firmas

La firma de esta propuesta técnico-comercial por ambas partes constituye la aceptación de todos los términos aquí establecidos y da inicio al proceso de elaboración del contrato formal.

---

**Por el cliente:**

| Campo | Datos |
|---|---|
| **Nombre completo** | Carlos Mendoza Ríos |
| **Cargo** | Gerente General |
| **Empresa** | FerreMax S.A.S. |
| **NIT** | 901.234.567-8 |
| **Fecha de aceptación** | _________________ |
| **Firma** | _________________ |

---

**Por el proveedor:**

| Campo | Datos |
|---|---|
| **Nombre completo** | _________________ |
| **Cargo** | Representante Legal |
| **Empresa** | DevSol Colombia S.A.S. |
| **NIT** | _________________ |
| **Fecha** | _________________ |
| **Firma** | _________________ |

---

> 📎 Este documento es parte del caso de estudio FerreMax — Bootcamp de Propuesta Técnica.
> Para la propuesta técnica completa (§1-§7), ver [`07-propuesta-tecnica-borrador.md`](./07-propuesta-tecnica-borrador.md).

*Cadena de Formación · Tecnólogo ADSO · Semana 8 de 9*
