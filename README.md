Reportes Ciudadanos con Vue.js

Situación problemática

En San Miguel muchas personas cuando ven accidentes, calles dañadas o emergencias lo publican en redes sociales o lo comentan con otras personas, pero no hay un lugar donde se guarde toda esa información de forma ordenada.

Esto hace que muchas veces los problemas no sean atendidos porque se pierden entre tantas publicaciones o no llegan a las autoridades.

Sectores a los que va dirigido

Esta aplicación puede servir para:
- Personas de la comunidad
- Alcaldía
- Instituciones de emergencia

Solución

Se hizo una página web donde las personas pueden registrar reportes de problemas.

La persona escribe el título, una descripción y selecciona el tipo de problema. Luego ese reporte se guarda en una lista donde se puede ver y también eliminar.

Esto ayuda a tener mejor control de los problemas.

Funciones del sistema

- Agregar reportes
- Ver lista de reportes
- Validar que no estén vacíos los campos
- Eliminar reportes

¿Qué es Vue.js y cuál es su función?

Vue.js es una herramienta de JavaScript que sirve para hacer páginas web interactivas. En este proyecto se utilizó para manejar los datos y actualizar la pantalla sin recargar la página.

Variables reactivas utilizadas

- titulo: guarda el título
- descripcion: guarda la descripción
- tipo: guarda el tipo de problema
- reportes: guarda todos los reportes
- error: muestra mensajes si algo está mal
- tituloPagina: muestra el título principal

Diferencia entre v-bind y v-model

v-bind se usa para conectar datos con atributos HTML.
v-model se usa para que los inputs guarden lo que el usuario escribe.

Evento utilizado

Se utilizó el evento click para agregar y eliminar reportes.

Uso de v-for

Se usa para mostrar la lista de reportes que el usuario va agregando.

Uso de v-if

Se usa para mostrar un mensaje de error cuando los campos están vacíos.

Validación de datos

Se verifica que los campos no estén vacíos antes de guardar un reporte. Esto es importante para evitar información incompleta.

integrantes: Jasson ali ramos guadique SMSS041323
             Melvin Alexis Jiménez López SMIS093020