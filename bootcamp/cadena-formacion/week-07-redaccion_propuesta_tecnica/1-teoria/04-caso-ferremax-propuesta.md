# 📋 Caso FerreMax — Propuesta Técnica (Borrador Guía)

> **Referencia**: Cadena de Formación · Semana 7 · Teoría 04  
> Este documento es el **modelo de referencia** para el taller práctico y para el entregable S07.  
> Los datos provienen de los casos FerreMax de las semanas 2 al 6.

---

# PROPUESTA TÉCNICA

**Sistema de Gestión Integrada FerreMax**

| Campo | Detalle |
|-------|---------|
| Versión | v1.0 |
| Fecha de emisión | 15 de noviembre de 2024 |
| Válida hasta | 15 de diciembre de 2024 |
| Cliente | FerreMax S.A.S. — Cali, Colombia |
| Contacto cliente | Carlos Ramírez — Gerente General |
| Proveedor | Equipo de Desarrollo CF-ADSO |
| Estado | Borrador para revisión |

---

## 1. Información General

**Control de versiones del documento**

| Versión | Fecha | Descripción | Autor |
|---------|-------|-------------|-------|
| v0.1 | 08/11/2024 | Borrador inicial para revisión interna | Dev A |
| v1.0 | 15/11/2024 | Primera versión formal entregada al cliente | Dev A + Dev B |

---

## 2. Resumen Ejecutivo

FerreMax S.A.S. opera actualmente tres puntos de venta en la ciudad de Cali sin un sistema unificado que permita controlar el inventario, registrar las ventas y gestionar la cartera de clientes. Esta situación genera inconsistencias en el stock entre sucursales, dificultades para la facturación y ausencia de información consolidada para la toma de decisiones gerenciales.

La presente propuesta plantea el desarrollo de un sistema web de gestión integrada que centralizará el inventario, las ventas y la información de clientes y proveedores de las tres sucursales en tiempo real. La solución estará construida sobre tecnologías de código abierto (Python, FastAPI, PostgreSQL, React), lo que elimina costos de licenciamiento y asegura una base tecnológica sostenible a largo plazo.

El proyecto se ejecutará en 15 semanas mediante una metodología iterativa con entrega por módulo, lo que permitirá a FerreMax validar el avance y realizar ajustes de forma oportuna. El equipo está conformado por dos desarrolladores con experiencia en el stack tecnológico propuesto.

El costo total del proyecto asciende a **$99,165,000 COP**, con una condición de pago escalonada: 30% al inicio del proyecto, 40% al completar los módulos intermedios y 30% en la entrega final. La presente propuesta tiene una validez de 30 días calendario a partir de la fecha de emisión.

---

## 3. Antecedentes y Análisis del Problema

### 3.1 Descripción de la organización cliente

FerreMax S.A.S. es una empresa familiar con doce años de operación en el sector ferretero de la ciudad de Cali, Colombia. Cuenta con tres puntos de venta activos en los barrios Alameda, Chapinero y El Poblado, con un total de quince empleados distribuidos entre vendedores, bodegueros y personal administrativo. El volumen mensual de ventas promedio de la empresa es de $120,000,000 COP, con picos de demanda en los meses de agosto y diciembre.

La empresa ha experimentado un crecimiento sostenido en los últimos tres años, lo que ha incrementado la complejidad operativa de gestionar tres puntos de venta de forma independiente sin una plataforma tecnológica integradora.

### 3.2 Situación actual

En la actualidad, FerreMax gestiona sus operaciones con las siguientes herramientas:

| Proceso | Herramienta actual | Limitación identificada |
|---------|-------------------|------------------------|
| Control de inventario | Archivos Excel compartidos por WhatsApp | Versiones desactualizadas; sin trazabilidad de cambios |
| Registro de ventas | Facturas talonario en papel | Difícil auditoría; riesgo de pérdida de documentos |
| Gestión de clientes | Agenda personal del gerente + contactos del celular | Sin historial estructurado; no compartible entre sucursales |
| Gestión de proveedores | Carpetas físicas con cotizaciones | Sin comparativa de precios; búsqueda manual lenta |
| Reportes gerenciales | Construidos manualmente en Excel cada semana | 3–4 horas semanales de trabajo no productivo |

### 3.3 Problemática identificada

El análisis de la situación actual permite identificar cuatro problemas principales:

- **P01 — Inconsistencia de stock entre sucursales**: El mismo producto puede aparecer con stock disponible en la sucursal A mientras registra agotado en la sucursal B, sin cruce de información en tiempo real. Esto genera ventas fallidas y compras duplicadas.
- **P02 — Pérdida de trazabilidad en ventas**: No existe un historial digital de ventas asociado a clientes específicos ni a vendedores, lo que impide identificar la cartera activa, los clientes frecuentes o los productos de mayor rotación.
- **P03 — Carga operativa en reportes gerenciales**: El gerente invierte entre 3 y 4 horas semanales construyendo reportes consolidados de ventas e inventario de forma manual, tiempo que podría dedicarse a actividades estratégicas.
- **P04 — Riesgo de pérdida de información**: Los archivos principales de la empresa están almacenados en los computadores locales de cada punto de venta sin respaldo automático, lo que representa un riesgo operativo ante fallo de hardware o robo.

---

## 4. Propuesta de Solución Técnica

### 4.1 Descripción general de la solución

Se propone el desarrollo de un sistema web de acceso multi-sucursal denominado **FerreMax GI (Gestión Integrada)**, que centralizará el inventario, las ventas y la gestión de clientes y proveedores de los tres puntos de venta en una única plataforma de acceso web.

Los empleados accederán al sistema desde cualquier dispositivo con conexión a internet (computador, tablet) mediante credenciales personales. El sistema implementará un modelo de roles y permisos diferenciado por cargo (administrador, vendedor, bodeguero, gerente), de modo que cada usuario accede únicamente a las funcionalidades correspondientes a su rol.

### 4.2 Módulos del sistema

El sistema estará conformado por seis módulos funcionales:

| Módulo | Descripción funcional | Usuarios que lo usan |
|--------|----------------------|---------------------|
| M1 — Autenticación y usuarios | Registro de usuarios, inicio de sesión seguro, gestión de roles y permisos por sucursal | Administrador |
| M2 — Inventario | Catálogo de productos, stock por sucursal, alertas de stock mínimo, entrada/salida de mercancía | Bodeguero, vendedor, administrador |
| M3 — Clientes y proveedores | CRUD completo de clientes y proveedores, historial de compras por cliente, búsqueda avanzada | Vendedor, administrador |
| M4 — Ventas y facturación | Registro de ventas, generación de factura, relación automática con stock, resumen de caja | Vendedor, cajero |
| M5 — Reportes y dashboard | Tableros de indicadores: ventas por sucursal, rotación de inventario, clientes activos | Gerente |
| M6 — Configuración | Gestión de sucursales, parámetros del sistema, rangos de alerta de stock | Administrador |

### 4.3 Stack tecnológico propuesto

| Capa | Tecnología | Justificación para FerreMax |
|------|-----------|----------------------------|
| Backend | Python 3.12 + FastAPI | Alto rendimiento, curva de aprendizaje baja, licencia open source (MIT) |
| Base de datos | PostgreSQL 16 | Robusto, gratuito, soporta múltiples usuarios concurrentes, backups automáticos |
| Frontend | React 18 + Vite | Interfaz reactiva, compatible con navegadores de escritorio, responsive para tablet |
| Infraestructura | AWS EC2 + S3 | Disponibilidad 99.9 %, despliegue regional en São Paulo, precios en USD con facturación mensual |
| Autenticación | JWT (JSON Web Token) | Estándar de la industria para autenticación stateless en APIs REST |
| Control de versiones | Git + GitHub (privado) | Trazabilidad de cambios, entrega de código fuente al cliente al cierre del proyecto |

### 4.4 Arquitectura general

La solución sigue una arquitectura cliente-servidor de tres capas: el frontend en React consume una API REST construida con FastAPI, que a su vez se comunica con la base de datos PostgreSQL. Todos los componentes están alojados en AWS (región sa-east-1, São Paulo) con acceso HTTPS y certificado SSL gestionado por Let's Encrypt.

Las copias de seguridad de la base de datos se ejecutan automáticamente cada 24 horas con retención de 7 días. El código fuente del proyecto se entrega al cliente al cierre del proyecto en un repositorio GitHub privado, con licencia de uso perpetuo.

---

## 5. Alcance del Proyecto

### 5.1 Funcionalidades incluidas en el precio

El presente contrato incluye el desarrollo e implementación de los siguientes módulos y funcionalidades:

- Módulo M1: Registro, autenticación, roles y permisos (administrador, vendedor, bodeguero, gerente)
- Módulo M2: Catálogo de productos, gestión de stock por sucursal, alertas de mínimo, movimientos de inventario
- Módulo M3: CRUD de clientes, CRUD de proveedores, historial de compras por cliente
- Módulo M4: Registro de venta con selección de productos, cálculo automático de total, reserva de stock, generación de factura en PDF
- Módulo M5: Dashboard con 5 indicadores clave (ventas del día, stock crítico, ventas por sucursal, clientes nuevos del mes, productos más vendidos)
- Módulo M6: Creación y edición de sucursales, parámetros de stock mínimo por categoría
- Despliegue en ambiente de producción (AWS EC2 + S3 + dominio .com.co)
- Una sesión de inducción al sistema para el equipo de FerreMax (máximo 2 horas)
- 30 días de garantía de corrección de defectos post-entrega

### 5.2 Fuera del alcance

Las siguientes funcionalidades y servicios **no están incluidos** en el precio de esta propuesta:

- Integración con facturación electrónica DIAN
- Aplicación móvil nativa para Android o iOS
- Migración de datos históricos de archivos Excel anteriores al año 2022
- Diseño de identidad visual corporativa (logos, paleta de colores, material de marketing)
- Capacitaciones adicionales a la sesión de inducción incluida
- Módulo de contabilidad o nómina
- Pasarelas de pago en línea (PSE, tarjeta de crédito)
- Soporte técnico mensual posterior al período de garantía (cotizable aparte)

---

## 6. Metodología de Desarrollo

El proyecto se ejecutará mediante una metodología **iterativa e incremental** organizada en cinco fases:

| Fase | Semanas | Actividades principales | Entregable |
|------|---------|------------------------|-----------|
| Fase 1 — Inicio | S1 | Configuración de ambientes, repositorio, acuerdo de tecnologías, kick-off con FerreMax | Ambiente de desarrollo funcional |
| Fase 2 — Módulos base | S2–S5 | Desarrollo de M1 (autenticación) y M2 (inventario) | Demo funcional de M1 + M2 para validación |
| Fase 3 — Módulos de negocio | S6–S10 | Desarrollo de M3 (clientes/proveedores), M4 (ventas) y M6 (configuración) | Demo funcional de M3 + M4 + M6 |
| Fase 4 — Reportes y pruebas | S11–S13 | Desarrollo de M5 (reportes), pruebas de integración, pruebas de usuario | Sistema completo en staging para revisión del cliente |
| Fase 5 — Despliegue y entrega | S14–S15 | Despliegue en producción, sesión de inducción, entrega de código | Sistema en producción + código fuente |

**Herramientas de gestión**: GitHub Projects (tablero de tareas abierto al cliente), Google Meet (check-in semanal de 30 minutos).

---

## 7. Cronograma

El proyecto tiene una duración total de **15 semanas** (equivalente a 3 meses y tres semanas de trabajo continuo).

| Semana | Actividad principal | Hito |
|--------|--------------------|----|
| S1 | Inicio: acuerdos, configuración de ambiente, repositorio | ✓ Ambiente listo |
| S2–S3 | M1 — Autenticación y roles | |
| S4–S6 | M2 — Inventario (módulo más extenso) | |
| S7 | Demo M1 + M2 — Revisión del cliente | ✓ Aprobación Fase 2 |
| S8–S9 | M3 — Clientes y proveedores | |
| S9–S11 | M4 — Ventas y facturación | |
| S12 | Demo M3 + M4 + M6 — Revisión del cliente | ✓ Aprobación Fase 3 |
| S11–S13 | M5 — Reportes + pruebas de integración | |
| S13 | Prueba de aceptación usuario (UAT) | ✓ UAT aprobado |
| S14–S15 | Despliegue producción + inducción + entrega código | ✓ Entrega final |

**Fecha de inicio estimada**: lunes 18 de noviembre de 2024  
**Fecha de entrega estimada**: viernes 28 de febrero de 2025

---

## 8. Estimación de Costos

El costo total del proyecto es el resultado de sumar los costos de recurso humano, infraestructura, contingencia y margen de ganancia, según la metodología de presupuestación aplicada en la Semana 6.

| Concepto | Valor (COP) |
|----------|-------------|
| Desarrollo del sistema — 6 módulos (Dev A + Dev B) | $75,000,000 |
| Infraestructura (AWS EC2, S3, dominio) | $597,000 |
| Gestión y control del proyecto | $7,000,000 |
| Reserva técnica y contingencia | $7,568,000 |
| **Subtotal** | **$90,165,000** |
| IVA (si aplica según régimen tributario del proveedor) | A convenir |
| **TOTAL PROPUESTA** | **$99,165,000 COP** |

**Condiciones de pago**:

| Momento | Porcentaje | Valor aproximado |
|---------|------------|-----------------|
| Anticipo (firma del contrato) | 30% | $29,749,500 |
| Entrega Fase 3 (semana 12) | 40% | $39,666,000 |
| Entrega final (semana 15) | 30% | $29,749,500 |
| **Total** | **100%** | **$99,165,000** |

---

## 9. Equipo del Proyecto

| Perfil | Rol | Experiencia | Dedicación al proyecto |
|--------|-----|-------------|----------------------|
| Dev A | Desarrollador semi-senior full-stack · Líder técnico | 3 años en Python/React, 2 proyectos de gestión comercial entregados | 80% |
| Dev B | Desarrollador junior full-stack · Soporte y QA | 1.5 años en Python/React, participación en 1 proyecto CRUD multi-módulo | 80% |

---

## 10. Supuestos, Condiciones y Firma

### 10.1 Supuestos del proyecto

| ID | Supuesto |
|----|----------|
| SP-01 | FerreMax proporcionará acceso a la red interna y al dominio web en los primeros 5 días hábiles del proyecto. |
| SP-02 | Los precios del servidor AWS pueden variar ±10% sin afectar el presupuesto aceptado (cubierto por la reserva técnica). |
| SP-03 | FerreMax realizará revisiones y entregas de retroalimentación en un plazo máximo de 5 días hábiles por entregable. Demoras adicionales pueden extender el cronograma y el costo. |
| SP-04 | El stack tecnológico descrito en la sección 4.3 es aprobado por FerreMax antes del inicio del desarrollo. Cambios de tecnología implican una revisión del cronograma. |
| SP-05 | No se requiere integración con sistemas externos de terceros. Las integraciones adicionales tienen costo cotizable aparte. |

### 10.2 Condiciones comerciales

- **Validez de la propuesta**: 30 días calendario desde la fecha de emisión.
- **Cambios de alcance**: Cualquier funcionalidad no descrita en la Sección 5.1 requiere una adenda escrita al contrato. Los cambios de alcance pueden implicar ajuste de precio y cronograma.
- **Propiedad del código**: Al realizar el pago total, FerreMax recibirá el código fuente con licencia de uso perpetuo. El proveedor puede conservar fragmentos de código genérico reutilizable.
- **Confidencialidad**: Ambas partes acuerdan mantener la confidencialidad de la información compartida durante el proyecto.

### 10.3 Firma de aceptación

Al firmar este documento, FerreMax S.A.S. acepta los términos, el alcance, el cronograma y el precio descritos en esta propuesta técnica. Esta firma constituye un acuerdo de intención previo a la firma del contrato de desarrollo de software.

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

> **Nota pedagógica**: Este documento es el producto de integrar todos los entregables S02–S06. En la semana 8 se completará con la propuesta comercial (condiciones detalladas, matriz de riesgos y aspectos legales básicos).

---

*Cadena de Formación · Tecnólogo ADSO · Caso FerreMax · Semana 7 de 9*
