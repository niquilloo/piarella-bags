# Piarella Bags – Tienda web

Tienda en línea de **Industrias Marzzelli Perú Cueros E.I.R.L.** (Piarella Bags): carteras, mochilas, morrales, calzado, correas, billeteras y monederos.

- Un solo archivo: `index.html` (HTML + CSS + JavaScript, sin dependencias, fuentes incrustadas). Se abre con doble clic, también sin internet.
- Diseño v7: estilo minimalista de lujo (marfil, negro, tipografías Cardo e Inter).
- Pedidos por WhatsApp; pago con Yape, Plin o transferencia.
- Logo en `logo/` (logotipo y monograma, en negro y blanco) y `favicon.svg`.

## Panel administrativo (v8)
Entrar a `#/admin` (enlace "Administración" en el pie de página).
- La **primera cuenta** que se registre ahí queda como administradora.
- Productos: crear, editar, ocultar y eliminar; precio, stock, descripción, colores, etiqueta "Nuevo" y **fotos** (se reducen y suben solas).
- Pedidos y reclamos: ver detalle y cambiar su estado. Mensajes de contacto y suscriptores.

## Base de datos (Supabase)
- Proyecto `piarella-bags` (São Paulo). URL y clave pública en el bloque `SB` de `index.html`.
- Tablas: `productos`, `pedidos`, `reclamos`, `mensajes`, `suscriptores`, `admins`. Fotos en el bucket `productos`.
- Seguridad con RLS: el público solo ve productos visibles; solo el administrador ve pedidos y edita.
- Los pedidos se crean con la función `crear_pedido`, que toma precios y stock de la base (el navegador no puede alterar precios) y descuenta el stock.
- Sin conexión, la tienda muestra el último catálogo guardado.

## Datos del negocio
Editar el bloque `CFG` dentro de `index.html` (WhatsApp, Yape/Plin, cuenta bancaria, correo). Hoy son datos de demostración.

## Demo
- Código de descuento de prueba: `BIENVENIDA10`.
- Carrito y favoritos se guardan en el navegador de cada cliente.

## Historial
Cada commit es una versión de la tienda (ver `git log`).
