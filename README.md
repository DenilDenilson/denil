# Denil Portfolio

Portafolio web personal de Denilson Trujillo, construido con Astro y Tailwind
CSS. La interfaz toma inspiración de un editor de código: navegación con rutas
tipo archivo, paneles laterales, secciones plegables y una estética oscura para
presentar experiencia, proyectos y formas de contacto.

## Stack

- Astro 5
- Tailwind CSS 4
- Vite
- Bun como gestor recomendado, indicado por `bun.lock`
- Fuentes Fira Code servidas desde `public/fonts`

## Rutas

- `/`: portada con presentación y enlace a GitHub.
- `/experience`: experiencia profesional.
- `/projects`: galería de proyectos con filtros visuales por tipo de habilidad.
- `/about-me`: perfil personal y secciones sobre trabajo actual/estudios.
- `/contact-me`: datos de contacto, enlaces sociales y formulario visual.
- `/404`: página personalizada para rutas no encontradas.

## Estructura del proyecto

```text
.
├── public/
│   ├── fonts/          # Fuentes locales usadas por la interfaz
│   ├── icons/          # Iconos SVG públicos
│   └── favicon.svg
├── src/
│   ├── assets/         # Imágenes y recursos importados por Astro
│   ├── components/     # Navegación, footer, tarjetas y secciones
│   ├── layouts/        # Layout base compartido por las páginas
│   ├── pages/          # Rutas del sitio
│   └── styles/         # Estilos globales y tokens de Tailwind
├── astro.config.mjs
├── package.json
├── TODO.md
└── tsconfig.json
```

## Requisitos

- Bun instalado, o Node.js si prefieres usar otro gestor compatible con Astro.

## Instalación

```bash
bun install
```

## Scripts

```bash
bun run dev
```

Inicia el servidor de desarrollo local.

```bash
bun run build
```

Genera la versión de producción en `dist/`.

```bash
bun run preview
```

Sirve localmente el build de producción para revisarlo antes de desplegar.

```bash
bun run astro
```

Ejecuta comandos directos de Astro.

## Desarrollo

El layout principal está en `src/layouts/Layout.astro` y carga la navegación, el
footer y los estilos globales. Los colores y la tipografía se definen en
`src/styles/global.css` usando `@theme` de Tailwind CSS.

Las páginas están separadas por ruta en `src/pages`. Los componentes de cada
sección viven en carpetas específicas, por ejemplo:

- `src/components/projects/` para tarjetas, filtros y contenedores de proyectos.
- `src/components/experience/` para bloques plegables de experiencia.
- `src/components/aboutme/` y `src/components/contacme/` para secciones móviles.

## Estado actual

El proyecto ya tiene la estructura base del portafolio, navegación responsive,
estilos globales y páginas principales. Algunas áreas siguen en progreso:

- Las tarjetas de proyectos usan contenido de ejemplo.
- El formulario de contacto es visual y no tiene envío conectado.
- `TODO.md` lista pendientes como recomendaciones, carrusel en "sobre mí" y
  habilidades en experiencia.

## Despliegue

Astro genera un sitio estático por defecto, así que el proyecto puede desplegarse
en servicios como Vercel, Netlify, Cloudflare Pages o GitHub Pages. Antes de
desplegar, ejecuta:

```bash
bun run build
```
