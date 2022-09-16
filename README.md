# Infraestructura Virtual - Pedro Antonio Mayorgas Parejo Curso 2022-2023.

## Lógica de negocio. Problemas planteados.

Las empresas potenciales, son empresas minoristas o mayoristas que venden productos a otras empresas o clientes. Las cuales tienen dos necesidades clave para el funcionamiento de sus negocios.

### Objetivo 1: Gestión, filtrado, etiquetado y clasificación de prioridad de las peticiones o incidencia de los clientes relacionadas con los productos.
---
La empresa tiene que gestionar cientas de peticiones/incidencias relacionadas con diferentes pedidos realizados por sus clientes. La empresa pierde mucho tiempo intentando clasificar de manera manual si dicha petición/incidencia entrante nueva, debe tener una prioridad mayor, media, poca,... Entonces el sistema de prioridad clasifica en base a los siguientes parámetros de mayor a menor prioridad: 

<ul>
    <li>El cliente tiene una media de gasto alta/baja</li>
    <li>El cliente hace compras recurrentes del pedido del mismo tipo en un periodo a elegir por la empresa que utilice el software.</li>
    <li>El pedido realizado es caro/o no. Con caro, se determina en el sistema si está en el cuartil 3 de la estadística de los presupuestos de los pedidos.</li>
    <li>Si la petición se ha recibido desde hace cierto tiempo, conforme pase cierto tiempo, se incrementa la prioridad para responderla para que no muera de "hambre".</li>
</ul>

Para resolver este objetivo el cliente necesita un sistema de prioridad que les ayude a clasificar las peticiones y reaccionar más apropiadamente con sus clientes.

### Objetivo 2: Filtrado de datos y visualización del margen de beneficio del producto.

Las empresas suelen tener problemas a la hora de evaluar si un producto está siendo rentable, ya que los precios de los proveedores fluctúan. La empresa tiene un precio de venta a sus cliente y un porcentaje de margen de beneficio. Cuando se realiza un pedido en fábrica realizado por volumen,  quieren saber si el producto ha dejado de ser rentable porque están obteniendo un porcentaje de beneficio menor al introducido para ese producto.

Quieren tener un sistema que les indique de manera automática si ha bajado la rentabilidad y desde qué periodo de tiempo. Para decidir si dejar de pedirlo, cambiar de proveedor, etc... Antes de que les ocasione una pérdida de ingresos grande.

---
### Lenguaje y licencia utilizado para llevar a cabo el proyecto

Se usa como lenguaje Go.