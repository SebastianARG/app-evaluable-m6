# Aplicación de Facturación - Documentación

Esta carpeta contiene los componentes principales de la aplicación Spring Boot.

### Subcarpetas:
- `controllers/`: Controladores de la API REST.
- `logica/`: Entidades JPA que representan las tablas de la base de datos.
- `repositories/`: Repositorios JPA para realizar operaciones con la base de datos.
- `services/`: Servicios con la lógica de negocio.
- `resources/`: Archivos de configuración, como `application.properties` y scripts SQL.

### Notas:
1. La clase principal de la aplicación está en `MainApp.java`.
2. Configura el archivo `application.properties` para definir la conexión a la base de datos.

# Aplicación Principal (Main)

Esta carpeta contiene la clase principal que inicia la aplicación Spring Boot. También se incluye la configuración básica para ejecutar la aplicación y probar las APIs REST.

## Clase Principal

- **`MainApp.java`**:
    - Clase principal con la anotación `@SpringBootApplication`.
    - Es el punto de entrada de la aplicación.

## Cómo debería estar estructurado el `MainApp.java`:

```java
package com.sebas;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class MainApp {
    public static void main(String[] args) {
        SpringApplication.run(MainApp.class, args);
        System.out.println("Aplicación iniciada. Accede a http://localhost:8080/");
    }
}
