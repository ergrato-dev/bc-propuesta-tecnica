# 📄 Propuesta Técnica — Sistema de Gestión de Inventario FerreMax

> Documento de ejemplo para el taller · **No es una propuesta real**
> Versión simplificada con fines didácticos

---

## SECCIÓN 1 — Presentación del Proveedor

**Empresa proveedora:** CodeSoft SAS
**Dirección:** Carrera 10 # 72-45, Bogotá D.C.
**Contacto:** Juan Valdés — juanvaldes@codesoft.com.co — 300-456-7890
**Sitio web:** www.codesoft.com.co
**Experiencia:** 6 años desarrollando soluciones web para el sector comercial en Colombia.

Proyectos anteriores similares:
- Sistema de inventario para Ferretería El Clavo Dorado (2023) — Medellín
- Sistema de punto de venta para Suministros El Norte (2024) — Barranquilla

---

## SECCIÓN 2 — Contexto y Problema del Cliente

FerreMax S.A.S. es una ferretería con dos sedes en Bogotá (Kennedy y Fontibón) que actualmente gestiona su inventario mediante archivos Excel independientes sin sincronización entre sedes. La comunicación de actualizaciones de stock se realiza por WhatsApp, lo que genera errores frecuentes como venta de productos agotados y facturación con precios desactualizados.

**Impacto económico estimado por el cliente:** pérdida de 3 pedidos grandes en el último mes, equivalentes a aproximadamente $2.400.000 COP en ventas no concretadas.

**Necesidad:** Sistema web centralizado que permita gestionar el inventario en tiempo real desde ambas sedes.

---

## SECCIÓN 3 — Alcance del Proyecto

### Lo que SÍ incluye esta propuesta:

- Módulo de registro y consulta de productos (código, nombre, categoría, precio, stock)
- Módulo de movimientos de inventario (entradas y salidas)
- Módulo de ventas con descuento automático del stock
- Reportes básicos: stock actual, movimientos del día, ventas por vendedor
- Panel de administración con acceso por roles (administrador, vendedor)
- Capacitación de 4 horas para el equipo de FerreMax
- Soporte técnico por 3 meses después de la entrega

### Lo que NO incluye esta propuesta:

- Facturación electrónica DIAN (puede agregarse en una segunda fase)
- Integración con software contable externo
- Aplicación móvil nativa (la versión web es responsive para celulares)
- Migración de datos históricos de Excel (los datos anteriores se entregan como archivo de importación)

---

## SECCIÓN 4 — Requisitos del Sistema

El sistema debe cumplir con los siguientes requisitos identificados durante la reunión con Carlos Mendoza y Laura Gómez:

**Requisitos de funcionalidad:**

1. El sistema debe permitir registrar productos con código, nombre, categoría, precio de compra y precio de venta.
2. El sistema debe permitir registrar entradas de inventario (compras a proveedores) y salidas (ventas o mermas).
3. El sistema debe actualizar el stock disponible de forma automática cada vez que se registre una venta.
4. El sistema debe permitir consultar el stock actual de cualquier producto desde cualquier sede.
5. El sistema debe generar un reporte de ventas del día, exportable a PDF.
6. El sistema debe enviar una alerta cuando un producto llegue al stock mínimo configurado.

**Requisitos de calidad:**

7. El sistema debe responder a cualquier consulta en menos de 3 segundos con conexión de al menos 5 Mbps.
8. El sistema debe estar disponible el 99% del tiempo en horario comercial (lunes a sábado, 7am–7pm).

---

## SECCIÓN 5 — Cronograma Estimado

| Fase | Actividades | Tiempo estimado |
|------|------------|-----------------|
| Análisis | Levantamiento detallado de requisitos, revisión de datos actuales | 2 semanas |
| Diseño | Arquitectura, base de datos, prototipos de pantallas | 1 semana |
| Desarrollo | Construcción de módulos y pruebas unitarias | 6 semanas |
| Pruebas | Pruebas con datos reales de FerreMax, ajustes | 2 semanas |
| Entrega | Capacitación, despliegue en producción, soporte inicial | 1 semana |
| **Total** | | **12 semanas** |

Fecha de inicio estimada: 2 semanas después de la firma del contrato.

---

## SECCIÓN 6 — Presupuesto

| Concepto | Costo (COP) |
|----------|------------|
| Análisis y diseño (40h × $65.000/h) | $2.600.000 |
| Desarrollo backend (120h × $70.000/h) | $8.400.000 |
| Desarrollo frontend (60h × $60.000/h) | $3.600.000 |
| Pruebas y ajustes (30h × $55.000/h) | $1.650.000 |
| Infraestructura (hosting + dominio, primer año) | $480.000 |
| Capacitación y documentación | $600.000 |
| **Total** | **$17.330.000 COP** |

**Forma de pago:** 40% al iniciar, 30% a mitad del proyecto, 30% a la entrega.

**Validez de esta propuesta:** 30 días calendario a partir de la fecha de emisión.

---

*Cadena de Formación · Semana 1 · Documento de práctica — no usar fuera del bootcamp*
