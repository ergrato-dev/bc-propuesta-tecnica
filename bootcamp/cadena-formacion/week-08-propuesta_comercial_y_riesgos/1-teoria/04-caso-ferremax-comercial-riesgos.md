# 04 — Caso FerreMax: Propuesta Comercial Completa y Matriz de Riesgos

> **Propósito:** Este documento es el modelo de referencia completo para la semana 8. Muestra la sección comercial y la matriz de riesgos del proyecto FerreMax GI tal como se entregaría al cliente. Use este documento como guía para los talleres y como referencia de nivel de calidad esperado.

---

# PROPUESTA TÉCNICA Y COMERCIAL
## Sistema FerreMax GI — Secciones 8 a 12

> *(Las secciones 1 a 7 corresponden al documento elaborado en la Semana 7)*

---

## §8 Tabla de Costos

La inversión total para el desarrollo completo del sistema **FerreMax GI** asciende a **$99,165,000 COP** (noventa y nueve millones ciento sesenta y cinco mil pesos colombianos), correspondientes a los servicios descritos a continuación:

| Categoría | Descripción del servicio | Valor COP |
|---|---|---|
| Desarrollo de software | Ingeniería, programación y pruebas de los 6 módulos del sistema (15 semanas) | $74,528,000 |
| Gestión de proyecto | Coordinación técnica, reuniones de avance semanales, control de versiones y documentación | $8,120,000 |
| Infraestructura en la nube | Servidor AWS EC2 + base de datos RDS — 6 meses de operación inicial | $3,600,000 |
| Licencias de software | Herramientas de desarrollo (Python, React, PostgreSQL — código abierto) | $0 |
| Contingencia (10%) | Reserva para imprevistos técnicos no contemplados en el alcance definido | $8,624,800 |
| Utilidad del proveedor (15%) | Margen de operación sobre el costo total del proyecto | $4,292,200 |
| **TOTAL DEL PROYECTO** | | **$99,165,000 COP** |

> *Todos los valores incluyen IVA. Los precios son válidos hasta el 15 de diciembre de 2024.*

---

## §9 Condiciones Comerciales

### 9.1 Condiciones de Pago

El pago se realizará en tres cuotas, vinculadas a hitos verificables del proyecto:

| Cuota | Porcentaje | Valor COP | Momento de pago | Hito que lo activa |
|---|---|---|---|---|
| Anticipo | 30% | $29,749,500 | Al firmar el contrato | Inicio del proyecto |
| Segundo pago | 40% | $39,666,000 | Semana 6 del proyecto | Aprobación de la demo funcional de módulos M1, M2 y M3 |
| Pago final | 30% | $29,749,500 | Semana 15 del proyecto | Aceptación formal del sistema en producción |
| **Total** | **100%** | **$99,165,000** | | |

El pago podrá realizarse mediante transferencia bancaria, consignación o cualquier otro medio acordado entre las partes. El proveedor emitirá factura de venta por cada cuota recibida.

El retraso en cualquier pago superior a **15 días hábiles** habilitará al proveedor para suspender la ejecución del proyecto hasta regularizar la situación, sin que esto genere penalización al equipo de desarrollo.

### 9.2 Garantía Post-Entrega

El proveedor garantiza la **corrección de errores de programación (bugs)** sin costo adicional durante los **30 días calendario** posteriores a la fecha formal de entrega del sistema en producción.

La garantía **no cubre**:

- Nuevas funcionalidades no contempladas en el alcance original (§5 del documento técnico)
- Errores causados por modificaciones al código realizadas por el cliente o terceros no autorizados
- Problemas de conectividad a internet o fallas de hardware en instalaciones del cliente
- Cambios en normativa externa (DIAN, SuperIndustria, etc.) que requieran ajustes al sistema
- Comportamientos derivados de datos incorrectos ingresados por el cliente durante la operación

Transcurrido el período de garantía, el mantenimiento correctivo y evolutivo se cotizará por separado.

### 9.3 Propiedad Intelectual

La **propiedad intelectual del código fuente**, bases de datos, documentación técnica y demás activos digitales desarrollados exclusivamente para este proyecto será transferida a **FerreMax S.A.S.** una vez recibido el pago total acordado ($99,165,000 COP).

Hasta tanto no se complete el pago total, los activos digitales son propiedad del proveedor (DevSoft ADSO - SENA).

El proveedor se reserva el derecho de re-utilizar **componentes genéricos y librerías de código abierto** que formen parte del sistema, en proyectos con otros clientes, sin comprometer información confidencial de FerreMax S.A.S.

### 9.4 Confidencialidad

El equipo de desarrollo se compromete a no divulgar información confidencial de FerreMax S.A.S. (bases de datos de clientes, precios, proveedores, estrategia comercial) a terceros durante la ejecución del proyecto y por un período de **2 años** posteriores a la entrega final.

### 9.5 Validez de la Oferta

La presente propuesta técnica y comercial tiene validez hasta el **15 de diciembre de 2024** (30 días calendario desde la fecha de emisión). Transcurrida esta fecha sin confirmación formal del cliente, los precios y condiciones podrán ser revisados por el proveedor.

---

## §10 Equipo del Proyecto

*(Ver Sección 9 del documento técnico — Semana 7)*

| Perfil | Rol | Dedicación |
|---|---|---|
| Desarrollador A (Semi-senior) | Líder técnico, backend Python/FastAPI | 80% — 92 días efectivos |
| Desarrollador B (Junior+) | Frontend React, pruebas funcionales | 80% — 112 días efectivos |

---

## §11 Supuestos del Proyecto

*(Ver Sección 10 del documento técnico — Semana 7)*

| ID | Supuesto |
|---|---|
| SP-01 | Las 3 sucursales cuentan con internet ≥5 Mbps |
| SP-02 | El cliente designa representante técnico con disponibilidad ≥2h/semana |
| SP-03 | Los datos en Excel se entregan limpios en la Semana 1 |
| SP-04 | La infraestructura AWS se contrata a nombre de FerreMax S.A.S. |
| SP-05 | Los cambios de alcance generan control de cambios con costo adicional |

---

## §12 Matriz de Riesgos

Los siguientes riesgos fueron identificados en el proceso de análisis previo a la presentación de esta propuesta. La calificación utiliza la escala **Probabilidad × Impacto (P×I)**, donde cada dimensión se valora de 1 a 5.

> El diagrama visual de la matriz se encuentra en `0-assets/01-matriz-riesgos.svg`

![Matriz de riesgos 5×5 — Proyecto FerreMax GI](../0-assets/01-matriz-riesgos.svg)

### Tabla de Riesgos Identificados

| ID | Descripción del riesgo | Categoría | P | I | P×I | Nivel | Estrategia |
|---|---|---|---|---|---|---|---|
| R01 | El cliente solicita cambios en el alcance sin seguir el proceso formal de control de cambios | Gestión | 4 | 4 | 16 | 🔴 Crítico | Mitigar |
| R02 | Un miembro del equipo de desarrollo abandona el proyecto antes de finalizar | Recursos | 2 | 5 | 10 | 🟠 Alto | Mitigar |
| R03 | El cliente no está disponible para validar entregables en el tiempo acordado | Comunicación | 3 | 3 | 9 | 🟠 Alto | Mitigar |
| R04 | Los datos en Excel del cliente tienen errores que complican la migración | Técnico | 3 | 4 | 12 | 🔴 Crítico | Mitigar |
| R05 | Falla en la infraestructura cloud (AWS) durante la etapa de producción | Técnico | 2 | 3 | 6 | 🟡 Medio | Transferir |
| R06 | El cliente incumple alguna cuota de pago acordada | Financiero | 2 | 5 | 10 | 🟠 Alto | Mitigar |
| R07 | Los requisitos levantados en S02 resultan ambiguos o incompletos al iniciar el desarrollo | Técnico | 3 | 4 | 12 | 🔴 Crítico | Mitigar |
| R08 | La estimación de tiempo resulta insuficiente para algún módulo del sistema | Gestión | 2 | 4 | 8 | 🟠 Alto | Mitigar |
| R09 | El rendimiento del sistema es insuficiente con las 3 sucursales operando simultáneamente | Técnico | 2 | 3 | 6 | 🟡 Medio | Mitigar |
| R10 | Cambio en normativa de facturación electrónica DIAN que impacte el módulo de ventas | Externo | 1 | 3 | 3 | 🟢 Bajo | Aceptar |

### Planes de Respuesta Detallados

#### R01 — Cambios de alcance (Crítico 🔴)
**Estrategia:** Mitigar  
**Acción:** Incluir cláusula de control de cambios en el contrato (SP-05). Cualquier solicitud fuera del alcance definido en §5 genera una adendas de oferta formal que debe ser aprobada y pagada antes de ejecutarse. Se realiza revisión del alcance en cada reunión semanal con acta firmada.  
**Responsable:** Desarrollador A (Líder técnico) + cliente

#### R02 — Rotación del equipo (Alto 🟠)
**Estrategia:** Mitigar  
**Acción:** El código se documenta semana a semana con comentarios en inglés y README actualizado. Se practica pair programming en módulos críticos (M2, M4). En caso de retiro, el nuevo desarrollador tendrá acceso a documentación completa. El código se mantiene en GitHub con acceso del cliente como observador.  
**Responsable:** Ambos desarrolladores

#### R03 — Cliente no disponible (Alto 🟠)
**Estrategia:** Mitigar  
**Acción:** Acordar en el contrato que el cliente designa un representante técnico con disponibilidad mínima de 2 horas por semana. Las aprobaciones tienen un plazo máximo de 3 días hábiles. Si no hay respuesta en 3 días, la entrega se considera aprobada y el cronograma avanza. Se documenta en actas de reunión.  
**Responsable:** Desarrollador A + representante FerreMax

#### R04 — Datos Excel con errores (Crítico 🔴)
**Estrategia:** Mitigar  
**Acción:** En la Semana 1 se realiza una auditoría de los archivos Excel del cliente. Se entregará un informe de calidad de datos con los errores encontrados antes de comprometerse con la migración. Si los errores superan el 20% de los registros, se cotizará limpieza de datos como servicio adicional.  
**Responsable:** Desarrollador B

#### R07 — Requisitos ambiguos (Crítico 🔴)
**Estrategia:** Mitigar  
**Acción:** En la Semana 1 del proyecto se realiza taller de validación de requisitos con el cliente (2 horas). Todos los requisitos deben quedar aprobados por escrito (correo o acta) antes de iniciar el desarrollo. Los prototipos de pantalla se presentan en la Semana 2 para validar la comprensión.  
**Responsable:** Ambos desarrolladores

---

## §13 Firma de Aceptación

Al firmar este documento, el cliente y el proveedor expresan su acuerdo con los términos técnicos, comerciales, el alcance definido, el cronograma y los supuestos descritos en esta propuesta.

| Rol | Nombre y cargo | Firma | Fecha |
|---|---|---|---|
| **Cliente** | Andrés Morales — Gerente General, FerreMax S.A.S. | _________________________ | ___/___/___ |
| **Proveedor** | Equipo DevSoft ADSO — SENA Ficha 2847361 | _________________________ | ___/___/___ |

---

> 📌 **Nota para instructores:** Este documento integra el entregable de la Semana 7 (secciones 1–7) con el complemento comercial de la Semana 8 (secciones 8–13). Al final del bootcamp, el aprendiz deberá tener sus versiones de ambos documentos integrados como única propuesta completa para defender en la Semana 9.

*Cadena de Formación · Tecnólogo ADSO · Caso de Estudio FerreMax · Semana 8*
