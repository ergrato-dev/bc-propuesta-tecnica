# 💰 Caso FerreMax — Semana 6: Presupuesto y Cotización

> Documento maestro de estimación de costos del proyecto FerreMax.
> Construido a partir de los insumos de la Semana 4 (esfuerzo) y la Semana 5 (cronograma).

---

## Contexto del Caso

**Cliente**: FerreMax S.A.S. — ferretería mediana con 3 puntos de venta en Cali, Colombia  
**Proyecto**: Sistema de Gestión de Inventario, Ventas y Clientes (web, multi-sucursal)  
**Equipo consultor**: 2 desarrolladores independientes (Dev A y Dev B)  
**Base de estimación**: 194 días-persona (Semana 4) · 15 semanas de duración (Semana 5)

---

## Insumos de Semanas Anteriores

| Insumo | Semana | Valor |
|--------|--------|-------|
| Esfuerzo total estimado | S04 | 194 días-persona |
| Duración del proyecto | S05 | 15 semanas (75 días hábiles) |
| Módulos en ruta crítica | S05 | M1 → M4 → M5 |
| Número de desarrolladores | S05 | 2 (al 80% de dedicación) |

---

## Sección A — Recurso Humano

### Perfiles del equipo

| Perfil | Nivel | Tarifa/hora (COP) | Justificación |
|--------|-------|-------------------|---------------|
| Dev A | Semi-senior full-stack | $55,000 | Lidera módulos críticos (autenticación, reportes, ventas) |
| Dev B | Junior+ full-stack | $38,000 | Módulo inventario, configuración, soporte ventas |

> Fuente tarifas: Torre.co · Computrabajo Colombia · Encuesta Stack Overflow 2024. Rango semi-senior: $45k–$70k/h; rango junior+: $28k–$45k/h.

### Distribución del trabajo (días-persona por módulo)

| Módulo | Dev A (días) | Dev B (días) | Total (días-persona) |
|--------|-------------|-------------|----------------------|
| M0 — Inicio y configuración | 5 | 5 | 10 |
| M1 — Autenticación y usuarios | 31 | — | 31 |
| M2 — Inventario | — | 67 | 67 |
| M3 — Clientes y proveedores | 12 | — | 12 |
| M4 — Ventas y facturación | 24 | 24 | 48 |
| M5 — Reportes y dashboard | 20 | — | 20 |
| M6 — Configuración multi-sucursal | — | 16 | 16 |
| **TOTAL** | **92 días** | **112 días** | **204 días** |

> Nota: El total es 204 días-persona (vs. 194 de S04) porque Dev A y Dev B trabajan en paralelo en M0 y M4. Los 194 días son el esfuerzo neto; los 204 incluyen el tiempo calendario con paralelismo. La diferencia de 10 días (~5%) está dentro del margen de contingencia.

### Cálculo de costo de recurso humano

**Dev A:**
```
92 días × 8 horas/día × $55,000/hora = $40,480,000
```

**Dev B:**
```
112 días × 8 horas/día × $38,000/hora = $34,048,000
```

| Perfil | Días | Horas totales | Tarifa | Subtotal RH |
|--------|------|---------------|--------|-------------|
| Dev A (semi-senior) | 92 | 736 | $55,000/h | $40,480,000 |
| Dev B (junior+) | 112 | 896 | $38,000/h | $34,048,000 |
| **Subtotal Sección A** | **204** | **1,632** | | **$74,528,000** |

---

## Sección B — Infraestructura y Servicios

> Costos de servidores, dominio y almacenamiento durante el desarrollo y primer mes productivo (4 meses total).

| Ítem | Especificación | Costo unitario | Cantidad | Subtotal |
|------|----------------|----------------|----------|----------|
| Servidor desarrollo (AWS EC2 t3.micro) | Entorno dev + staging | $90,000/mes | 4 meses | $360,000 |
| Servidor producción (AWS EC2 t3.small) | Entorno producción | $160,000/mes | 1 mes | $160,000 |
| Almacenamiento S3 | Imágenes de productos (~10 GB) | ~$8,000/mes | 4 meses | $32,000 |
| Dominio `.com.co` | Registro anual | $45,000/año | 1 año | $45,000 |
| Certificado SSL | Let's Encrypt (renovación automática) | $0 | — | $0 |
| **Subtotal Sección B** | | | | **$597,000** |

---

## Sección C — Licencias y Software

> Evaluación de necesidad de licencias según stack tecnológico del proyecto.

| Herramienta / Software | Licencia | Costo |
|------------------------|----------|-------|
| Python 3.x | Open source (PSF) | $0 |
| FastAPI / SQLAlchemy | Open source (MIT) | $0 |
| PostgreSQL | Open source (PostgreSQL License) | $0 |
| React.js / Vite | Open source (MIT) | $0 |
| VS Code | Gratuito (Microsoft) | $0 |
| Figma (free tier) | Gratuito hasta 3 proyectos | $0 |
| Git / GitHub (repositorio privado free) | Gratuito | $0 |
| **Subtotal Sección C** | | **$0** |

> ✅ El stack tecnológico de FerreMax es 100 % open source. Sin costos de licencias.

---

## Sección D — Contingencia

> Reserva para cubrir incertidumbre y riesgos identificados durante la ejecución del proyecto.

**Base de cálculo**: Subtotal (A + B + C) antes de contingencia  

```
Base = $74,528,000 + $597,000 + $0 = $75,125,000
Contingencia (10%) = $75,125,000 × 0.10 = $7,512,500
```

**Justificación del 10 %** (y no del 15 % o 20 %):
- Los requisitos están bien documentados (Semana 2)
- El alcance está definido y aceptado (Semana 3)
- El equipo conoce las tecnologías del stack
- Es el primer proyecto juntos → se podría usar 15 %; se optó por 10 % para ser competitivos

| Sección | Subtotal |
|---------|----------|
| A — Recurso humano | $74,528,000 |
| B — Infraestructura | $597,000 |
| C — Licencias | $0 |
| **Base para contingencia** | **$75,125,000** |
| D — Contingencia (10 %) | $7,512,500 |
| **Subtotal costos del proyecto** | **$82,637,500** |

---

## Consolidado del Presupuesto Interno

| Categoría | Monto (COP) | % del total costos |
|-----------|-------------|-------------------|
| A. Recurso humano | $74,528,000 | 90.2 % |
| B. Infraestructura | $597,000 | 0.7 % |
| C. Licencias | $0 | 0 % |
| D. Contingencia (10 %) | $7,512,500 | 9.1 % |
| **Total costos internos** | **$82,637,500** | **100 %** |

---

## Cotización al Cliente

### Cálculo del valor de la propuesta

```
Subtotal costos internos:  $82,637,500
+ Margen de ganancia 20%:  $82,637,500 × 0.20 = $16,527,500
= TOTAL COTIZACIÓN:        $99,165,000
```

> El margen del 20 % cubre la utilidad del negocio y los costos indirectos (overhead) no incluidos en las tarifas por hora (internet, software de gestión, tiempo de ventas).

### Tabla ejecutiva para el cliente

| Concepto | Valor (COP) |
|----------|-------------|
| Desarrollo del sistema completo | $75,000,000 |
| Infraestructura y configuración | $597,000 |
| Soporte y gestión de proyecto | $7,000,000 |
| Reserva y ajustes técnicos | $7,568,000 |
| **TOTAL PROPUESTA** | **$90,165,000** |
| IVA (si aplica) | A convenir |
| **TOTAL con IVA estimado** | **$99,165,000** |

> Nota pedagógica: la tabla ejecutiva no revela tarifas individuales de los desarrolladores. Muestra conceptos agregados comprensibles para el cliente no técnico.

---

## Condiciones Comerciales

| Condición | Detalle |
|-----------|---------|
| Validez de la cotización | 30 días calendario desde la fecha de emisión |
| Forma de pago | 30 % anticipo · 40 % entrega hitos intermedios · 30 % cierre y entrega final |
| Moneda | Pesos colombianos (COP) |
| Ajuste por cambios de alcance | Cualquier cambio debe ser documentado y aprobado con adenda al contrato |
| Revisiones incluidas | Hasta 2 ciclos de revisión por módulo entregado |
| Soporte post-entrega | 30 días de garantía de corrección de defectos sin costo adicional |

---

## Supuestos del Presupuesto

| ID | Supuesto |
|----|----------|
| SP-01 | El cliente proporciona acceso a su red interna en los primeros 5 días hábiles del proyecto. |
| SP-02 | Las tarifas de infraestructura (AWS) son las vigentes en noviembre de 2024; variaciones de precio de hasta 10 % están cubiertas por la contingencia. |
| SP-03 | El cliente realiza revisiones y aprobaciones en máximo 5 días hábiles por entregable; demoras adicionales pueden extender el cronograma y el costo. |
| SP-04 | El stack tecnológico (Python, FastAPI, PostgreSQL, React) es aprobado por el cliente antes del inicio del desarrollo. |
| SP-05 | No se requiere integración con sistemas externos de terceros (ERP, plataformas de pago externas). Integraciones adicionales tienen costo aparte. |

---

## Análisis Comparativo (Referencia para el Cliente)

| Alternativa | Costo estimado | Observación |
|-------------|----------------|-------------|
| SaaS genérico (Siigo, Alegra, etc.) | $1,500,000 – $3,500,000 / año | No cubre multi-sucursal con necesidades específicas de FerreMax |
| Agencia de desarrollo regional (Cali) | $80,000,000 – $130,000,000 | Similar alcance; rango alto del mercado |
| **Esta propuesta** | **$99,165,000 (pago único)** | **Desarrollo a la medida + soporte incluido** |
| Mantenimiento anual (post-proyecto) | $8,000,000 – $12,000,000/año | Estimado para futuras actualizaciones |

> Punto de equilibrio: En 3 años de uso, el sistema a la medida cuesta sobre ~$120M ($99M desarrollo + $21M mantenimiento) vs. $4.5M–$10.5M/año en SaaS. Si el cliente permanece 5+ años, el desarrollo es la opción más económica.

---

## Conexión con Semanas Anteriores y Posteriores

| Semana | Entregable | Relación con S06 |
|--------|------------|------------------|
| S02 | Lista de requisitos funcionales (RF-001 a RF-022) | Requisitos = módulos = insumo de esfuerzo |
| S03 | Alcance definido (WBS + factibilidad) | WBS determinó los módulos; fuera del alcance = fuera del costo |
| S04 | Estimación de esfuerzo (194 días-persona) | Insumo directo para cálculo de costo RH |
| S05 | Cronograma (15 semanas, equipo de 2) | Define tiempo de uso de infraestructura |
| **S06** | **Presupuesto y cotización** | Combina todo para producir el precio final |
| S07 | Propuesta técnica escrita | Incluirá tabla de costos resumida de este documento |
| S08 | Propuesta comercial y condiciones | Formalizará las condiciones de pago aquí definidas |

---

*Cadena de Formación · Tecnólogo ADSO · Caso FerreMax — Semana 6 de 9*
