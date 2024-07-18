# Proyecto Final: Sistema de Gestión de Proveedores de Productos

## Descripción General:
El proyecto consiste en desarrollar un sistema de gestión de proveedores de productos que permita administrar productos, proveedores y pedidos. El backend se implementará en .NET para crear una API que gestione los datos, mientras que el frontend se desarrollará en React para consumir esta API y proporcionar una interfaz interactiva a los usuarios.

## Funcionalidades del Proyecto:
1. **Gestión de Productos:**
   - Registrar nuevos productos.
   - Listar todos los productos.
   - Actualizar información de productos.
   - Eliminar productos.

2. **Gestión de Proveedores:**
   - Registrar nuevos proveedores.
   - Listar todos los proveedores.
   - Actualizar información de proveedores.
   - Eliminar proveedores.

3. **Gestión de Pedidos:**
   - Crear nuevos pedidos.
   - Listar todos los pedidos.
   - Actualizar información de pedidos.
   - Eliminar pedidos.

## Endpoints de la API:
1. **Productos:**
   - `GET /products` - Listar todos los productos.
   - `POST /products` - Registrar un nuevo producto.
   - `GET /products/{id}` - Obtener detalles de un producto específico.
   - `PUT /products/{id}` - Actualizar información de un producto.
   - `DELETE /products/{id}` - Eliminar un producto.

2. **Proveedores:**
   - `GET /suppliers` - Listar todos los proveedores.
   - `POST /suppliers` - Registrar un nuevo proveedor.
   - `GET /suppliers/{id}` - Obtener detalles de un proveedor específico.
   - `PUT /suppliers/{id}` - Actualizar información de un proveedor.
   - `DELETE /suppliers/{id}` - Eliminar un proveedor.

3. **Pedidos:**
   - `GET /orders` - Listar todos los pedidos.
   - `POST /orders` - Crear un nuevo pedido.
   - `GET /orders/{id}` - Obtener detalles de un pedido específico.
   - `PUT /orders/{id}` - Actualizar información de un pedido.
   - `DELETE /orders/{id}` - Eliminar un pedido.

## Funcionalidades extras:

   **Dashboard:**
   -   Se puede crear un panel principal que muestre información resumida sobre:
      - Proveedores con más productos.
      - Pedidos con más productos.
      - Productos más populares.

## Requisitos Técnicos:
   - Crear una API RESTful utilizando ASP.NET Core.
   - Utilizar Entity Framework Core para la gestión de la base de datos.
   - Implementar controladores y servicios para manejar las operaciones CRUD.
   - Crear una aplicación de React para consumir la API.
   - Diseñar componentes reutilizables para mostrar y gestionar productos, proveedores y pedidos.

## Entregables:
1. Código fuente del backend y frontend.
2. Instrucciones para configurar y ejecutar el proyecto.


# Ejemplos de Cuerpos de Mensajes JSON POST

1. **Registrar un nuevo producto (POST /products)**
    - **Cuerpo**: 
        ```json
        {
            "productName": "Nombre del Producto",
            "description": "Descripción detallada del producto",
            "price": 49.99,
            "quantityAvailable": 100,
            "supplierId": 1
        }
        ```

2. **Crear un nuevo proveedor (POST /suppliers)**
    - **Cuerpo**: 
        ```json
        {
            "supplierName": "Nombre del Proveedor",
            "address": "Dirección del proveedor",
            "city": "Ciudad",
            "country": "País",
            "phone": "(123) 456-7890",
            "email": "proveedor@example.com",
        }
        ```

3. **Crear un nuevo pedido (POST /orders)**
    - **Cuerpo**: 
        ```json
        {
            "orderDate": "2024-07-18T10:00:00Z",
            "items": [{
                "productId": 1,
                "quantity": 10,
                "unitPrice": 5.99,
                "discount": 0.1
            },
            {
                "productId": 2,
                "quantity": 20,
                "unitPrice": 67.99,
                "discount": 0.15
            }]
        }
        ```