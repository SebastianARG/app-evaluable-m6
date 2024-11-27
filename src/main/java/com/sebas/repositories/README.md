# Repositories

Esta carpeta contiene los repositorios de Spring Data JPA. Los repositorios son interfaces que permiten realizar operaciones CRUD y consultas personalizadas sobre las entidades.

## Repositorios en esta carpeta

- **`ClientRepository.java`**:
    - Maneja la entidad `Client`.
    - Métodos típicos:
        - `findByNif(String nif)`: Encuentra un cliente por su NIF.

- **`FacturaRepository.java`**:
    - Maneja la entidad `Factura`.
    - Métodos típicos:
        - `findByClientId(Long clientId)`: Encuentra facturas de un cliente específico.

- **`LiniaRepository.java`**:
    - Maneja la entidad `Linia`.
    - Métodos típicos:
        - `findByFacturaId(Long facturaId)`: Encuentra las líneas de una factura específica.

- **`ProducteRepository.java`**:
    - Maneja la entidad `Producte`.
    - Métodos típicos:
        - `findByNom(String nom)`: Encuentra un producto por su nombre.

## Notas
- Todos los repositorios extienden de `JpaRepository` o `CrudRepository`.
- Métodos adicionales pueden definirse usando consultas derivadas (query methods).
