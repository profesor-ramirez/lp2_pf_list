# Proyecto Final: Servicio de Gestión de Paquetes

## Descripción General:
El proyecto consiste en desarrollar un sistema de gestión de paquetería que permita administrar paquetes, envíos y seguimiento de entregas. El backend se implementará en .NET para crear una API que gestione los datos, mientras que el frontend se desarrollará en React para consumir esta API y proporcionar una interfaz interactiva a los usuarios.

## Funcionalidades del Proyecto:
1. **Gestión de Paquetes:**
   - Registrar nuevos paquetes.
   - Listar todos los paquetes.
   - Actualizar información de paquetes.
   - Eliminar paquetes.

2. **Gestión de Envíos:**
   - Crear nuevos envíos.
   - Listar todos los envíos.
   - Actualizar información de envíos.
   - Eliminar envíos.

3. **Seguimiento de Entregas:**
   - Asignar estados a los paquetes.
   - Listar estados de un paquete específico.
   - Actualizar estados de los paquetes.

## Endpoints de la API:
1. **Paquetes:**
   - `GET /packages` - Listar todos los paquetes.
   - `POST /packages` - Registrar un nuevo paquete.
   - `GET /packages/{id}` - Obtener detalles de un paquete específico.
   - `PUT /packages/{id}` - Actualizar información de un paquete.
   - `DELETE /packages/{id}` - Eliminar un paquete.

2. **Envíos:**
   - `GET /shipments` - Listar todos los envíos.
   - `POST /shipments` - Crear un nuevo envío.
   - `GET /shipments/{id}` - Obtener detalles de un envío específico.
   - `PUT /shipments/{id}` - Actualizar información de un envío.
   - `DELETE /shipments/{id}` - Eliminar un envío.

3. **Seguimiento de Entregas:**
   - `GET /tracking` - Listar todos los estados de los paquetes.
   - `POST /tracking` - Asignar un nuevo estado a un paquete.
   - `GET /tracking/{packageId}` - Obtener el historial de estados de un paquete específico.
   - `PUT /tracking/{trackingId}` - Actualizar información de un estado.
   - `DELETE /tracking/{trackingId}` - Eliminar un estado.

## Requisitos Técnicos:
   - Crear una API RESTful utilizando ASP.NET Core.
   - Utilizar Entity Framework Core para la gestión de la base de datos.
   - Implementar controladores y servicios para manejar las operaciones CRUD.
   - Crear una aplicación de React para consumir la API.
   - Diseñar componentes reutilizables para mostrar y gestionar paquetes, envíos y seguimientos.

## Consideraciones:
- Asegurarse de que la API devuelva respuestas claras y útiles (códigos de estado HTTP y mensajes de error significativos).
- Documentar la API utilizando Swagger o similar.
- Crear una interfaz intuitiva y fácil de usar para el frontend.
- Probar todas las funcionalidades para asegurar que el sistema funcione correctamente.

## Entregables:
1. Código fuente del backend y frontend.
2. Instrucciones para configurar y ejecutar el proyecto.

### Ejemplos de Cuerpos de Mensajes JSON para el Proyecto de Servicio de Paquetería y Gestión de Paquetes

#### Registrar un nuevo paquete (`POST /packages`)
```json
{
  "packageId": "PKG12345",
  "senderName": "Pedro Perez",
  "receiverName": "Juan Soto",
  "origin": "San Cristobal",
  "destination": "Samana",
  "weight": 2.5,
  "status": "Pending",
  "estimatedDelivery": "2024-07-25"
}
```

#### Registrar un nuevo envío (`POST /shipments`)
```json
{
  "shipmentId": "SHIP12345",
  "packageId": "PKG12345",
  "departureTime": "2024-07-18T08:00:00",
  "arrivalTime": "2024-07-18T20:00:00",
  "currentLocation": "Santo Domingo"
}
```

#### Registrar una actualización de estado (`POST /tracking`)
{
  "packageId": "PKG12345",
  "status": "In Transit",
  "timestamp": "2024-07-18T10:00:00",
  "location": "Santo Domingo"
}

