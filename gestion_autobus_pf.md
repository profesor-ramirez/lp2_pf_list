# Proyecto Final: Gestión de Autobuses

## Descripción General:
El proyecto consiste en desarrollar un sistema de gestión de autobuses que permita administrar rutas, autobuses y horarios. El backend se implementará en .NET para crear una API que gestione los datos, mientras que el frontend se desarrollará en React para consumir esta API y proporcionar una interfaz interactiva a los usuarios.

## Funcionalidades del Proyecto:
1. **Gestión de Autobuses:**
   - Registrar nuevos autobuses.
   - Listar todos los autobuses.
   - Actualizar información de autobuses.
   - Eliminar autobuses.

2. **Gestión de Rutas:**
   - Crear nuevas rutas.
   - Listar todas las rutas.
   - Actualizar información de rutas.
   - Eliminar rutas.

3. **Gestión de Horarios:**
   - Asignar horarios a los autobuses para las rutas.
   - Listar horarios de una ruta específica.
   - Actualizar horarios.
   - Eliminar horarios.

## Endpoints de la API:
1. **Autobuses:**
   - `GET /buses` - Listar todos los autobuses.
   - `POST /buses` - Registrar un nuevo autobús.
   - `GET /buses/{id}` - Obtener detalles de un autobús específico.
   - `PUT /buses/{id}` - Actualizar información de un autobús.
   - `DELETE /buses/{id}` - Eliminar un autobús.

2. **Rutas:**
   - `GET /routes` - Listar todas las rutas.
   - `POST /routes` - Crear una nueva ruta.
   - `GET /routes/{id}` - Obtener detalles de una ruta específica.
   - `PUT /routes/{id}` - Actualizar información de una ruta.
   - `DELETE /routes/{id}` - Eliminar una ruta.

3. **Horarios:**
   - `GET /schedules` - Listar todos los horarios.
   - `POST /schedules` - Asignar un nuevo horario a un autobús en una ruta.
   - `GET /schedules/{id}` - Obtener detalles de un horario específico.
   - `PUT /schedules/{id}` - Actualizar información de un horario.
   - `DELETE /schedules/{id}` - Eliminar un horario.

4. **Reserva:**
   - `GET /reservations` - Listar todas las reservas.
   - `POST /reservations` - Crear una reserva.
   - `GET /reservations/{id}` - Obtener reserva especifica.
   - `DELETE /reservations/{id}` - Eliminar una reserva.
   
## Requisitos Técnicos:
   - Crear una API RESTful utilizando ASP.NET Core.
   - Utilizar Entity Framework Core para la gestión de la base de datos.
   - Implementar controladores y servicios para manejar las operaciones CRUD.
   - Crear una aplicación de React para consumir la API.
   - Diseñar componentes reutilizables para mostrar y gestionar autobuses, rutas y horarios.


## Entregables:
1. Código fuente del backend y frontend.
2. Instrucciones para configurar y ejecutar el proyecto.


### Ejemplos de Cuerpos de Mensajes JSON para el Proyecto de Gestión de Autobuses

#### Registrar un nuevo autobús (`POST /buses`)
```json
{
  "busNumber": "1234",
  "model": "Volvo B9R",
  "capacity": 50,
  "year": 2018,
  "status": "Active"
}
```

#### Registrar una nueva ruta (`POST /routes`)
```json
{
  "routeName": "Ruta 1",
  "origin": "Ciudad A",
  "destination": "Ciudad B",
  "distance": 150.5
}
```

#### Registrar un nuevo horario (`POST /schedules`)
```json
{
  "busId": 1,
  "routeId": 1,
  "departureTime": "2024-07-18T08:00:00",
  "arrivalTime": "2024-07-18T12:00:00"
}
```

#### Registrar una nueva reserva (`POST /reservations`)
```json
{
  "scheduleId": 1,
  "passengerName": "John Doe",
  "seatNumber": 10,
  "reservationDate": "2024-07-15"
}
```