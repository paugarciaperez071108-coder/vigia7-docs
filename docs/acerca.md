# Sobre esta web

Esta documentación es la **Práctica 3 del Projecte Intermodular** (1.º de DAM): un sitio web estático hecho con **MkDocs** y el tema **Material**, publicado en **GitHub Pages**.

- **Autor:** Pau García Pérez
- **Tema:** el desarrollo de mi juego, Vigía-7
- **Código fuente:** [repositorio en GitHub](https://github.com/paugarciaperez071108-coder/vigia7-docs)

## Estructura del proyecto

```text
vigia7-docs/
├── mkdocs.yml              ← configuración y menú de navegación
└── docs/
    ├── index.md            ← Inicio
    ├── acerca.md           ← esta página
    ├── historial/          ← historial de versiones (5 páginas)
    ├── nave/               ← la oficina, las cámaras y el final
    ├── personajes/         ← resumen, enemigos, Aberración, Slaimi
    ├── css/extra.css       ← estilos propios
    └── img/                ← todas las imágenes
```

## Elementos de Markdown usados

| Elemento | Dónde se ve |
|---|---|
| Cabeceras, párrafos, **negrita** y *cursiva* | En todas las páginas |
| Imágenes y galerías | [La oficina](nave/oficina.md), [Las cámaras](nave/camaras.md), [Personajes](personajes/enemigos.md) |
| Listas numeradas y con viñetas | [Inicio](index.md), [El final](nave/final.md) |
| Tablas | [Historial](historial/index.md) y sus etapas |
| Bloques de código | [Inicio](index.md), [Historial](historial/index.md), esta página |
| Enlaces internos y externos | En todas las páginas |
| Cajas tipo *awesomebox* (*admonitions*) | En todas las páginas |
| Pestañas | [Los enemigos](personajes/enemigos.md), [La oficina](nave/oficina.md) |
| Teclas | [Inicio](index.md) (++q++, ++e++…) |

## Las cajas (estilo awesomebox)

Material incluye las *admonitions*, que son el equivalente a las cajas de awesomebox. Se escriben así:

```markdown
!!! warning "Título de la caja"
    Texto de dentro, con cuatro espacios de sangría.
```

Estos son todos los tipos que se usan en la web:

!!! note "note"
    Una nota informativa.

!!! info "info"
    Información extra.

!!! tip "tip"
    Un consejo.

!!! success "success"
    Algo que salió bien.

!!! warning "warning"
    Un aviso.

!!! danger "danger"
    Un peligro.

!!! bug "bug"
    Un fallo y cómo se arregló.

!!! example "example"
    Un ejemplo.

!!! quote "quote"
    Una cita.

!!! abstract "abstract"
    Un resumen.

??? question "question (plegable)"
    Con `???` en vez de `!!!` la caja sale cerrada y se abre con un clic.

## Cómo se ha hecho

### 1. Instalar MkDocs y el tema

```bash
pip install mkdocs mkdocs-material
mkdocs --version
```

### 2. Crear el proyecto y verlo en local

```bash
mkdocs new vigia7-docs
cd vigia7-docs
mkdocs serve
```

El servidor está configurado en el puerto 4000 (`dev_addr` en `mkdocs.yml`), así que la web se ve en <http://127.0.0.1:4000/>.

### 3. Configuración (`mkdocs.yml`)

Un trozo de la configuración:

```yaml
site_name: Vigía-7 · Documentación
site_author: Pau García Pérez
theme:
  name: material
  language: es
  palette:
    - scheme: slate      # modo oscuro por defecto
      primary: black
      accent: red
markdown_extensions:
  - admonition           # las cajas
  - pymdownx.tabbed      # las pestañas
  - pymdownx.keys        # las teclas
```

### 4. Subirlo a GitHub

```bash
git init
git add .
git commit -m "Primera versión de la documentación de Vigía-7"
git branch -M main
git remote add origin https://github.com/paugarciaperez071108-coder/vigia7-docs.git
git push -u origin main
```

### 5. Publicarlo en GitHub Pages

```bash
mkdocs gh-deploy
```

Este comando construye la web y la sube a la rama **`gh-pages`**. Después, en el repositorio: **Settings → Pages → Branch: `gh-pages`**.
