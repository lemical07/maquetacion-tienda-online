# LíShop

LíShop es una tienda en línea estática para mostrar prendas y accesorios. La interfaz utiliza HTML y CSS, con navegación entre las páginas principales de la tienda.

## Estructura del proyecto

```text
.
├── README.md
├── index.html                  Página de bienvenida y entrada a la tienda
├── css/
│   ├── base.css                Estilos globales, reset y elementos comunes
│   ├── component.css           Estilos de portada, categorías y catálogo
│   ├── layout.css              Estructura de navegación y contenido
│   ├── page-components.css     Componentes para formularios, tablas y pedidos
│   ├── pages.css               Composición específica de cada página
│   └── variables.css           Colores, tipografía y medidas reutilizables
├── img/                        Recursos gráficos de la interfaz y el catálogo
└── pages/
    ├── carrito.html            Vista del carrito de compras
    ├── catalogo.html           Catálogo organizado por categorías
    ├── checkout.html           Formulario de finalización de compra
    ├── historial.html          Historial de pedidos
    ├── perfil.html             Perfil y opciones de cuenta
    ├── principal.html          Selección de categorías
    ├── producto.html           Detalles de productos
    └── vacio.html              Vista de opciones aún no disponibles
```

## Tecnologías

- HTML para la estructura y el contenido.
- CSS para el diseño y las interacciones visuales.
- Google Fonts para la tipografía Playfair Display, con Georgia como alternativa.

## Uso

Abre `index.html` en un navegador para recorrer la tienda.

## Alcance

La aplicación es estática y no incluye JavaScript ni un servicio de backend. El carrito, los pagos y la persistencia de datos son vistas de interfaz y no procesan transacciones ni guardan información.
