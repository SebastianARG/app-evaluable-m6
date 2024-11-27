# Services

Los servicios contienen la lógica de negocio de la aplicación. Actúan como intermediarios entre los controladores y los repositorios.

## Servicios en esta carpeta

- **`ClientService.java`**:
    - Lógica para gestionar clientes.
    - Métodos típicos:
        - `createClient(Client client)`: Valida y guarda un cliente.
        - `updateClient(Long id, Client client)`: Actualiza datos de un cliente.

- **`FacturaService.java`**:
    - Lógica para gestionar facturas.
    - Métodos típicos:
        - `calculateTotal(Long facturaId)`: Calcula el total de una factura basada en las líneas asociadas.

- **`ProducteService.java`**:
    - Lógica para gestionar productos.
    - Métodos típicos:
        - `isProductAvailable(Long productId)`: Verifica si un producto existe y está disponible.

## Notas
- Los servicios deben ser anotados con `@Service` para que Spring los gestione.
- Es importante manejar excepciones y validaciones dentro de los servicios.
