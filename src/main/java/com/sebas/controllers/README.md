# Controllers

Los controladores son responsables de manejar las solicitudes HTTP de la API REST. Cada controlador se asocia con una entidad específica (Client, Factura, Linia, Producte) y define las rutas necesarias para realizar operaciones CRUD (Crear, Leer, Actualizar, Eliminar) y otras operaciones personalizadas.

## Funcionalidad de los Controladores

- **`ClientController.java`**:
    - Maneja las operaciones relacionadas con los clientes.
    - Endpoints esperados:
        - `GET /clients`: Devuelve la lista de todos los clientes.
        - `GET /clients/{id}`: Obtiene un cliente específico por su ID.
        - `POST /clients`: Crea un nuevo cliente.
        - `PUT /clients/{id}`: Actualiza los datos de un cliente.
        - `DELETE /clients/{id}`: Elimina un cliente por su ID.

- **`FacturaController.java`**:
    - Maneja las operaciones relacionadas con las facturas.
    - Endpoints esperados:
        - `GET /facturas`: Devuelve todas las facturas.
        - `GET /facturas/{id}`: Obtiene una factura específica.
        - `POST /facturas`: Crea una nueva factura.
        - `PUT /facturas/{id}`: Actualiza una factura existente.
        - `DELETE /facturas/{id}`: Elimina una factura.

- **`LiniaController.java`**:
    - Maneja las operaciones relacionadas con las líneas de factura.
    - Endpoints esperados:
        - `GET /linies`: Devuelve todas las líneas.
        - `POST /linies`: Añade una nueva línea a una factura.
        - `DELETE /linies/{id}`: Elimina una línea.

- **`ProducteController.java`**:
    - Maneja las operaciones relacionadas con los productos.
    - Endpoints esperados:
        - `GET /productes`: Lista todos los productos disponibles.
        - `POST /productes`: Crea un nuevo producto.
        - `PUT /productes/{id}`: Actualiza los datos de un producto.
        - `DELETE /productes/{id}`: Elimina un producto por su ID.

## Notas
- Cada clase debe tener anotaciones como `@RestController` y rutas específicas con `@RequestMapping`.
- Las clases deben interactuar con los **servicios** para realizar operaciones lógicas y delegar consultas a los repositorios.
