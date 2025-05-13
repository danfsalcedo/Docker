# Docker

`docker --version`
sirve para visualizar la version de docker

`docker ps`
nos muestra los contenedores que estan en ejecuccion

las imagenes son los sistemas operativos (ejemplo "ubuntu")

app que la maquina esta corriendo

`docker stop (nombre del contenedor o ID del contenedor)`
Inicia el contenedor que se especifica con el nombre

`docker start (nombre del contenedor o ID del contenedor)`
Detiene el contenedor que se especifica con el nombre
`docker ps -a` 
Muestra los contenedores tanto los que estan en ejecccion como las que no


`docker run -it ubuntu bash` para que se tenga una imagen de ejemplo de los comandos
`docker container run` sirve para ejecutar un contenedor
el alias de este comando es 
`docker run` se usa mas comunmente este
`docker compose` tambien sirve para ejecutar un contenedor pero se le pueden adicionar muchas mas configuraciones
`docker run -t --rm -p 80:80 rancher/hello-world` 
el primer 80 cambia el puerto para que se vea por fuera
el segundo 80 

`exit` comando para salir del contenedor

`cat /etc/os-release`
sirve para revisar si se conecto a nuestro contenedor

`-t` conctarme a la terminal de ese volumen

`--rm` elimina el contenedor automaticamente y elimina los volumenes que exsitan

el volumen es el disco duro 
la vm puede tener volumen

`docker container -rm (numero o nombre del contenedor)` sirve para eliminar los contenedores
el alias seria:
`docker rm (numero o nombre del contenedor` 

`docker images`
nos muestra las imagenes que se tienen descargadas

`docker rmi (numero o nombre del contenedor)`
elimina la imagen

`docker excec -it (codigo hash del contenedor) bash`
se usa para conectarnos a una terminal de ese contenedor

`--name` nombre personalizado al contenedor

`-d` ejecuta el contenedor por debajo para poder seguir digitando comandos en la misma terminal que tenemos abierta(libera la terminal)


`--name` le puedo dar un nombre personalizado a mi contenedor

## Comandos Linux 

`cat`
nos permite visualizar el contenido de algun archivo

`sudo`
nos otorga privilegios de administrador temporalmente

`sudo apt update`  
baja las librerias de los repositorios que tiene que actualizar 

`sudo apt upgrade` 
permie descargar las librerias para actualizar

`pwd`
Muestra el PATH, muestra donde estamos ubicados actualmente

`cd/`
Volver ala raiz del disco duro 

`ls`
Muestra la lista de contenido del directorio 

`ls -a`
Muestra las carpetas y archivos ocultos 

`ls -l `
Muestra lo mismo que el comando "ls -a" pero de forma mas detallada 

`cd : nombre de la carpeta `
Ingresar a una carpeta (Dandole a tabulador antes de enviar la carpeta se muestra lo que esta dentro de la carpeta)

`cd..` 
para devolver una carpeta atras

`clear ` 
Limpiar pantalla

`mkdir nombre`
Crear una carpeta

`touch`
crear un archivo

`man "Nombre de comando"`
Ayuda de ese comando

`tree`
Muestra la estructura de carpetas en forma de un arbol

`remove docker compose`
borrar 

`apt install docker-compose`
instalar docker

`mkdir nombre`
crear carpeta

`docker-compose`
instalar docker

`apt install docker.io`
instalar docker

`docker -v`
ver version de docker

`git status`
ver en que area està

`git add .`
los archivos pasan a la siguiente area

`git commit -m "mensaje"`
para enviar commit

`git push`
para hacer push

`htop`
sirve para ver los procesos de la maquina

`sudo apt install htop`
para instalar htop

## Comandos Windows

`DIR`

Muestra la lista del contenido del directorio 

`cd : nombre de la carpeta `

Ingresar a una carpeta (Dandole a tabulador antes de enviar la carpeta se muestra lo que esta dentro de la carpeta)

`cd..` 

para devolver una carpeta atras

`cd /`

Volver a la raiz del disco duro

`sudo mkdir nombre`

Crear una carpeta

`cls ` 

Limpiar pantalla

`mkdir nombre`

Crear una carpeta
