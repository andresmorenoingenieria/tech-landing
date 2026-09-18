# Nexora — Landing Page de Tecnología

Landing page minimalista y de alta calidad para una plataforma tecnológica ficticia, construida con **Astro** y **Tailwind CSS v4**. 100% responsive, accesible y optimizada para rendimiento.

## ✨ Características

- ⚡ **Astro 7** — HTML estático generado al momento del build, sin JavaScript en el cliente salvo el menú móvil.
- 🎨 **Tailwind CSS v4** — Configuración de tema mediante `@theme` en CSS, sin `tailwind.config`.
- 🔤 **Tipografía auto-alojada** — Variable font `Inter` a través de `@fontsource-variable`, sin requests externos.
- ♿ **Accesibilidad** — HTML semántico, `aria` en el menú móvil, `alt` en imágenes, soporte `prefers-reduced-motion` y foco visible.
- 📱 **Responsive** — Mobile-first desde 320 px hasta pantallas grandes, con menú hamburguesa.
- 🔍 **SEO** — Meta tags, Open Graph, Twitter Cards, canonical, JSON-LD y `lang="es"`.
- 🚀 **Listo para Vercel** — Detección automática del framework, sin configuración extra.

## 🚀 Inicio rápido

```bash
# Instalar dependencias
npm install

# Servidor de desarrollo en http://localhost:4321
npm run dev

# Build de producción en ./dist/
npm run build

# Previsualizar el build localmente
npm run preview

# Comprobación de tipos con Astro check
npm run check
```

## 📦 Despliegue en Vercel

### Opción A — Dashboard de Vercel (recomendada)

1. Sube el proyecto a un repositorio de GitHub/GitLab/Bitbucket.
2. Entra en [vercel.com](https://vercel.com) → *Add New → Project*.
3. Importa el repositorio. Vercel detecta **Astro** automáticamente (build: `npm run build`, output: `dist`).
4. Haz clic en **Deploy**. El enlace generado actuará como dominio canónico y raíz de las meta etiquetas automáticamente.

### Opción B — CLI

```bash
npm i -g vercel
vercel        # preview
vercel --prod # producción
```

## 🗂 Estructura del proyecto

```text
/
├── public/
│   ├── favicon.svg       # Favicon de la marca
│   └── og-image.svg      # Imagen para Open Graph / Twitter
├── src/
│   ├── components/       # Secciones de la landing (Header, Hero, Pricing, ...)
│   ├── layouts/
│   │   └── Layout.astro  # Layout base con SEO y fuentes
│   ├── pages/
│   │   └── index.astro   # Página principal
│   └── styles/
│       └── global.css    # Theme de Tailwind v4 y estilos globales
├── astro.config.mjs      # Configuración de Astro + plugin de Tailwind
└── tsconfig.json         # TypeScript estricto
```

## 🎨 Personalización

- **Colores y fuentes**: edita el bloque `@theme` en `src/styles/global.css` (paleta `brand` e `ink`, variable `--font-sans`).
- **Contenido**: cada sección vive en un componente de `src/components/`, con los textos declarados al inicio de su frontmatter.
- **SEO**: ajusta `title` y `description` en `src/layouts/Layout.astro`. La URL canónica y las imágenes de Open Graph se generan automáticamente a partir del dominio de despliegue.

## 🧰 Stack técnico

| Tecnología | Versión | Uso |
| ---------- | ------- | --- |
| Astro | 7.x | Framework de contenido + build |
| Tailwind CSS | 4.x | Estilos utilitarios |
| @tailwindcss/vite | 4.x | Plugin de Vite para Tailwind |
| @fontsource-variable/inter | — | Tipografía auto-alojada |
| TypeScript | 5.x | Tipado estricto |

## ✅ QA

- `npm run build` compila sin errores.
- TypeScript configurado en modo estricto (`astro/tsconfigs/strict`).
- HTML válido, semántico y con encabezados jerárquicos.
- La navegación funciona sin JavaScript (los anclajes son nativos).
- Se respeta `prefers-reduced-motion`.

## 📄 Licencia

MIT# tech-landing
