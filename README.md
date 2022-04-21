# BACKEND (Comisión 30920) - PRIMERA ENTREGA PROYECTO FINAL
### EMMANUEL PINTO

## Para iniciar el proyecto localmente correr el comando "npm start"

## Rutas disponibles:

### Productos
- `/api/productos` GET: Devuelve todos los productos.
- `/api/productos/:idProduct` GET: Devuelve un producto según su ID. 
- `/api/productos` POST: Recibe y agrega un producto, y lo devuelve con su id asignando (Solo para admins). Campos requeridos: title, price, thumnail (archivo imagen), description, code y stock.
- `/api/productos/:idProduct` PUT: Recibe y actualiza un producto según su ID (Solo para admins).
- `/api/productos/:idProduct` DELETE: Elimina un producto según su ID (Solo para admins).

### Carrito
- `/api/carrito` POST: Crea un carrito y lo guarda en el servidor. Campos requeridos: products (array con ids de productos a agregar).
- `/api/carrito/:idCart/productos` POST: Agrega productos a un carrito existente. Campos requeridos: products (array con ids de productos a agregar).
- `/api/carrito/:idCart/productos` GET: Obtiene los datos de un carrito específico por ID.
- `/api/carrito/:idCart` DELETE: Vacia y elimina un carrito del servidor.
- `/api/carrito/:idCart/productos/:idProduct` DELETE: Elimina un producto específico de un carrito en particular.

### Login
- `/login` POST: Inicia sesión como administrador (true or false), y redirecciona al index.
- `/logout` GET: Cierra Sesión como administrador.

### Vistas
- `/`: Index, muestra los productos disponibles en el catálogo, agregar un producto al carrito, ir a carrito, iniciar/cerrar sesión y, si somos adminis, editar o eliminar un producto.
- `/agregar.html`: Formulario para agregar un producto al catálogo (solo para admins).
- `/edit.html?id=:idProduct`: Formulario para edición de un producto (solo para admins).
- `/carrito.html`: Muestra los productos agregados a un carrito (si existen) y te permite vaciar el carrito completo, o eliminar por producto individualmente.

### FILES
- Los arrays de productos y carritos persisten en dos archivos en la carpera `/data`.

### Thumbnails
- Las imágenes de cada producto agregado al catálogo se almacenan en la carpera `/public/images`.

