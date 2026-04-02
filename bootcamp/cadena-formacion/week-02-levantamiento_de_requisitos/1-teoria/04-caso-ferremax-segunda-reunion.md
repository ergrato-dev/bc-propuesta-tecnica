# 📖 04 — Caso FerreMax: Segunda Reunión con el Cliente

> Teoría · Semana 2 · Cadena de Formación
> Caso de estudio: **FerreMax S.A.S.**

---

## 🎯 Objetivos

- Ver en acción el proceso de levantamiento de requisitos aplicado al caso FerreMax
- Leer e interpretar una transcripción de reunión real (simulada)
- Identificar requisitos funcionales y no funcionales dentro de una conversación natural
- Entender cómo se elabora el acta y los primeros requisitos documentados

---

## Contexto

Después de la primera reunión (semana 1), el consultor revisó el contexto de FerreMax y elaboró una lista de preguntas sin responder. Esta semana se llevó a cabo la **segunda reunión**, con el objetivo de resolver esas dudas y documentar los requisitos formalmente.

**Participantes:**
- Carlos Mendoza — Gerente General, FerreMax S.A.S.
- Laura Gómez — Jefa de Bodega, FerreMax S.A.S.
- Consultor (el tú, el aprendiz como profesional)

**Fecha:** Miércoles 8 de abril de 2026, 3:00 p.m.
**Modalidad:** Google Meet (30 minutos)

---

## Acta de Reunión — Segunda Sesión FerreMax

---

**Proyecto:** Sistema de Gestión de Inventario — FerreMax S.A.S.
**Fecha:** 08/04/2026
**Hora inicio:** 3:02 p.m. **Hora fin:** 3:36 p.m.
**Modalidad:** Google Meet

| Nombre | Cargo | Empresa |
|--------|-------|---------|
| Carlos Mendoza | Gerente General | FerreMax S.A.S. |
| Laura Gómez | Jefa de Bodega | FerreMax S.A.S. |
| [Consultor] | Analista / Consultor | [Empresa consultora] |

---

### 1. Objetivo de la Reunión

Resolver las preguntas técnicas pendientes de la primera reunión y levantar los requisitos funcionales y no funcionales del sistema de inventario de FerreMax.

---

### 2. Resumen de la Reunión (transcripción editada)

**Consultor:** Buenos días Carlos, buenas Laura. Gracias por conectarse. La semana pasada identificamos los problemas principales. Hoy quiero resolver unas preguntas específicas antes de definir qué va a incluir el sistema. ¿Les parece bien?

**Carlos:** Claro, adelante.

---

**Consultor:** Empiezo con algo importante: ¿necesitan que el sistema genere facturas electrónicas para la DIAN?

**Carlos:** No todavía. Nosotros facturamos en papel y en Excel. La contadora nos dijo que por el monto que facturamos no estamos obligados aún. Eso puede quedarse así por ahora.

**Consultor:** Entendido. ¿Tienen algún software contable como Siigo, Alegra o Contasoft?

**Carlos:** No. Ana, la contadora, trabaja con Excel. Ella pide el reporte de ventas a fin de mes y lo registra en su propio archivo.

**Consultor:** ¿Necesitarían que el sistema exporte ese reporte en algún formato que le sirva a ella?

**Carlos:** Sí, ella siempre pide que le manden el reporte en Excel. Si pudiera descargar el reporte mensual directamente en Excel, sería perfecto.

---

**Laura:** Yo también quiero agregar algo sobre los reportes. A mí me interesa más saber qué productos se están agotando. Que el sistema me avise cuando el stock baje de cierto límite, no cuando ya se agotó.

**Consultor:** Perfecto. ¿Ese límite lo definiría usted, o sería fijo para todos los productos?

**Laura:** Cada producto es diferente. Para el cemento, por ejemplo, si tenemos menos de 50 bultos, ya hay que pedir más. Para un martillo, con 5 es suficiente. Necesito poder definirlo producto por producto.

**Consultor:** Anotado. ¿Y esa alerta llega por correo, por el sistema, por WhatsApp?

**Laura:** Por el sistema está bien. No quiero más mensajes de WhatsApp.

---

**Consultor:** Carlos, una pregunta sobre acceso. ¿Quién puede modificar los precios del catálogo?

**Carlos:** Solo yo. Los vendedores no pueden cambiar precios — ya tuve ese problema antes.

**Consultor:** ¿Y quién puede registrar productos nuevos en el sistema?

**Carlos:** Laura y yo. Nadie más.

**Consultor:** ¿Y las ventas, quién las registra?

**Carlos:** Todos los vendedores. Pedro en Kennedy, Marcela en Fontibón. Cuando entra un pedido, el vendedor lo registra.

---

**Consultor:** ¿Cómo piensan migrar los datos del Excel actual? ¿Lo hacen gradualmente o quieren que el sistema arranque con todo el catálogo desde el primer día?

**Carlos:** Mmm... no lo había pensado. ¿Qué nos recomienda?

**Consultor:** Lo ideal es que el sistema tenga el catálogo completo desde el día uno para evitar confusión. Podríamos preparar un archivo de importación desde el Excel actual. ¿Tienen un Excel "oficial" con todos los productos actualizados?

**Laura:** Yo tengo el más actualizado. Tiene unas 2.300 referencias activas. Pero está un poco desordenado — hay columnas que ya no se usan.

**Consultor:** Con eso podemos trabajar. Cuando tengamos el sistema en pruebas, me comparte ese archivo y lo revisamos juntos para la migración.

---

**Consultor:** ¿Quién va a administrar el sistema cuando se entregue? Por ejemplo, quién crea nuevos usuarios, quién configura los productos.

**Carlos:** Laura puede hacer eso. Ella es la que más entiende del inventario.

**Laura:** Sí, yo lo haría. Pero necesito que sea fácil — no soy programadora.

**Consultor:** El panel de administración va a ser simple. Pero voy a necesitar que uno de los dos tome una capacitación de 2-3 horas cuando entreguemos el sistema. ¿Está bien?

**Carlos:** Perfecto.

---

**Consultor:** Última pregunta por hoy: ¿van a tener proveedores que necesiten ver el sistema? Por ejemplo, para ver si su pedido llegó o consultar su saldo.

**Carlos:** No. Los proveedores no necesitan entrar. Eso se maneja por teléfono.

---

**Consultor:** Muy bien. Déjenme resumir lo que acordamos:
1. No se requiere facturación electrónica DIAN en esta versión.
2. El sistema debe exportar el reporte mensual en Excel.
3. El sistema debe alertar sobre stock bajo definido por producto.
4. Solo Carlos puede modificar precios; Laura y Carlos pueden registrar productos nuevos.
5. Todos los vendedores pueden registrar ventas.
6. La migración de datos se hace desde el Excel de Laura al momento del lanzamiento.
7. Laura será la administradora del sistema y recibirá capacitación.
8. Los proveedores no tienen acceso al sistema.

**Carlos:** Todo correcto.

**Laura:** Sí, así es.

**Consultor:** Perfecto. Les voy a enviar el acta por correo esta tarde. Necesito que la confirmen para avanzar con el documento de requisitos formal.

---

### 3. Requisitos Identificados en Esta Reunión

> Nota: estos son preliminares — se formalizarán en el documento de requisitos completo.

| ID | Descripción | Tipo | Prioridad |
|----|-------------|------|-----------|
| RF-001 | El sistema debe registrar productos con código, nombre, categoría, precio de costo y precio de venta | RF | Alta |
| RF-002 | El sistema debe actualizar el stock automáticamente al registrar una venta | RF | Alta |
| RF-003 | El sistema debe mostrar el inventario disponible en tiempo real para todas las sedes | RF | Alta |
| RF-004 | El sistema debe permitir registrar ventas desde cualquier sede | RF | Alta |
| RF-005 | El sistema debe enviar una alerta interna cuando el stock de un producto baje del mínimo definido | RF | Alta |
| RF-006 | El sistema debe permitir configurar el stock mínimo por producto individualmente | RF | Alta |
| RF-007 | El sistema debe generar un reporte de ventas mensual exportable en formato Excel (.xlsx) | RF | Alta |
| RF-008 | El sistema debe generar un reporte de ventas del día, visible desde el panel del gerente | RF | Media |
| RF-009 | El sistema debe permitir importar el catálogo de productos desde un archivo Excel en el despliegue inicial | RF | Media |
| RF-010 | El sistema debe tener roles de usuario: Administrador, Gerente y Vendedor | RF | Alta |
| RNF-001 | Solo el usuario con rol Administrador o Gerente puede modificar precios | RNF | Alta |
| RNF-002 | Solo el usuario con rol Administrador o Gerente puede registrar o eliminar productos | RNF | Alta |
| RNF-003 | El sistema debe funcionar en celulares Android desde la versión 8.0 | RNF | Alta |
| RNF-004 | El panel de administración debe ser comprensible sin formación técnica (usabilidad básica) | RNF | Media |
| RNF-005 | El sistema no requiere integración con software contable externo en esta versión | RNF | N/A |

---

### 4. Acuerdos y Compromisos

| # | Acuerdo | Responsable | Fecha límite |
|---|---------|-------------|--------------|
| 1 | Laura envía el archivo Excel de catálogo de productos | Laura Gómez | 13/04/2026 |
| 2 | El consultor envía el acta por correo hoy | Consultor | 08/04/2026 |
| 3 | Carlos y Laura confirman el acta por correo | Carlos / Laura | 10/04/2026 |
| 4 | El consultor entrega el documento de requisitos completo | Consultor | 15/04/2026 |

---

### 5. Preguntas Pendientes

- ¿Debe el sistema llevar historial de cambios de precio? (Carlos no respondió esto)
- ¿Los reportes deben incluir devoluciones o solo ventas directas?
- ¿Quién recibe las alertas de stock bajo si Laura no está? (¿también Carlos?)

---

### 6. Próxima Reunión

**Fecha propuesta:** Martes 15 de abril de 2026
**Objetivo:** Revisión y validación del documento de requisitos completo

---

## Análisis del Caso

### ¿Qué funcionó bien en esta reunión?

- El consultor fue con preguntas preparadas — no improvisó
- Confirmó lo entendido antes de cerrar: "Déjenme resumir..."
- Incluyó a Laura (usuario técnico de bodega), no solo al gerente
- Descubrió requisitos que nadie había mencionado (límite de stock por producto, exportar en Excel)

### ¿Qué requisitos eran implícitos y se descubrieron?

- Control de roles y permisos (nadie lo pedía, pero es crítico)
- Migración de datos desde Excel (el cliente no había pensado en esto)
- Exportación del reporte para la contadora en formato que ella usa

### ¿Qué quedó pendiente para confirmar?

- Historial de cambios de precio
- Devoluciones en reportes
- Quién recibe alertas si el administrador no está disponible

---

*Caso FerreMax · Cadena de Formación · Semana 2 de 9*
