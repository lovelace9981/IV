### [M1] API de ingestión de datos que obtenga de los depósitos de datos que haya disponibles, los productos pendientes de revisión.

Se define una API que permita recibir datos desde los depósitos de datos del almacen, la información de los productos pendientes de revisión. Almacenándose temporalmente en un depósito de datos propio intermedio. La API de ingestión solo acepta los siguientes datos:

Identificador del producto devuelto.
Tag de departamento adecuado para su revisión.

---

### [M2] Módulo preprocesamiento de los datos de los productos pendientes de revisión y generador de la estructura de datos de estos.

A partir del milestone anterior como entrada de datos, se define un módulo que tiene como objetivo preparar las estructuras de datos necesarias para que el balanceo de carga realice asignaciones de revisión a los técnicos del departamento objetivo. 

El módulo genera una estructura de datos, que define como clave el departamento y una cola de productos pendientes de revisión.

---

### [M3] API de ingestión de los trabajadores en activo para el balanceo de carga.

Se define una API que permita recibir desde los depósitos de datos del almacen, la información de los trabajadores en activo para revisión. S
En concreto la estructura de datos definida es como sigue:

Identificador de trabajador
Departamento

---

### [M5] Módulo de preprocesamiento de los datos de los trabajadores y generador de la estructura de datos de estos.

Método que dada la información ingresada en la API en el milestone 3 de los trabajadores, permita clasificar a los trabajadores en una super-estructura de datos clasificada por departamento, para hacer más eficiente el trabajo del balanceador. En concreto se define una lista de trabajadores del departamento y a los trabajadores se le asocia una cola de productos pendientes.

---

### [M6] Módulo de balanceo de carga.

Se define el módulo de balanceo de carga como clase, que dada las estructuras de datos introducidas y generadas por los métodos y APIs de los milestone sucesivos. Realice las asignaciones de productos a revisar, al trabajador del deparamento adecuado y que el trabajador sea el que menor número de productos pendientes tenga. Todo ello alterando la estructura de datos que hay generada de Departamento-Empleado y la de productos pendientes.

---

### [M7] API de obtención de datos de productos pendientes del trabajador.

API que partiendo de la estructura de departamentos de los trabajadores generada en el milestone 4, obtiene los datos y genera en un formato universal, los productos pendientes por revisar de un trabajador que se le indique.

---

### [M8] API que permite la obtención del listado de tareas pendientes de todo un departamento.

Método que permite a partir de los datos del milestone 4, muestre la información de tareas pendientes de todo un departamento filtrada y ordenada en, Trabajador - Producto pendiente de revisión, generada en un formato universal.

---

### Milestones en GitHub: 

https://github.com/lovelace9981/IV/milestones
