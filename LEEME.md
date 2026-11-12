# Catálogo mayorista Posmart · Pavco

## Qué contiene

| Archivo | Para qué sirve |
|---|---|
| `index.html` | La tienda que ven tus clientes (sin contraseña) |
| `admin.html` | Tu panel para editar precios, cantidades y descripciones |
| `productos.json` | Todos los productos y precios (aquí se guardan tus cambios) |
| `logo-posmart.webp`, `logo-pavco.webp` | Logos |

## 1. Subirlo a GitHub (una sola vez)

1. Entra a github.com y crea un repositorio nuevo, por ejemplo `catalogo`. Debe ser **público**.
2. Pulsa **Add file → Upload files** y sube los 5 archivos (no el .zip, sus archivos ya descomprimidos).
3. Ve a **Settings → Pages**. En *Branch* elige `main` y carpeta `/ (root)`. Pulsa **Save**.
4. Espera 1 o 2 minutos. Tu tienda quedará en:
   `https://TU-USUARIO.github.io/catalogo/`
   y tu panel en:
   `https://TU-USUARIO.github.io/catalogo/admin.html`

## 2. Crear tu token para poder publicar cambios (una sola vez)

1. En GitHub: foto de perfil → **Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token**.
2. *Repository access*: **Only select repositories** y elige `catalogo`.
3. *Permissions → Repository permissions → Contents*: **Read and write**.
4. Genera el token y cópialo (solo se muestra una vez).
5. Abre tu panel `admin.html`, entra a **Ajustes** y completa:
   - Repositorio: `TU-USUARIO/catalogo`
   - Rama: `main`
   - Token: el que copiaste

El token se guarda solo en el navegador donde lo pegaste.

## 3. Cambiar precios o productos

1. Abre `admin.html`, edita lo que necesites en la tabla (precio, caja, bolsas por caja, UMV, descripción).
2. Botones útiles:
   - **Ajustar precios (%)**: sube o baja todos los precios que estén filtrados (por ejemplo, toda una categoría).
   - **⧉** duplica una fila, sirve para agregar otra medida al mismo producto.
   - **Activo**: desmárcalo para ocultar un producto sin borrarlo.
   - **+ Producto**: agrega un producto nuevo.
3. Pulsa **Guardar y publicar en GitHub**. En 1 o 2 minutos los clientes ven los cambios.

Si no quieres usar token, pulsa **Descargar productos.json** y sube ese archivo a GitHub reemplazando el anterior.

## Descargar el pedido en PDF

En el carrito, el cliente pulsa **Descargar PDF**. Se genera una hoja ordenada con el logo de Posmart y de Pavco en cada página, los datos del cliente (RUC, razón social y dirección, si los llenó), una tabla por categoría con medida, cantidad, unidades, precio unitario e importe, el subtotal de cada categoría y el total. Necesita conexión a internet para generarse.

## Sobre los precios

Los precios del catálogo salen de la columna **18%** de tu Excel. Si el Excel cambia, vuelve a pasarme el archivo o corrige los precios desde el panel.

## Cosas a tener en cuenta

- **Los precios son públicos.** Al no haber contraseña, cualquiera que tenga el enlace puede ver el catálogo y los precios. No publiques el enlace en redes si es solo para clientes.
- **El panel no tiene contraseña propia.** Cualquiera que abra `admin.html` puede ver la pantalla, pero **no puede publicar nada** sin tu token. No compartas tu token.
- Cuando agregues una medida nueva a un producto, ponla justo debajo de las otras medidas del mismo producto (usa el botón ⧉) para que salgan juntas en la tienda.
- No abras `index.html` ni `admin.html` con doble clic desde tu computadora: necesitan abrirse desde GitHub Pages para poder leer `productos.json`.
