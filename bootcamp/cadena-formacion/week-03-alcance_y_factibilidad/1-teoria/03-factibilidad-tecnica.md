# Análisis de Factibilidad

## 🎯 Objetivos

- Entender qué es la factibilidad y por qué se evalúa antes de iniciar el proyecto
- Aplicar los tres tipos de factibilidad: técnica, operativa y económica básica
- Identificar criterios concretos de evaluación para cada tipo
- Llegar a una conclusión de viabilidad documentada

---

## 1. ¿Qué es la Factibilidad?

Antes de comprometerse a construir un proyecto, hay que hacerse una pregunta honesta: **¿Este proyecto se puede hacer?**

La **factibilidad** es el análisis que responde esa pregunta desde tres ángulos distintos:

| Tipo | Pregunta que responde |
|------|----------------------|
| **Técnica** | ¿Tenemos la tecnología y las habilidades para construirlo? |
| **Operativa** | ¿El cliente puede adoptar y operar el sistema una vez entregado? |
| **Económica** | ¿El proyecto vale la inversión? ¿Tiene sentido financiero? |

> 📌 **¿Por qué es importante evaluar la factibilidad?**
> Comprometerse a construir algo sin analizarlo primero es una de las principales causas de fracaso en proyectos de software. No es suficiente con que el cliente quiera el sistema: el equipo debe poder construirlo, el cliente debe poder usarlo, y el costo debe tener sentido frente al beneficio.

---

## 2. Factibilidad Técnica

La **factibilidad técnica** evalúa si el equipo tiene las herramientas, tecnologías y habilidades necesarias para construir el sistema.

### Criterios para evaluar la factibilidad técnica

| Criterio | Preguntas clave |
|----------|----------------|
| **Tecnología disponible** | ¿Las herramientas o frameworks necesarios existen? ¿Son accesibles (open source o low cost)? |
| **Habilidades del equipo** | ¿El equipo (o el aprendiz) conoce las tecnologías necesarias o puede aprenderlas en el tiempo disponible? |
| **Infraestructura** | ¿Se cuenta con servidor, hosting o servicio de nube para desplegar el sistema? |
| **Complejidad técnica** | ¿El sistema requiere integraciones muy complejas o algoritmos que estén fuera del alcance del equipo? |
| **Tiempo disponible** | ¿El tiempo disponible para desarrollar es suficiente dada la complejidad del sistema? |

### Ejemplo: Factibilidad técnica para sistema web PYME colombiana

| Criterio | Evaluación | Resultado |
|----------|-----------|-----------|
| Tecnología | Python/FastAPI, React o Django — open source, amplia documentación | ✅ Viable |
| Habilidades | El equipo conoce Python y bases de datos relacionales | ✅ Viable |
| Infraestructura | Hosting compartido (~$15.000 COP/mes) o VPS económico | ✅ Viable |
| Complejidad | CRUD + autenticación + reportes básicos — complejidad media | ✅ Viable |
| Tiempo | 16 semanas de desarrollo disponibles para el sistema propuesto | ✅ Viable |

**Conclusión técnica**: El proyecto es técnicamente viable.

### Señales de alerta en factibilidad técnica

- ❌ El sistema requiere inteligencia artificial avanzada, blockchain o tecnologías que el equipo no conoce
- ❌ Se necesita hardware especializado que no está disponible
- ❌ El tiempo de aprendizaje de las tecnologías consumiría la mayor parte del proyecto
- ❌ No hay infraestructura disponible y el cliente no puede costearla

---

## 3. Factibilidad Operativa

La **factibilidad operativa** evalúa si el cliente y sus colaboradores podrán adoptar y operar el sistema una vez entregado. Un sistema que los usuarios no pueden o no quieren usar no aporta valor, aunque técnicamente sea perfecto.

### Criterios para evaluar la factibilidad operativa

| Criterio | Preguntas clave |
|----------|----------------|
| **Disposición del usuario** | ¿Los empleados están dispuestos a cambiar sus procesos actuales? ¿Hay resistencia al cambio? |
| **Nivel técnico del usuario** | ¿Los usuarios finales pueden manejar un sistema web? ¿Necesitan capacitación intensiva? |
| **Equipos disponibles** | ¿La empresa tiene computadores o dispositivos suficientes para usar el sistema? |
| **Conectividad** | ¿Hay acceso a internet estable en los puntos donde se usará el sistema? |
| **Continuidad del negocio** | ¿Se puede implementar el sistema sin interrumpir las operaciones del negocio? |

### Ejemplo: Factibilidad operativa para FerreMax

| Criterio | Evaluación | Resultado |
|----------|-----------|-----------|
| Disposición | Carlos Mendoza está motivado — fue él quien solicitó el sistema | ✅ Favorable |
| Nivel técnico | Los empleados manejan PC y Excel — curva de aprendizaje moderada | ✅ Manejable |
| Equipos | Cada sede tiene 2 computadores — suficiente para el sistema propuesto | ✅ Suficiente |
| Conectividad | Ambas sedes tienen internet de negocio estable | ✅ Adecuada |
| Continuidad | Se puede lanzar primero en una sede (Kennedy) y migrar la otra después | ✅ Viable |

**Conclusión operativa**: El sistema es operativamente viable con capacitación básica al personal.

---

## 4. Factibilidad Económica Básica

La **factibilidad económica** evalúa si la inversión en el proyecto tiene sentido desde el punto de vista financiero. En términos simples: ¿lo que gana el cliente por tener el sistema vale más que lo que le cuesta construirlo?

> ⚠️ **Nota para aprendices**: En proyectos de aprendizaje (proyecto de grado), el objetivo es demostrar que la propuesta tiene sentido económico, no realizar un análisis financiero exhaustivo. Una evaluación razonada de beneficios vs. costo es suficiente.

### Costo estimado del proyecto

El costo del proyecto se calculará en detalle en las Semanas 5 y 6. Para la factibilidad, basta con una estimación de orden de magnitud:

**Componentes típicos de costo para un proyecto de software de aprendizaje:**

| Componente | Costo estimado (COP) |
|-----------|---------------------|
| Horas de desarrollo (X horas × tarifa) | $X.XXX.XXX |
| Infraestructura / hosting (N meses) | $XXX.XXX |
| Licencias de software (si aplica) | $XXX.XXX |
| **Total estimado** | **~$X.XXX.XXX – $XX.XXX.XXX** |

> Para el mercado TI de Colombia (2024-2025), un desarrollador junior-medio cobra entre $25.000 y $60.000 COP/hora.

### Beneficios esperados del sistema

Los beneficios no siempre son directamente monetarios. Incluyen:

| Tipo de beneficio | Ejemplo concreto |
|------------------|-----------------|
| **Ahorro de tiempo** | Registrar un producto demora 2 minutos en sistema vs. 10 minutos en Excel → ahorro de 8 min por transacción |
| **Reducción de errores** | El sistema valida datos — menos errores en inventario que cuestan dinero (mermas, sobrantes) |
| **Mejor toma de decisiones** | Carlos puede ver cuántos tornillos vendió en el último mes — antes no podía |
| **Escalabilidad** | El sistema permite crecer a nuevas sedes sin rehacer todo |
| **Imagen profesional** | La empresa se ve más profesional ante clientes y proveedores |

### Evaluación de viabilidad económica simplificada

Para proyectos de aprendizaje, se usa una evaluación cualitativa:

| Aspecto | Evaluación |
|---------|-----------|
| ¿El costo del proyecto es razonable para la empresa? | Sí / No / Parcialmente |
| ¿Los beneficios justifican la inversión? | Sí / No / A largo plazo |
| ¿La empresa tiene capacidad de pago? | Sí / No / Con financiamiento |
| **Conclusión** | Viable / No viable / Viable con ajustes |

---

## 5. Consolidar el Análisis: Conclusión de Factibilidad

Después de analizar los tres tipos, se consolida una conclusión:

| Tipo | Resultado |
|------|-----------|
| Técnica | ✅ Viable |
| Operativa | ✅ Viable con capacitación |
| Económica | ✅ Viable — beneficios superan costos estimados |
| **Conclusión general** | **El proyecto es viable y se recomienda proceder** |

Si alguno de los tres tipos no es viable, hay dos opciones:
1. **Redefinir el alcance** — hacer un sistema más pequeño que sí sea viable
2. **Comunicar al cliente** — informar que no es conveniente proceder bajo esas condiciones

---

## 6. Dónde Aparece la Factibilidad en la Propuesta Técnica

La sección de factibilidad en la propuesta técnica es breve (1-2 páginas) y va incluida en la misma sección del alcance. Responde tres preguntas:

1. ¿Tenemos la capacidad técnica para construirlo? (factibilidad técnica)
2. ¿El cliente puede operar el sistema? (factibilidad operativa)
3. ¿Vale la inversión? (factibilidad económica básica)

El análisis profundo de costos se documenta en las semanas 5 y 6. Aquí solo se necesita una evaluación de viabilidad inicial.

---

## ✅ Checklist de Comprensión

- [ ] ¿Cuáles son los tres tipos de factibilidad?
- [ ] ¿Por qué es importante analizar la factibilidad operativa (no solo la técnica)?
- [ ] ¿Qué tipos de beneficios puede tener un sistema de software para una PYME?
- [ ] ¿Qué haces si uno de los tres tipos de factibilidad no es viable?
- [ ] ¿En qué semanas se profundiza el análisis económico?

---

*Anterior: [← 02 — Entregables y WBS Básico](./02-entregables-y-wbs-basico.md)*
*Siguiente: [04 — Caso FerreMax: Alcance y Factibilidad →](./04-caso-ferremax-alcance.md)*
