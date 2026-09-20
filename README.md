# SOCCEUS · Psicología — Landing Page

Landing page institucional para la sección Psicología de SOCCEUS (Sociedad Científica Cordobesa de Estudiantes de la Salud).

## Stack

- [Next.js 15](https://nextjs.org/) (App Router)
- [TypeScript](https://www.typescriptlang.org/)
- [Tailwind CSS v4](https://tailwindcss.com/)
- [Vercel Analytics](https://vercel.com/analytics)

## Inicio rápido

```bash
# Instalar dependencias
pnpm install

# Servidor de desarrollo
pnpm dev
```

Abrir [http://localhost:3000](http://localhost:3000).

## Estructura

```
socceus-psicologia/
├── app/
│   ├── layout.tsx                        # Layout raíz con metadata
│   ├── page.tsx                          # Landing principal
│   ├── globals.css                       # Estilos globales + tokens
│   └── publicable/
│       ├── [slug]/
│       │   ├── page.tsx                  # Artículo individual
│       │   └── article.css              # Estilos de artículo
│       └── ediciones/
│           └── [edition]/
│               └── page.tsx             # Edición completa (txt → HTML)
├── components/
│   └── ui/
│       └── button.tsx
├── content/
│   ├── edition-1.txt
│   ├── edition-2.txt
│   └── edition-3.txt
├── lib/
│   └── utils.ts
└── public/
    └── icon.svg
```

## Agregar contenido

### Nuevo artículo
Agregar una entrada en el objeto `articles` de `app/publicable/[slug]/page.tsx`.

### Nuevo conversatorio
Agregar un `<Event />` en la sección `#conversatorios` de `app/page.tsx`.

### Nueva edición completa
1. Crear `content/edition-N.txt`
2. Registrarla en el objeto `editions` de `app/publicable/ediciones/[edition]/page.tsx`
3. Agregar tarjeta en la sección archivo de `app/page.tsx`

## Deploy

El proyecto está optimizado para Vercel. Conectar el repo y deployar directamente.
