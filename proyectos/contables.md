# CONTAPP

Participé en el `Backend` de un proyecto para desarrollar una aplicación de contaduría, enfocado en la gestión de las operaciones contables. La primera fase del proyecto se centró en la creación de un sistema de facturación

> [!NOTE]
> La aplicación está disponible en el siguiente link: [CONTAPP](http://contables.unicauca.edu.co/#/)

## Mis responsabilidades específicas incluyeron:

### Inicio de Sesión:

Implementé el sistema de autenticación y autorización utilizando Keycloak, asegurando un acceso controlado a la aplicación. Desarrollé endpoints para la gestión de usuarios.

### Catálogo de Cuentas:

Diseñé y desarrollé el módulo del catálogo de cuentas, permitiendo el CRUD de cuentas contables. Implementé funcionalidades para obtener la estructura jerárquica del catálogo.

### Gestión de Empresas:

Estuve a cargo de la gestión de empresas dentro de la aplicación, desarrollando endpoints para el CRUD de registros de empresas. Además, implementé multitenancy, permitiendo que la base de datos se filtrara dependiendo del usuario que accediera a través de un token, asegurando que cada usuario solo pudiera acceder a los datos correspondientes a su empresa.

![Escenario](https://res.cloudinary.com/dilrruxyx/image/upload/v1718310860/keycloak_pdryin.jpg)

![](https://res.cloudinary.com/dilrruxyx/image/upload/v1718338073/secuencia_aqaqtp.jpg)

### Gestión de Usuarios

| Método   | Endpoint                           | Descripción                                              |
|----------|------------------------------------|----------------------------------------------------------|
| **GET**  | `/keycloak/users`                  | Recupera una lista de todos los usuarios en Keycloak.    |
| **GET**  | `/keycloak/users/{username}`       | Recupera una de usuarios que coincidan con el username   | 
| **GET**  | `/keycloak/user/{userId}`          | Recupera los detalles de un usuario por su ID de usuario.|
| **GET**  | `/keycloak/getCurrentUser`         | Recupera los detalles del usuario actualmente autenticado. |
| **DELETE**| `/keycloak/delete/{userId}`       | Elimina un usuario de Keycloak.                          |

## Catálogo de Cuentas:

| Método   | Endpoint                                                    | Descripción                                              |
|----------|-------------------------------------------------------------|----------------------------------------------------------|
| **GET**  | `/api/accountCatalogue/trees/{idEnterprise}` | Obtener árbol del catalogo de cuenta de una empresa.                     |
| **GET**  | `/api/accountCatalogue/tree/{code}/{idEnterprise}` | Obtener padre y sus hijos a partir del código. | 
| **GET**  | `/api/accountCatalogue/accountByCode/{code}/{idEnterprise}` | Obtener la información de una cuenta. |
| **POST**  | `/api/accountCatalogue/` | Crear una cuenta |
| **DELETE**| `/api/accountCatalogue/{id}` | Eliminar una cuenta por su Id                         |
| **PUT** | `/api/accountCatalogue/{id}` | Actulizar una cuenta por su Id |

## Gestión de Empresas:

| Método   | Endpoint                           | Descripción                                              |
|----------|------------------------------------|----------------------------------------------------------|
| **GET**  | `/api/enterprises/enterprise/{id}` | Obtener información de una empresa por ID                |
| **GET**  | `/api/enterprises/`                | Obtener todas las empresas activas  | 
| **POST**  | `/api/enterprises/`               | Crear una empresa |
| **PUT**  | `/api/enterprises/update/{id}`     | Actulizar una empresa por su ID |
| **PUT** | `/api/enterprises/update/status/{id}/{state}`          | Actulizar estado de una empresa       |

## Imágenes del frontend desarrolladas por mis compañeros consumiendo los servicio.

![](https://res.cloudinary.com/dilrruxyx/image/upload/v1719449272/Captura_desde_2024-06-26_19-47-43_b1dbez.png)

![](https://res.cloudinary.com/dilrruxyx/image/upload/v1719449351/Captura_desde_2024-06-26_19-49-00_fdblx0.png)


![](https://res.cloudinary.com/dilrruxyx/image/upload/v1719449502/Captura_desde_2024-06-26_19-51-22_guiytn.png)

![](https://res.cloudinary.com/dilrruxyx/image/upload/v1719449685/Captura_desde_2024-06-26_19-54-35_mgxyxf.png)
