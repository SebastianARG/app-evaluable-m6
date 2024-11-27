# Lógica (Entidades JPA)

Esta carpeta contiene las **entidades JPA**, que son clases que mapean las tablas de la base de datos. Estas entidades son gestionadas por Hibernate o JPA para realizar operaciones con la base de datos.

## Clases en esta carpeta

- **`Client.java`**:
    - Representa la tabla `clients`.
    - Atributos principales:
        - `id`: Identificador único.
        - `nif`: Número de identificación fiscal único.
        - `nom`: Nombre del cliente.

- **`Factura.java`**:
    - Representa la tabla `facturas`.
    - Atributos principales:
        - `id`: Identificador único.
        - `data`: Fecha de la factura.
        - `client`: Relación con un cliente (`@ManyToOne`).
        - `linies`: Lista de líneas de factura (`@OneToMany`).

- **`Linia.java`**:
    - Representa las líneas de una factura.
    - Atributos principales:
        - `id`: Identificador único.
        - `producte`: Producto asociado (`@ManyToOne`).
        - `quantitat`: Cantidad del producto en la línea.
        - `factura`: Factura a la que pertenece (`@ManyToOne`).

- **`Producte.java`**:
    - Representa la tabla `productes`.
    - Atributos principales:
        - `id`: Identificador único.
        - `nom`: Nombre del producto.
        - `preu`: Precio del producto.

## Notas
- Cada clase debe tener las anotaciones `@Entity` y `@Table` para mapearlas correctamente.
- Usa relaciones como `@OneToMany` y `@ManyToOne` para definir dependencias entre entidades.
