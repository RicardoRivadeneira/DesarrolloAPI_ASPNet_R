# DesarrolloAPI_ASPNet_R

## Descripción

Este proyecto utiliza una API RESTful creada con ASP.NET Core y basada en un tutorial del canal de YouTube Codigo Estudiante. La API está diseñada para gestionar productos almacenados en una base de datos de SQL Server que se encuentra en un contenedor Docker.

## Uso de la API

### Conexión a la Base de Datos

El tutorial proporcionó el código necesario para establecer la conexión con la base de datos Oracle a través de un contenedor Docker. Esto permite realizar operaciones CRUD en la tabla de productos desde la API.

### Seguridad y Autenticación

La seguridad en la API se ha implementado utilizando middleware y tokens JWT (JSON Web Tokens). Para acceder a los datos de productos a través de solicitudes GET, primero se debe solicitar un token de autenticación a través de una solicitud POST. Una vez obtenido el token, se debe incluir en la cabecera de autorización de las solicitudes GET para obtener acceso a los datos protegidos.

### Uso de Thunder en Visual Studio Code

La extensión Thunder en Visual Studio Code facilita la realización de solicitudes HTTP a la API. Es especialmente útil para simular las solicitudes POST y GET necesarias para la autenticación y la obtención de datos.

## Requisitos de Autenticación

1. **Obtener un Token de Acceso:** Enviar una solicitud POST al endpoint de autenticación con las credenciales adecuadas para recibir un token de acceso.
2. **Incluir el Token en las Solicitudes GET:** Al realizar una solicitud GET para obtener la lista de productos, incluir el token obtenido en la cabecera de autorización de la solicitud para acceder a los datos protegidos.

## Ejemplo de Uso

Para obtener acceso a la lista de productos:
1. Realizar una solicitud POST al endpoint de autenticación para obtener un token.
2. Copiar el token obtenido.
3. Realizar una solicitud GET a la lista de productos utilizando Thunder en Visual Studio Code.
4. En la cabecera de la solicitud GET, agregar el token como parte del encabezado de autorización.

## Recursos Adicionales

- [[Enlace al tutorial del canal de YouTube Codigo Estudiante](https://www.youtube.com/watch?v=3NJbzf-41f0)](#) (Enlace al video/tutorial utilizado como referencia para la implementación).
