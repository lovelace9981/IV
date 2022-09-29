### [M1] Módulo preprocesamiento de los datos de los productos pendientes de revisión y generador de la estructura de datos de estos.

Sedefine un módulo que tiene como objetivo preparar las estructuras de datos necesarias para que el balanceo de carga realice asignaciones de revisión a los técnicos del departamento objetivo. 

El módulo genera una estructura de datos, que define como clave el departamento y una cola de productos pendientes de revisión.

---

### [M2] API de ingestión de datos que obtenga de los depósitos de datos que haya disponibles, los productos pendientes de revisión.

Se define una API que permita recibir datos desde los depósitos de datos del almacen, la información de los productos pendientes de revisión. Almacenándose temporalmente en un depósito de datos propio intermedio definido en el M1. La API de ingestión solo acepta los siguientes datos:

Identificador del producto devuelto.
Tag de departamento adecuado para su revisión.

---

### [M3] Módulo de preprocesamiento de los datos de los técnicos y generador de la estructura de datos de estos.

Módulo que prepare la estructura de datos que clasifique a los técnicos por su departamento. Tiene como clave el departamento, para hacer más eficiente el trabajo del balanceador. Se define una lista de técnicos. Luego por cada técnico se define una cola de productos pendientes única.

---

### [M4] API de ingestión de los técnicos en activo.

Se define una API que permita recibir desde los depósitos de datos del almacen, la información de los técnicos en activo para revisión y se almacena la información resultante en las estructuras de datos definidas en el M3. En concreto la estructura de datos definida es como sigue:

Identificador de técnico
Departamento

---

### [M5] Módulo de balanceo de carga.

Se define el módulo de balanceo de carga como clase, que dada las estructuras de datos generadas mediante los módulos y los datos introducidos mediante las APIs de los milestone anteriores. Realice las asignaciones de productos a revisar, al téncico del departamento adecuado y que el técnico sea el que menor número de productos pendientes tenga. Todo ello alterando las estructuras de datos que hay generadas de Departamento-Empleado y la de productos pendientes. Añadiendo el producto a la cola del técnico y quitándola de la cola del departamento.

---

### [M6] API de obtención de productos pendientes de revisión del técnico.

API que partiendo de la estructura de departamentos de los técnicos generada en el M5, obtiene los datos y genera en un formato universal, los productos pendientes por revisar de un técnico indicado.

---

### [M7] API de obtención del listado de revisiones pendientes de todo un departamento.

API que partiendo de la misma estructura del M6, muestre la información de tareas pendientes de todo un departamento filtrada y ordenada en, Técnico - Producto pendiente de revisión, generada en un formato universal.

---

### Milestones en GitHub: 

https://github.com/lovelace9981/IV/milestones
