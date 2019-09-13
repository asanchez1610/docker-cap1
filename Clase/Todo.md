# Introduccion a Docker

* Docker nos permite ejecutar aplicaciones en "espacios unicos" ( microservicios )
* Linux/Windows
* Escalabilidad 

## Imagenes 

Las imágenes en Docker, vienen a ser el corazón para un contenedor, es decir, sin la imagen el contenedor no puede existir.
Las imagenes albergan un sistema operativo, una aplicacion, un sandbox, etc. 
Por medio de las imagenes podemos personalizarlas para crear desarrollos personalizados. 
Dentro de una imagen podemos indicarle que puerto usar así como la ejecución de un script de requerirse.
Multi-stage ( ejecución de n-imagenes para obtener una imagen resultante deseada ) 

### Comandos/Imagenes 

* Para buscar imagenes: 
> docker search mongo 

**OBS**

Docker Hub, es el repositorio publico que usa Docker para poder descargar imagenes, no obstante tambien podemos tener nuestro propio **registry**

* Para descargar una imagen:
> docker pull mongo 

* Para listar una imagen descargada: 
> docker image ls // docker images

**OBS**

Desde la version 18.X de Docker se incorpora que "images" liste directamente imagenes sin depender de *ls* 

* Para borrar una imagen
> docker rmi ID_IMAGEN

## Contenedores

* Los contenedores son "espacios" donde una aplicación puede "existir" mediante una imagen predeterminada o pre-definida.
* "La imagen es  la punta de lanza para el contenedor".
* Un contenedor para una aplicación.
* Podemos asignar recursos definidos como %CPU, %RAM a los contenedores. 

## Comandos/Contenedores

* Para iniciar un contenedor:
> docker run mongo 

* Para ver el estado de un contenedor: 
> docker ps -a  // docker container ls -a // docker container ps -a 

* Para detener un contendor:
> docker stop ID_CONTAINER

* Para iniciar un contenedor en base a un nombre:
> docker run --name db_mongo mongo

* Para iniciar un contenedor en background:
> docker run -dit --name db_mongo mongo

* Para eliminar un contenedor:
> docker rm -fv ID_CONTAINER

### TIP

* Para borrar contenedores en una sola linea:
>  docker rm -fv $(docker ps -qa) 

* Para ver el detalle de un contenedor:
> docker inspect ID_CONTAINER 

**OBS**

Se pueden aplicar filtros, por ejm. docker inspect ID_CONTAINER | grep IPA 

* Para ver el log que se ejecuta dentro de un contenedor: 
> docker logs ID_CONTAINER 

* Para entran en un contendor:
> docker exec -it ID_CONTAINER bash 

* Para ejecutar un comando en un contenedor sin acceder a el:
> docker exec ID_CONTAINER mkdir -p /tmp/prueba  ||  docker exec ID_CONTAINER ls -lta /tmp 


# REDES 



# VOLUMENES


Segunda Parte
[segunda parte](https://github.com/kdetony/docker-practico)


