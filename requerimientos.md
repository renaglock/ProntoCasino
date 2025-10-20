# TOMA DE REQUERIMIENTOS SIMPLE DE PUNTO CASINO UNIVERSIDAD

## 1. Descripción del Cliente y Problema

* **Cliente:** Nuestro cliente es cualquier persona que compre en cualquiera de los casinos de la Universidad Católica de Temuco.
* **Problema Principal:** El problema principal nace en la cotidianidad de hacer fila para comprar algún producto en especifico, y al llegar a la caja sorprendernos con que éste se encuentra agotado. 

---

## 2. Usuarios y Perfiles (Roles)

### Lista de Usuarios
* *Administrador*
* *Vendedor*
* *Usuario/Cliente*

### Perfiles y Permisos
* **Administrador:**
    * *Descripción:* Supervisa todo el sistema.
    * *Permisos:* Crear/Editar/Eliminar usuarios, ver reportes de ventas, gestionar categorías de productos, etc.
* **Vendedor:**
    * *Descripción:* Gestiona el inventario y las ventas.
    * *Permisos:* Crear/Editar productos, ver órdenes pendientes, marcar órdenes como enviadas, etc.
* **Usuario/Cliente:**
    * *Descripción:* El comprador final que usa la plataforma.
    * *Permisos:* Registrarse, iniciar sesión, ver productos, agregar al carrito, realizar una compra, ver su historial de pedidos.

---

## 3. Funciones Indispensables por Perfil

*Aquí se encuentran las funciones más importantes que debe tener cada perfil.*

**Administrador:**
1.  CRUD (Crear, Leer, Actualizar, Borrar) de Vendedores.
2.  Ver dashboard de métricas de ventas.
3.  Administrar perfiles, horarios, productos, etc.

**Vendedor:**
1.  CRUD de Productos (incluyendo stock).
2.  Gestión de Órdenes (ver, procesar, enviar).
3.  Notificar al Cliente.

**Usuario/Cliente:**
1.  Registro e Inicio de Sesión (Autenticación).
2.  Ver catálogo de productos.
3.  Realizar un pedido (Checkout).
4.  Pedir reparto a sala.

---

## 4. Datos Básicos a Almacenar (Entidades)

* **Usuario (User):** `nombre`, `email`, `password_hash`, `rol` (Admin, Vendedor, Cliente), `teléfono`, `carrera`. 
* **Producto (Product):** `nombre`, `descripcion`, `precio`, `stock`, `vendedor_id` (referencia al Vendedor)...
* **Orden (Order):** `cliente_id`, `productos` (array de productos), `total`, `estado` (pendiente, enviado, entregado), `fecha`...
* **Entrega(Delivery):** `vendeor_id`, `cliente_id`, `orden_id`, `sala`, `fecha`, `hora`, etc...

**Productos** (El producto que se tiene dentro de la tienda):

* id_producto (La ID del producto, EMPA-01).
* Nombre del producto (Empanada).
* Precio del producto ($2.000 pesos).
* Stock (Esto si hay inventario).

**Pedido** (El pedido que hace el cliente):

* id_pedido (ID del pedido del cliente).
* nombre_cliente (Nombre de la persona que compra).
* id_producto (Los productos que pide el cliente).
* Nombre (Nombre del producto).
* Cantidad (Cantidad de artículos que lleva el cliente).
* Precio (Precio de los artículos).
* Total de la venta (El total a pagar).

**Usuarios** (Personal de la tienda):

* id_usuario (La ID de la persona que trabaja en la tienda).
* Nombre (Nombre de la persona).
* Rol (Puede ser rol como: Administrador o Cajero).

## 5. Lista de requisitos funcionales y no funcionales

**Funcionales**

* El sistema debe registrar un pedido hecho por el cliente.
* El sistema debe mostrar una lista de productos disponibles.
* El cajero puede confirmar un pedido en su app.
* Incluye sistema de inventario básico.

**No funcionales**

* Función donde el cajero pueda dar de baja un producto por falta de stock o por algún otro motivo.
* Reservar producto.
* Interfaz amigable y clara.

## 6. Definición del MVP (qué incluye / qué queda para futuras versiones)

**Qué incluye:**

* Que el cliente pueda buscar un producto y reservarlo desde su terminal (Puede ser un cliente o un invitado).
* Que el cajero pueda dar el visto bueno y confirmar el pedido para posteriormente ser entregado.

**Qué queda para futuras versiones:**

* Incluir un menú de registro (Sign in).
* Menú colación diaria.
* Notificaciones de promociones. Ejemplo: (Promo completo + bebida 20%).
* Sistema de inventarios.
* Producto del día o de la semana.
* Uso de la APP desde una computadora (uso desde un navegador).
* Estadisticas de venta (Métrica)



## 7. Prueba de que funciona git.

* Este texto es una prueba (Jorge Mendoza)
* Este texto es otra prueba 2 (Jorge Mendoza)
* estamos en la kk (yeremi)
* Hoy toca prieta (Mario) 

## 8. Plazo deseado 

* Fase de analsis y diseño: 2 semanas 
* Desarrollo de pruebas: 6 semanas
* Prueba piloto: 2 semanas 
* Entrega final: 10 semanas desde el inicio del proyecto.

## 9. Flujo principal del sistema 

* inicio de sesion/registro 
* visualizacion del menu 
* seleccion del pedido 
* pago
* confirmacion 
* generacion qr
* notificacion para retiro 

## Requisitos no funcionales 

* Seguridad: cifrado de datos y autificacion 
* Usabilidad: interfaz intuitiva y accesible 
* compatibilidad: soporte para dispositivos Android 10+ e IOS 14+ 
* Mantenibilidad: codigo modular y documentado
* Escalabilidad: soporte para minimo 800 usuarios simultaneos  
---

## 14. Próximos Pasos

Una vez aprobados los requerimientos y el alcance del MVP definidos en este documento, el equipo procederá con las siguientes fases:

### 1. Fase de Diseño Funcional y Técnico (Entrega 2)

El siguiente gran hito es la creación del documento `DISENO.md`, que incluirá:

* **Diagramas Visuales:** Creación de diagramas de casos de uso y el diagrama de arquitectura técnica (API, MongoDB, Redis, Docker).
* **Modelo de Datos:** Definición detallada de las colecciones y esquemas de Mongoose, incluyendo el esquema de `users` y las relaciones principales.
* **Diseño de API:** Especificación de los endpoints RESTful principales (rutas, métodos, permisos y estructuras de datos de input/output).
* **Estrategia de Caché:** Definición de qué datos se almacenarán en Redis y cómo se gestionará su invalidación.
* **Wireframes:** Creación de mockups simples para las vistas clave del sistema.

### 2. Configuración del Entorno de Desarrollo

En paralelo al diseño, se iniciarán las tareas de configuración técnica:

* Estructura inicial del proyecto (carpetas y archivos).
* Configuración de Docker (`docker-compose.yml`) para levantar los servicios (API, MongoDB, Redis).
* Preparación del repositorio para el trabajo colaborativo (protección de la rama `develop`, plantillas de Pull Request).

### 3. Planificación del Sprint 1

Basado en el MVP, se desglosarán las primeras historias de usuario y tareas técnicas en el backlog. El Sprint 1 se enfocará en:

* Autenticación (Login/Registro).
* CRUD básico del recurso principal (ej. `products`).