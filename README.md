# PARPA2 — Audiovisual Studio

Sitio del estudio. Guadalajara, MX.

## Estructura

```
parpa2-site/
├── index.html          ← todo el sitio
├── vercel.json
└── assets/images/      ← thumbnails 1600×900
```

## Agregar un proyecto

Todo el contenido vive en el bloque `PROJECTS` dentro de `index.html`,
justo después de la sección `2 · PROYECTOS`. No hace falta tocar HTML ni CSS.

1. Sube el thumbnail (1600×900, <300 KB) a `assets/images/`
2. Copia un bloque y cambia los valores:

```js
{
  category: 'live-shows',        // music-videos | live-shows | live-sessions
  artist:   'Nombre del artista',
  title:    'Título del proyecto',
  year:     2026,
  tag:      'Live Show',         // etiqueta que sale sobre la imagen
  video:    { id: 'ABC123XYZ' }, // o { playlist: 'PL...' }
  image:    'lsh-nombre-archivo.jpg'
},
```

3. Guarda y sube. El sitio se reordena solo: numeración, conteo por
   categoría, rango de años y lista de clientes se calculan automáticamente.

### Destacar un proyecto

Añade `featured: true` y la tarjeta ocupa el ancho completo de su sección.

### Cambiar el reel del hero

En el bloque `CONFIG`, arriba de `PROJECTS`:

```js
heroVideoId: 'ID_DEL_VIDEO'
```

## Deploy

vercel.com → arrastra esta carpeta → Deploy.
