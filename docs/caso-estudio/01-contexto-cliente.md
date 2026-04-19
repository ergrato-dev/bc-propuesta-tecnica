# 📋 FerreMax — Semana 1: Contexto del Cliente

> Documento del caso de estudio · Semana 1
> Uso: teoría y prácticas de ambas versiones del bootcamp

---

## 1. Ficha del Cliente

| Campo | Detalle |
|-------|---------|
| **Empresa** | FerreMax S.A.S. |
| **NIT** | 900.456.123-7 |
| **Sector** | Ferretería y suministros para construcción |
| **Actividad principal** | Venta al detal y al por mayor de materiales de ferretería |
| **Sede principal** | Carrera 68 # 42-15, Kennedy, Bogotá D.C. |
| **Sede secundaria** | Calle 17A # 70B-20, Fontibón, Bogotá D.C. |
| **Empleados** | ~25 (12 en Kennedy, 8 en Fontibón, 5 administrativos) |
| **Años en el mercado** | 12 años (fundada en 2014) |
| **Contacto principal** | Carlos Mendoza — Gerente General |
| **Correo** | cmendoza@ferremax.com.co |
| **Teléfono** | 601-345-6789 / 300-789-0123 |

---

## 2. ¿Qué hace FerreMax?

FerreMax S.A.S. vende materiales de ferretería y suministros para la industria de la construcción. Su catálogo tiene más de 2.000 referencias activas, divididas en categorías como:

- Herramientas manuales y eléctricas
- Tornillería y anclaje
- Tubería y plomería
- Pinturas y acabados
- Material eléctrico
- Cemento, arena y materiales de obra

Sus clientes principales son constructoras pequeñas, contratistas independientes (plomeros, electricistas, carpinteros) y el público en general.

---

## 3. La Situación Actual (en palabras del cliente)

> "Llevamos el inventario en Excel. Cada vendedor tiene su propio archivo. Cuando alguien vende algo en Fontibón, nos llaman por WhatsApp para que actualicemos el archivo en Kennedy. A veces nos olvidamos, y terminamos vendiendo productos que ya no tenemos. El mes pasado perdimos tres pedidos grandes porque no teníamos claro el stock real. También nos ha pasado que facturamos productos a precios desactualizados porque el vendedor usó un Excel viejo."
>
> — Carlos Mendoza, entrevista inicial, marzo 2026

---

## 4. Problemas Identificados

| # | Problema | Área afectada | Evidencia |
|---|----------|--------------|-----------|
| P-01 | Inventario en múltiples Excel sin sincronización entre sedes | Bodega / Ventas | Múltiples archivos con versiones distintas |
| P-02 | Comunicación de stock por WhatsApp — informal y sin trazabilidad | Ventas | Mensajes perdidos, actualizaciones olvidadas |
| P-03 | Venta de productos sin stock real disponible | Ventas / Atención al cliente | 3 pedidos perdidos en marzo 2026 |
| P-04 | Precios desactualizados en archivos locales | Facturación | Facturación incorrecta, diferencias con clientes |
| P-05 | Sin historial de movimientos de inventario | Administración | Imposible auditar mermas o detectar pérdidas |

**Impacto económico estimado:** ~$2.400.000 COP en ventas no concretadas durante marzo 2026.

---

## 5. Stakeholders del Caso

| Nombre | Cargo | Sede | Rol en el Proyecto |
|--------|-------|------|-------------------|
| Carlos Mendoza | Gerente General | Kennedy | Sponsor — toma decisiones y aprueba el presupuesto |
| Laura Gómez | Jefa de Bodega | Kennedy | Usuario clave — valida módulo de inventario |
| Pedro Arias | Vendedor Senior | Kennedy | Usuario final — registra ventas en mostrador |
| Marcela Torres | Vendedora | Fontibón | Usuario final — necesita acceso remoto en tiempo real |
| Ana Reyes | Contadora | Remoto | Usuario final — usa reportes para facturación mensual |

---

## 6. Lo que Quiere el Cliente (peticiones iniciales)

En la reunión de inicio, Carlos Mendoza expresó las siguientes necesidades:

1. "Que cualquier vendedor pueda ver el inventario en tiempo real desde cualquier sede"
2. "Que cuando se venda algo, el stock se actualice solo"
3. "Que yo pueda ver desde mi celular cuántos productos tenemos"
4. "Que haya un reporte de lo que se vendió en el día"
5. "Que sea fácil de usar — mis empleados no son muy tecnológicos"

---

## 7. Preguntas Sin Responder (para semana 2)

Estas preguntas surgieron del análisis inicial pero no fueron respondidas en la primera reunión:

- ¿Requiere facturación electrónica DIAN? (obligatoria en Colombia desde cierto nivel de facturación)
- ¿Habrá integración con software contable existente?
- ¿Cómo se migrará el historial de datos de Excel?
- ¿Quién administrará el sistema una vez entregado?
- ¿Hay proveedores que deban tener acceso al sistema para ver pedidos?

---

## 8. Tecnología Actual

| Herramienta | Uso actual | Problema |
|-------------|-----------|---------|
| Excel (Office 365) | Gestión de inventario | Archivos independientes, sin sincronización |
| WhatsApp Business | Comunicación entre sedes | Sin trazabilidad, informal |
| Factura en papel / Excel | Facturación a clientes | Errores de precio, sin registro digital |
| Sin software contable | — | Contadora trabaja con hojas de cálculo externas |

**Conectividad:**
- Kennedy: fibra óptica 100/100 Mbps (ETB)
- Fontibón: internet móvil 4G (Movistar)

**Dispositivos disponibles:**
- 3 computadores de escritorio en Kennedy (Windows 10)
- 1 portátil en Fontibón
- Celulares Android (vendedores y gerente)

---

*Caso FerreMax · Semana 1 de 9 · Solo para uso en teoría y prácticas del bootcamp*
