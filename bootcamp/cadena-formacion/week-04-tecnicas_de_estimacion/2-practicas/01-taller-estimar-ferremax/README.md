# Taller: Estimación de Módulos — FerreMax S.A.S.

## 📋 Descripción

Este taller aplica las **tres técnicas de estimación** vistas en la Semana 4 al caso FerreMax. Trabajarás con un WBS simplificado (versión de práctica) y producirás una tabla de estimación consolidada.

**Duración estimada:** 2.5 – 3 horas  
**Modalidad:** Individual o en parejas (Planning Poker requiere mínimo 2 personas)

---

## 🎯 Lo que lograrás al terminar

- Aplicar T-shirt sizing a una lista de funcionalidades
- Simular una sesión de Planning Poker para un ítem complejo
- Documentar supuestos de estimación
- Producir una tabla de estimación lista para incluir en una propuesta técnica

---

## 📌 Instrucciones generales

1. Lee este README completo antes de empezar
2. Abre `plantilla-estimacion-ferremax.md` — allí completarás cada paso
3. Usa la teoría de las clases como referencia (carpeta `1-teoria/`)
4. Al terminar, verifica el checklist del final de este documento

---

## 📁 Archivos del taller

| Archivo | Descripción |
|---------|-------------|
| `README.md` (este archivo) | Instrucciones del taller |
| `plantilla-estimacion-ferremax.md` | Plantilla guiada para completar |

---

## Paso 1: Revisa el WBS de práctica

El WBS del taller es una versión **simplificada** del caso FerreMax. Tiene 4 módulos (en lugar de 6) para que el taller sea manejable en el tiempo disponible:

```
FerreMax — Sistema de Gestión v1.0 (versión taller)

Módulo A: Autenticación
  A.1  Inicio y cierre de sesión
  A.2  Gestión de usuarios (CRUD)
  A.3  Asignación de roles

Módulo B: Inventario
  B.1  Registro y edición de productos
  B.2  Control de stock (entradas y salidas)
  B.3  Alertas de stock mínimo
  B.4  Sincronización entre sedes (Kennedy ↔ Fontibón)

Módulo C: Ventas
  C.1  Registro de ventas (punto de venta)
  C.2  Historial de ventas con búsqueda
  C.3  Generación de factura electrónica (DIAN)

Módulo D: Reportes
  D.1  Reporte de ventas por período
  D.2  Reporte de stock actual
```

---

## Paso 2: T-Shirt Sizing — Módulos A, B y D

El moderador del taller (o tú mismo si trabajas solo) define la **ancla de referencia**:

> **A.1 Inicio y cierre de sesión = M** (mediano)
> 
> *(Formulario login, validación de credenciales, gestión de sesión JWT, redirección por rol)*

Ahora asigna tallas a los ítems restantes de los módulos **A, B y D** en la plantilla.

**Recordatorio de la escala:**

| Talla | Días estimados |
|-------|---------------|
| XS | 1–2 días |
| S | 3–5 días |
| M | 6–10 días |
| L | 11–20 días |
| XL | 21–35 días |

**Pasos a seguir:**
1. Para cada ítem, pregúntate: ¿Es más simple, igual de complejo o más complejo que A.1 (la referencia M)?
2. Asigna una talla (XS / S / M / L / XL)
3. Elige un número de días dentro del rango de esa talla
4. Escribe en la columna "Razonamiento" por qué elegiste esa talla

---

## Paso 3: Planning Poker — Módulo C (Ventas)

El módulo C tiene el ítem más complejo del taller: **C.3 Factura electrónica**. Aplicarás Planning Poker.

### Si trabajas en pareja o grupo:

1. El moderador lee el ítem:
   > *"El sistema debe generar facturas electrónicas válidas ante la DIAN. Debe integrarse con un PAC (Proveedor Autorizado de Certificación) usando su API. Debe funcionar en ambiente de producción."*

2. Ronda 1: Cada persona elige su carta en secreto y la revela simultáneamente
3. Discuten diferencias (especialmente si hay diferencias de 2+ posiciones en la escala Fibonacci)
4. Ronda 2: Cada persona revisa y propone nuevo número
5. Adoptan el valor de consenso

**Escala Fibonacci disponible:** 1 · 2 · 3 · 5 · 8 · 13 · 21 · ?

**Conversión sugerida:**
- 1–2 puntos → XS (1–2 días)
- 3–5 puntos → S o M (3–8 días)
- 8 puntos → M o L (8–12 días)
- 13 puntos → L (13–20 días)
- 21 puntos → XL (21–30 días)
- ? → más información requerida

### Si trabajas solo:

Documenta **dos perspectivas propias**:
1. Tu estimado "optimista" (mejor caso si todo sale bien)
2. Tu estimado "pesimista" (si hay imprevistos técnicos)
3. Adopta el promedio como estimado final

Para los ítems C.1 y C.2 del Módulo C usa T-shirt sizing normalmente.

---

## Paso 4: Consolidación y tabla final

Con los estimados de los 3 pasos anteriores, completa la tabla de consolidación en la plantilla:

- Agrupa por módulo
- Suma el total de días por módulo
- Suma el total general de esfuerzo
- Documenta el supuesto principal de cada módulo XL

---

## Paso 5: Reflexión

Al final de la plantilla hay 3 preguntas de reflexión. Respóndelas con honestidad — no hay respuesta correcta única, lo importante es el razonamiento.

---

## ✅ Checklist de verificación

Antes de entregar el taller, confirma:

- [ ] Todos los ítems del WBS de práctica tienen talla asignada
- [ ] Cada talla tiene un número de días asociado (dentro del rango)
- [ ] Cada ítem tiene al menos una frase de razonamiento
- [ ] El ítem C.3 tiene registro de las rondas de Planning Poker (o las dos perspectivas si trabajaste solo)
- [ ] La tabla de consolidación suma correctamente
- [ ] Los supuestos de los ítems XL están documentados
- [ ] Las 3 preguntas de reflexión están respondidas

---

## 📚 Referencias

- Teoría semana 4 → `1-teoria/02-tecnicas-cualitativas.md`
- Teoría semana 4 → `1-teoria/03-tshirt-y-planning-poker.md`
- Caso FerreMax completo → `1-teoria/04-caso-ferremax-estimacion.md`
