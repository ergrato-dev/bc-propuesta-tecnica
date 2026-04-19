# 📋 Caso de Estudio — Documento 07: Propuesta Técnica FerreMax GI

> **Propósito:** Documento maestro de referencia para instructores y aprendices. Presenta la propuesta técnica completa del proyecto FerreMax GI, integrando todos los entregables construidos en las semanas 2 al 6. Este documento representa el nivel de calidad esperado al finalizar la Semana 7.
>
> **Versión:** v1.0 — Propuesta Final  
> **Caso:** FerreMax S.A.S. — Sistema de Gestión Integrada  
> **Semana:** 7 — Redacción de la Propuesta Técnica

---

# PROPUESTA TÉCNICA

## Sistema de Gestión Integrada — FerreMax GI

---

| Campo | Valor |
|---|---|
| **Nombre del documento** | Propuesta Técnica — Sistema FerreMax GI |
| **Versión** | v1.0 |
| **Fecha de emisión** | 15 de noviembre de 2024 |
| **Válida hasta** | 15 de diciembre de 2024 (30 días calendario) |
| **Cliente** | FerreMax S.A.S. |
| **Contacto del cliente** | Andrés Morales — Gerente General |
| **Proveedor** | DevSoft ADSO (Equipo de Desarrollo SENA) |
| **Ficha SENA** | 2847361 |

### Control de Cambios

| Versión | Fecha | Autor | Descripción del cambio |
|---|---|---|---|
| v0.1 | 12/11/2024 | Equipo Dev | Borrador inicial — estructura base |
| v0.9 | 14/11/2024 | Equipo Dev | Revisión de costos y cronograma |
| v1.0 | 15/11/2024 | Equipo Dev | Versión final aprobada para envío |

---

## 2. Resumen Ejecutivo

FerreMax S.A.S. es una empresa ferretera con 12 años de trayectoria en Cali, con 3 sucursales y 15 empleados que factura aproximadamente $120 millones de pesos mensuales. La empresa administra su inventario mediante hojas de cálculo independientes en cada sucursal, lo que genera inconsistencias en los registros, pérdidas estimadas en $4.2 millones de pesos mensuales por diferencias de inventario, y una ausencia total de información consolidada para la toma de decisiones gerenciales.

Se propone desarrollar **FerreMax GI**, un sistema web de gestión integrada que centralice el inventario, ventas, clientes y reportes de las 3 sucursales en una plataforma única y accesible desde cualquier dispositivo con conexión a internet. El sistema contará con 6 módulos principales: autenticación y roles de usuario, gestión de inventario, gestión de clientes y proveedores, registro de ventas, reportes gerenciales y configuración del sistema.

El proyecto se ejecutará en **15 semanas** mediante una metodología iterativa con entregas funcionales cada 3 semanas. El equipo estará conformado por 2 desarrolladores con experiencia en tecnologías web modernas (Python, React y PostgreSQL), con disponibilidad del 80% durante toda la duración del proyecto. Se garantiza la participación del equipo de FerreMax en las sesiones de validación semanales.

La inversión requerida para el desarrollo completo del sistema es de **$99,165,000 COP**, pagaderos en 3 cuotas: 30% al inicio del proyecto, 40% al entregar los módulos principales y 30% al completar la implementación y capacitación. Esta propuesta tiene una validez de 30 días calendario a partir de la fecha de emisión.

---

## 3. Antecedentes y Análisis del Problema

### 3.1 Descripción del Cliente

**FerreMax S.A.S.** es una empresa ferretera caleña fundada en 2012, dedicada a la comercialización de materiales de construcción, herramientas y acabados para el sector de la construcción y consumidores finales. Opera 3 sucursales en la ciudad de Cali (sedes Chipichape, Sur y Norte), con un equipo de 15 empleados y una facturación mensual promedio de $120 millones de pesos.

La empresa ha experimentado un crecimiento sostenido en los últimos 3 años, lo que ha hecho evidente la necesidad de modernizar sus procesos de gestión interna para soportar la operación de múltiples sucursales de forma eficiente.

### 3.2 Herramientas y Procesos Actuales

| Proceso | Herramienta actual | Limitación principal |
|---|---|---|
| Control de inventario | Hoja de cálculo Excel (una por sucursal) | Sin sincronización entre sucursales |
| Registro de ventas | Cuaderno físico + archivo Excel sin estructura | Sin totales automáticos, errores frecuentes |
| Gestión de clientes | Libreta de contactos + correo electrónico | Sin historial de compras ni seguimiento |
| Gestión de proveedores | Notas en papel + mensajes WhatsApp | Sin registro de pedidos ni condiciones de pago |
| Reportes gerenciales | Elaborados manualmente cada mes | No son en tiempo real, toman 3–4 días cada cierre |

### 3.3 Problemas Identificados

A partir de la entrevista con el gerente Andrés Morales y la revisión de los procesos actuales, se identificaron 4 problemas críticos:

| ID | Problema | Impacto en el negocio |
|---|---|---|
| P01 | Inventario desconectado entre las 3 sucursales | Pérdidas estimadas de $4.2M/mes por diferencias no detectadas a tiempo |
| P02 | Ausencia de historial de ventas unificado | Imposibilidad de calcular rentabilidad real ni identificar productos estrella |
| P03 | Sin trazabilidad de clientes frecuentes | Pérdida de oportunidades de fidelización y ventas recurrentes |
| P04 | Reportes gerenciales tardíos y manuales | El gerente recibe la información con 3–4 días de retraso, afectando decisiones de compra |

---

## 4. Propuesta de Solución

### 4.1 Descripción de la Solución

Se propone desarrollar **FerreMax GI** (Gestión Integrada), un sistema web centralizado que unifica la operación de las 3 sucursales en una única plataforma. El sistema permitirá registrar y consultar inventario en tiempo real desde cualquier sucursal, gestionar ventas con comprobantes digitales, administrar el directorio de clientes y proveedores con historial completo, y generar reportes gerenciales automáticos disponibles en cualquier momento.

El acceso al sistema será por medio de cualquier navegador web desde equipos de escritorio o dispositivos móviles. No se requiere instalación de software adicional. Cada empleado tendrá un usuario con permisos definidos según su rol (administrador, vendedor, bodeguero).

### 4.2 Módulos del Sistema

| ID | Módulo | Funcionalidad principal |
|---|---|---|
| M1 | Autenticación y Roles | Login seguro, gestión de usuarios y permisos por rol |
| M2 | Gestión de Inventario | Registro de productos, entradas/salidas, alertas de stock mínimo en tiempo real |
| M3 | Clientes y Proveedores | Directorio con historial de compras, contacto y condiciones comerciales |
| M4 | Registro de Ventas | Punto de venta básico con comprobante digital y descuentos configurables |
| M5 | Reportes Gerenciales | Dashboard con ventas, inventario, clientes activos y márgenes en tiempo real |
| M6 | Configuración del Sistema | Parámetros generales: sucursales, impuestos, categorías de productos |

### 4.3 Tecnologías Propuestas

| Componente | Tecnología | Justificación |
|---|---|---|
| Backend (lógica del negocio) | Python 3.12 + FastAPI | Alta productividad, documentación automática con Swagger, amplia comunidad |
| Base de datos | PostgreSQL 16 | Motor robusto y gratuito, ideal para datos transaccionales con múltiples usuarios |
| Frontend (interfaz web) | React 18 + Vite | Interfaz reactiva y moderna, rendimiento óptimo en dispositivos con conexión lenta |
| Autenticación | JWT (JSON Web Tokens) | Estándar de la industria, seguro y sin estado de sesión en servidor |
| Infraestructura | AWS EC2 + RDS (capa gratuita inicial) | Disponibilidad 99.9%, escalable sin costo de mantenimiento de hardware |
| Control de versiones | Git + GitHub | Trazabilidad completa del código, trabajo colaborativo entre desarrolladores |

### 4.4 Arquitectura del Sistema

El sistema sigue una arquitectura de 3 capas: presentación, lógica de negocio y datos. El frontend en React se comunica con el backend en FastAPI mediante una API REST documentada. La base de datos PostgreSQL almacena todos los datos de las 3 sucursales en un servidor centralizado en la nube. Las copias de seguridad automáticas se realizarán cada 24 horas.

---

## 5. Alcance del Proyecto

### 5.1 Incluido en este contrato

- Desarrollo de los módulos M1, M2, M3, M4, M5 y M6 según especificaciones
- Diseño de la base de datos con estructura multi-sucursal
- Interfaz web responsiva compatible con Chrome, Firefox y Brave
- API REST documentada con Swagger
- Pruebas funcionales unitarias y de integración
- Migración de datos existentes (hasta 500 productos y 200 clientes del archivo Excel actual)
- Capacitación al equipo de FerreMax (4 horas en modalidad virtual)
- Manual de usuario básico en formato PDF
- 30 días de soporte post-implementación (corrección de errores, sin nuevas funcionalidades)

### 5.2 Excluido de este contrato

- Aplicación móvil nativa (iOS o Android)
- Integración con plataformas de e-commerce (Rappi, Mercado Libre, página web)
- Módulo de contabilidad o facturación electrónica DIAN
- Mantenimiento correctivo después de los 30 días de soporte incluidos
- Migración de datos adicionales que superen los volúmenes declarados en §5.1
- Infraestructura de hardware (equipos, impresoras, red local de las sucursales)

---

## 6. Metodología de Desarrollo

El proyecto se ejecutará mediante una **metodología iterativa simplificada**, con entregas funcionales al final de cada fase. El cliente podrá probar cada módulo antes de que comience el siguiente. Las revisiones se harán en reuniones virtuales de 30 minutos semanales.

| Fase | Semanas | Actividad principal | Entregable |
|---|---|---|---|
| Fase 1: Inicio y diseño | S1 | Análisis detallado de requisitos, diseño de base de datos, arquitectura de módulos | Documento técnico de diseño |
| Fase 2: Desarrollo núcleo | S2–S6 | Desarrollo M1 (autenticación), M2 (inventario) y M3 (clientes/proveedores) | Módulos M1-M3 funcionales |
| Fase 3: Funcionalidades avanzadas | S7–S11 | Desarrollo M4 (ventas), M5 (reportes) y M6 (configuración) | Sistema completo v0.9 |
| Fase 4: Pruebas | S12–S13 | Pruebas funcionales, corrección de errores, pruebas de carga básica | Informe de pruebas |
| Fase 5: Implementación | S14–S15 | Despliegue en servidor, migración de datos, capacitación y soporte inicial | Sistema en producción |

---

## 7. Cronograma

El proyecto inicia el **18 de noviembre de 2024** y finaliza el **28 de febrero de 2025**, en un total de **15 semanas**.

| Semana | Período | Actividad | Hito |
|---|---|---|---|
| S1 | 18–22 Nov | Análisis y diseño | ✅ Documento de diseño aprobado |
| S2 | 25–29 Nov | Desarrollo M1 (autenticación) | — |
| S3 | 2–6 Dic | Desarrollo M2 (inventario) — parte 1 | — |
| S4 | 9–13 Dic | Desarrollo M2 (inventario) — parte 2 | ✅ Módulo de inventario funcional |
| S5 | 16–20 Dic | Desarrollo M3 (clientes/proveedores) | — |
| S6 | 6–10 Ene | Ajustes M1-M3 + integración parcial | ✅ Demo módulos M1-M3 al cliente |
| S7 | 13–17 Ene | Desarrollo M4 (ventas) — parte 1 | — |
| S8 | 20–24 Ene | Desarrollo M4 (ventas) — parte 2 | ✅ Módulo de ventas funcional |
| S9 | 27–31 Ene | Desarrollo M5 (reportes) | — |
| S10 | 3–7 Feb | Desarrollo M6 (configuración) | ✅ Sistema v0.9 — todos los módulos |
| S11 | 10–14 Feb | Integración final y ajustes | — |
| S12 | 17–21 Feb | Pruebas funcionales y UAT | — |
| S13 | 24–28 Feb | Corrección de errores | ✅ Sistema aprobado por cliente |
| S14 | 3–7 Mar | Despliegue en servidor de producción | — |
| S15 | 10–14 Mar | Migración de datos + capacitación | ✅ Sistema en producción — entrega final |

> **Nota:** La semana del 23 al 27 de diciembre no tiene actividades (cierre de año). La semana 6 inicia el 6 de enero.

---

## 8. Estimación de Costos

### Resumen de Inversión para el Cliente

| Concepto | Descripción | Valor COP |
|---|---|---|
| Desarrollo de software | Ingeniería, programación y pruebas (15 semanas) | $74,528,000 |
| Gestión de proyecto | Coordinación, reuniones y documentación | $8,120,000 |
| Servicios en la nube | AWS EC2 + RDS — 6 meses (despliegue + soporte) | $3,600,000 |
| Licencias de software | Herramientas de desarrollo (uso gratuito) | $0 |
| Contingencia (10%) | Reserva para imprevistos técnicos | $8,624,800 |
| Utilidad del proveedor (15%) | Margen de operación | $4,292,200 |
| **TOTAL** | | **$99,165,000 COP** |

> ⚠️ Todos los precios incluyen IVA. No se cobran costos de licencias adicionales. El mantenimiento post-soporte de 30 días tiene un valor diferenciado que se cotizará por separado si el cliente lo requiere.

### Condiciones de Pago

| Cuota | Porcentaje | Valor COP | Momento de pago |
|---|---|---|---|
| Anticipo | 30% | $29,749,500 | Al firmar el contrato |
| Segundo pago | 40% | $39,666,000 | Al aprobar la demo de módulos M1-M3 (Semana 6) |
| Pago final | 30% | $29,749,500 | Al recibir el sistema en producción (Semana 15) |
| **Total** | **100%** | **$99,165,000** | |

---

## 9. Equipo del Proyecto

| Perfil | Rol en el proyecto | Dedicación | Experiencia |
|---|---|---|---|
| Desarrollador A (Semi-senior) | Líder técnico, backend Python/FastAPI, arquitectura del sistema | 80% (92 días efectivos) | 4 años en desarrollo web, Python y bases de datos relacionales |
| Desarrollador B (Junior+) | Frontend React, integración de módulos, pruebas funcionales | 80% (112 días efectivos) | 2 años en desarrollo frontend, React y JavaScript moderno |

> Ambos desarrolladores son parte del programa Tecnólogo ADSO del SENA — Ficha 2847361. El Desarrollador A actúa como punto de contacto técnico con el cliente.

---

## 10. Supuestos, Condiciones y Firma

### 10.1 Supuestos del Proyecto

| ID | Supuesto |
|---|---|
| SP-01 | Las 3 sucursales de FerreMax cuentan con conexión a internet estable (mínimo 5 Mbps) |
| SP-02 | El cliente designará un representante técnico que validará los entregables en un plazo máximo de 3 días hábiles |
| SP-03 | Los datos actuales en Excel serán entregados al equipo de desarrollo en la Semana 1, en formato limpio |
| SP-04 | La infraestructura en la nube (AWS) será contratada a nombre de FerreMax S.A.S. al inicio del proyecto |
| SP-05 | Los cambios en el alcance posteriores al inicio del proyecto serán cotizados por separado mediante control de cambios |

### 10.2 Condiciones Comerciales

- La propuesta tiene **validez de 30 días calendario** a partir de la fecha de emisión.
- Cualquier modificación al alcance acordado generará un control de cambios con costo adicional.
- El soporte post-implementación cubre **errores de programación** exclusivamente, no peticiones de nuevas funcionalidades.
- La propiedad intelectual del código desarrollado pasa al cliente una vez realizado el **pago total** del proyecto.
- El incumplimiento en los pagos acordados suspende automáticamente la ejecución del proyecto hasta regularización.

### 10.3 Firma de Aceptación

Al firmar este documento, el cliente y el proveedor manifiestan su acuerdo con los términos, alcance, cronograma, costos y condiciones aquí descritos.

| Rol | Nombre | Firma | Fecha |
|---|---|---|---|
| **Cliente** | Andrés Morales — Gerente FerreMax S.A.S. | _________________________ | ___/___/___ |
| **Proveedor** | Equipo DevSoft ADSO — SENA Ficha 2847361 | _________________________ | ___/___/___ |

---

> 📌 **Nota para instructores:** Este documento integra los entregables de las Semanas 2 al 6. Puede usarse como plantilla de referencia para evaluar la propuesta final del aprendiz en la Semana 9. Los números de FerreMax (costos, semanas, módulos) deben permanecer consistentes en todos los documentos del caso de estudio.

*Cadena de Formación · Tecnólogo ADSO · Caso de Estudio FerreMax · Documento 07*
