# Proyectos y Mantenimientos RD — Sitio Web

Página web de una sola página (one-page) para una empresa de construcción y
mantenimiento en la República Dominicana: **sheetrock, remodelación de fachadas
e interiores, plomería, electricidad, aires acondicionados, cerámica y pisos**.

El sitio es **autónomo**: todo (HTML, estilos y JavaScript) vive en un solo
archivo, `index.html`. No necesita servidor ni base de datos. Lo puedes abrir
con doble clic o publicarlo gratis en GitHub Pages, Netlify, etc.

---

## 🚀 Cómo verlo

- **En tu PC:** abre `index.html` con tu navegador (Chrome, Edge, etc.).
- **Publicado gratis:** sube la carpeta a GitHub Pages, Netlify o Vercel.

---

## ✏️ Qué cambiar antes de publicar (IMPORTANTE)

Casi todo lo personalizable está en **un solo lugar**. Abre `index.html`, baja
hasta el final (sección `<script>`) y busca el bloque **`CONFIG`**:

```js
const CONFIG = {
  whatsapp: '18090000000',              // 👉 tu WhatsApp (1 + 809/829/849 + número)
  telefono: '18090000000',              // 👉 tu teléfono
  telefonoDisplay: '+1 (809) 000-0000', // 👉 cómo se ve en pantalla
  email: 'contacto@proyectosrd.com',    // 👉 tu correo
  facebook: 'https://www.facebook.com/...',   // 👉 tu Facebook (o '#')
  instagram: 'https://www.instagram.com/...'  // 👉 tu Instagram (o '#')
};
```

> El número de WhatsApp y teléfono van **con código de país y SIN el signo “+”
> ni espacios**. Para RD: `1` + `809/829/849` + número.
> Ejemplo: `18091234567`.

Cambiando solo ese bloque, el WhatsApp, el teléfono, el correo y las redes se
actualizan **automáticamente** en toda la página (botones, footer, barra móvil,
botón flotante, formulario).

### Otras cosas que conviene revisar (busca la palabra `REEMPLAZAR`)

| Qué | Dónde |
|-----|-------|
| Dominio real del sitio | etiquetas `canonical`, `og:url`, `og:image`, `sitemap.xml`, `robots.txt` |
| Foto para compartir en WhatsApp/Facebook | crea una imagen `og-image.jpg` de **1200×630px** y súbela a la raíz |
| Estadísticas (años, proyectos, %) | en `index.html`, atributos `data-count` de la sección “¿Por qué elegirnos?” |
| Testimonios | sección “Testimonios” (reemplaza por comentarios reales de clientes) |
| Datos del negocio para Google | bloque `application/ld+json` (dirección, horario, redes) |
| Horario de atención | footer y FAQ |

---

## 🖼️ Cómo poner tus fotos reales

Ahora la galería y la sección de sheetrock muestran **ilustraciones** generadas
por código (mientras consigues fotos). Cuando tengas fotos reales:

1. Crea una carpeta `img/` y guarda ahí tus fotos (de preferencia `.webp` o
   `.jpg` optimizadas, máx. ~300 KB cada una).
2. En la galería, reemplaza un bloque como este:
   ```html
   <div class="scn" data-design="panels" data-pal="navy" role="img" aria-label="..."></div>
   ```
   por una imagen normal:
   ```html
   <img class="scn" src="img/fachada.jpg" alt="Renovación de fachada en Santo Domingo"
        loading="lazy" width="600" height="400">
   ```
3. Usa siempre `alt` (descripción), `loading="lazy"` y `width`/`height` para que
   cargue rápido y se vea bien en Google.

---

## ✅ Mejoras incluidas en esta versión

- **SEO:** título y descripción optimizados, etiquetas para compartir en redes
  (Open Graph/Twitter), datos del negocio para Google (Schema.org
  `HomeAndConstructionBusiness` + `FAQPage`), favicon, `robots.txt` y `sitemap.xml`.
- **Accesibilidad:** enlace “saltar al contenido”, etiquetas de formulario
  correctas, textos para lectores de pantalla, foco visible para teclado,
  y respeto a “reducir movimiento” del sistema.
- **Conversión / más clientes:** barra fija en móvil con **Llamar / WhatsApp**,
  botón de WhatsApp en el hero, sección de **Preguntas Frecuentes**, mensajes de
  confianza junto al formulario y confirmación de envío.
- **Robustez:** el contenido se ve aunque el JavaScript falle, configuración
  centralizada en un solo bloque, y un campo anti-spam en el formulario.

---

## 📁 Archivos

```
index.html        → el sitio completo (HTML + CSS + JS)
favicon.svg       → ícono del sitio
site.webmanifest  → datos para “instalar” el sitio en el celular
robots.txt        → permisos para buscadores
sitemap.xml       → mapa del sitio para Google
README.md         → esta guía
```

---

¿Dudas para editarlo? Todo lo importante está marcado con comentarios dentro de
`index.html` y con la palabra **REEMPLAZAR**.
