# Cronograma del Proyecto — [Nombre de tu Proyecto]

> **Instrucciones generales**: Completa cada sección usando los datos de estimación de tu `entregable-s04-estimacion.md`. Este documento es la Sección 5 de tu propuesta técnica. Usa lenguaje formal y no incluyas información de FerreMax — este documento es sobre tu proyecto real.

---

## 1. Información del Proyecto

| Campo | Valor |
|-------|-------|
| **Nombre del proyecto** | |
| **Aprendiz** | |
| **Ficha** | |
| **Fecha de elaboración** | |
| **Versión del documento** | 1.0 |

---

## 2. Datos de Estimación (viene de S04)

<!-- 📝 Copia aquí el resumen de estimación de tu entregable-s04. Son los insumos para todo lo que sigue. -->

| Módulo | Esfuerzo estimado (días-persona) |
|--------|--------------------------------|
| <!-- Módulo 1 de tu proyecto --> | |
| <!-- Módulo 2 de tu proyecto --> | |
| <!-- Módulo 3 ... (agrega las filas necesarias) --> | |
| **Total** | |

---

## 3. Parámetros del Cronograma

<!-- 📝 Define los supuestos de tu equipo y capacidad. Estos valores los usarás para calcular la duración base.
     Ejemplo: si eres el único desarrollador trabajando 4 horas diarias: Personas = 1, Factor = 50% -->

| Parámetro | Valor | Justificación |
|-----------|-------|--------------|
| Número de personas en el equipo | | |
| Factor de capacidad real | <!-- Ej: 70%, 75%, 80% --> | |
| Días hábiles por semana | <!-- Ej: 5 días --> | |
| Festivos o pausas conocidas | <!-- Ej: "Semana de receso en semana 3" --> | |

---

## 4. Cálculo de Duración

<!-- 📝 Aplica la fórmula de conversión. Muestra los números para que el instructor pueda verificarlos.
     Fórmula: Duración base = Esfuerzo total ÷ (Personas × Factor de capacidad) -->

**Cálculo de duración base:**

```
Duración base = ______ ÷ (______ × ______) = ______ días ≈ ______ semanas
```

**Con buffer del 15%:**

```
Duración con buffer = ______ × 1.15 = ______ días ≈ ______ semanas
```

**Duración total estimada del proyecto:** _____________ semanas

---

## 5. Dependencias entre Módulos

<!-- 📝 Para cada módulo, indica si depende de otro. Esto determina el orden en que se pueden desarrollar.
     Si un módulo requiere que otro esté listo antes, son dependientes (FS = Finish to Start).
     Si pueden hacerse al mismo tiempo, son paralelos. -->

| Módulo | Depende de | ¿Puede ir en paralelo con? |
|--------|-----------|---------------------------|
| <!-- Ej: "Módulo de Login" --> | <!-- "Ninguno — es el primero" o "Módulo X" --> | <!-- "No tiene paralelos" o "Sí, con Módulo Y" --> |
| | | |
| | | |
| | | |

---

## 6. Cronograma — Vista por Semanas (Gantt)

<!-- 📝 Construye el Gantt de tu proyecto. Marca con ██ las semanas en que cada módulo está activo.
     Ajusta el número de semanas según la duración calculada en la Sección 4.
     Ejemplo: si tu proyecto dura 8 semanas, solo necesitas columnas S1 a S8. -->

```
Módulo / Actividad         | S1 | S2 | S3 | S4 | S5 | S6 | S7 | S8 | S9 |S10 |
---------------------------|----|----|----|----|----|----|----|----|----|----|
<!-- Módulo 1 de tu proyecto --> |    |    |    |    |    |    |    |    |    |    |
<!-- Módulo 2 de tu proyecto --> |    |    |    |    |    |    |    |    |    |    |
<!-- Módulo 3 ... --> |    |    |    |    |    |    |    |    |    |    |
<!-- (agrega o quita filas según tus módulos) --> |    |    |    |    |    |    |    |    |    |    |
Pruebas de integración     |    |    |    |    |    |    |    |    |    |    |
Despliegue y capacitación  |    |    |    |    |    |    |    |    |    |    |
```

> 💡 Puedes también construir el cronograma en Google Sheets o ProjectLibre y pegar una imagen aquí con `![Cronograma](cronograma.png)`.

---

## 7. Hitos del Proyecto

<!-- 📝 Define al menos 3 hitos. Un hito es un punto de control que marca el fin de una fase importante.
     El criterio de aceptación responde: "¿Qué debe estar funcionando o entregado para dar este hito por cumplido?"
     Usa criterios verificables — el cliente (o el instructor) debe poder confirmarlos. -->

<!-- Ejemplo:
| H1 | Módulo de autenticación listo | Semana 4 | El usuario final puede iniciar sesión con usuario y contraseña; se pueden crear y eliminar cuentas |
-->

| # | Nombre del hito | Semana estimada | Criterio de aceptación |
|---|----------------|-----------------|------------------------|
| H1 | | | |
| H2 | | | |
| H3 | | | |
| H4 (opcional) | Entrega final | Semana __ | Sistema en funcionamiento, documentación entregada, capacitación completada |

---

## 8. Ruta Crítica

<!-- 📝 Escribe la secuencia de módulos que forman la ruta crítica de tu proyecto.
     La ruta crítica es el camino más largo desde el inicio hasta el fin — cualquier retraso en ella retrasa todo el proyecto. -->

**Ruta crítica identificada:**

```
[Módulo 1] (S?) → [Módulo ?] (S?–S?) → [Módulo ?] (S?–S?) → Pruebas (S?–S?) → Entrega (S?)
```

**Módulo cuello de botella:** ___________________

**Justificación:**  
<!-- Escribe 2–3 oraciones explicando por qué ese módulo es el crítico. ¿Es el de mayor esfuerzo? ¿Bloquea a los demás? -->

---

## 9. Supuestos del Cronograma

<!-- 📝 Lista los supuestos que hiciste para construir este cronograma. Si alguno no se cumple, el cronograma puede cambiar.
     Heredados de S03 y S04: puedes referenciar los que ya documentaste. Agrega los nuevos que apliquen al cronograma. -->

<!-- Ejemplo: "SA-01: El cliente responderá preguntas y revisará entregables en menos de 3 días hábiles." -->

| ID | Supuesto | Impacto si no se cumple |
|----|---------|------------------------|
| SA-01 | | |
| SA-02 | | |
| SA-03 | | |

---

## 10. Resumen del Cronograma para la Propuesta Técnica

<!-- 📝 Esta tabla va directamente en el documento de propuesta técnica que entregarás al cliente.
     Resume el cronograma en fases lógicas con semanas y entregables visibles para el cliente. -->

| Fase | Semanas | Actividades principales | Entregable visible al cliente |
|------|---------|------------------------|-------------------------------|
| Fase 1: <!-- Nombre --> | S1–S? | | |
| Fase 2: <!-- Nombre --> | S?–S? | | |
| Fase 3: <!-- Nombre --> | S?–S? | | |
| Fase 4: Cierre | S?–S? | Pruebas, despliegue, capacitación | Sistema en producción, manual de usuario |

**Duración total del proyecto:** _______ semanas ≈ _______ meses de calendario

---

*Cadena de Formación · Tecnólogo ADSO · Semana 5 de 9*
