# 📋 FerreMax — Semana 2: Acta y Documento de Requisitos

> Documento del caso de estudio · Semana 2
> Uso: teoría y prácticas de ambas versiones del bootcamp

---

## Documento 1: Acta de la Segunda Reunión

---

**Proyecto:** Sistema de Gestión de Inventario — FerreMax S.A.S.
**Versión:** 1.0
**Fecha de reunión:** 08/04/2026
**Hora:** 3:02 p.m. – 3:36 p.m.
**Modalidad:** Google Meet

| Nombre | Cargo | Empresa |
|--------|-------|---------|
| Carlos Mendoza | Gerente General | FerreMax S.A.S. |
| Laura Gómez | Jefa de Bodega | FerreMax S.A.S. |
| [Consultor] | Analista de Requisitos | [Empresa consultora] |

### Objetivo

Resolver las preguntas técnicas pendientes de la primera reunión y completar el levantamiento de requisitos del sistema de inventario de FerreMax.

### Acuerdos

| # | Acuerdo | Responsable | Fecha límite |
|---|---------|-------------|--------------|
| 1 | Laura envía el archivo Excel con catálogo de productos | Laura Gómez | 13/04/2026 |
| 2 | El consultor envía el acta por correo | Consultor | 08/04/2026 |
| 3 | Carlos y Laura confirman el acta | Carlos / Laura | 10/04/2026 |
| 4 | El consultor entrega el documento de requisitos completo | Consultor | 15/04/2026 |

### Preguntas pendientes para la semana 3

- ¿Debe el sistema llevar historial de cambios de precio?
- ¿Los reportes deben incluir devoluciones o solo ventas directas?
- ¿Quién recibe las alertas de stock bajo si Laura no está disponible?

---

## Documento 2: Listado de Requisitos — FerreMax Sistema de Inventario

**Versión:** 1.0 (post segunda reunión)
**Fecha:** 15/04/2026

---

### Requisitos Funcionales

| ID | Descripción | Stakeholder | Prioridad |
|----|-------------|-------------|-----------|
| RF-001 | El sistema debe permitir registrar productos con código único, nombre, categoría, precio de costo y precio de venta | Laura Gómez | Alta |
| RF-002 | El sistema debe permitir editar la información de un producto existente | Laura Gómez / Carlos Mendoza | Alta |
| RF-003 | El sistema debe mostrar el inventario disponible en tiempo real con el stock actualizado de ambas sedes | Carlos Mendoza / Vendedores | Alta |
| RF-004 | El sistema debe permitir buscar productos por código, nombre o categoría | Vendedores | Alta |
| RF-005 | El sistema debe registrar ventas indicando: producto, cantidad vendida, precio unitario y fecha | Pedro Arias / Marcela Torres | Alta |
| RF-006 | El sistema debe actualizar el stock automáticamente al registrar una venta | Sistema automático | Alta |
| RF-007 | El sistema debe permitir configurar el stock mínimo por producto de forma individual | Laura Gómez | Alta |
| RF-008 | El sistema debe enviar una alerta interna cuando el stock de un producto baje del mínimo configurado | Laura Gómez | Alta |
| RF-009 | El sistema debe mostrar un panel de resumen con las ventas del día para el gerente | Carlos Mendoza | Media |
| RF-010 | El sistema debe generar un reporte de ventas mensual exportable en formato Excel (.xlsx) | Ana Reyes | Alta |
| RF-011 | El sistema debe permitir importar el catálogo de productos desde un archivo Excel en el despliegue inicial | Laura Gómez | Media |
| RF-012 | El sistema debe tener módulo de gestión de usuarios con roles: Administrador, Gerente y Vendedor | Carlos Mendoza | Alta |
| RF-013 | El sistema debe mostrar el inventario accesible desde el navegador web de un celular Android | Carlos Mendoza | Alta |

---

### Requisitos No Funcionales

| ID | Descripción | Categoría | Stakeholder |
|----|-------------|-----------|-------------|
| RNF-001 | El sistema debe responder a cualquier operación en menos de 3 segundos con una conexión 4G o Wi-Fi normal | Rendimiento | Carlos Mendoza |
| RNF-002 | Solo los usuarios con rol Administrador o Gerente pueden modificar los precios del catálogo | Seguridad | Carlos Mendoza |
| RNF-003 | Solo los usuarios con rol Administrador o Gerente pueden registrar, editar o eliminar productos | Seguridad | Carlos Mendoza |
| RNF-004 | El sistema debe estar disponible durante todo el horario laboral de FerreMax (lunes a sábado, 7:00 a.m. – 7:00 p.m.) | Disponibilidad | Carlos Mendoza |
| RNF-005 | El sistema debe funcionar correctamente en navegadores web de celulares Android desde la versión 8.0 | Compatibilidad | Carlos Mendoza / Marcela Torres |
| RNF-006 | Un vendedor sin experiencia técnica debe poder registrar una venta completa en menos de 5 pasos | Usabilidad | Carlos Mendoza |
| RNF-007 | El sistema no requiere integración con software contable externo en esta versión | Restricción técnica | Ana Reyes |
| RNF-008 | El sistema no requiere facturación electrónica DIAN en esta versión | Restricción legal | Carlos Mendoza |

---

### Requisitos Pendientes de Aclaración

| ID | Descripción actual | Aclaración necesaria |
|----|-------------------|----------------------|
| RF-PND-01 | El sistema debe registrar devoluciones | ¿Requieren registrar devoluciones de productos en esta versión? ¿Quién las autoriza? |
| RF-PND-02 | El sistema debe mantener historial de cambios de precio | ¿Necesitan ver quién cambió un precio y cuándo? ¿Por cuánto tiempo? |
| RNF-PND-01 | Las alertas de stock bajo llegan a... | Si Laura no está, ¿quién más debe recibir la alerta? ¿Solo en el sistema o también por correo? |

---

## Notas del Consultor

- Carlos tiene desconfianza histórica de sistemas por una mala experiencia previa (proveedor que no cumplió). Manejar expectativas desde el inicio, mostrar avances frecuentes.
- Laura será la administradora funcional del sistema. Capacitar en panel de administración.
- La conexión en la bodega de Kennedy puede ser débil — confirmar en visita presencial.
- Los precios varían por sede (descubierto en análisis del Excel): confirmar en semana 3 si es un requisito formal o una excepción histórica.

---

*Caso FerreMax · Semana 2 de 9 · Solo para uso en teoría y prácticas del bootcamp*
