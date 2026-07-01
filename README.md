# Full Repair SPA — Sitio Web

Sitio web de una sola página (HTML/CSS/JS puro, sin frameworks ni build steps) para
**Full Repair SPA — Servicio Automotriz**, Concepción, Chile.

## Estructura del proyecto

```
fullrepair-web/
├── index.html          → todo el contenido y secciones del sitio
├── css/
│   └── style.css        → estilos (paleta, tipografía, layout, responsive)
├── js/
│   └── script.js         → menú móvil, header al hacer scroll, animaciones
└── assets/
    └── img/               → logo, fotos del taller y promociones
```

No requiere instalación ni dependencias. Es HTML/CSS/JS estático: se abre
directo en el navegador o se publica en cualquier hosting estático (GitHub Pages,
Netlify, Vercel, etc).

## Editar contenido más adelante

- **Textos y secciones** → `index.html` (están comentados por sección: HERO, SERVICIOS, CATÁLOGO, etc.)
- **Colores, tipografía, espaciados** → `css/style.css`, arriba de todo en `:root{ }` (variables `--red`, `--black`, etc.)
- **Nuevas fotos o promociones** → agrégalas a `assets/img/` y referencia el archivo en `index.html`
- **Número de WhatsApp** → aparece varias veces como `https://wa.me/56967235839...`. Si cambia el número, busca y reemplaza `56967235839` en todo `index.html`.

---

## Publicar en GitHub Pages (paso a paso)

### 1. Crear la organización (si aún no la tienes)
1. Ve a [github.com/account/organizations/new](https://github.com/account/organizations/new)
2. Elige el plan gratuito ("Free")
3. Ponle un nombre, por ejemplo `fullrepair-spa`
4. Termina el asistente de creación

### 2. Crear el repositorio
1. Dentro de la organización, click en **New repository**
2. Nombre sugerido: `fullrepair-web` (o `fullrepair-spa.github.io` si quieres que el nombre del repo defina la URL, ver nota abajo)
3. Déjalo en **Public** (GitHub Pages gratuito requiere repo público, salvo plan de pago)
4. No marques "Add README" (ya tienes uno) — click en **Create repository**

### 3. Subir los archivos
Desde tu computador, en la carpeta `fullrepair-web`:

```bash
cd fullrepair-web
git init
git add .
git commit -m "Sitio web Full Repair SPA"
git branch -M main
git remote add origin https://github.com/NOMBRE-ORGANIZACION/fullrepair-web.git
git push -u origin main
```

(Reemplaza `NOMBRE-ORGANIZACION` por el nombre real de tu organización)

Si prefieres no usar la terminal: en la página del repo vacío, click en
**uploading an existing file**, arrastra toda la carpeta y confirma el commit.

### 4. Activar GitHub Pages
1. En el repo, ve a **Settings → Pages**
2. En "Source", selecciona la rama `main` y la carpeta `/ (root)`
3. Guarda. En 1-2 minutos tu sitio queda publicado en:
   `https://NOMBRE-ORGANIZACION.github.io/fullrepair-web/`

> **Nota:** si nombras el repositorio exactamente `NOMBRE-ORGANIZACION.github.io`,
> la URL queda más corta: `https://NOMBRE-ORGANIZACION.github.io/` directamente,
> sin la parte `/fullrepair-web`.

### 5. Dominio propio (opcional, más adelante)
Si más adelante compras un dominio (ej. `fullrepair.cl`), en **Settings → Pages →
Custom domain** puedes apuntarlo al sitio de GitHub Pages.

---

## Checklist antes de publicar

- [ ] Revisar que el WhatsApp, correo e Instagram sean correctos
- [ ] Revisar precios de las promociones (pueden vencer / cambiar)
- [ ] Probar el botón "Cómo llegar" y el mapa
- [ ] Probar el sitio en un celular real, no solo en el computador
