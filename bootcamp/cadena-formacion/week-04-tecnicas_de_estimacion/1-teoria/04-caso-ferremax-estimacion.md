# FerreMax: Aplicando Técnicas de Estimación

## 🎯 Objetivos de esta clase

- Aplicar las 3 técnicas de estimación al caso FerreMax paso a paso
- Ver cómo los resultados de diferentes técnicas se comparan y se reconcilian
- Producir la tabla de estimación consolidada que alimentará la propuesta técnica

---

## 1. Contexto — ¿Dónde estamos en el proyecto FerreMax?

En la **Semana 3** definimos el alcance del sistema y construimos el WBS. Sabemos exactamente qué módulos y subcomponentes tiene el sistema. Ahora el equipo necesita responder la pregunta del cliente Carlos Mendoza:

> *"¿Cuánto tiempo va a tomar desarrollar esto?"*

El equipo de consultores de FerreMax (Ana, Luis y Camila) decidió aplicar **tres técnicas** para tener un estimado más confiable:

1. **Analogía** — para el módulo más complejo (Inventario)
2. **T-shirt Sizing** — para todos los módulos del WBS
3. **Planning Poker** — para los módulos con más incertidumbre

Al final, reconciliarán los resultados en un **estimado consolidado**.

---

## 2. Recordatorio: WBS de FerreMax (Semana 3)

El sistema tiene 6 módulos principales con los siguientes subcomponentes:

| ID | Módulo / Subcomponente |
|----|------------------------|
| **1** | **Autenticación y Seguridad** |
| 1.1 | Inicio y cierre de sesión |
| 1.2 | Gestión de usuarios |
| 1.3 | Roles y permisos por módulo |
| **2** | **Inventario** |
| 2.1 | Registro y edición de productos |
| 2.2 | Control de stock (entradas/salidas) |
| 2.3 | Sincronización entre sedes |
| 2.4 | Alertas de stock mínimo |
| 2.5 | Integración con lector de barras |
| **3** | **Clientes** |
| 3.1 | Registro y edición de clientes |
| 3.2 | Historial de compras por cliente |
| **4** | **Ventas y Facturación** |
| 4.1 | Registro de ventas (punto de venta) |
| 4.2 | Generación de factura electrónica |
| 4.3 | Historial y búsqueda de ventas |
| **5** | **Reportes** |
| 5.1 | Reporte de ventas por período |
| 5.2 | Reporte de inventario (stock actual) |
| 5.3 | Reporte de productos más vendidos |
| **6** | **Configuración y Documentación** |
| 6.1 | Parámetros del sistema |
| 6.2 | Manual de usuario |
| 6.3 | Capacitación (2 sesiones) |

---

## 3. Técnica 1: Analogía — Módulo de Inventario

El módulo de inventario es el más complejo y el que más riesgo tiene (integración con hardware). Ana busca un proyecto de referencia.

**Proyecto de referencia encontrado:**

> Sistema de inventario para ferretería mediana en Cali — desarrollado en 2022.  
> Duración real del módulo: **47 días hábiles** (2 desarrolladores).  
> No tenía integración con lectores de barras ni sincronización multisede.

**Comparativa de diferencias:**

| Aspecto | Proyecto referencia (Cali) | FerreMax |
|---------|---------------------------|---------|
| Registro de productos | ✅ Incluido | ✅ Incluido |
| Control de stock (entradas/salidas) | ✅ Incluido | ✅ Incluido |
| Alertas de stock mínimo | ✅ Incluido | ✅ Incluido |
| Sincronización entre sedes | ❌ No tenía | ✅ Requerida (+20%) |
| Integración lector de barras | ❌ No tenía | ✅ Requerida (+15%) |
| Catálogo de productos en línea | ✅ Tenía | ❌ No aplica (−10%) |

**Cálculo del estimado por analogía:**

```
Base (proyecto Cali):             47 días
Ajuste + sincronización sedes:   + 9.4 días   (+20%)
Ajuste + integración barcode:    + 7.0 días   (+15%)
Ajuste − catálogo en línea:      − 4.7 días   (−10%)

Estimado por analogía =  47 + 9.4 + 7.0 − 4.7 = 58.7 ≈ 59 días
```

**Resultado técnica 1:**  
Módulo de Inventario → **59 días** (por analogía)

**Supuesto clave:** El proyecto de referencia tenía 2 desarrolladores con tecnología similar (Python + MySQL). FerreMax usará Django + PostgreSQL → la diferencia tecnológica es menor, se asume sin ajuste adicional.

---

## 4. Técnica 2: T-Shirt Sizing — Todos los Módulos

El equipo completo (Ana, Luis, Camila) aplica T-shirt sizing a todos los subcomponentes del WBS.

**Ítem de referencia (ancla):** `1.1 Inicio y cierre de sesión = M`  
*(formulario de login + validación + gestión de sesión = complejidad mediana)*

**Tabla de estimación por tallas:**

| ID | Funcionalidad | Talla | Razonamiento |
|----|--------------|-------|-------------|
| 1.1 | Inicio y cierre de sesión | **M** | Referencia. Login + JWT + redirect |
| 1.2 | Gestión de usuarios | **M** | CRUD usuarios + validaciones |
| 1.3 | Roles y permisos | **L** | Múltiples roles, permisos por módulo, interfaz admin |
| 2.1 | Registro y edición de productos | **M** | CRUD + barcode como texto libre |
| 2.2 | Control de stock (entradas/salidas) | **L** | Lógica de movimientos, historial, ajustes |
| 2.3 | Sincronización entre sedes | **XL** | API intermedia, resolución de conflictos, tiempo real |
| 2.4 | Alertas de stock mínimo | **S** | Regla de negocio simple + notificación |
| 2.5 | Integración lector de barras | **L** | Driver lectura + validación + sincronización |
| 3.1 | Registro y edición de clientes | **S** | CRUD simple, pocos campos |
| 3.2 | Historial de compras cliente | **M** | Query optimizado + paginación |
| 4.1 | Punto de venta (registro ventas) | **L** | Flujo complejo: buscar prod → carrito → aplicar descuento → guardar |
| 4.2 | Factura electrónica | **XL** | Integración DIAN (Colombia) — altamente complejo |
| 4.3 | Historial y búsqueda de ventas | **M** | Filtros + exportar + paginación |
| 5.1 | Reporte ventas por período | **M** | Query + gráfico + exportar PDF |
| 5.2 | Reporte stock actual | **S** | Query simple + tabla + exportar |
| 5.3 | Reporte productos más vendidos | **M** | Agregación + ordenamiento + gráfico |
| 6.1 | Parámetros del sistema | **S** | Formulario simple de configuración |
| 6.2 | Manual de usuario | **M** | Redacción + screenshots + formato |
| 6.3 | Capacitación (2 sesiones) | **S** | Preparación + ejecución de 2 sesiones |

**Conversión de tallas a días:**

| Talla | Días estimados | Cantidad de ítems | Subtotal |
|-------|---------------|-------------------|---------|
| XS | 1–2 días | 0 | 0 días |
| S | 3–5 días (media: 4) | 5 ítems | 20 días |
| M | 6–10 días (media: 8) | 8 ítems | 64 días |
| L | 11–20 días (media: 15) | 4 ítems | 60 días |
| XL | 21–35 días (media: 28) | 2 ítems | 56 días |

**Total T-shirt sizing: 200 días de trabajo individual**

> 💡 "Días de trabajo individual" significa que si el módulo XL de sincronización toma 28 días, se refiere a 28 días de un desarrollador. Con 2 desarrolladores trabajando en paralelo, la duración del calendario podría reducirse a ~14 días — esto se analiza en detalle en la Semana 5.

---

## 5. Técnica 3: Planning Poker — Módulos con mayor incertidumbre

Los módulos **XL** generaron más debate en el equipo. El equipo decide hacer Planning Poker en los 2 ítems XL para asegurarse de que el estimado sea confiable.

### Ítem 2.3 — Sincronización entre sedes

**Lectura del ítem:**
> *"El sistema debe sincronizar el inventario entre la sede Kennedy y la sede Fontibón en tiempo real, garantizando que los cambios en una sede se reflejen en la otra en menos de 5 segundos."*

**Primera ronda:**

```
Ana:    [21]
Luis:   [34]    ← valor más alto
Camila: [13]    ← valor más bajo
```

**Discusión de extremos:**
- Camila (13): "Pensé que podría hacerse con una cola de mensajes simple."
- Luis (34): "Una sincronización en menos de 5 segundos con resolución de conflictos es una funcionalidad de nivel enterprise. Hay que cubrir los casos de conexión interrumpida y datos contradictorios."

Tras la discusión, el equipo aclara que "en tiempo real" en el contexto de FerreMax acepta hasta 30 segundos de latencia (el cliente confirmará). Esto reduce la complejidad.

**Segunda ronda:**

```
Ana:    [21]
Luis:   [21]
Camila: [21]
```

**Consenso: 21 puntos** → conversión: XL, ~25 días con la nueva clarificación.

---

### Ítem 4.2 — Factura electrónica

**Lectura del ítem:**
> *"El sistema debe generar facturas electrónicas válidas ante la DIAN usando la API de un proveedor tecnológico autorizado (PAC/PAYROLL)."*

**Primera ronda:**

```
Ana:    [?]     ← no tiene información suficiente
Luis:   [34]
Camila: [21]
```

Ana votó "?" porque no sabe cuál PAC usarán ni si el cliente ya tiene contrato.

**Discusión:**
- El equipo identifica que la factura electrónica requiere: contratar un PAC (proveedor autorizado DIAN), integrar su API, y hacer pruebas en ambiente de certificación.
- Sin saber el PAC, la estimación puede variar entre 15 días (PAC con buena documentación) y 35 días (PAC con soporte deficiente).
- **Decisión del equipo:** Registrar como **supuesto** que se usará Siigo o Alegra (PAC con API bien documentada), y mantener el estimado con esa condición.

**Segunda ronda:**

```
Ana:    [21]
Luis:   [21]
Camila: [13]
```

Tras nueva discusión sobre que Alegra tiene SDK Python: se adopta **21 puntos** → ~25 días.

---

## 6. Consolidación de Estimados

El equipo compara los resultados de las 3 técnicas para los módulos donde aplicaron más de una:

| Módulo | Analogía | T-shirt | Planning Poker | Estimado final |
|--------|----------|---------|---------------|----------------|
| Inventario (completo) | **59 días** | 63 días (sum) | — | **61 días** |
| Sincronización sedes | — | ~28 días | **25 días** | **26 días** |
| Factura electrónica | — | ~28 días | **25 días** | **26 días** |

**Criterio de reconciliación:** Se promedian cuando las técnicas coinciden dentro del 15%. Cuando hay diferencia mayor, se usa el estimado más alto y se documenta como supuesto.

---

## 7. Tabla de Estimación Final — FerreMax S.A.S.

Esta tabla es la que va en la propuesta técnica:

| Módulo | Subcomponente | Talla | Días estimados | Supuestos |
|--------|--------------|-------|---------------|-----------|
| **1. Autenticación** | Inicio/cierre sesión | M | 8 | — |
| | Gestión de usuarios | M | 8 | — |
| | Roles y permisos | L | 15 | Sistema de roles predefinidos (no configurable por usuario) |
| **Subtotal Módulo 1** | | | **31 días** | |
| **2. Inventario** | Registro/edición productos | M | 8 | Barcode como texto libre inicialmente |
| | Control de stock | L | 15 | Incluye historial de movimientos |
| | Sincronización sedes | XL | 26 | Latencia aceptable: hasta 30 segundos |
| | Alertas stock mínimo | S | 4 | Notificación por pantalla (sin email en v1) |
| | Integración lector barras | L | 15 | Driver USB estándar, Linux/Windows |
| **Subtotal Módulo 2** | | | **68 días** | |
| **3. Clientes** | Registro/edición clientes | S | 4 | — |
| | Historial de compras | M | 8 | — |
| **Subtotal Módulo 3** | | | **12 días** | |
| **4. Ventas** | Punto de venta | L | 15 | Sin manejo de múltiples formas de pago en v1 |
| | Factura electrónica | XL | 26 | PAC: Alegra o Siigo con SDK Python disponible |
| | Historial y búsqueda | M | 8 | — |
| **Subtotal Módulo 4** | | | **49 días** | |
| **5. Reportes** | Ventas por período | M | 8 | Exportar a PDF y Excel |
| | Stock actual | S | 4 | — |
| | Productos más vendidos | M | 8 | — |
| **Subtotal Módulo 5** | | | **20 días** | |
| **6. Configuración** | Parámetros del sistema | S | 4 | — |
| | Manual de usuario | M | 8 | Manual en PDF (no sistema de ayuda en línea) |
| | Capacitación | S | 4 | 2 sesiones × 2 horas |
| **Subtotal Módulo 6** | | | **16 días** | |
| | | | | |
| **TOTAL ESFUERZO** | | | **196 días** | Este es esfuerzo total, no duración del calendario |

---

## 8. ¿Qué sigue?

Con estos **196 días de esfuerzo total estimado**, el equipo tiene la información base para:

- **Semana 5:** Convertir días de esfuerzo a duración del calendario (considerando el tamaño del equipo y las dependencias)
- **Semana 6:** Calcular el costo total (días × tarifa diaria por perfil)
- **Semana 7:** Incluir la tabla de estimación en la propuesta técnica

> ⚠️ **Nota pedagógica:** Los números de FerreMax son intencionalmente realistas pero simplificados. En un proyecto real, la integración DIAN puede tomar de 20 a 60 días dependiendo del PAC elegido. Los estimados siempre deben acompañarse de los supuestos documentados.

---

## ✅ Checklist de verificación

Al terminar esta clase, deberías poder:

- [ ] Explicar por qué el equipo aplicó 3 técnicas distintas en vez de una sola
- [ ] Leer la tabla de T-shirt sizing y calcular el total de días
- [ ] Identificar los supuestos asociados a los módulos XL
- [ ] Explicar qué significa "196 días de esfuerzo" vs. "duración del proyecto"
- [ ] Reconocer que los estimados deben actualizarse cuando cambian los supuestos
