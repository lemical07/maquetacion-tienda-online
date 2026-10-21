# LíShop — Tienda online de ropa de lujo

Proyecto web estático en **HTML5 y CSS3 puro**. Sin JavaScript, sin frameworks, sin preprocesadores. Única dependencia externa: la fuente *Playfair Display* de Google Fonts. Diseñado **solo para escritorio** (no responsive; `min-width: 1280px`).

## Estructura de carpetas

```
.
├── index.html          Punto de entrada
├── pages/
│   ├── principal.html  Categorías
│   ├── catalogo.html   Catálogo (ofertas + 4 categorías)
│   ├── producto.html   Detalle de productos (anclas por id)
│   ├── carrito.html
│   ├── checkout.html
│   ├── historial.html
│   ├── perfil.html
│   └── vacio.html      Página en construcción
├── css/
│   ├── variables.css   Tokens: colores, fuente, radios, medidas
│   ├── base.css        Reset, estilos globales, título con línea decorativa
│   ├── layout.css      Header, contenedor, barra del catálogo, grids
│   ├── component.css   Estilos locales del catálogo y portada
│   ├── page-components.css  Botones, tabla, formularios y pedidos
│   └── pages.css       Composición propia de cada página
└── img/                Recursos gráficos
```

**Justificación de `pages.css`:** `component.css` queda reservado a piezas reutilizables y `layout.css` a la estructura común; lo que solo existe en una página (portada, detalle de producto, rejilla del checkout, perfil) vive en `pages.css`. No se crearon carpetas adicionales: no hay fuentes locales ni más recursos que justifiquen `assets/` o `fonts/`.

## Instrucciones de uso

1. Abre `index.html` en el navegador (no requiere servidor). Para probar en local con servidor: `python -m http.server` desde la raíz del proyecto.
2. Para ver la fuente necesitas conexión a internet; sin ella se usa Georgia como respaldo.

## Notas de comportamiento (sin JavaScript)

- El detalle de producto usa anclas: `producto.html#chesterfield`. El producto enlazado se resalta con `:target`.
- Los botones "✕" del carrito y "Ver detalles" del historial son decorativos.
- "Confirmar y Pagar" envía el formulario a `historial.html` (GET); la validación `required` es nativa del navegador.
- Al elegir "Pago contra entrega" el campo de tarjeta se atenúa y se bloquea con CSS (`:has()`, navegadores modernos). Sin JS no se puede quitar su obligatoriedad, por eso no lleva `required`.
- Las ofertas del catálogo enlazan al mismo detalle que el producto normal (precio de lista).
- Si prefieres `prefers-reduced-motion`, ya está respetado en `base.css`.

## Imágenes necesarias (carpeta `img/`)

La carpeta compartida contiene **21 imágenes**. La plantilla espera los 62 archivos listados abajo; los recursos de producto que aún no están disponibles conservan sus rutas previstas y no se mostrarán hasta agregar las imágenes con esos nombres.

**Interfaz** (10)

`favicon.png`, `fondo.png`, `logotipo.png`, `carrito.png`, `perfil.png`, `exp-btn.png`, `abrigo.png`, `camisa.png`, `pantalon.png`, `accesorio.png`

**Ofertas** (4)

`of-chesterfield.png`, `of-trench-coat.png`, `of-gurkha-pants.png`, `of-corbata-seda.png`

**Abrigos** (12)

`ab-chesterfield.png`, `ab-inverness-cape.png`, `ab-peacoat-gala.png`, `ab-polo-coat.png`, `ab-trench-coat.png`, `ab-ulster-coat.png`, `ab-crombie.png`, `ab-duffle-coat.png`, `ab-raglan-coat.png`, `ab-guards-coat.png`, `ab-car-coat.png`, `ab-vicuna-overcoat.png`

**Camisas** (12)

`ca-jacquard.png`, `ca-oxford-clasica.png`, `ca-pinpoint-oxford.png`, `ca-popelina-egipcia.png`, `ca-franela-lana.png`, `ca-sea-island-cotton.png`, `ca-chambray.png`, `ca-twill-satinada.png`, `ca-cuello-mao.png`, `ca-cuello-italiano.png`, `ca-doble-puno.png`, `ca-lino-irlandes.png`

**Pantalones** (12)

`pa-calvary-twill.png`, `pa-tuxedo-trousers.png`, `pa-gurkha-pants.png`, `pa-vestir-italiano.png`, `pa-lana-fria.png`, `pa-chino-lujo.png`, `pa-pana.png`, `pa-mezclilla-premium.png`, `pa-palazzo.png`, `pa-pinza.png`, `pa-sarga.png`, `pa-lino-belga.png`

**Accesorios** (12)

`ac-gemelos-oro.png`, `ac-corbata-seda.png`, `ac-panuelo-bolsillo.png`, `ac-cinturon-cuero.png`, `ac-reloj-vestir.png`, `ac-sombrero-fedora.png`, `ac-guantes-cuero.png`, `ac-bufanda-cachemira.png`, `ac-broche-corbata.png`, `ac-cartera-cuero.png`, `ac-baston-cana.png`, `ac-pisacorbatas.png`

Total: **62** archivos.

Las imágenes del carrito, checkout e historial reutilizan las del catálogo y las de ofertas; no hay archivos adicionales.
