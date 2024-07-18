# Proyecto Final: Gestión de Gimnasio

## Descripción General:
El proyecto consiste en desarrollar un sistema de gestión de gimnasio que permita administrar clases, entrenadores y reservas de clases. El backend se implementará en .NET para crear una API que gestione los datos, mientras que el frontend se desarrollará en React para consumir esta API y proporcionar una interfaz interactiva a los usuarios.

## Funcionalidades del Proyecto:
1. **Gestión de Clases:**
   - Registrar nuevas clases.
   - Listar todas las clases.
   - Actualizar información de clases.
   - Eliminar clases.

2. **Gestión de Entrenadores:**
   - Registrar nuevos entrenadores.
   - Listar todos los entrenadores.
   - Actualizar información de entrenadores.
   - Eliminar entrenadores.

3. **Gestión de Reservas:**
   - Crear nuevas reservas de clases.
   - Listar todas las reservas.
   - Actualizar información de reservas.
   - Eliminar reservas.

## Endpoints de la API:
1. **Clases:**
   - `GET /classes` - Listar todas las clases.
   - `POST /classes` - Registrar una nueva clase.
   - `GET /classes/{id}` - Obtener detalles de una clase específica.
   - `PUT /classes/{id}` - Actualizar información de una clase.
   - `DELETE /classes/{id}` - Eliminar una clase.

2. **Entrenadores:**
   - `GET /trainers` - Listar todos los entrenadores.
   - `POST /trainers` - Registrar un nuevo entrenador.
   - `GET /trainers/{id}` - Obtener detalles de un entrenador específico.
   - `PUT /trainers/{id}` - Actualizar información de un entrenador.
   - `DELETE /trainers/{id}` - Eliminar un entrenador.

3. **Reservas:**
   - `GET /reservations` - Listar todas las reservas.
   - `POST /reservations` - Crear una nueva reserva.
   - `GET /reservations/{id}` - Obtener detalles de una reserva específica.
   - `PUT /reservations/{id}` - Actualizar información de una reserva.
   - `DELETE /reservations/{id}` - Eliminar una reserva.

## Funcionalidades extras:

-   **Dashboard:**
    -   Se puede crear un panel principal que muestre información resumida sobre el estado actual del gimnasio, como la cantidad de entrenadores, clases programadas y reservas realizadas.


## Requisitos Técnicos:
   - Crear una API RESTful utilizando ASP.NET Core.
   - Utilizar Entity Framework Core para la gestión de la base de datos.
   - Implementar controladores y servicios para manejar las operaciones CRUD.
   - Crear una aplicación de React para consumir la API.
   - Diseñar componentes reutilizables para mostrar y gestionar clases, entrenadores y reservas.


## Entregables:
1. Código fuente del backend y frontend.
2. Instrucciones para configurar y ejecutar el proyecto.