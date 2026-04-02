# Alcance del Proyecto y Análisis de Factibilidad

> **Instrucciones**: Completa este documento con la información de **tu proyecto real**.
> No uses información del caso FerreMax — ese es solo para las prácticas.
> Cuando termines, NO deben quedar secciones con `<!-- Completar -->` sin responder.

---

## 1. Información del Proyecto

**Nombre del proyecto:**
**Aprendiz:**
**Ficha:**
**Instructor:**
**Fecha de elaboración:**
**Versión del documento:** S03-v1.0

---

## 2. Declaración de Alcance

### 2.1. In Scope — Versión 1 del Sistema

<!-- 📝 Instrucción: Lista los módulos o funcionalidades que SÍ construirás en la versión 1.
     Sé específico: no escribas solo el nombre del módulo — describe qué hace.
     Ejemplo: "Módulo de autenticación: acceso con usuario y contraseña; roles administrador y operativo"
     Incluye el RF de S02 que cada ítem cubre.
     Mínimo 4 módulos / funcionalidades. -->

| # | Módulo / Funcionalidad | Requisitos S02 que cubre |
|---|----------------------|------------------------|
| 1 | | |
| 2 | | |
| 3 | | |
| 4 | | |

### 2.2. Out of Scope — Versión 1 del Sistema

<!-- 📝 Instrucción: Lista las funcionalidades que NO entrarán en esta versión.
     Justifica brevemente por qué quedan fuera.
     El out of scope protege al consultor: si no está documentado, el cliente puede reclamarlo después.
     Mínimo 3 ítems con justificación. -->

> *Las siguientes funcionalidades no hacen parte del alcance de la versión 1 del sistema. Podrán considerarse para una fase posterior, sujeto a nueva negociación y presupuesto.*

| # | Funcionalidad excluida | Motivo |
|---|----------------------|--------|
| 1 | | |
| 2 | | |
| 3 | | |

---

## 3. Lista de Entregables del Proyecto

<!-- 📝 Instrucción: Lista todos los resultados concretos que el proyecto producirá.
     Incluye tanto módulos de software como documentos.
     La columna "Verificable cuando..." describe cómo sabes que ese entregable está terminado.
     Mínimo 6 entregables: 4 de software y 2 de documentación. -->

| Código | Entregable | Tipo | Verificable cuando... |
|--------|-----------|------|----------------------|
| E-001 | | Software | |
| E-002 | | Software | |
| E-003 | | Software | |
| E-004 | | Software | |
| E-005 | | Documentación | |
| E-006 | | Documentación | |

---

## 4. WBS Básico — Estructura de Desglose del Trabajo

<!-- 📝 Instrucción: Construye el WBS de tu proyecto con 2 niveles.
     Nivel 1 = módulos principales
     Nivel 2 = subcomponentes de cada módulo
     Cada módulo de nivel 1 debe tener entre 2 y 5 subcomponentes.
     Ejemplo:
     
     1. Gestión de Clientes
        1.1 CRUD de clientes (registrar, editar, consultar, inactivar)
        1.2 Búsqueda y filtros de clientes
        1.3 Historial de actividad del cliente
     
     Documenta todos los módulos de tu in scope + un grupo de Documentación. -->

```
[Nombre de tu proyecto]
│
├── 1. [Módulo 1]
│   ├── 1.1 
│   ├── 1.2 
│   └── 1.3 
│
├── 2. [Módulo 2]
│   ├── 2.1 
│   ├── 2.2 
│   └── 2.3 
│
├── 3. [Módulo 3]
│   ├── 3.1 
│   └── 3.2 
│
└── 4. Documentación del Proyecto
    ├── 4.1 Propuesta técnica completa
    ├── 4.2 Diagrama de base de datos
    └── 4.3 Manual de usuario
```

---

## 5. Análisis de Factibilidad

### 5.1. Factibilidad Técnica

<!-- 📝 Instrucción: Evalúa si tienes la tecnología y las habilidades para construir el sistema.
     Para cada criterio, escribe un análisis breve y un resultado: ✅ Viable / ⚠️ Con riesgo / ❌ No viable.
     Sé honesto — si hay algo que no sabes, es mejor documentarlo que ignorarlo. -->

| Criterio | Evaluación | Resultado |
|----------|-----------|-----------|
| Tecnología disponible (frameworks, lenguajes) | | |
| Habilidades del equipo / del aprendiz | | |
| Infraestructura (hosting, servidor, nube) | | |
| Complejidad técnica del sistema propuesto | | |
| Tiempo disponible para el desarrollo | | |

**Conclusión técnica:**

<!-- 📝 Escribe 2-3 oraciones resumiendo si el proyecto es técnicamente viable. -->

### 5.2. Factibilidad Operativa

<!-- 📝 Instrucción: Evalúa si el cliente y sus colaboradores pueden adoptar el sistema.
     Responde cada criterio con un análisis y resultado. -->

| Criterio | Evaluación | Resultado |
|----------|-----------|-----------|
| Disposición del cliente para adoptar el sistema | | |
| Nivel técnico de los usuarios finales | | |
| Equipos disponibles (computadores, dispositivos) | | |
| Conectividad a internet en el punto de uso | | |

**Conclusión operativa:**

<!-- 📝 Escribe 2-3 oraciones sobre si el sistema puede ser adoptado por el cliente. -->

### 5.3. Factibilidad Económica Básica

<!-- 📝 Instrucción: Evalúa si la inversión tiene sentido para el cliente.
     No necesitas calcular el costo exacto aún (lo harás en S05-S06).
     Describe los beneficios esperados y evalúa si justifican la inversión. -->

**Beneficios esperados del sistema:**

| Tipo de beneficio | Descripción concreta |
|------------------|---------------------|
| Ahorro de tiempo | |
| Reducción de errores | |
| Mejor toma de decisiones | |
| Otro beneficio | |

**Conclusión económica:**

<!-- 📝 Escribe 2-3 oraciones sobre si el costo del proyecto se justifica con los beneficios. -->

### 5.4. Conclusión General de Factibilidad

| Tipo | Resultado |
|------|-----------|
| Técnica | |
| Operativa | |
| Económica | |
| **Recomendación** | **[Proceder / Proceder con ajustes / No proceder]** |

---

## 6. Restricciones del Proyecto

<!-- 📝 Instrucción: Lista las condiciones fijas que limitan tu proyecto.
     Una restricción es algo que NO puedes cambiar (plazo, presupuesto máximo, tecnología obligatoria).
     Incluye al menos 2 restricciones con descripción y su impacto en el proyecto. -->

| ID | Restricción | Tipo | Impacto en el proyecto |
|----|------------|------|----------------------|
| R-001 | | Tiempo / Presupuesto / Tecnología / Regulación | |
| R-002 | | | |
| R-003 | | | |

---

## 7. Supuestos del Proyecto

<!-- 📝 Instrucción: Lista las condiciones que asumes como verdaderas para que el proyecto funcione.
     Un supuesto puede cambiar — si cambia, el plan debe revisarse.
     Incluye al menos 2 supuestos con la consecuencia si cambian. -->

| ID | Supuesto | Consecuencia si cambia |
|----|----------|----------------------|
| S-001 | | |
| S-002 | | |
| S-003 | | |

---

## 8. Aprobación del Alcance

<!-- 📝 Este espacio es para que el cliente o instructor valide el alcance antes de continuar.
     En un proyecto real, el cliente firma aquí. En el bootcamp, el instructor lo revisa. -->

| Rol | Nombre | Firma / Aprobación | Fecha |
|-----|--------|-------------------|-------|
| Aprendiz | | | |
| Instructor | | | |
| Cliente (si aplica) | | | |

---

*Semana 03 · Cadena de Formación · Tecnólogo ADSO*
*Documento: Sección 3 de la Propuesta Técnica*
