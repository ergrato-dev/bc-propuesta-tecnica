# PROPUESTA TÉCNICA — Sistema de Gestión Integrada FerreMax

> **Instrucciones**: Este es el archivo de trabajo del taller S07.  
> Completa todas las secciones marcadas con `<!-- Completar -->`.  
> Los campos ya resueltos son ejemplos o datos fijos del caso FerreMax.

---

## PORTADA

| Campo | Valor |
|-------|-------|
| Nombre del documento | Propuesta Técnica |
| Nombre del proyecto | Sistema de Gestión Integrada FerreMax |
| Versión | <!-- Completar → Usa v1.0 para la primera versión formal --> |
| Fecha de emisión | <!-- Completar → Fecha de hoy en formato DD/MM/AAAA --> |
| Válida hasta | <!-- Completar → 30 días después de la fecha de emisión --> |
| Cliente | FerreMax S.A.S. — Cali, Colombia |
| Contacto cliente | Carlos Ramírez — Gerente General |
| Proveedor | <!-- Completar → Tu nombre o nombre del equipo --> |
| Ficha SENA | <!-- Completar → Número de la ficha de tu grupo --> |

**Control de cambios del documento**

| Versión | Fecha | Descripción del cambio | Autor |
|---------|-------|------------------------|-------|
| v0.1 | <!-- Completar --> | Borrador inicial para revisión interna | <!-- Completar → Tu nombre --> |
| v1.0 | <!-- Completar → fecha formal --> | Primera versión entregada al cliente | <!-- Completar --> |

---

## 1. Información General

Este documento presenta la propuesta técnica para el desarrollo del **Sistema de Gestión Integrada FerreMax**, elaborada en respuesta a la necesidad de FerreMax S.A.S. de contar con una plataforma tecnológica que centralice y optimice sus operaciones comerciales en sus tres puntos de venta en la ciudad de Cali, Colombia.

---

## 2. Resumen Ejecutivo

<!-- 📝 Instrucciones:
     Redacta 4 párrafos siguiendo la estructura:
     P1: El problema de FerreMax (3 sucursales, sin sistema, inconsistencias de stock)
     P2: La solución propuesta (sistema web, módulos, tecnología open source)
     P3: Cómo y cuánto (metodología iterativa, 15 semanas, 2 desarrolladores)
     P4: Precio ($99,165,000 COP) + condiciones principales (30/40/30)
     Extensión total: 200 a 350 palabras. Sin tecnicismos ni siglas sin definir. -->

FerreMax S.A.S. opera actualmente tres puntos de venta en la ciudad de Cali sin un sistema unificado que permita controlar el inventario, registrar las ventas y gestionar la cartera de clientes. Esta situación genera inconsistencias en el stock entre sucursales, dificultades para la facturación y ausencia de información consolidada para la toma de decisiones gerenciales.

<!-- Completar → Párrafo 2: Describe la solución propuesta (sistema web, módulos, stack open source) -->

<!-- Completar → Párrafo 3: Describe la metodología (iterativa, 15 semanas, equipo de 2 desarrolladores) -->

<!-- Completar → Párrafo 4: Indica el precio total en COP y las condiciones de pago 30/40/30 -->

---

## 3. Antecedentes y Análisis del Problema

### 3.1 Descripción de la organización cliente

FerreMax S.A.S. es una empresa familiar con doce años de operación en el sector ferretero de la ciudad de Cali, Colombia. Cuenta con tres puntos de venta en los barrios Alameda, Chapinero y El Poblado, con un total de quince empleados distribuidos entre áreas de ventas, bodega y administración. El volumen mensual de ventas promedio de la empresa es de $120,000,000 COP.

<!-- Completar → Agrega 1 párrafo adicional sobre el crecimiento de la empresa o el contexto del sector ferretero en Colombia -->

### 3.2 Situación actual

En la actualidad, FerreMax gestiona sus operaciones con las siguientes herramientas:

| Proceso | Herramienta actual | Limitación identificada |
|---------|-------------------|------------------------|
| Control de inventario | Archivos Excel compartidos por WhatsApp | <!-- Completar → ¿qué problema operativo genera? --> |
| Registro de ventas | Facturas talonario en papel | <!-- Completar → ¿qué problema genera para la auditoría? --> |
| Gestión de clientes | Agenda personal del gerente | Sin historial estructurado ni información compartida |
| Gestión de proveedores | Carpetas físicas con cotizaciones | Sin comparativa de precios; búsqueda manual lenta |
| Reportes gerenciales | Construidos manualmente en Excel | <!-- Completar → ¿cuánto tiempo pierde el gerente cada semana? --> |

### 3.3 Problemática identificada

El análisis de la situación actual permite identificar los siguientes problemas principales:

- **P01 — Inconsistencia de stock entre sucursales**: El mismo producto puede aparecer con stock disponible en la sucursal A mientras registra agotado en la sucursal B, sin cruce de información en tiempo real.
- **P02 — Pérdida de trazabilidad en ventas**: No existe un historial digital de ventas por cliente ni por vendedor.
- **P03** — <!-- Completar → Describe el problema de los reportes gerenciales con datos concretos -->
- **P04** — <!-- Completar → Describe el problema de riesgo de pérdida de información (archivos locales, sin backup) -->

---

## 4. Propuesta de Solución Técnica

### 4.1 Descripción general de la solución

Se propone el desarrollo de un sistema web de acceso multi-sucursal denominado **FerreMax GI (Gestión Integrada)**, que centralizará el inventario, las ventas y la gestión de clientes y proveedores de los tres puntos de venta en una única plataforma de acceso web.

<!-- Completar → Agrega un párrafo sobre el modelo de acceso (desde cualquier dispositivo, credenciales, roles diferenciados) -->

### 4.2 Módulos del sistema

El sistema estará conformado por seis módulos funcionales:

| Módulo | Descripción funcional | Usuarios que lo usan |
|--------|----------------------|---------------------|
| M1 — Autenticación y usuarios | Registro de usuarios, inicio de sesión seguro, gestión de roles y permisos | Administrador |
| M2 — Inventario | Catálogo de productos, stock por sucursal, alertas de stock mínimo, movimientos de mercancía | Bodeguero, vendedor, administrador |
| M3 — Clientes y proveedores | CRUD de clientes y proveedores, historial por cliente | Vendedor, administrador |
| M4 — Ventas y facturación | <!-- Completar → Describe qué hace este módulo en 1 oración --> | Vendedor, cajero |
| M5 — Reportes y dashboard | <!-- Completar → Describe qué hace este módulo en 1 oración (nombre al menos 2 indicadores) --> | Gerente |
| M6 — Configuración | Gestión de sucursales, parámetros del sistema, alertas de stock | Administrador |

### 4.3 Stack tecnológico propuesto

| Capa | Tecnología | Justificación para FerreMax |
|------|-----------|----------------------------|
| Backend | Python 3.12 + FastAPI | <!-- Completar → min. 10 palabras de justificación --> |
| Base de datos | PostgreSQL 16 | <!-- Completar → min. 10 palabras --> |
| Frontend | React 18 + Vite | <!-- Completar → min. 10 palabras --> |
| Infraestructura | AWS EC2 + S3 | <!-- Completar → min. 10 palabras --> |
| Autenticación | JWT (JSON Web Token) | Estándar para autenticación stateless en APIs REST; sin sesiones en servidor |
| Control de versiones | Git + GitHub (privado) | Trazabilidad de cambios; código fuente entregado al cliente al cierre |

### 4.4 Arquitectura general

<!-- Completar → Describe en 3 a 5 oraciones cómo se conectan los componentes: frontend → API → base de datos.
     Incluye: HTTPS, JWT, backup automático, región AWS. No uses diagramas, solo texto. -->

---

## 5. Alcance del Proyecto

### 5.1 Funcionalidades incluidas en el precio

El presente contrato incluye el desarrollo e implementación de los siguientes módulos y funcionalidades:

- Módulo M1: Registro, autenticación, roles y permisos (administrador, vendedor, bodeguero, gerente)
- Módulo M2: Catálogo de productos, gestión de stock por sucursal, alertas de mínimo, movimientos de inventario
- Módulo M3: CRUD de clientes, CRUD de proveedores, historial de compras por cliente
- Módulo M4: Registro de venta con selección de productos, cálculo de total, reserva de stock, factura en PDF
- Módulo M5: Dashboard con 5 indicadores clave (ventas del día, stock crítico, ventas por sucursal, clientes nuevos, productos más vendidos)
- Módulo M6: Creación y edición de sucursales, parámetros de stock mínimo
- Despliegue en ambiente de producción (AWS EC2 + S3 + dominio .com.co)
- Una sesión de inducción al sistema (máximo 2 horas)
- 30 días de garantía de corrección de defectos post-entrega

### 5.2 Fuera del alcance

Las siguientes funcionalidades **no están incluidas** en el precio de esta propuesta:

- Integración con facturación electrónica DIAN
- <!-- Completar → Agrega un ítem fuera del alcance relacionado con dispositivos móviles -->
- <!-- Completar → Agrega un ítem fuera del alcance relacionado con datos históricos -->
- Módulo de contabilidad o nómina
- <!-- Completar → Agrega un ítem adicional relevante para el tipo de sistema -->

---

## 6. Metodología de Desarrollo

El proyecto se ejecutará mediante una metodología iterativa e incremental con entregas por módulo.

| Fase | Semanas | Actividades principales | Entregable |
|------|---------|------------------------|-----------|
| Fase 1 — Inicio | S1 | Configuración de ambientes, repositorio, kick-off con FerreMax | Ambiente de desarrollo funcional |
| Fase 2 — Módulos base | S2–S6 | Desarrollo de M1 y M2 | <!-- Completar → ¿cuál es el entregable al terminar esta fase? --> |
| Fase 3 — Módulos de negocio | S7–S11 | Desarrollo de M3, M4 y M6 | Demo de M3 + M4 + M6 para validación |
| Fase 4 — Reportes y pruebas | S12–S13 | M5, pruebas de integración y usuario | <!-- Completar → ¿cuál es el entregable? --> |
| Fase 5 — Despliegue y entrega | S14–S15 | Despliegue en producción, inducción, entrega código | Sistema en producción + código fuente |

---

## 7. Cronograma

El proyecto tiene una duración total de **15 semanas** a partir de la firma del contrato.

| Semana | Actividad principal | Hito |
|--------|--------------------|----|
| S1 | Inicio: acuerdos, ambiente, repositorio | ✓ Ambiente listo |
| S2–S3 | M1 — Autenticación y roles | |
| S4–S6 | M2 — Inventario | |
| S7 | <!-- Completar → ¿qué hito ocurre en la semana 7? --> | ✓ <!-- Completar --> |
| S8–S9 | M3 — Clientes y proveedores | |
| S9–S11 | M4 — Ventas y facturación | |
| S12 | <!-- Completar → ¿qué hito ocurre en la semana 12? --> | ✓ <!-- Completar --> |
| S11–S13 | M5 — Reportes + pruebas de integración | |
| S13 | Prueba de aceptación usuario (UAT) | ✓ UAT aprobado |
| S14–S15 | Despliegue + inducción + entrega código | ✓ Entrega final |

**Fecha de inicio estimada**: <!-- Completar → fecha de lunes siguiente a la firma -->  
**Fecha de entrega estimada**: <!-- Completar → 15 semanas después del inicio -->

---

## 8. Estimación de Costos

El costo total del proyecto incluye recurso humano, infraestructura, contingencia y margen de ganancia conforme al presupuesto detallado en la Semana 6.

| Concepto | Valor (COP) |
|----------|-------------|
| Desarrollo del sistema — 6 módulos | $75,000,000 |
| Infraestructura (AWS EC2, S3, dominio) | $597,000 |
| Gestión y control del proyecto | $7,000,000 |
| Reserva técnica y contingencia | $7,568,000 |
| **Subtotal** | **$90,165,000** |
| IVA (si aplica) | A convenir |
| **TOTAL PROPUESTA** | **$99,165,000 COP** |

**Condiciones de pago**:

| Momento | Porcentaje | Valor aproximado |
|---------|------------|-----------------|
| Anticipo (firma del contrato) | 30% | $29,749,500 |
| Entrega Fase 3 (semana <!-- Completar -->) | 40% | $39,666,000 |
| Entrega final (semana 15) | 30% | $29,749,500 |
| **Total** | **100%** | **$99,165,000** |

---

## 9. Equipo del Proyecto

| Perfil | Rol | Experiencia | Dedicación |
|--------|-----|-------------|------------|
| Dev A | Desarrollador semi-senior full-stack · Líder técnico | 3 años en Python/React | 80% |
| Dev B | Desarrollador junior full-stack · Soporte y QA | 1.5 años en Python/React | 80% |

<!-- Completar → Agrega 1–2 oraciones describiendo las fortalezas del equipo para este tipo de proyecto -->

---

## 10. Supuestos, Condiciones y Firma

### 10.1 Supuestos del proyecto

| ID | Supuesto |
|----|----------|
| SP-01 | FerreMax proporcionará acceso a la red interna y al dominio web en los primeros 5 días hábiles del proyecto. |
| SP-02 | Los precios del servidor AWS pueden variar ±10% sin afectar el presupuesto (cubierto por la reserva técnica). |
| SP-03 | FerreMax realizará revisiones en un plazo máximo de 5 días hábiles por entregable. Demoras adicionales pueden extender el cronograma. |
| SP-04 | El stack tecnológico descrito en la sección 4.3 es aprobado por FerreMax antes del inicio del desarrollo. |
| SP-05 | No se requiere integración con sistemas externos de terceros. |
| SP-06 | <!-- Completar → Escribe un supuesto adicional propio, específico para el proyecto FerreMax --> |

### 10.2 Condiciones comerciales

- **Validez de la propuesta**: 30 días calendario desde la fecha de emisión.
- **Cambios de alcance**: Las funcionalidades que no estén descritas en la Sección 5.1 requieren una adenda escrita y pueden implicar ajuste de precio y cronograma.
- **Propiedad del código**: Al realizar el pago total, FerreMax recibirá el código fuente con licencia de uso perpetuo.
- **Confidencialidad**: Ambas partes acuerdan mantener la confidencialidad de la información compartida durante el proyecto.

### 10.3 Firma de aceptación

```
ACEPTACIÓN DE LA PROPUESTA TÉCNICA

Cliente
Nombre completo:  ______________________________
Cargo:            ______________________________
Empresa:          FerreMax S.A.S.
Fecha:            ______________________________
Firma:            ______________________________

Proveedor
Nombre completo:  ______________________________
Cargo:            ______________________________
Fecha:            ______________________________
Firma:            ______________________________
```

---

*Taller S07 · Cadena de Formación · Tecnólogo ADSO · Semana 7 de 9*
