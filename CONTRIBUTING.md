# 🤝 Guía de Contribución

¡Gracias por tu interés en contribuir al **Bootcamp Propuesta Técnica Zero to Hero**! Este es un proyecto educativo de código abierto dirigido a la comunidad SENA ADSO en Colombia.

---

## 📋 Código de Conducta

Al participar en este proyecto, te comprometes a respetar el [Código de Conducta](CODE_OF_CONDUCT.md). Por favor léelo antes de contribuir.

---

## 🚀 ¿Cómo Contribuir?

### 1. Reportar un Error o Sugerencia

Antes de abrir un issue, verifica que no exista uno similar:

1. Ve a [GitHub Issues](https://github.com/ergrato-dev/bc-propuesta-tecnica/issues)
2. Busca el problema que quieres reportar
3. Si no existe, abre un nuevo issue usando la plantilla correspondiente

**Tipos de issues:**
- 🐛 **Bug**: Error en contenido (dato incorrecto, enlace roto, etc.)
- ✨ **Feature**: Sugerencia de nuevo contenido o mejora
- 📚 **Docs**: Mejora de documentación o redacción
- 🎨 **Design**: Mejora de recursos visuales (SVG, diagramas)

### 2. Hacer una Contribución de Código/Contenido

```bash
# 1. Fork del repositorio en GitHub

# 2. Clonar tu fork
git clone https://github.com/TU_USUARIO/bc-propuesta-tecnica.git
cd bc-propuesta-tecnica

# 3. Crear una rama descriptiva
git checkout -b feat/week-03-ejercicio-wbs
# o
git checkout -b fix/semana02-enlace-roto
# o
git checkout -b docs/mejorar-glosario-semana01

# 4. Hacer tus cambios (ver sección de estándares abajo)

# 5. Commit con Conventional Commits
git add .
git commit -m "feat(week-03): add WBS exercise for fictional case study"

# 6. Push a tu fork
git push origin feat/week-03-ejercicio-wbs

# 7. Abrir un Pull Request en GitHub
```

---

## 📏 Estándares de Commits

Usa [Conventional Commits](https://www.conventionalcommits.org/):

```
<tipo>(<alcance>): <descripción en inglés, imperativo, minúsculas>
```

**Tipos:**

| Tipo | Uso |
|---|---|
| `feat` | Nuevo contenido (ejercicio, teoría, plantilla, semana) |
| `fix` | Corrección de errores en contenido existente |
| `docs` | Mejoras de documentación (README, instrucciones) |
| `style` | Formato, ortografía, sin cambio de contenido |
| `refactor` | Reorganización de carpetas o reestructuración |
| `chore` | Tareas de mantenimiento (.gitignore, configs) |

**Ejemplos:**

```bash
feat(week-01): add theory file for project context
feat(week-05): add estimation spreadsheet template
fix(week-03): correct WBS example in fictional case
docs(readme): update week 4 navigation links
style(glosario): fix typos in week-02 glossary
refactor: rename week folders to standard scheme
chore: update .gitignore with solution folders
```

---

## 📂 Estándares de Contenido

### Nomenclatura de Archivos

- Kebab-case, sin tildes, sin espacios
- Teoría: `01-nombre-del-tema.md`
- Plantillas: `plantilla-nombre.md`
- Entregables: `entregable-nombre.md`
- Glosario: `README.md` dentro de `5-glosario/`

### Estructura de Semana

Toda semana nueva debe seguir la estructura estándar:

```
week-XX-tema_principal/
├── README.md
├── rubrica-evaluacion.md
├── 0-assets/
├── 1-teoria/
├── 2-practicas/
├── 3-proyecto/
│   ├── README.md
│   ├── starter/
│   └── solution/      ← NUNCA se sube al repo (está en .gitignore)
├── 4-recursos/
│   ├── ebooks-free/
│   ├── videografia/
│   └── webgrafia/
└── 5-glosario/
    └── README.md
```

### Idioma

- ✅ Documentación, teoría y guías: **español**
- ✅ Términos técnicos estándar: en su forma internacional (WBS, EDT, KPI, etc.)
- ❌ No mezclar idiomas dentro de un mismo párrafo

### Plantillas para Aprendices

- ✅ Siempre incluir instrucción en comentario HTML: `<!-- 📝 Instrucción: ... -->`
- ✅ Siempre incluir al menos un ejemplo parcialmente resuelto
- ❌ Nunca dejar secciones completamente vacías sin guía

### Recursos Visuales (SVG)

- ✅ Tema dark, sin degradés, paleta #1565C0
- ✅ Fuentes sans-serif (Inter, Roboto, Open Sans, System UI)
- ✅ Todo SVG debe estar vinculado en al menos un archivo de teoría o práctica
- ❌ Sin ASCII art en diagramas

### Caso de Estudio Ficticio

- ✅ Usar **siempre** el caso definido en `docs/caso-estudio/`
- ❌ No inventar casos distintos por semana — la continuidad es clave pedagógica

---

## 📋 Checklist de Pull Request

Antes de abrir un PR verifica:

- [ ] El contenido está en español (documentación y teoría)
- [ ] Se usa el caso de estudio ficticio de `docs/caso-estudio/` (no uno inventado)
- [ ] Las plantillas tienen instrucciones claras y ejemplos (sin secciones vacías)
- [ ] La carpeta `solution/` NO está incluida en el PR
- [ ] Los archivos SVG están vinculados en al menos un `.md`
- [ ] Los commits siguen Conventional Commits
- [ ] El nivel de profundidad es coherente con la versión (OA vs CF)
- [ ] Los entregables encadenan con semanas anteriores y posteriores
- [ ] El README de semana tiene navegación (← anterior / siguiente →)
- [ ] La rúbrica de evaluación tiene los 3 tipos de evidencia (conocimiento/desempeño/producto)

---

## 📋 Áreas donde más se Necesita Ayuda

- ✨ **Ejercicios adicionales** para las prácticas (caso de estudio ficticio)
- 📚 **Mejoras en material teórico** (más ejemplos colombianos, referencias NTC)
- 🎨 **Recursos visuales SVG** (matrices, diagramas de procesos, comparativas)
- 📋 **Plantillas mejoradas** para los entregables del proyecto real
- 🔗 **Recursos en webgrafia/** (enlaces a estándares, herramientas, videos en español)
- 🌐 **Traducción al inglés** del material teórico

---

## ❓ Preguntas

- 💬 [GitHub Discussions](https://github.com/ergrato-dev/bc-propuesta-tecnica/discussions)
- 🐛 [GitHub Issues](https://github.com/ergrato-dev/bc-propuesta-tecnica/issues)

---

_Gracias por contribuir a la educación de la comunidad SENA ADSO 🇨🇴_
