### [M1] API de ingestión de datos que obtenga de los depósitos de datos que haya disponibles, los productos pendientes de revisión.

Se define una API que permita recibir datos desde los depósitos de datos del almacen, la información de los productos pendientes de revisión. Almacenándose temporalmente en un depósito de datos propio intermedio. La API de ingestión solo acepta los siguientes datos:

Identificador del producto devuelto.
Tag de departamento adecuado para su revisión.

---

### [M2] Módulo preprocesamiento de los datos de los productos pendientes de revisión y generador de la estructura de datos de estos.

A partir del M1 deposito de datos, se define un módulo que tiene como objetivo preparar las estructuras de datos necesarias para que el balanceo de carga realice asignaciones de revisión a los técnicos del departamento objetivo. 

El módulo genera una estructura de datos, que define como clave el departamento y una cola de productos pendientes de revisión.

---

### [M3] API de ingestión de los técnicos en activo para el balanceo de carga.

Se define una API que permita recibir desde los depósitos de datos del almacen, la información de los técnicos en activo para revisión. En concreto la estructura de datos definida es como sigue:

Identificador de técnico
Departamento

---

### [M4] Módulo de preprocesamiento de los datos de los técnicos y generador de la estructura de datos de estos.

Módulo que dada la información ingresada en la API en el M3 de los técnicos, clasifique a los técnicos en una super-estructura de datos que tiene como clave el departamento, para hacer más eficiente el trabajo del balanceador. La lista de técnicos se asocia a la clave del departamento y se define una cola de productos pendientes única por técnico.

---

### [M5] Módulo de balanceo de carga.

Se define el módulo de balanceo de carga como clase, que dada las estructuras de datos introducidas y generadas por los métodos y APIs de los milestone anteriores. Realice las asignaciones de productos a revisar, al téncico del departamento adecuado y que el técnico sea el que menor número de productos pendientes tenga. Todo ello alterando la estructura de datos que hay generada de Departamento-Empleado y la de productos pendientes. Añadiendo el producto a la cola del técnico y quitándola de la cola del departamento.

---

### [M6] API de obtención de productos pendientes de revisión del técnico.

API que partiendo de la estructura de departamentos de los técnicos generada en el M5, obtiene los datos y genera en un formato universal, los productos pendientes por revisar de un técnico indicado.

---

### [M7] API de obtención del listado de revisiones pendientes de todo un departamento.

API que partiendo de la misma estructura del M6, muestre la información de tareas pendientes de todo un departamento filtrada y ordenada en, Técnico - Producto pendiente de revisión, generada en un formato universal.

---

### Milestones en GitHub: 

https://github.com/lovelace9981/IV/milestones
