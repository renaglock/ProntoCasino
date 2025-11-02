# DISEÑO FUNCIONAL Y TÉCNICO DE PRONTO CASINO UNIVERSIDAD


# 1. Introducción

**1.1 Objetivo**

El objetivo de este documento es principalmente informar a nuestros desarroladores en que consiste la creacion de este software, detallado con diagramas para que no exista ninguna confucion al respecto a la hora de desarrolar, en este caso, la creacion de una API que pueda realizar CRUD en un casino universitario, creando solo el motor que está detrás (backend).

**1.2 Alcance**

En este documento solo será efectiva y detallada el MVP mostrado en el anterior documento (REQUERIMIENTOS.MD), en este caso será solamente,  que el cliente pueda buscar un producto y reservarlo desde su terminal (Puede ser un cliente o un invitado), Que el cajero pueda dar el visto bueno y confirmar el pedido para posteriormente ser entregado, Incluir un menú de registro (Sign in) y un sistema de inventarios.

**1.3 Definiciones y acrónimos**

En este apartado del documento se mostrará las deficiones que usaremos en este trabajo y tambien acronimos representativos para el entendimiento de este documento, obviamente orientado a desarrolladores. 

*CRUD: Crear, Leer, Actualizar y Borrar*

*API: Application Programming Interface*

# 2. Descripción general

**2.1 Resumen del sistema**

La applicacion consiste en la reserva de productos alimenticios en un local tipo casino universitario, generando la reserva del producto, puede ir directo al local, pagar y retirar, generando ganacias a la empresa por muchos clientes que no tienen tiempo para selecionar en el mismo local. 

**2.2 Contexto y entorno**

El sistema se usa con el telefono celular, cliente abre la APP, se registra y puede ver una seleccion de productos, luego de reserva debe ir a la caja donde hace efectiva la venta usando la maquina transbank o pagando en efectivo y ya como uiltimo el cliente recive su producto. Dentro de las restricciones de entorno de momento la APP no cuenta con interfaz web desde el computador o sistema android o IOS.


**2.3 Usuarios y roles**

## **2. Usuarios y Perfiles (Roles)**

| **Rol** | **Descripción** | **Permisos Principales** |
|----------|------------------|---------------------------|
| **Administrador** | Supervisa y controla todas las operaciones del sistema. | - Crear, editar y eliminar usuarios.<br>- Gestionar categorías de productos.<br>- Ver y exportar reportes de ventas.<br>- Configurar parámetros generales del sistema.<br>- Acceso completo a todos los módulos. |
| **Vendedor** | Gestiona el inventario y las operaciones de venta diarias. | - Crear y editar productos.<br>- Ver órdenes pendientes y marcarlas como listas.<br>- Consultar historial de ventas propias.<br>- Gestionar stock y actualizaciones de precios. |
| **Usuario / Cliente** | Comprador final que interactúa con la plataforma para adquirir productos. | - Registrarse e iniciar sesión.<br>- Ver productos y sus detalles.<br>- Agregar productos al carrito.<br>- Realizar compras y pagos.<br>- Consultar historial de pedidos.<br>- Actualizar su información personal. |


# 3. Requisitos funcionales










