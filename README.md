# Sitio web — TerraFix SpA

Página de una sola vista (landing page) hecha en **HTML + CSS + JavaScript puro**.
No necesita servidor, base de datos ni instalar nada: es un sitio "estático", el más simple
y económico de mantener y de subir a internet.

## Estructura

```
terrafix-web/
├── index.html          → toda la página (textos, secciones, estilos y funciones)
├── admin/               → panel de administración para subir fotos/videos sin código
│   ├── index.html
│   └── config.yml
├── content/
│   └── gallery.json     → lista de fotos/videos de la galería (la edita el panel, o tú a mano)
└── assets/
    ├── logo.png                  → logo transparente (usado en menú y pie de página)
    ├── favicon-icon.png          → ícono de la pestaña del navegador
    ├── logo-sticker.png          → versión "sticker" del logo (para redes sociales / impresión)
    ├── galeria-instalacion.jpg
    ├── galeria-pisos.jpg
    ├── galeria-calces.jpg
    ├── galeria-entregada.jpg
    ├── galeria-madera.jpg
    └── galeria-decorativo.jpg    → fotos reales de la presentación en PDF
```

## Cómo verla en tu computador

Solo abre `index.html` haciendo doble clic. Se abre en tu navegador (Chrome, Edge, etc.) tal como se verá en internet.

## Cómo modificar textos

Abre `index.html` con cualquier editor de texto (recomendado: **VS Code**, gratis) y busca el texto
que quieres cambiar — está todo escrito en español, tal como se ve en la página. Por ejemplo,
para cambiar el teléfono, busca `946163281` y `+56 9 4616 3281` (aparecen varias veces: botón de
WhatsApp, teléfono, pie de página).

## Cómo agregar fotos y videos (panel de administración)

Como vas a subir contenido seguido (cada 3 días), dejé la página conectada a un **panel de administración**
propio, gratis, que se usa desde el celular o el computador sin tocar código — parecido a publicar en
una red social. Se llama Decap CMS y funciona así, una vez activado (activación explicada abajo):

1. Entra a `tusitio.netlify.app/admin` (o `tudominio.cl/admin` cuando tengas dominio).
2. Inicia sesión con tu correo.
3. Entra a "Galería del sitio" → "Fotos y videos" → agrega un elemento nuevo: título, descripción corta,
   y la foto o el video.
4. Guarda y publica. En 1-2 minutos el cambio ya está visible en la página para cualquiera que la visite.

**Sobre subir videos:** funciona, pero úsalo solo para videos cortos y livianos (menos de 20 MB aprox.),
porque este panel guarda los archivos dentro del mismo sitio. Para videos más largos o pesados, sigue
usando el link/botón directo a tu TikTok — ahí sí no hay límite y ya está listo en la página.

### Activación del panel (se hace una sola vez)

El panel necesita que el sitio esté conectado a una cuenta de GitHub (gratis) en vez de solo Netlify.
Pasos, todos hechos con clics, sin usar la terminal:

1. Crea una cuenta gratis en https://github.com (si no tienes una).
2. Crea un repositorio nuevo (botón verde "New"), y sube ahí todos los archivos de la carpeta
   `terrafix-web` arrastrándolos a la página de GitHub ("uploading an existing file").
3. En Netlify: "Add new site" → "Import an existing project" → conecta tu cuenta de GitHub → elige
   ese repositorio → "Deploy". Esto reemplaza el método de "arrastrar y soltar" (ya no lo necesitas,
   porque ahora Netlify sigue automáticamente los cambios del repositorio).
4. En el sitio dentro de Netlify: "Site configuration" → "Identity" → "Enable Identity".
5. En esa misma sección: "Enable Git Gateway".
6. En "Identity" → "Invite users", escribe tu propio correo y acéptalo desde el mail que te llega.
7. Entra a `tusitio.netlify.app/admin`, inicia sesión con ese correo, y define tu contraseña. Desde
   ahí ya puedes empezar a subir fotos y videos cuando quieras.

Si prefieres, dime cuando tengas la cuenta de GitHub y Netlify creadas y te ayudo a revisar cada paso.

## Sobre la sección de TikTok

Hoy la sección de TikTok es un botón directo a **@terrafixspa** — funciona de inmediato y no requiere
configuración. Es importante ser honesto sobre esto: **TikTok no ofrece hoy una forma gratuita de
"sincronizar automáticamente" cada video nuevo dentro de una página propia** sin usar una API de pago
o un servicio externo. Lo que sí se puede hacer, y es gratis:

- Dejar el botón directo a tu perfil (ya está listo).
- Si quieres destacar 1 o 2 videos puntuales dentro de la página, TikTok permite "insertar" un video
  específico: en la app de TikTok, abre el video → compartir → "Insertar" (Embed), copia el código,
  y pégalo donde quieras dentro de la sección `#galeria` de `index.html`. Puedo ayudarte a insertar
  cualquier video puntual cuando quieras.

## Cómo funciona el formulario de cotización

El formulario usa **FormSubmit** (formsubmit.co), un servicio gratuito que envía las respuestas
directo a `terrafixspa@gmail.com`, sin necesidad de programar un servidor.

**Importante — activación la primera vez:** apenas alguien complete el formulario por primera vez
después de publicar la página, FormSubmit enviará un correo de confirmación a `terrafixspa@gmail.com`
pidiendo hacer clic en "Confirmar". Desde ese momento todos los envíos futuros llegan directo,
sin pasos adicionales. Si quieres probarlo tú mismo primero, completa el formulario apenas la
página esté publicada.

Mientras tanto, el botón de WhatsApp (arriba a la derecha, flotante abajo a la derecha, y en la
sección de cotización) funciona siempre, sin ninguna configuración.

## Cómo publicarla en internet (gratis)

Como vas a usar el panel de administración para subir fotos y videos seguido, **publica el sitio
conectando GitHub con Netlify** (pasos detallados arriba, en "Activación del panel") en vez del
método antiguo de "arrastrar y soltar". Es prácticamente el mismo esfuerzo, pero además deja
listo el panel.

Si en algún momento decides que no vas a usar el panel y prefieres seguir editando fotos a mano,
sí puedes usar el método simple:
1. Entra a https://app.netlify.com/drop
2. Arrastra la carpeta `terrafix-web` completa a la página.
3. En segundos obtienes un link (ej: `terrafix-spa.netlify.app`) ya funcionando — pero en ese caso
   el panel `/admin` no podrá guardar cambios, porque no queda conectado a un repositorio.

## Cuando compres el dominio (ej: terrafixspa.cl o terrafixspa.com)

1. Compra el dominio en cualquier proveedor (NIC Chile para `.cl`, o GoDaddy/Namecheap para `.com`).
2. En Netlify (o el hosting que uses), ve a "Domain settings" → "Add custom domain" y sigue las
   instrucciones para apuntar el dominio comprado hacia tu sitio.
3. No necesitas volver a subir nada: el sitio sigue siendo el mismo, solo cambia la dirección.

## Cómo promocionarla ya, sin tener dominio propio

No necesitas comprar un dominio para empezar a mostrarla. El plan más simple:

1. **Publícala en Netlify** (ver sección de arriba, "Cómo publicarla en internet"). Netlify te da gratis
   una dirección tipo `nombre-que-elijas.netlify.app` — puedes elegir tú el nombre (ej: `terrafixspa.netlify.app`)
   en "Site settings" → "Change site name". Esa dirección ya es pública y funciona igual que un dominio propio,
   solo que más larga.
2. Comparte ese link en:
   - El estado de WhatsApp Business y en la descripción/catálogo de tu WhatsApp Business.
   - La biografía de tu TikTok (@terrafixspa) e Instagram, si tienes.
   - Tu ficha de Google Business Profile (perfil de empresa en Google Maps) — si aún no la tienes creada, es
     gratis y ayuda mucho a que te encuentren buscando "instalación porcelanato Santiago".
   - El pie de tu cotización en PDF y tu firma de correo.
3. Genera un código QR gratis (hay varios generadores gratuitos en línea) que apunte a ese link, y ponlo en:
   tarjetas de presentación, la camioneta/vehículo de trabajo, o al final de la cotización en PDF.
4. Cuando cotices por WhatsApp, comparte el link junto con tu respuesta — refuerza que eres una empresa formal.

Cuando más adelante compres el dominio con el nombre TerraFix, solo apuntas ese dominio hacia el mismo sitio
en Netlify (paso ya explicado arriba) — el link corto de Netlify puede dejar de usarse, sin perder nada.

## Colores y tipografías usadas (por si quieres ajustarlos)

Todo está definido una sola vez, arriba del archivo `index.html`, dentro de `:root { ... }`:

- Azul TerraFix: `#002F51`
- Naranjo TerraFix: `#F57800`
- Gris TerraFix: `#6E6F6F`
- Tipografía de títulos: Oswald (condensada, técnica)
- Tipografía de texto: Manrope
- Tipografía de datos/etiquetas: IBM Plex Mono

Cambiar cualquiera de estos valores actualiza automáticamente toda la página.
