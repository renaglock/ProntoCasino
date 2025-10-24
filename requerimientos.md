# TOMA DE REQUERIMIENTOS SIMPLE DE PUNTO CASINO UNIVERSIDAD

## **1. Descripción del Cliente y Problema

* **Cliente:** Nuestro cliente es cualquier persona que compre en cualquiera de los casinos de la Universidad Católica de Temuco.
* **Problema Principal:** El problema principal nace en la cotidianidad de hacer fila para comprar algún producto en especifico, y al llegar a la caja sorprendernos con que éste se encuentra agotado. 

## **2. Usuarios y Perfiles (Roles)

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

## **3. Funciones Indispensables por Perfil

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

## **4. Datos Básicos a Almacenar (Entidades)

* **Usuario (User):** `nombre`, `email`, `password_hash`, `rol` (Admin, Vendedor, Cliente), `teléfono`, `carrera`. 
* **Producto (Product):** `nombre`, `descripcion`, `precio`, `stock`, `vendedor_id` (referencia al Vendedor)...
* **Orden (Order):** `cliente_id`, `productos` (array de productos), `total`, `estado` (pendiente, enviado, entregado), `fecha`...
* **Entrega(Delivery):** `vendeor_id`, `cliente_id`, `orden_id`, `sala`, `fecha`, `hora`, etc...

## **5. Lista de requisitos funcionales y no funcionales

**Funcionales**

* El sistema debe registrar un pedido hecho por el cliente.
* El sistema debe mostrar una lista de productos disponibles.
* El cajero puede confirmar un pedido en su app.
* Incluye sistema de inventario básico.

**No funcionales**

* Función donde el cajero pueda dar de baja un producto por falta de stock o por algún otro motivo.
* Reservar producto.
* Interfaz amigable y clara.

## **6. Definición del MVP (qué incluye / qué queda para futuras versiones)

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

## **7. Plazo deseado 

* Fase de analsis y diseño: 2 semanas.
* Desarrollo de pruebas: 6 semanas
* Prueba piloto: 2 semanas.
* Entrega final: 10 semanas desde el inicio del proyecto.

## **8. Flujo principal del sistema 

* Inicio de sesion/registro. 
* Visualización del menu. 
* Selección del pedido. 
* Pago.
* Confirmación. 
* Generacion QR.
* Notificación para retiro. 
 
## **9. Definición de Alcance y Presupuesto**

**Alcance acordado:**  
Desarrollo exclusivo de una **API REST** utilizando **Node.js (Express)** y **MongoDB** como base de datos.  
No se incluye interfaz gráfica ni componentes visuales.

### **Detalle del alcance y costos**

| Componente | Descripción | Costo CLP | Costo USD |
|-------------|-------------|------------|------------|
| **Creación de API REST** | Desarrollo de la API según los requerimientos establecidos: creación de pedidos, confirmación y entrega. | $1.200.000 | $1.100 |
| **Base de datos NoSQL (MongoDB)** | Implementación y configuración de una base de datos para almacenar información de productos, clientes, vendedores y administradores. | $1.500.000 | $1.400 |
| **Servidor Express (Node.js)** | Configuración del servidor web con Express para la definición de rutas, controladores y comunicación con la base de datos. | $900.000 | $800 |

**Total estimado:** CLP $3.600.000 (≈ USD $3.300)

## **10. Propuesta Formal y Cronograma de Trabajo (API-only)**

### **Objetivo del proyecto**
Desarrollar una **API REST** que optimice la gestión de pedidos y reduzca la congestión en el local mediante la digitalización del proceso de reservas, compras y validaciones por parte de los administradores.

### **Alcance**
Incluye el desarrollo del backend (**API REST + MongoDB + Express**).  
No incluye frontend, interfaz de usuario ni aplicaciones móviles.

### **Metodología**
Se empleará una metodología **ágil (Scrum)**, con trabajo colaborativo entre los desarrolladores y revisión continua de avances.  
Las herramientas principales serán: **Node.js**, **Express**, **MongoDB**, **GitHub** y entornos locales de desarrollo.

### **Entregables**
- Código fuente del proyecto (repositorio GitHub).  
- Documentación técnica de la API (endpoints, modelos, instalación y uso).  
- Producto funcional instalado en el entorno acordado.  

### **Presupuesto y recursos**
- 4 desarrolladores.  
- 200 horas de trabajo distribuidas entre diseño, programación y pruebas.

### **Cronograma tentativo**

| Fase | Actividad | Duración | Entregable |
|------|------------|-----------|-------------|
| Semana 1–2 | Diseño e implementación de la API | 2 semanas | Endpoints funcionales |
| Semana 3 | Configuración y pruebas con MongoDB | 1 semana | Base de datos conectada |
| Semana 4–5 | Integración con Express y pruebas finales | 2 semanas | API operativa y documentada |

## **11. Criterios de Aceptación**

El sistema será considerado **aceptado y completado** cuando cumpla los siguientes requisitos:

1. El cliente puede **reservar y comprar productos** desde la API.  
2. El administrador puede **visualizar, aprobar o rechazar pedidos** desde los endpoints correspondientes.  
3. Todos los datos se almacenan y consultan correctamente en **MongoDB**.  
4. La API devuelve respuestas válidas (códigos de estado HTTP correctos).  
5. La documentación de endpoints está actualizada y accesible.  
6. Las pruebas unitarias y de integración se completan con éxito.

## **12. Soporte y Mantenimiento (opcional)**

Se ofrece:  
- **Inducción inicial:** sesión de capacitación para el uso e instalación del sistema.  
- **Garantía legal de 6 meses:** incluye soporte ante errores, dudas o ajustes menores relacionados con el funcionamiento del software.  
- Posibilidad de **extender el mantenimiento** mediante un contrato adicional (actualizaciones, nuevas funciones o mejoras de seguridad).

###  **Sugerencias adicionales**
- Incluir una sección de **riesgos y mitigaciones** (por ejemplo: “riesgo de retraso por cambios en los requisitos” → mitigación: reuniones semanales de control).  
- Añadir una **sección de contacto o responsables** al final (nombre, rol, correo).  
- Si es para un cliente, agregar logotipo y datos de la empresa.

## 13. Próximos Pasos

Una vez aprobados los requerimientos y el alcance del MVP definidos en este documento, el equipo procederá con las siguientes fases:

### 13.1 Fase de Diseño Funcional y Técnico (Entrega 2)

El siguiente gran hito es la creación del documento `DISENO.md`, que incluirá:

* **Diagramas Visuales:** Creación de diagramas de casos de uso y el diagrama de arquitectura técnica (API, MongoDB, Redis, Docker).
* **Modelo de Datos:** Definición detallada de las colecciones y esquemas de Mongoose, incluyendo el esquema de `users` y las relaciones principales.
* **Diseño de API:** Especificación de los endpoints RESTful principales (rutas, métodos, permisos y estructuras de datos de input/output).
* **Estrategia de Caché:** Definición de qué datos se almacenarán en Redis y cómo se gestionará su invalidación.
* **Wireframes:** Creación de mockups simples para las vistas clave del sistema.

### 13.2 Configuración del Entorno de Desarrollo

En paralelo al diseño, se iniciarán las tareas de configuración técnica:

* Estructura inicial del proyecto (carpetas y archivos).
* Configuración de Docker (`docker-compose.yml`) para levantar los servicios (API, MongoDB, Redis).
* Preparación del repositorio para el trabajo colaborativo (protección de la rama `develop`, plantillas de Pull Request).

### 13.3 Planificación del Sprint 1

Basado en el MVP, se desglosarán las primeras historias de usuario y tareas técnicas en el backlog. El Sprint 1 se enfocará en:

* Autenticación (Login/Registro).
* CRUD básico del recurso principal (ej. `products`).
* Escalabilidad: soporte para minimo 800 usuarios simultaneos  
