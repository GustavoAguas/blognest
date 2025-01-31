# Blog Personal Nest

Este es un proyecto de blog personal desarrollado con NestJS.

## Descripción

Este proyecto es un blog personal desarrollado utilizando el framework NestJS, que permite a los usuarios **crear**, **leer**, **actualizar** y **eliminar** **publicaciones**. Además, se ha implementado la funcionalidad de comentarios, permitiendo a los usuarios interactuar y dejar comentarios en las publicaciones. Utiliza una arquitectura modular y está diseñado siguiendo los principios de RESTful API.

## Funcionalidades

- Crear una nueva publicación
- Leer una publicación existente
- Actualizar una publicación existente
- Eliminar una publicación existente
- Comentar en una publicación

## Tecnologías utilizadas

- NestJS
- TypeScript
- UUID

## Instalación

1. Clona este repositorio: `git clone https://github.com/GustavoAguas/blognest.git`
2. Instala las dependencias: `npm install`

## Uso

1. Inicia el servidor de desarrollo: `npm run start:dev`
2. Realiza las peticiones HTTP utilizando tu herramienta favorita como Thunder Client.

## Endpoints

- `GET /posts`: Obtener todas las publicaciones
- `GET /posts/:id`: Obtener una publicación por su ID
- `POST /posts`: Crear una nueva publicación
- `PUT /posts/:id`: Actualizar una publicación existente
- `DELETE /posts/:id`: Eliminar una publicación existente
- `GET /posts/:postId/comments`: Obtener todos los comentarios de una publicación
- `POST /posts/:postId/comments`: Crear un nuevo comentario en una publicación

## Implementación de la funcionalidad de comentarios

La funcionalidad de comentarios se implementó mediante la creación de un nuevo módulo de comentarios (`CommentsModule`), que contiene un controlador (`CommentsController`) y un servicio (`CommentsService`). El controlador maneja las solicitudes HTTP relacionadas con los comentarios, mientras que el servicio se encarga de la lógica de negocio para gestionar los comentarios.

El modelo de comentario (`Comment`) define la estructura de los comentarios, incluyendo su ID, el ID de la publicación a la que pertenecen y el contenido del comentario.

Al realizar una solicitud `POST /posts/:postId/comments`, se crea un nuevo comentario asociado a la publicación específica identificada por `:postId`. El servicio de comentarios genera un ID único para el comentario y lo almacena junto con el contenido del comentario y el ID de la publicación.

## Tarea Sugerida
Siguiendo los pasos del tutorial se puedo crear el proyecto propuesto y funcionó correctamente.

## Mejoras Futuras

- [❌] Agregar autenticación y autorización para proteger las rutas y los recursos.
- [❌] Mejorar la validación de datos en las solicitudes POST y PUT.

## Sugerencia

¡Antes de clonar o realizar un fork de este repositorio, te animamos a que intentes crear el proyecto desde cero siguiendo el [tutorial](tutorial.md)!

## Contribuyendo

¡Las contribuciones son bienvenidas! Si tienes alguna sugerencia, mejora o corrección, por favor crea un pull request.

## Licencia

Este proyecto está bajo la licencia [MIT](LICENSE).
