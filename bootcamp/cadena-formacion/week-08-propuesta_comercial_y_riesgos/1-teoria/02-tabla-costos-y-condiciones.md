# 02 — Tabla de Costos Final y Condiciones Comerciales

## 🎯 Objetivos

- Construir la tabla de costos final para presentar al cliente (sin tarifas internas)
- Establecer condiciones de pago claras con cuotas, porcentajes y momentos
- Redactar las condiciones comerciales básicas: garantía, propiedad intelectual y validez

---

## 1. De Presupuesto a Tabla de Costos Final

En la Semana 6 construiste el **presupuesto detallado** del proyecto: cuántas horas trabaja cada perfil, cuánto cobra por hora, qué se paga de infraestructura y licencias. Ese documento es **interno** — es la base de cálculo del equipo.

La **tabla de costos final** que aparece en la propuesta comercial es diferente: muestra al cliente solo las categorías generales y el total. **Nunca se muestran las tarifas por hora ni los costos internos de operación.**

### ¿Por qué no mostrar las tarifas internas?

| Razón | Explicación |
|---|---|
| Confidencialidad | El cliente no necesita saber cuánto gana cada desarrollador |
| Negociación | Si el cliente ve las tarifas, puede intentar negociar perfil a perfil |
| Margen | La utilidad del proveedor es información empresarial interna |
| Protección | Evita que el cliente contrate directamente a los desarrolladores |

---

## 2. Estructura de la Tabla de Costos Final

La tabla de costos para el cliente se organiza por **categorías de servicio**, no por personas:

| Categoría | Descripción | Ejemplo FerreMax GI |
|---|---|---|
| **Desarrollo de software** | Ingeniería, programación y pruebas de todos los módulos | $74,528,000 |
| **Gestión de proyecto** | Coordinación, reuniones con el cliente, documentación | $8,120,000 |
| **Infraestructura y servicios cloud** | Servidores, base de datos, almacenamiento (6 meses) | $3,600,000 |
| **Licencias de software** | Herramientas de desarrollo (si aplica) | $0 |
| **Contingencia** | Reserva para imprevistos técnicos (10% del desarrollo) | $8,624,800 |
| **Utilidad del proveedor** | Margen de operación sobre el total del proyecto (15%) | $4,292,200 |
| **TOTAL** | | **$99,165,000 COP** |

> ⚠️ **Regla de oro:** El cliente solo ve lo que está en esta tabla. El desglose de tarifas por hora queda en el presupuesto interno (S06).

---

## 3. Cómo Presentar los Montos

Los montos en COP deben estar correctamente formateados. En Colombia se usa:

- **Punto** como separador de miles: `$99.165.000`
- O notación con espacio: `$99 165 000`
- O la forma simplificada en tablas: `$99,165,000`

En documentos técnicos formales se recomienda incluir la abreviatura "COP" para claridad internacional:

```
Total de la inversión: $99,165,000 COP (noventa y nueve millones 
ciento sesenta y cinco mil pesos colombianos)
```

> 💡 Escribir el valor en letras evita ambigüedades y es una práctica recomendada en contratos colombianos.

---

## 4. Condiciones de Pago

Las condiciones de pago especifican **cuándo** y **cuánto** paga el cliente en cada momento. El esquema más usado en proyectos de software de mediana escala en Colombia es **30/40/30**:

| Cuota | Porcentaje | Momento de pago | Propósito |
|---|---|---|---|
| **Anticipo** | 30% | Al firmar el contrato / aceptar la propuesta | Cubre los costos de inicio (análisis, diseño, herramientas de desarrollo) |
| **Pago intermedio** | 40% | Al aprobar la demo de los módulos principales | Valida que el proyecto avanza según lo pactado antes de continuar |
| **Pago final** | 30% | Al recibir el sistema en producción y aceptación formal | Garantiza que el cliente solo paga el 100% cuando tiene el sistema funcionando |

### ¿Por qué este esquema protege a ambas partes?

- **Al proveedor**: El anticipo cubre los costos del equipo desde el primer día. Sin anticipo, el proveedor financia el proyecto con su capital.
- **Al cliente**: No paga el 100% hasta tener el sistema. El 30% final queda "retenido" como garantía de calidad.

### Otros esquemas posibles

| Esquema | Cuotas | Cuándo se usa |
|---|---|---|
| 50/50 | Inicio y entrega final | Proyectos cortos (<8 semanas) |
| 30/30/40 | Inicio, hito intermedio, entrega | Proyectos con 2 fases bien definidas |
| 20/40/40 | Inicio menor, dos pagos grandes | Cuando el cliente tiene flujo de caja limitado |
| Mensual | Cuotas iguales cada mes | Contratos de mantenimiento o SaaS |

---

## 5. Garantía Post-Entrega

La garantía define qué cubre el proveedor después de entregar el sistema:

```
GARANTÍA

El proveedor garantiza la corrección de errores de programación 
(bugs) sin costo adicional durante los 30 días calendario 
posteriores a la fecha de entrega del sistema en producción.

La garantía NO cubre:
- Nuevas funcionalidades no contempladas en el alcance original
- Errores causados por modificaciones del cliente al código fuente
- Problemas de conectividad o infraestructura no suministrada por el proveedor
- Cambios en la legislación que requieran modificaciones al sistema
```

### ¿Cuántos días de garantía ofrecer?

| Tipo de proyecto | Garantía recomendada |
|---|---|
| Sistema simple (1-3 módulos) | 15 días |
| Sistema mediano (4-6 módulos, FerreMax) | 30 días |
| Sistema grande (>7 módulos, integraciones) | 60 días |
| Plataforma crítica (facturación, salud, financiero) | 90 días + SLA |

---

## 6. Propiedad Intelectual

La cláusula de propiedad intelectual define a quién pertenece el código fuente:

```
PROPIEDAD INTELECTUAL

La propiedad intelectual del código fuente, bases de datos, 
documentación técnica y demás activos digitales desarrollados 
durante la ejecución de este proyecto será transferida al cliente 
(FerreMax S.A.S.) una vez realizado el pago total acordado 
($ 99,165,000 COP).

Hasta tanto no se complete el pago total, los activos digitales 
son propiedad del proveedor. El proveedor se reserva el derecho 
de usar los componentes genéricos y reutilizables del código en 
otros proyectos, sin divulgar información confidencial del cliente.
```

> ⚠️ **Importante:** Si el cliente no paga el total, legalmente el código sigue siendo del proveedor. Incluir esta cláusula protege signiferentemente al equipo de desarrollo.

---

## 7. Validez de la Oferta

Todos los precios de una propuesta tienen fecha de vencimiento. Los costos de desarrollo cambian (salarios, inflación, disponibilidad del equipo):

```
VALIDEZ DE LA OFERTA

Esta propuesta técnica y comercial tiene una validez de 30 días 
calendario contados a partir de la fecha de emisión (15 de 
noviembre de 2024). Transcurrido este plazo sin confirmación 
formal del cliente, los precios y condiciones aquí establecidos 
podrán ser revisados.
```

### Plazos de validez comunes

| Duración del proyecto | Validez recomendada de la oferta |
|---|---|
| < 4 semanas | 15 días |
| 1–4 meses | 30 días |
| 4–6 meses | 45 días |
| > 6 meses | 60 días |

---

## 8. Ejemplo Integrado: Sección Comercial de FerreMax GI

A continuación se muestra cómo quedaría la sección comercial integrada en la propuesta:

---

### §8 Tabla de Costos

La inversión total para el desarrollo de FerreMax GI asciende a **$99,165,000 COP** (noventa y nueve millones ciento sesenta y cinco mil pesos colombianos), detallados en la siguiente tabla:

| Categoría | Descripción | Valor COP |
|---|---|---|
| Desarrollo de software | Ingeniería, programación y pruebas (15 semanas) | $74,528,000 |
| Gestión de proyecto | Coordinación, documentación, reuniones de avance | $8,120,000 |
| Infraestructura en la nube | AWS EC2 + RDS — 6 meses iniciales | $3,600,000 |
| Contingencia (10%) | Reserva para imprevistos técnicos | $8,624,800 |
| Utilidad del proveedor (15%) | Margen de operación | $4,292,200 |
| **TOTAL** | | **$99,165,000 COP** |

### §9 Condiciones Comerciales

**9.1 Condiciones de pago**

| Cuota | Porcentaje | Valor COP | Momento |
|---|---|---|---|
| Anticipo | 30% | $29,749,500 | Al firmar el contrato |
| Segundo pago | 40% | $39,666,000 | Al aprobar la demo de módulos M1-M3 (Semana 6) |
| Pago final | 30% | $29,749,500 | Al recibir el sistema en producción (Semana 15) |

**9.2 Garantía**  
Se garantiza la corrección de errores (bugs) durante 30 días calendario post-entrega, sin costo adicional.

**9.3 Propiedad intelectual**  
Los activos digitales se transferirán al cliente al completar el pago total.

**9.4 Validez**  
Esta propuesta tiene validez hasta el 15 de diciembre de 2024.

---

## ✅ Checklist de Verificación

- [ ] La tabla de costos muestra solo categorías generales (no tarifas por hora)
- [ ] El total de la tabla coincide con el presupuesto de la Semana 6
- [ ] Las condiciones de pago tienen porcentajes, montos en COP y momento de pago
- [ ] La propuesta incluye cláusula de garantía con número de días
- [ ] Se incluye cláusula de propiedad intelectual
- [ ] La propuesta tiene fecha de validez explícita

---

*Cadena de Formación · Tecnólogo ADSO · Semana 8 de 9*
