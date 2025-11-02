#  DISEÑO FUNCIONAL Y TÉCNICO — PRONTO CASINO UNIVERSIDAD

---

## 1. Introducción

### **1.1 Objetivo**

El objetivo de este documento es informar a los desarrolladores sobre la creación del software, detallando los aspectos funcionales y técnicos, acompañados de diagramas que eviten cualquier confusión durante el desarrollo.  
En este caso, se aborda la creación de una **API que permita realizar operaciones CRUD** dentro de un **casino universitario**, construyendo únicamente el motor que opera detrás del sistema (backend).

---

### **1.2 Alcance**

Este documento cubre exclusivamente el **MVP** (Producto Mínimo Viable) descrito en el documento anterior **REQUERIMIENTOS.MD**.  
El alcance incluye las siguientes funcionalidades:

- Que el cliente (registrado o invitado) pueda **buscar un producto** y **reservarlo** desde su terminal.  
- Que el **cajero** pueda **confirmar el pedido** y dar el visto bueno para su entrega.  
- Incluir un **menú de registro (Sign In)** para clientes y empleados.  
- Implementar un **sistema básico de inventario** para la gestión de productos disponibles.

---

### **1.3 Definiciones y Acrónimos**

En esta sección se presentan las definiciones y acrónimos utilizados en este documento, orientados a desarrolladores:

| **Término / Acrónimo** | **Definición** |
|--------------------------|----------------|
| **CRUD** | Crear, Leer, Actualizar y Borrar (Create, Read, Update, Delete). |
| **API** | *Application Programming Interface*: conjunto de funciones y procedimientos que permiten la interacción entre aplicaciones. |

---

## 2. Descripción general

### **2.1 Resumen del sistema**

La aplicación consiste en un sistema para **reservar productos alimenticios** en un local tipo **casino universitario**.  
El cliente puede **seleccionar y reservar productos** desde su dispositivo móvil, acudir al local, **pagar** (mediante Transbank o efectivo) y **retirar su pedido**, optimizando el flujo de atención y aumentando las ventas al reducir los tiempos de espera.

---

### **2.2 Contexto y entorno**

El sistema está diseñado para su uso en **dispositivos móviles**.  
El flujo básico es el siguiente:

1. El cliente **abre la aplicación**, se **registra o inicia sesión**.  
2. **Visualiza los productos** disponibles y **realiza una reserva**.  
3. Acude al **mostrador**, donde el **cajero confirma y cobra** la orden.  
4. Finalmente, el cliente **recibe su producto**.

**Restricciones actuales:**
- La aplicación **no cuenta con una versión web**.  
- La interfaz se utilizará en entorno de **prueba local (development environment)**.

---

### **2.3 Usuarios y roles**

#### **2. Usuarios y Perfiles (Roles)**

| **Rol** | **Descripción** | **Permisos Principales** |
|----------|------------------|---------------------------|
| **Administrador** | Supervisa y controla todas las operaciones del sistema. | - Crear, editar y eliminar usuarios.<br>- Gestionar categorías de productos.<br>- Ver y exportar reportes de ventas.<br>- Configurar parámetros generales del sistema.<br>- Acceso completo a todos los módulos. |
| **Vendedor** | Gestiona el inventario y las operaciones de venta diarias. | - Crear y editar productos.<br>- Ver órdenes pendientes y marcarlas como listas.<br>- Consultar historial de ventas propias.<br>- Gestionar stock y actualizar precios. |
| **Usuario / Cliente** | Comprador final que interactúa con la plataforma para adquirir productos. | - Registrarse e iniciar sesión.<br>- Ver productos y sus detalles.<br>- Agregar productos al carrito.<br>- Realizar compras y pagos.<br>- Consultar historial de pedidos.<br>- Actualizar su información personal. |

---

## 3. Requisitos funcionales

> *Esta sección se completará con el detalle de cada funcionalidad (CRUD de productos, reservas, registro de usuarios, control de inventario y flujo de ventas), junto con sus casos de uso y diagramas correspondientes.*

---










