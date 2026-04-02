# 📼 Transcripción — Primera Reunión con FerreMax

> Documento de práctica · Semana 2 · Cadena de Formación
> Caso de estudio: **FerreMax S.A.S.**

---

> ⚠️ **Nota pedagógica:** Esta es una **transcripción simulada** de la primera reunión exploratoria con Carlos Mendoza. El consultor la tiene para analizar y extraer requisitos. Este documento es diferente al acta formal — es el registro bruto de la conversación, con los silencios, los cambios de tema y las expresiones informales del cliente.

---

**Fecha:** Lunes 30 de marzo de 2026
**Lugar:** Sede Kennedy — Oficina de gerencia, FerreMax S.A.S.
**Duración:** ~45 minutos
**Presentes:** Carlos Mendoza (gerente), consultor

---

## Transcripción

---

**Consultor:** Hola Carlos, buenas tardes. Gracias por recibirme. Voy a grabar la reunión si no le importa — solo para no perder ningún detalle.

**Carlos:** No hay problema. Siéntese. ¿Quiere tinto?

**Consultor:** Claro, gracias. Le cuento, lo que queremos hacer hoy es entender bien su negocio y cuáles son los problemas principales antes de hablar de desarrollo. ¿Cómo van hoy con el inventario?

**Carlos:** Pues mal, para ser sincero. Llevamos el inventario en Excel. Tenemos un archivo en esta computadora y otro en Fontibón, y los dos son diferentes. Cuando alguien vende algo allá, nos llaman por WhatsApp para que actualicemos este. Pero a veces uno está atendiendo un cliente y se le olvida actualizar.

**Consultor:** ¿Con qué frecuencia ocurre eso?

**Carlos:** Todos los días pasa algo así. El mes pasado nos pasó tres veces que le prometimos a un cliente que teníamos el producto y cuando fuimos a buscarlo no estaba. Dos de esos clientes no volvieron.

**Consultor:** ¿Y los precios? ¿También los manejan en Excel?

**Carlos:** Sí. Y ahí también tenemos problemas. Pedro a veces usa una copia vieja del archivo y factura con precios del mes pasado. La semana pasada le vendimos cemento a precio de enero. Perdimos plata.

**Consultor:** Entiendo. ¿Me puede contar cómo es el proceso cuando llega un cliente a comprar?

**Carlos:** Claro. El cliente llega y le dice al vendedor qué quiere. El vendedor busca en el Excel si hay stock. Si hay, hace la factura a mano o en Excel. Si no sabe si hay en bodega, le grita a Laura o le manda WhatsApp. Laura va y mira físicamente. Eso a veces tarda 10 o 15 minutos.

**Consultor:** ¿Laura Gómez es la jefa de bodega?

**Carlos:** Sí. Ella es la que más sabe del inventario. Hace 8 años que está con nosotros.

**Consultor:** ¿Podría estar Laura en la siguiente reunión?

**Carlos:** Claro. Le digo que esté.

---

**Consultor:** ¿Qué es lo que más le preocupa a usted del sistema que quieren construir?

**Carlos:** Que sea confiable. No me sirve un sistema bonito que se caiga. Y que mis vendedores puedan usarlo — ellos no son técnicos. El vendedor de Fontibón tiene 50 años y le cuesta hasta el Excel.

**Consultor:** ¿Qué operaciones necesitan los vendedores hacer en el sistema?

**Carlos:** Principalmente dos cosas: buscar si hay un producto y registrar la venta. Y que las dos sedes vean lo mismo en tiempo real. Eso es lo más importante.

**Consultor:** ¿Y usted qué quiere ver?

**Carlos:** Yo quiero ver desde el celular cuánto stock tenemos. Y saber qué se vendió en el día. Que si estoy en una reunión o en otra parte, pueda mirar en el teléfono.

---

**Consultor:** ¿Tienen presupuesto definido para este proyecto?

**Carlos:** Todavía no. Por eso quiero ver primero qué me van a proponer. Pero no somos una empresa grande — no podemos pagar una millonada.

**Consultor:** Entendido. ¿Alguna vez han tenido un sistema de este tipo antes?

**Carlos:** Intentamos con un programa que nos vendió un sobrino de un empleado. Duró tres meses y no funcionó. Se perdían datos, no actualizaba bien. Desde ahí quedé desconfiado de esas cosas.

**Consultor:** ¿Qué falló específicamente?

**Carlos:** Se perdían registros. Una vez cerraron el programa y se fue todo lo que habían metido ese día. Y el sobrino no respondía los mensajes. Eso fue hace como 4 años.

---

**Consultor:** ¿Qué otras funciones les gustaría tener además del inventario y las ventas?

**Carlos:** A Laura le gustaría saber cuándo un producto se está acabando. Que el sistema avise antes de que se agote, para hacer el pedido a tiempo. Y yo quería una app para el celular, pero entiendo que eso puede costar más.

**Consultor:** ¿La aplicación móvil es algo indispensable o podría funcionar con una página web en el navegador del celular?

**Carlos:** Si se ve bien en el celular, con eso me conformo. No tiene que ser una app descargada.

---

**Consultor:** ¿Qué pasa con los datos del Excel que ya tienen? ¿Cómo les gustaría pasarlos al nuevo sistema?

**Carlos:** Uf, ni lo había pensado. Tenemos 12 años de datos ahí. Bueno, tampoco necesitamos todo el historial — con que el sistema arranque con el catálogo actualizado me sirve. El historial de ventas viejas no me importa tanto.

**Consultor:** ¿Y la seguridad? ¿Quién puede cambiar el precio de los productos?

**Carlos:** Solo yo. Los vendedores no deben poder cambiar precios. Ya pasó que un vendedor le hizo un descuento a un amigo y yo me enteré después. No puede volver a pasar.

---

**Consultor:** Para cerrar la reunión, déjeme resumir lo que entendí. ¿Correcto hasta aquí?

El problema principal es que el inventario está desincronizado entre sedes y los vendedores trabajan con datos desactualizados. Necesitan un sistema web que funcione en celular, donde los vendedores puedan consultar stock y registrar ventas en tiempo real. Usted quiere ver reportes desde su celular. Solo usted puede cambiar precios. Y Laura quiere alertas de stock bajo.

**Carlos:** Exacto. Eso es lo que necesitamos.

**Consultor:** Perfecto. Voy a preparar unas preguntas adicionales para la próxima reunión. ¿Puede estar Laura disponible?

**Carlos:** Sí, hágame saber el horario.

**Consultor:** Muchas gracias por su tiempo, Carlos.

---

## Notas del Consultor (al margen)

> Estas son observaciones propias del consultor durante la visita — no son declaraciones del cliente.

- El archivo Excel en el escritorio tiene última modificación en febrero. Está desactualizado.
- Pedro Arias (vendedor) tiene dos versiones del archivo en diferentes carpetas. Riesgo alto.
- La oficina tiene Wi-Fi pero la señal en la bodega es débil — ¿afecta al sistema en tiempo real?
- Carlos mencionó "una app para el celular" — explorar si con web responsive es suficiente ✅
- Requiero preguntar: facturación DIAN, software contable, quién administra el sistema.
- El sobrino que hizo el sistema anterior — Carlos tiene desconfianza histórica. Importante manejar las expectativas desde el principio.

---

*Caso FerreMax · Cadena de Formación · Semana 2 de 9 · Solo para uso en prácticas del bootcamp*
