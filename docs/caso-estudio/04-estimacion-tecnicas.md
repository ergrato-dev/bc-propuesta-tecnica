# FerreMax S.A.S. — Estimación con Técnicas de Estimación

**Versión del documento:** 1.0  
**Semana del bootcamp:** 4 — Técnicas de Estimación  
**Fecha de estimación ficticia:** Marzo 2025  
**Equipo de consultores:** Ana Pérez, Luis Gómez, Camila Torres  
**Cliente:** Carlos Mendoza — FerreMax S.A.S.

> Este documento es la continuación directa de `03-alcance-wbs.md`. Parte del WBS aprobado y produce la tabla de estimación que alimentará el presupuesto (Semana 6) y el cronograma (Semana 5).

---

## 1. Contexto

Con el WBS aprobado por el cliente en la reunión del 14 de febrero de 2025, el equipo de consultores procedió a realizar la estimación del esfuerzo de desarrollo usando tres técnicas complementarias:

1. **Estimación por Analogía** — para el módulo de inventario (el más complejo)
2. **T-Shirt Sizing** — para todos los módulos del WBS
3. **Planning Poker** — para los dos ítems catalogados como XL

La combinación de técnicas reduce el riesgo de sesgo individual y proporciona más confianza en los números presentados al cliente.

---

## 2. Supuestos Generales de la Estimación

Todos los estimados se basan en los siguientes supuestos, acordados por el equipo antes de comenzar:

| ID | Supuesto | Impacto si no se cumple |
|----|----------|------------------------|
| SG-01 | El equipo de desarrollo tendrá 2 desarrolladores full-stack a tiempo completo | Los días se multiplican si hay menos personas o si son part-time |
| SG-02 | El cliente provee acceso a ambas sedes para pruebas durante el desarrollo | Sin acceso, las pruebas de sincronización se retrasan |
| SG-03 | Carlos Mendoza (cliente) está disponible 2 horas por semana para revisiones | Sin disponibilidad, el ciclo de revisión-corrección se alarga |
| SG-04 | Se usará Django 4.x + PostgreSQL + React (stack acordado en Semana 2) | Un cambio de stack reinicia gran parte de la estimación |
| SG-05 | La integración DIAN se hará con Alegra o Siigo (PAC con SDK Python documentado) | Un PAC sin SDK puede duplicar el tiempo de integración |
| SG-06 | La sincronización entre sedes acepta latencia de hasta 30 segundos | Sincronización en tiempo real estricto (<1s) requiere infraestructura diferente |

---

## 3. Técnica 1: Analogía — Módulo de Inventario

### Proyecto de referencia

| Campo | Valor |
|-------|-------|
| Nombre | Sistema de inventario — Distribuidora El Corredor (Cali, 2023) |
| Tipo | Web + escritorio, base de datos centralizada |
| Módulo comparable | Gestión de inventario (registro, stock, alertas) |
| Duración real del módulo | 47 días hábiles (2 desarrolladores) |
| Tecnología | Python + Flask + MySQL |

### Tabla de diferencias y ajustes

| Diferencia | Dirección | Ajuste aplicado | Razonamiento |
|-----------|-----------|----------------|-------------|
| Tec. Django vs Flask | Neutral | 0% | Equipo ya conoce Django (curva ≈ 0) |
| Sincronización entre sedes | Mayor complejidad | +20% | Nueva funcionalidad que implica conflictos de datos |
| Integración lector de barras | Mayor complejidad | +15% | Driver USB + validación + pruebas hardware |
| Catálogo en línea (no aplica) | Menor scope | −10% | El proyecto referencia tenía catálogo para clientes externos |

### Cálculo

```
Base:                           47 días
+ Sincronización entre sedes:   + 9.4 días   (+20%)
+ Integración barcode:          + 7.1 días   (+15%)
− Catálogo en línea:            − 4.7 días   (−10%)

Estimado por analogía:          ≈ 59 días
```

**Resultado Módulo Inventario (por analogía): 59 días**

---

## 4. Técnica 2: T-Shirt Sizing — Todos los Módulos

### Ítem de referencia (ancla)

> **1.1 Inicio y cierre de sesión = M (8 días)**  
> *Formulario login + validación de credenciales + JWT + redirección por rol*

### Tabla de estimación completa

| ID | Funcionalidad | Talla | Días | Razonamiento |
|----|--------------|-------|------|-------------|
| **Módulo 1 — Autenticación** | | | | |
| 1.1 | Inicio y cierre de sesión | M | 8 | Referencia. Login + JWT + redirect |
| 1.2 | Gestión de usuarios (CRUD) | M | 8 | CRUD estándar + validaciones de email |
| 1.3 | Roles y permisos por módulo | L | 15 | 4 roles × 6 módulos = matriz de 24 permisos + UI de administración |
| **Módulo 2 — Inventario** | | | | |
| 2.1 | Registro y edición de productos | M | 8 | CRUD + barcode como campo de texto |
| 2.2 | Control de stock (entradas/salidas) | L | 15 | Historial de movimientos + ajustes manuales + lógica de negocio |
| 2.3 | Sincronización entre sedes | XL | 25* | *Ajustado por Planning Poker (ver Sección 5) |
| 2.4 | Alertas de stock mínimo | S | 4 | Regla simple: if stock < mínimo → notificación en pantalla |
| 2.5 | Integración lector de barras | L | 15 | Driver + validación + pruebas con hardware real |
| **Módulo 3 — Clientes** | | | | |
| 3.1 | Registro y edición de clientes | S | 4 | CRUD con pocos campos, sin lógica compleja |
| 3.2 | Historial de compras por cliente | M | 8 | Query con joins + paginación + filtros de fecha |
| **Módulo 4 — Ventas** | | | | |
| 4.1 | Registro de ventas (punto de venta) | L | 15 | Flujo: buscar → carrito → descuento → stock → guardar |
| 4.2 | Factura electrónica (DIAN) | XL | 25* | *Ajustado por Planning Poker (ver Sección 5) |
| 4.3 | Historial y búsqueda de ventas | M | 8 | Filtros + exportar Excel/PDF + paginación |
| **Módulo 5 — Reportes** | | | | |
| 5.1 | Reporte ventas por período | M | 8 | Query + chart.js + exportar PDF |
| 5.2 | Reporte stock actual | S | 4 | Query simple + tabla + exportar |
| 5.3 | Reporte productos más vendidos | M | 8 | Agregación + ordenamiento DESC + gráfico |
| **Módulo 6 — Configuración** | | | | |
| 6.1 | Parámetros del sistema | S | 4 | Formulario de configuración simple |
| 6.2 | Manual de usuario | M | 8 | Redacción + screenshots + formato PDF |
| 6.3 | Capacitación (2 sesiones) | S | 4 | Preparación + ejecución de 2 sesiones × 2h |

---

## 5. Técnica 3: Planning Poker — Ítems XL

### 5.1 Ítem 2.3 — Sincronización entre sedes

**Historia:**
> *"El sistema debe sincronizar el inventario entre la sede Kennedy y la sede Fontibón, garantizando que los cambios en una sede se reflejen en la otra en un tiempo aceptable para las operaciones del negocio."*

**Ronda 1:**

| Experto | Carta | Supuesto |
|---------|-------|---------|
| Ana | 21 | Asume que "tiempo aceptable" = hasta 60 segundos |
| Luis | 34 | Asume tiempo real estricto < 5 segundos |
| Camila | 13 | Asume sincronización batch cada 5 minutos |

**Discusión:** El equipo consultó con Carlos Mendoza. Conclusión: la sincronización de hasta 30 segundos es aceptable para las operaciones de FerreMax (ventas no son simultáneas entre sedes con frecuencia alta).

**Ronda 2:**

| Experto | Carta revisada |
|---------|---------------|
| Ana | 21 |
| Luis | 21 |
| Camila | 21 |

**Consenso: 21 puntos → 25 días** (escala XL refinada)  
**Supuesto registrado:** Latencia aceptable ≤ 30 segundos. Si el cliente cambia a sincronización en tiempo real estricto, el estimado sube a 40–50 días.

---

### 5.2 Ítem 4.2 — Factura electrónica (DIAN)

**Historia:**
> *"El sistema debe generar facturas electrónicas válidas ante la DIAN usando la API de un Proveedor Autorizado de Certificación (PAC). El cliente ya tiene RUT activo y está obligado a facturar electrónicamente."*

**Ronda 1:**

| Experto | Carta | Supuesto |
|---------|-------|---------|
| Ana | ? | No conoce el PAC específico |
| Luis | 34 | Asume PAC con poca documentación |
| Camila | 21 | Asume Alegra con SDK Python bien documentado |

**Discusión:** El equipo investigó. FerreMax no tiene PAC contratado. El equipo recomendó Alegra (tarifa ~$50.000 COP/mes para PYMES). Carlos Mendoza aceptó evaluar Alegra. Se adopta el supuesto de SDK disponible.

**Ronda 2:**

| Experto | Carta revisada |
|---------|---------------|
| Ana | 21 |
| Luis | 21 |
| Camila | 21 |

**Consenso: 21 puntos → 25 días**  
**Supuesto registrado:** Se usa Alegra o Siigo como PAC con SDK Python. Si el PAC no tiene SDK, el estimado puede subir hasta XL+ (35–45 días).

---

## 6. Tabla Consolidada de Estimación

### Por módulo (esfuerzo total)

| Módulo | Días de esfuerzo |
|--------|-----------------|
| 1 — Autenticación y Seguridad | 31 días |
| 2 — Inventario | 67 días |
| 3 — Clientes | 12 días |
| 4 — Ventas y Facturación | 48 días |
| 5 — Reportes | 20 días |
| 6 — Configuración y Documentación | 16 días |
| **TOTAL ESFUERZO DE DESARROLLO** | **194 días** |

### Reserva de contingencia (recomendada)

| Factor | Porcentaje | Días adicionales |
|--------|-----------|-----------------|
| Riesgos técnicos no previstos | +10% | 19 días |
| Revisiones y ajustes del cliente | +5% | 10 días |
| **Total con contingencia** | | **~223 días** |

---

## 7. Reconciliación Analogía vs. T-Shirt Sizing

Para el Módulo de Inventario, se aplicaron dos técnicas:

| Técnica | Resultado |
|---------|-----------|
| Analogía (Sección 3) | 59 días |
| T-Shirt Sizing (Sección 4) | 67 días (suma subcomponentes) |
| Diferencia | 8 días (~13%) |

La diferencia está dentro del margen de tolerancia del 15%. Se adopta el valor T-Shirt (67 días) por ser más detallado en los subcomponentes. Se documenta la analogía como validación independiente.

---

## 8. Próximos Pasos

Con estos 194 días de esfuerzo estimado:

- **Semana 5:** Distribución del esfuerzo en el calendario (Gantt básico, con equipo de 2 personas). Conversión de días de esfuerzo a duración de proyecto.
- **Semana 6:** Multiplicar días × tarifa diaria por perfil → tabla de costos del proyecto.
- **Semana 7:** Esta tabla aparece en la sección "Estimación de Esfuerzo" de la propuesta técnica.

---

## 9. Historial del documento

| Versión | Fecha | Cambios |
|---------|-------|---------|
| 1.0 | Marzo 2025 | Primera versión — estimación inicial con 3 técnicas |
