# League Static

[![License: AGPL v3](https://img.shields.io/badge/License-AGPL%20v3-blue.svg)](https://www.gnu.org/licenses/agpl-3.0)
[![Build Status](https://travis-ci.org/PFeynman/proyecto-iv.svg?branch=master)](https://travis-ci.org/PFeynman/proyecto-iv)
[![Deployment](https://www.herokucdn.com/deploy/button.svg)](https://league-static.herokuapp.com/status)
[![Build DockerHub](https://img.shields.io/badge/build-DockerHub-blue.svg?logo=docker)](https://hub.docker.com/r/pfeynman/proyecto-iv/)

Repositorio del proyecto desarrollado a lo largo de la asignatura Infraestructura Virtual de 4º del Grado de Ingeniería Informática en la Universidad de Granada.

El proyecto se tratará de un servicio para consultar datos estáticos del videojuego League of Legends.

## Instalación

Descaragar el repositorio y ejecutar _npm install_ 
Para utilizar la app, ejecutar _npm start_

## Clases

### Routes

Esta [clase](https://github.com/PFeynman/proyecto-iv/blob/master/src/routes/routeProvider.ts) define las rutas de la API y realiza la llamada a las funciones que gestionan las peticiones que se realicen. Estas funciones están en la clase [ChampionAPI](https://github.com/PFeynman/proyecto-iv/blob/master/src/routes/Champions-API.ts) e [ItemAPI](https://github.com/PFeynman/proyecto-iv/blob/master/src/routes/Items-API.ts). Se encargan de devolver todos los campeones/ítems o uno concreto identificado por su _id

### Modelos
El modelo [Champion](https://github.com/PFeynman/proyecto-iv/blob/master/src/models/champion.ts) almacena el **_id**, el **nombre** y el **título** de los diferentes campeones. También he creado la interfaz IChampion para trabajar fácilmente con los objetos de campeones y las respuestas de la base de datos.

El modelo [Item](https://github.com/PFeynman/proyecto-iv/blob/master/src/models/item.ts) almacena el **_id**, el **nombre** de los objetos, así como los objetos en los que puede convertirse un objeto. También he creado la interfaz IItem para trabajar fácilmente con los objetos de ítems y las respuestas de la base de datos.

Para testearlas es necesario instalar las dependencias con _npm install_ y ejecutar los tests con '''npm run test'''.

## Documentación
* [Herramientas utilizadas](https://github.com/PFeynman/proyecto-iv/blob/master/doc/herramientas.md)
* [Despliegue en Heroku](https://github.com/PFeynman/proyecto-iv/blob/master/doc/despliegue.md)
* [Despliegue usando Docker](https://github.com/PFeynman/proyecto-iv/blob/master/doc/docker.md)
* [Añadir imagen a DockerHub](https://github.com/PFeynman/proyecto-iv/blob/master/doc/dockerhub.md)
* [Despliegue final de la aplicación](https://github.com/PFeynman/proyecto-iv/blob/master/doc/despliegue_final.md)

## Despliegue

* **/status** muestra el estado (OK) y el resto de rutas disponibles.
* **/champions** mostrará todos los campeones disponibles.
* **/champion/:id** mostrará información de un campeón específico.
* **/items** mostrará todos los objetos disponibles.
* **/item/:id** mostrará información de un objeto específico.

Contenedor: https://league-static.herokuapp.com/status

Despliegue final: 142.93.235.169

## Authors

* __Pablo Rey__ - _Creador y contribuidor principal_ - [GitHub](https://github.com/PFeynman) [Twitter](https://twitter.com/PabloRPedrosa)
