# Cronograma Básico y Diagrama de Gantt

## 🎯 Objetivos

- Comprender qué es un cronograma y para qué sirve en una propuesta técnica
- Identificar los componentes de un cronograma: hitos, tareas, dependencias
- Construir un cronograma básico con representación tipo Gantt
- Identificar la ruta crítica del proyecto

---

## 1. ¿Qué es un cronograma de proyecto?

Un **cronograma** es la representación ordenada en el tiempo de todas las actividades del proyecto, indicando cuándo empieza cada una, cuánto dura, a qué otras actividades está vinculada y cuáles son los puntos de control.

En la propuesta técnica, el cronograma le responde al cliente:

> *"¿Cuándo estará listo cada módulo?, ¿cuándo puedo ver algo funcionando?, ¿cuándo estará el sistema completo?"*

Un cronograma bien elaborado:
- Genera confianza en el cliente
- Permite detectar dependencias críticas antes de que causen problemas
- Es la base del contrato de tiempos de entrega

---

## 2. Componentes de un cronograma

### 2.1 Tarea (actividad)

Unidad básica de trabajo planificable. Tiene:
- **Nombre descriptivo** (qué se hace)
- **Duración** (cuánto tiempo toma)
- **Responsable** (quién lo hace)

Ejemplos:
- "Desarrollo del módulo de autenticación" — 19 días — Dev 1
- "Configuración de la base de datos" — 3 días — Dev 2

### 2.2 Hito (milestone)

Punto de control temporal que marca la finalización de una fase o la entrega de un resultado verificable. Los hitos **no duran** — son un momento en el tiempo.

| Hito | Descripción | Criterio de cumplimiento |
|------|-------------|--------------------------|
| H1 | Base de datos y autenticación lista | Módulos 1 y estructura BD en staging |
| H2 | Módulo de inventario entregado | Demo funcional aprobada por cliente |
| H3 | Sistema completo en pruebas | Todos los módulos desplegados en staging |
| H4 | Entrega final | Sistema en producción + capacitación completada |

### 2.3 Dependencia

Restricción de orden entre tareas. Los tipos más comunes:

| Tipo | Notación | Descripción | Ejemplo |
|------|----------|-------------|---------|
| **Finish to Start (FS)** | A → B | B no puede iniciar hasta que A termine | Login debe estar antes que módulo de ventas |
| **Start to Start (SS)** | A ‖ B | B puede iniciar cuando A inicia | Documentación puede iniciar cuando empieza el desarrollo |
| **Finish to Finish (FF)** | A ═ B | B no puede terminar hasta que A termine | Pruebas terminan cuando desarrollo termina |

Para proyectos del nivel de este bootcamp, usamos principalmente **Finish to Start (FS)** — el tipo más común.

### 2.4 Ruta crítica

La **ruta crítica** es la cadena más larga de tareas dependientes cuyo retraso impacta directamente la fecha de entrega total del proyecto.

> **Regla clave:** Cualquier retraso en una tarea de la ruta crítica retrasa el proyecto completo en la misma cantidad de días.

Las tareas que **no** están en la ruta crítica tienen **holgura** (float o slack) — pueden retrasarse un poco sin afectar la entrega total.

---

## 3. El Diagrama de Gantt

El **diagrama de Gantt** es la representación visual más usada para cronogramas de proyectos. Fue creado por Henry Gantt en 1917 y sigue siendo el estándar en gestión de proyectos.

### Estructura:

```
Módulo / Tarea             | Sem 1 | Sem 2 | Sem 3 | Sem 4 | Sem 5 |
---------------------------|-------|-------|-------|-------|-------|
1. Autenticación           |▓▓▓▓▓▓▓▓▓▓▓|       |       |       |
   1.1 Login/logout        |▓▓▓▓▓▓▓|    |       |       |       |
   1.2 Gestión usuarios    |       |▓▓▓▓|       |       |       |
   1.3 Roles y permisos    |       |    |▓▓▓▓▓▓▓|       |       |
2. Base de datos           |▓▓▓▓▓▓▓▓▓▓▓|       |       |       |
● Hito: Autenticación OK   |       |    |    ●  |       |       |
3. Inventario              |       |    |       |▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓|
```

Cada barra representa la duración de una tarea. El símbolo ● es un hito.

### Cómo leerlo:

- Las barras de la **misma columna de tiempo** se ejecutan en **paralelo**
- Las barras que empiezan después de que otra termina son **tareas dependientes**
- El hito ● aparece al final de la fase que representa

---

## 4. Construcción de un cronograma — Paso a paso

### Paso 1: Lista todas las tareas del WBS

Usa el WBS de la Semana 3 y los estimados de duración de la Semana 5, teoría 01.

### Paso 2: Identifica dependencias

Pregunta para cada tarea: ¿Hay alguna otra tarea que DEBE completarse antes de que esta pueda iniciar?

**Regla de dependencias en sistemas web típicos:**

```
Base de datos → (todos los módulos dependen de ella)
Autenticación → (todos los módulos requieren login)
Módulos funcionales → pueden ir en paralelo entre sí (si el equipo lo permite)
Integración / reportes → dependen de los módulos funcionales
Pruebas de sistema → dependen de todos los módulos
Despliegue → depende de pruebas de sistema
Capacitación → depende del despliegue
```

### Paso 3: Define hitos y criterios de aceptación

Para cada hito, define qué debe ser verdad para considerar que se cumplió. Sin criterios claros, los hitos son ambiguos.

| Hito | Criterio de aceptación |
|------|------------------------|
| Autenticación y BD lista | Login funciona, roles asignados, BD en staging con datos de prueba |
| Inventario completo | Carlos Mendoza aprueba en demo: registro, stock, alertas, barcode |
| Sistema integrado | Todos los módulos funcionan conectados, sin errores críticos en staging |
| Entrega final | Sistema en producción, capacitación de 2 sesiones completadas |

### Paso 4: Asigna responsables y fechas

Con el equipo definido (2 devs para FerreMax), asigna qué módulo desarrolla cada quien. Considera:
- No sobrecargues a una persona mientras la otra espera
- Balancea la carga: suma total de días por persona debe ser similar

### Paso 5: Identifica la ruta crítica

Traza el camino más largo desde el inicio del proyecto hasta el final. Generalmente incluye: el módulo más complejo + sus dependencias directas.

---

## 5. Herramientas para crear Gantt

| Herramienta | URL / Descarga | Costo |
|-------------|---------------|-------|
| **ProjectLibre** | projectlibre.com | Gratuito, offline |
| **Google Sheets** (plantilla Gantt) | Búsqueda: "plantilla gantt google sheets gratis" | Gratuito |
| **ClickUp (free tier)** | clickup.com | Gratuito hasta ciertos límites |
| **GitHub Projects** | github.com/features/project-planning | Gratuito |
| **Miro (free tier)** | miro.com | Gratuito, online |
| **Diagrams.net (draw.io)** | diagrams.net | Gratuito, offline/online |

> 💡 **Para la propuesta técnica de este bootcamp:** Una tabla Gantt en markdown o Google Sheets es suficiente. La entrega no requiere herramienta de gestión de proyectos, solo una representación visual clara.

---

## 6. Gantt en formato Markdown

Para documentos de propuesta técnica, se puede usar una tabla Markdown como Gantt simplificado:

```markdown
| Módulo | S1 | S2 | S3 | S4 | S5 | S6 | S7 | S8 |
|--------|----|----|----|----|----|----|----|----|
| BD + Arquitectura | ██ | ██ |    |    |    |    |    |    |
| Autenticación     |    | ██ | ██ |    |    |    |    |    |
| Inventario        |    |    | ██ | ██ | ██ |    |    |    |
| Clientes          |    |    |    | ██ |    |    |    |    |
| Ventas            |    |    |    | ██ | ██ |    |    |    |
| Reportes          |    |    |    |    |    | ██ |    |    |
| Pruebas integrac. |    |    |    |    |    | ██ | ██ |    |
| Despliegue        |    |    |    |    |    |    | ██ |    |
| Capacitación      |    |    |    |    |    |    |    | ██ |
```

Los caracteres `██` representan semanas activas de trabajo en ese módulo.

---

## 7. Lo que el cronograma NO es

| Mito | Realidad |
|------|---------|
| "El cronograma es una promesa" | Es un plan con supuestos. Los supuestos cambian. |
| "Una vez aprobado no se toca" | Los cronogramas se revisan regularmente (cada sprint o fase) |
| "Debe ser exacto al día" | A nivel de propuesta técnica, precisión de semanas es suficiente |
| "Si hay retraso, el proyecto fracasó" | Los retrasos son normales. Lo importante es comunicarlos y replanificar |

---

## ✅ Checklist de verificación

Antes de pasar a la siguiente clase, verifica que puedes:

- [ ] Definir hito, tarea y dependencia con ejemplos propios
- [ ] Explicar los tipos de dependencia FS, SS, FF
- [ ] Leer un diagrama de Gantt básico e identificar qué va en paralelo y qué en secuencia
- [ ] Identificar la ruta crítica en un cronograma dado
- [ ] Nombrar al menos 2 herramientas gratuitas para crear Gantt

---

## 📚 Recursos adicionales

- PMBok 7ª edición, Sección de "Secuencia de actividades": tipos de dependencias y PDM
- ProjectLibre — Tutorial básico en español (buscar en YouTube: "ProjectLibre tutorial básico español")
- Google Sheets Gantt — Plantilla gratuita de Smartsheet: smartsheet.com/gantt-chart-template
