# Proyecto Final: Sistema de Préstamos de Libros para Biblioteca

## Funcionalidades
1. **Gestión de Libros**
    - Listar todos los libros disponibles.
    - Buscar libros por título, autor o categoría.
    - Agregar nuevos libros.
    - Actualizar información de libros existentes.
    - Eliminar libros.


2. **Gestión de socios**
    - Listar socios.
    - Obtener socio por ID.
    - Crear nuevo socio.
    - Editar socio existente.
    - Eliminar socio.

3. **Gestión de Préstamos**
    - Listar todos los préstamos activos.
    - Registrar un nuevo préstamo.
    - Finalizar un préstamo (devolución del libro).
    - Listar historial de préstamos.

## Endpoints

### Gestión de Libros

1. **Listar todos los libros**
    - **URL**: `/api/books`
    - **Método**: `GET`
    - **Descripción**: Obtiene una lista de todos los libros disponibles en la biblioteca.

2. **Buscar libros**
    - **URL**: `/api/books/search`
    - **Método**: `GET`
    - **Parámetros**: 
        - `title` (opcional): Filtrar por título.
        - `author` (opcional): Filtrar por autor.
        - `category` (opcional): Filtrar por categoría.
    - **Descripción**: Busca libros basados en los parámetros dados.

3. **Agregar un nuevo libro**
    - **URL**: `/api/books`
    - **Método**: `POST`
    - **Cuerpo**: 
        ```json
        {
            "title": "string",
            "author": "string",
            "category": "string",
            "isbn": "string",
            "publishedDate": "date"
        }
        ```
    - **Descripción**: Agrega un nuevo libro a la biblioteca.

4. **Actualizar información de un libro**
    - **URL**: `/api/books/{id}`
    - **Método**: `PUT`
    - **Cuerpo**: 
        ```json
        {
            "title": "string",
            "author": "string",
            "category": "string",
            "isbn": "string",
            "publishedDate": "date"
        }
        ```
    - **Descripción**: Actualiza la información de un libro existente.

5. **Eliminar un libro**
    - **URL**: `/api/books/{id}`
    - **Método**: `DELETE`
    - **Descripción**: Elimina un libro de la biblioteca.

### Gestión de Socios

1. **Listar todos los socios**
    - **URL**: `/api/members`
    - **Método**: `GET`
    - **Descripción**: Obtiene una lista de todos los socios disponibles en la biblioteca.

2. **Buscar socios**
    - **URL**: `/api/members/search`
    - **Método**: `GET`
    - **Parámetros**: 
        - `name` (opcional): Filtrar por name.
    - **Descripción**: Busca socios basados en los parámetros dados.

3. **Agregar un nuevo socio**
    - **URL**: `/api/members`
    - **Método**: `POST`
    - **Cuerpo**: 
        ```json
        {
            "name": "string",
            "email": "string",
            "tel": "string"
        }
        ```
    - **Descripción**: Agrega un nuevo socio a la biblioteca.

4. **Actualizar información de un socio**
    - **URL**: `/api/members/{id}`
    - **Método**: `PUT`
    - **Cuerpo**: 
        ```json
        {
            "name": "string",
            "email": "string",
            "tel": "string"
        }
        ```
    - **Descripción**: Actualiza la información de un socio existente.

5. **Eliminar un socio**
    - **URL**: `/api/members/{id}`
    - **Método**: `DELETE`
    - **Descripción**: Elimina un socio de la biblioteca.

### Gestión de Préstamos

1. **Listar todos los préstamos activos**
    - **URL**: `/api/loans`
    - **Método**: `GET`
    - **Descripción**: Obtiene una lista de todos los préstamos activos.

2. **Registrar un nuevo préstamo**
    - **URL**: `/api/loans`
    - **Método**: `POST`
    - **Cuerpo**: 
        ```json
        {
            "bookId": "int",
            "borrowerName": "string",
            "borrowDate": "date"
        }
        ```
    - **Descripción**: Registra un nuevo préstamo de un libro.

3. **Finalizar un préstamo (devolución del libro)**
    - **URL**: `/api/loans/{id}`
    - **Método**: `PUT`
    - **Cuerpo**: 
        ```json
        {
            "returnDate": "date"
        }
        ```
    - **Descripción**: Marca un préstamo como finalizado (devolución del libro).

4. **Listar historial de préstamos**
    - **URL**: `/api/loans/history`
    - **Método**: `GET`
    - **Descripción**: Obtiene un historial de todos los préstamos realizados.

## Frontend con React

- **Pantalla de Listado de Libros**: Mostrar la lista de libros disponibles y permitir búsquedas.
- **Pantalla de Detalle de Libro**: Mostrar detalles de un libro y permitir la edición o eliminación del mismo.
- **Formulario de Agregar/Editar Libro**: Formulario para agregar un nuevo libro o editar la información de un libro existente.
- **Pantalla de Préstamos Activos**: Mostrar la lista de préstamos activos.
- **Formulario de Nuevo Préstamo**: Formulario para registrar un nuevo préstamo.
- **Pantalla de Historial de Préstamos**: Mostrar el historial de todos los préstamos realizados.

## Funcionalidad extras

**Dashboard:**

- Se puede crear un vista principal que muestra información resumida sobre el estado actual de la biblioteca: es decir, 
- la cantidad de libros disponibles
- libros prestados
- socios activos
- préstamos vencidos.