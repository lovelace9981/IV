### [M1] Estructuras de datos para la lógica de negocio.

Las estructuras de datos que deben contener la información necesaria para poder realizar la lógica de negocio:

1. Estructura de datos Técnico:
* Identificador del departamento de revisión al que pertenece.
* Información de la carga actual, inicialmente ninguna.
* Cola de Productos Pendientes de revisión.

2. Estructura de datos Departamentos:
* Identificador del departamento. 
* Subesctructura contenedora de los técnicos.

3. Estructura de datos Productos pendientes de revisión
* Información del departamento de revisión objetivo.
* Identificador del producto. 

---

### [M2] Lógica de negocio

A partir de las estructuras de datos anteriores, se procede a la búsqueda y asignación del primer producto pendiente, al Técnico del departamento relacionado con el producto, con menor carga de trabajo disponible.

---

### [M3] Obtención de las tareas asignadas al empleado mediante una API.

A partir del milestone anterior de la lógica de negocio, se expone una API que según el identificador pasado como parámetro se devuelve la carga asignada al trabajador.

---

### Milestones en GitHub: 

https://github.com/lovelace9981/IV/milestones
