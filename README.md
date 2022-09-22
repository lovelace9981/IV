# Infraestructura Virtual - Pedro Antonio Mayorgas Parejo Curso 2022-2023.

---

## Clientes potenciales: Empresas de venta online.

### Problema:

El proceso de asignación para comprobación de productos devueltos de una empresa de venta online, se hace de manera manual y sin tener en cuenta la carga de trabajo pendiente del técnico especializado en el producto devuelto teniendo más técnicos disponibles perdiendo mucho tiempo.

### Solución:

El sistema en cuanto se haya aprobado la devolución de un producto, debe obtener el valor de a qué clase de técnico especializado debe asignarse. Una vez que obtiene la clase de técnico especializado, debe obtener la lista de colas de los técnicos que hay actualmente y seleccionar automáticamente al menos ocupado que hay disponible.

### Lógica:

Asignación por colas de productos devueltos a técnicos especializado en este. Método de balanceo de carga de menos ocupado.

### ¿Por qué en la nube?

La empresa puede tener más de un almacen de recepción de productos devueltos y el software debe estar preparado para la asignación de esos productos a los técnicos del almacen en el que se encuentren.

### Datos que deben ser aportados por las empresas que administran el software.

Relación de producto con especialidad del técnico.

Suposiciones, el paquete ya se ha escaneado por otros medios y se encuentra registrado en una cola de espera general.

### Estado del proyecto

* [X] Objetivo 0 

Se ha definido ya el proyecto y la lógica de negocio.

* [X] Objetivo 1

Se ha definido las user histories y los milestone MVP.

---
