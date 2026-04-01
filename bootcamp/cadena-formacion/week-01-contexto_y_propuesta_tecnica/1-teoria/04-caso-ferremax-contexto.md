# 📖 04 — Caso de Estudio: FerreMax S.A.S.

> Teoría · Semana 1 · Cadena de Formación
> Este caso ficticio se usará durante **las 9 semanas** del bootcamp.

---

## 🎯 Objetivos

- Conocer el cliente ficticio del bootcamp: FerreMax S.A.S.
- Identificar el problema de negocio que origina el proyecto
- Reconocer quiénes son los stakeholders del caso
- Leer la situación como lo haría un consultor de software

---

## 1. Ficha del Cliente

| Campo | Detalle |
|-------|---------|
| **Empresa** | FerreMax S.A.S. |
| **Sector** | Ferretería y suministros para construcción |
| **Ubicación** | Bogotá D.C. — Localidad de Kennedy |
| **Tamaño** | ~25 empleados, 2 sedes (Kennedy y Fontibón) |
| **Contacto** | Carlos Mendoza — Gerente General |
| **Teléfono** | 601-345-6789 |
| **Correo** | cmendoza@ferremax.com.co |
| **Años en el mercado** | 12 años |

---

## 2. ¿Qué hace FerreMax?

FerreMax S.A.S. vende materiales de ferretería y suministros para constructoras, carpinteros, plomeros y el público en general. Su catálogo tiene más de 2.000 referencias de productos: tornillos, cables eléctricos, tuberías, pintura, herramientas y mucho más.

Tienen dos sedes:
- **Kennedy** (sede principal): almacén grande, bodega, oficina administrativa
- **Fontibón** (sede secundaria): punto de venta más pequeño, sin bodega propia

---

## 3. El Problema (palabras del cliente)

> "Llevamos el inventario en Excel. Cada vendedor tiene su propio archivo. Cuando alguien vende algo en Fontibón, nos llaman por WhatsApp para que actualicemos el archivo en Kennedy. A veces nos olvidamos, y terminamos vendiendo productos que ya no tenemos. El mes pasado perdimos tres pedidos grandes porque no teníamos claro el stock real. También nos ha pasado que facturamos productos a precios desactualizados porque el vendedor usó un Excel viejo."

**Problemas identificados:**

| # | Problema | Impacto |
|---|----------|---------|
| 1 | Inventario en múltiples Excel sin sincronización | Datos desactualizados, errores de stock |
| 2 | Comunicación de ventas por WhatsApp | Pérdida de registros, errores humanos |
| 3 | Sin control de stock en tiempo real | Ventas de productos agotados |
| 4 | Precios desactualizados por archivos duplicados | Facturación incorrecta, pérdidas económicas |
| 5 | Sin historial de movimientos de inventario | Imposible auditar o detectar mermas |

---

## 4. Lo que quiere el cliente

Carlos Mendoza describió su necesidad así:

> "Quiero un sistema donde cualquier vendedor, desde cualquier sede, pueda ver el inventario en tiempo real. Que cuando se venda algo, el stock se actualice solo. Y que yo pueda ver desde mi celular cuántos productos tenemos y qué se ha vendido en el día."

**Peticiones clave del cliente:**
- Acceso desde cualquier sede (web o app)
- Actualización automática del inventario al vender
- Vista del stock en tiempo real
- Reportes de ventas diarias
- Acceso desde el celular del gerente

---

## 5. Stakeholders del Caso

| Nombre | Cargo | Relación con el proyecto |
|--------|-------|--------------------------|
| Carlos Mendoza | Gerente General | Sponsor: aprueba y paga el proyecto |
| Laura Gómez | Jefa de Bodega (Kennedy) | Usuario clave: valida el módulo de inventario |
| Pedro Arias | Vendedor (Kennedy) | Usuario final: registra ventas diarias |
| Marcela Torres | Vendedora (Fontibón) | Usuario final: necesita acceso remoto |
| Ana Reyes | Contadora | Usuario final: usa reportes para facturación |

---

## 6. Lo que el Cliente NO mencionó

Un consultor experimentado nota lo que el cliente **no dijo** pero que puede ser importante:

- ¿Necesita facturación electrónica DIAN? (obligatoria en Colombia para cierto nivel de ventas)
- ¿Habrá integración con proveedores o software contable existente?
- ¿Quién administrará el sistema cuando esté listo?
- ¿Qué pasa con el historial de ventas anterior (datos del Excel)?

> 📌 Estas preguntas se resolverán en la **Semana 2** cuando practiquemos el levantamiento de requisitos con el cliente.

---

## 7. Contexto Tecnológico Actual de FerreMax

Para entender bien el proyecto, un consultor también revisa qué tecnología tiene el cliente hoy:

| Aspecto | Situación actual |
|---------|-----------------|
| **Gestión de inventario** | Excel (Office 365) — archivos independientes por sede |
| **Comunicación interna** | WhatsApp Business |
| **Facturación** | Factura manual en Excel, impresión en papel |
| **Conectividad** | Internet por fibra óptica en Kennedy, Movistar 4G en Fontibón |
| **Dispositivos** | 3 computadores en Kennedy, 1 en Fontibón, celulares Android |
| **Software contable** | Ninguno — la contadora usa Excel |

**Conclusión para el consultor:** El cliente no tiene ningún sistema de software propio. El punto de partida es cero. Esto simplifica la migración de datos pero también significa que hay que construir todo desde el inicio.

---

## 8. Restricciones que Mencionó el Cliente

Carlos Mendoza dio información adicional que limita el proyecto:

- **Presupuesto:** "No quiero gastar más de $15 millones de pesos"
- **Tiempo:** "Necesito algo funcionando antes de diciembre, que es temporada alta"
- **Capacitación:** "Mis empleados no son muy tecnológicos — tiene que ser fácil de usar"
- **Soporte:** "Si algo falla un lunes en la mañana, necesito que alguien me atienda ese mismo día"

Estas restricciones son tan importantes como los requisitos. Las tendrás en cuenta cuando llegues a las semanas de estimación y presupuesto.

---

## ✅ Checklist del Caso

- [ ] Memoricé el nombre del cliente ficticio: **FerreMax S.A.S.**
- [ ] Conozco el problema principal: inventario en Excel sin sincronización
- [ ] Identifiqué al menos 3 stakeholders del caso
- [ ] Entiendo la situación tecnológica actual de FerreMax
- [ ] Reconozco las restricciones de presupuesto, tiempo y soporte

---

*Anterior: [03 — Propuesta Técnica ←](./03-propuesta-tecnica.md)*

*Siguiente paso: [Taller Práctico →](../2-practicas/01-taller-analisis-propuesta/README.md)*
