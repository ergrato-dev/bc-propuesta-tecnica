# 📖 Glosario — Semana 02

> **Levantamiento de Requisitos**
> Cadena de Formación · Semana 2 de 9

---

Los términos están ordenados alfabéticamente. Los marcados con ⭐ son los más usados en la semana.

---

## A

### Acta de Reunión ⭐
Documento formal que registra los participantes, temas tratados, acuerdos, compromisos y preguntas pendientes de una reunión. Debe elaborarse dentro de las 24 horas siguientes a la reunión y ser confirmada por el cliente.

**Uso:** Al terminar una entrevista de levantamiento de requisitos, el consultor elabora el acta y la envía al cliente para su validación.

---

### Ambigüedad
Propiedad de un requisito que permite más de una interpretación válida. Un requisito ambiguo genera malentendidos entre el cliente y el equipo de desarrollo.

**Ejemplo de requisito ambiguo:** "El sistema debe ser rápido."
**Cómo resolverlo:** "El sistema debe responder en menos de 3 segundos con conexión 4G."

---

## C

### Categoría de RNF
Clasificación de un requisito no funcional según la característica de calidad que representa. Las categorías principales son: Rendimiento, Seguridad, Usabilidad, Compatibilidad, Disponibilidad y Mantenibilidad.

---

### Consultor / Analista de Requisitos
Profesional que conduce el proceso de levantamiento, análisis y documentación de requisitos. En contextos pequeños, el mismo desarrollador asume este rol.

---

### Cuestionario ⭐
Técnica de levantamiento de requisitos que consiste en un formulario con preguntas predefinidas enviado a múltiples usuarios. Útil cuando hay muchos stakeholders o cuando no es posible reunirse con todos individualmente.

**Herramienta recomendada:** Google Forms (gratuito).

---

## D

### Disponibilidad
Categoría de requisito no funcional que define el tiempo en que el sistema debe estar operativo. Se expresa como porcentaje o como horario concreto.

**Ejemplo:** "El sistema debe estar disponible el 99% del tiempo en horario laboral."

---

## E

### Elicitación de Requisitos
Proceso de descubrir, recopilar y comprender lo que los stakeholders necesitan del sistema. En Colombia se usa más el término "levantamiento de requisitos".

---

### Entrevista ⭐
Conversación estructurada entre el consultor y el cliente o usuario con el objetivo de descubrir necesidades, problemas y expectativas. Es la técnica más usada en proyectos pequeños y medianos.

**Tipos de pregunta:** abiertas (explorar), cerradas (confirmar), de profundización, hipotéticas.

---

## I

### ID de Requisito
Identificador único asignado a cada requisito. El formato estándar es `RF-001`, `RF-002`... para funcionales y `RNF-001`, `RNF-002`... para no funcionales.

**Por qué es importante:** Permite referenciar requisitos específicos en reuniones, correos y documentos sin ambigüedad.

---

## L

### Levantamiento de Requisitos ⭐
Proceso de identificar, recopilar y documentar lo que el cliente y los usuarios necesitan del sistema. Incluye técnicas como entrevista, cuestionario, observación directa y análisis de documentos.

**Sinónimos:** elicitación de requisitos, relevamiento de requisitos (Argentina), toma de requerimientos.

---

## O

### Observación Directa
Técnica de levantamiento que consiste en visitar al cliente y observar cómo trabaja actualmente, sin interrumpirlo. Permite descubrir requisitos implícitos que el cliente no sabe cómo describir.

**Ejemplo FerreMax:** Al observar a Pedro Arias en mostrador, el consultor descubrió que llama a Laura por WhatsApp para confirmar stock — algo que Carlos nunca mencionó.

---

## P

### Prioridad ⭐
Nivel de importancia asignado a un requisito. Define qué se construye primero.

| Prioridad | Significado |
|-----------|-------------|
| **Alta** | Esencial — el sistema no cumple su propósito sin esto |
| **Media** | Importante pero puede esperar a una segunda fase |
| **Baja** | Deseable, no urgente |

> Regla práctica: si el cliente dice "sin eso no me sirve", es prioridad Alta.

---

## R

### Rendimiento
Categoría de requisito no funcional que define la velocidad de respuesta, capacidad de carga y eficiencia del sistema.

**Ejemplo:** "El sistema debe responder a cualquier consulta en menos de 3 segundos."

---

### Requerimiento
Término usado frecuentemente en Colombia como sinónimo de "requisito". Ambos son aceptados; el estándar internacional (IEEE) usa "requisito" o "requirement".

---

### Requisito ⭐
Condición o capacidad que el sistema debe tener para satisfacer la necesidad de un cliente o usuario. Es la unidad básica de documentación de lo que se va a construir.

**Fuente:** Adaptado de IEEE 830-1998.

---

### Requisito Funcional (RF) ⭐
Describe **qué debe hacer** el sistema. Especifica acciones, operaciones o comportamientos que el usuario puede ejecutar.

**Formato:** "El sistema debe [verbo de acción] [objeto] [condición opcional]."
**Ejemplo:** "El sistema debe permitir registrar ventas con producto, cantidad y precio."

---

### Requisito Implícito
Requisito que el cliente da por hecho pero nunca menciona explícitamente. El consultor debe descubrirlo haciendo preguntas "¿Qué pasa si...?"

**Ejemplo FerreMax:** Carlos nunca pidió autenticación con usuario y contraseña, pero es obvio que el sistema no puede dejarse abierto.

---

### Requisito Incompleto
Requisito al que le falta información necesaria para implementarlo sin ambigüedad.

**Ejemplo:** RF: "El sistema debe generar reportes." → ¿De qué? ¿En qué formato? ¿Para quién? ¿Con qué frecuencia?

---

### Requisito No Funcional (RNF) ⭐
Describe **cómo debe comportarse** el sistema en términos de calidad: rendimiento, seguridad, usabilidad, compatibilidad, disponibilidad o mantenibilidad.

**Formato:** Describe una característica medible del sistema, no una acción del usuario.
**Ejemplo:** "El sistema debe funcionar en celulares Android desde la versión 8.0."

---

## S

### Seguridad
Categoría de requisito no funcional que define controles de acceso, autenticación y protección de datos del sistema.

**Ejemplo:** "Solo el usuario con rol Administrador puede modificar los precios del catálogo."

---

### Scope Creep
Fenómeno donde los requisitos crecen descontroladamente durante el proyecto porque el cliente sigue pidiendo cosas nuevas. Se evita documentando bien el alcance desde el inicio (semana 3).

---

## U

### Usabilidad
Categoría de requisito no funcional que define qué tan fácil es usar el sistema para sus usuarios objetivo.

**Ejemplo:** "Un vendedor sin experiencia técnica debe poder registrar una venta en menos de 5 pasos."

---

### Usuario Clave
Stakeholder con conocimiento profundo del proceso del negocio que valida que los requisitos documentados son correctos. En FerreMax: Laura Gómez (Jefa de Bodega).

---

## V

### Validación de Requisitos
Proceso de confirmar con el cliente que los requisitos documentados reflejan correctamente sus necesidades. Se hace enviando el acta o el documento de requisitos para su revisión y firma.

**Importancia:** Un requisito validado y firmado es el respaldo del consultor ante cambios de opinión futuros del cliente.

---

*Cadena de Formación · Tecnólogo ADSO · Semana 2 de 9*

## A

### Acta de Reunión ⭐
Documento que registra formalmente los temas tratados, los acuerdos alcanzados, los compromisos adquiridos y las preguntas pendientes de una reunión de trabajo. Es evidencia del proceso de levantamiento.

**Importancia:** Si en el futuro el cliente dice "yo no pedí eso", el acta confirma lo que se acordó.

---

### Ambigüedad
Condición de un requisito que puede interpretarse de más de una manera. Los requisitos ambiguos son la causa más frecuente de malentendidos entre el cliente y el desarrollador.

**Ejemplo:**
- ❌ Ambiguo: "El sistema debe ser rápido."
- ✅ Claro: "El sistema debe responder en menos de 3 segundos al cargar el inventario."

---

## C

### Cuestionario
Formulario con preguntas predefinidas que se aplica a varios usuarios para recopilar sus necesidades y preferencias. Útil cuando hay muchos usuarios finales con perfiles distintos.

**Diferencia con entrevista:** En el cuestionario no se puede aclarar dudas en el momento.

---

## E

### Elicitación de Requisitos
Sinónimo técnico de *levantamiento de requisitos*. Proceso de descubrir, recopilar y documentar lo que los clientes y usuarios necesitan del sistema.

**Nota:** IEEE y PMI usan el término "elicitación" (del inglés *elicitation*). En el contexto del SENA colombiano es más común decir "levantamiento de requisitos".

---

### Entrevista ⭐
Conversación estructurada entre el consultor y el cliente o usuario para descubrir necesidades, problemas y expectativas. Es la técnica más usada en proyectos pequeños y medianos.

**Tipos de pregunta:**
- **Abierta:** Explora sin restricciones ("¿Cómo funciona hoy el proceso de inventario?")
- **Cerrada:** Confirma un dato específico ("¿Necesita el sistema funcionar en celular?")
- **De profundización:** Ahonda en una respuesta ("¿Con qué frecuencia ocurre ese problema?")

---

## L

### Levantamiento de Requisitos ⭐
Proceso de descubrir, identificar, documentar y validar los requisitos de un sistema de software. Incluye técnicas como entrevistas, cuestionarios y observación directa.

**Resultado esperado:** Un documento con todos los RF y RNF del proyecto, con ID, descripción y prioridad.

---

## O

### Observación Directa
Técnica de levantamiento de requisitos en la que el consultor visita al cliente y observa cómo trabaja actualmente, sin interrumpir. Permite descubrir problemas que el cliente no sabe cómo describir.

**Ejemplo FerreMax:** Al observar cómo Pedro registra una venta, el consultor ve que llama a Laura por WhatsApp cada vez, lo que revela un requisito que Carlos nunca mencionó explícitamente.

---

## P

### Pregunta Hipotética
Tipo de pregunta de entrevista que plantea un escenario imaginado para descubrir requisitos implícitos.

**Ejemplo:** "¿Qué pasa si dos vendedores intentan vender el último producto al mismo tiempo?"

---

### Prioridad ⭐
Clasificación del nivel de importancia de un requisito para determinar qué se construye primero.

| Nivel | Significado |
|-------|-------------|
| **Alta** | El sistema no funciona sin esto — es crítico para resolver el problema principal |
| **Media** | Importante pero el sistema puede funcionar temporalmente sin ello |
| **Baja** | Deseable, puede quedar para una versión futura |

---

## R

### Requisito ⭐
Condición o capacidad que un sistema debe tener o cumplir para satisfacer la necesidad de un cliente o usuario. Base de toda propuesta técnica.

---

### Requisito Funcional (RF) ⭐
Describe **qué debe hacer** el sistema — acciones, operaciones o comportamientos directos.

**Formato estándar:** "El sistema debe [verbo de acción] [objeto] [condición]."

**Ejemplos:**
- RF-001: El sistema debe permitir registrar productos con código, nombre y precio.
- RF-004: El sistema debe generar un reporte de ventas del día en formato PDF.

---

### Requisito Implícito
Requisito que el cliente da por hecho pero nunca menciona explícitamente. Es responsabilidad del consultor descubrirlos mediante preguntas y observación.

**Ejemplo FerreMax:** Carlos nunca dijo que el sistema necesita autenticación con usuario y contraseña — pero es obvio que el inventario no puede ser público.

---

### Requisito Incompleto
Requisito que le falta información para poder implementarlo con certeza.

**Ejemplo:**
- ❌ Incompleto: "El sistema debe generar un reporte."
- ✅ Completo: "El sistema debe generar un reporte de ventas del día en formato PDF, con columnas de producto, cantidad y total."

---

### Requisito No Funcional (RNF) ⭐
Describe **cómo debe comportarse** el sistema en términos de calidad, rendimiento, seguridad u otras características que no son acciones directas del usuario.

**Categorías comunes:** Rendimiento · Seguridad · Usabilidad · Compatibilidad · Disponibilidad

**Ejemplos:**
- RNF-001: El sistema debe responder en menos de 3 segundos con conexión 4G.
- RNF-002: Solo el gerente puede modificar los precios del catálogo. (Seguridad)

---

## S

### Scope Creep
Expansión descontrolada del alcance del proyecto por agregar requisitos nuevos sin evaluar su impacto en el tiempo y costo. Ocurre cuando el cliente sigue pidiendo más cosas durante el desarrollo.

**Cómo prevenir:** Documentar los requisitos formalmente al inicio y usar la reunión de validación para cerrar el alcance.

---

## V

### Validación de Requisitos
Proceso de confirmar con el cliente que los requisitos documentados reflejan correctamente lo que necesita. Se hace compartiendo el documento y pidiendo confirmación escrita.

**Diferencia con verificación:** *Validar* es confirmar con el cliente que documentamos lo correcto. *Verificar* es confirmar que el sistema lo implementó correctamente.

---

*Cadena de Formación · Tecnólogo ADSO · Semana 2 de 9*

