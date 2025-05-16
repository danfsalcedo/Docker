# Comandos de Docker

Este documento organiza los comandos esenciales de Docker en categorías para la gestión de contenedores, imágenes, volúmenes, redes y Docker Compose. Cada comando incluye una descripción y, cuando aplica utilizamos ejemplos para mayor claridad.

---

## 🐳 Gestión de Contenedores

| Comando                            | Descripción                                                                | Ejemplo                                       |
|------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------|
| `docker --version` o `docker -v`   | Muestra la versión de Docker instalada.                                    | `docker --version`                            |
| `docker ps`                        | Lista todos los contenedores en ejecución.                                 | `docker ps`                                   |
| `docker ps -a`                     | Lista todos los contenedores, incluyendo los detenidos.                    | `docker ps -a`                                |
| `docker run <imagen>`              | Crea y ejecuta un contenedor desde una imagen. Usa `-it` para terminal interactiva, `-d` en modo detached, `--rm` para eliminar al salir, y `-p <puerto_host>:<puerto_contenedor>` para mapear puertos. | `docker run -it ubuntu bash`<br>`docker run -d -p 80:80 rancher/hello-world`   |
|`-d` |ejecuta el contenedor por debajo para poder seguir digitando comandos en la misma terminal que tenemos abierta(libera la terminal)| ` docker run mi_ contenedor -d`|
| `docker start <contenedor>`        | Inicia un contenedor detenido por nombre o ID.                             | `docker start mi_contenedor`                  |
| `docker stop <contenedor>`         | Detiene un contenedor en ejecución por nombre o ID.                        | `docker stop mi_contenedor`                   |
| `docker rm <contenedor>`           | Elimina un contenedor. Debe estar detenido, a menos que se use `--force`.  | `docker rm mi_contenedor`                     |
| `docker exec -it <contenedor> bash`| Abre una terminal interactiva en un contenedor en ejecución.               | `docker exec -it mi_contenedor bash`          |
| `docker attach <contenedor>`       | Se conecta al terminal de un contenedor en ejecución.                      | `docker attach mi_contenedor`                 |
| `docker stats`                     | Muestra en tiempo real el uso de recursos de los contenedores (CPU, memoria).| `docker stats`                              |
| `exit`                             | Sale del terminal interactivo de un contenedor.                            | `exit`                                        |

---

## 📦 Gestión de Imágenes

| Comando                             | Descripción                                                                | Ejemplo                                      |
|-------------------------------------|----------------------------------------------------------------------------|----------------------------------------------|
| `docker images`                     | Lista todas las imágenes almacenadas localmente.                           | `docker images`                              |
| `docker rmi <imagen>`               | Elimina una imagen. Primero deben eliminarse los contenedores que la usan. | `docker rmi ubuntu`                          |
| `docker pull <imagen>[:tag]`        | Descarga una imagen desde un registro (ej. Docker Hub).                    | `docker pull debian:latest`                  |
| `docker search <imagen>`            | Busca imágenes en Docker Hub.                                              | `docker search ubuntu`                       |
| `docker build --pull --rm -f <Dockerfile> -t <nombre_imagen> <ruta>` | Construye una imagen desde un Dockerfile. `--pull` obtiene la imagen base más reciente. `--rm` elimina contenedores intermedios. | `docker build --pull --rm -f docker-compose/docker-files/ubuntu-mysql/Dockerfile -t ubuntu-mysql docker-compose/docker-files/ubuntu-mysql` |

---

## 💾  Gestión de Volúmenes

| Comando                              | Descripción                                                                | Ejemplo                                     |
|--------------------------------------|----------------------------------------------------------------------------|---------------------------------------------|
| `docker volume ls`                   | Lista todos los volúmenes de Docker.                                       | `docker volume ls`                          |
| `docker volume inspect <volumen>`    | Muestra información detallada sobre un volumen.                            | `docker volume inspect mi_volumen`          |
| `docker volume rm <volumen>`         | Elimina un volumen. No debe estar en uso por ningún contenedor si no primero borrar el contenedor para poder borrar el volumen, pero al parecer ya esta pacheado el poder eliminar un volumen asociado.            | `docker volume rm mi_volumen`               |
| `docker volume prune`                | Elimina todos los volúmenes no utilizados.                                 | `docker volume prune`                       |

---

## 🌐 Gestión de Redes

| Comando                       | Descripción                                                          | Ejemplo                                                  |
|-------------------------------|----------------------------------------------------------------------|----------------------------------------------------------|
| `docker network ls`           | Lista todas las redes de Docker.                                     | `docker network ls`                                      |
| `docker network prune`        | Elimina todas las redes no utilizadas que no estan asosciadas a ningun contenedor.| `docker network prune`                      |
| `docker inspect <contenedor>` | Muestra información detallada de un contenedor, incluyendo la IP y configuracion de red. | `docker inspect mi_contenedor`                           |

---

## 🧩 Docker Compose

| Comando                            | Descripción                                                               | Ejemplo                                        |
|------------------------------------|---------------------------------------------------------------------------|------------------------------------------------|
| `docker-compose`                   | Administra aplicaciones multicontenedor definidas en un archivo `docker-compose.yml`. | `docker-compose up -d`             |
| `apt install docker-compose`       | Instala Docker Compose en sistemas Linux.                                 | `sudo apt install docker-compose`              |

---

## 📝 Para tomar en cuenta

- **Nombrar Contenedores:** Usamos `--name <nombre>` para asignar un nombre personalizado a un contenedor 

  Ejemplo: `docker run --name mi_contenedor -it ubuntu bash`.

- **Mapeo de Puertos:** Usamos `-p <puerto_host>:<puerto_contenedor>` para exponer puertos del contenedor al host
 
  Ejemplo: `-p 80:80` o `3306:3307`.
  
- **Verificar el Sistema Operativo del Contenedor:** Ejecuta `cat /etc/os-release` dentro del contenedor.
  
- **Red Bridge vs Host:** La red `bridge` (predeterminada) aísla los contenedores para mayor seguridad. La red `host` utiliza la red del host, lo que puede ofrecer mayor rendimiento, pero menos aislamiento.

---
