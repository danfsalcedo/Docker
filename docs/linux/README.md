# 🐧 Comandos de Linux

Este documento organiza los comandos esenciales de Linux en categorías para la navegación por el sistema de archivos, gestión de paquetes, monitoreo de procesos y control de versiones con Git. Cada comando incluye una descripción y ejemplos cuando aplica.

---

## 💻 Navegación por el Sistema de Archivos

| Comando             | Descripción                                                                 | Ejemplo                   |
|---------------------|-----------------------------------------------------------------------------|---------------------------|
| `ls`                | Lista el contenido del directorio actual.                                  | `ls`                       |
| `ls -a`             | Lista todo el contenido, incluyendo archivos y directorios ocultos.        | `ls -a`                    |
| `ls -l`             | Lista contenido en formato detallado (permisos, propietario, etc.).        | `ls -l`                    |
| `ll`                | Alias de `ls -l`, muestra contenido detallado del directorio.              | `ll`                       |
| `cd <directorio>`   | Cambia al directorio especificado(con tabulador se muestra lo que esta dentro de la carpeta).| `cd /home/user`            |
| `cd ..`             | Sube un nivel en el árbol de directorios.                                  | `cd ..`                    |
| `cd /`              | Va al directorio raíz del sistema.                                         | `cd /`                     |
| `pwd`               | Muestra la ruta completa del directorio actual.                            | `pwd`                      |
| `mkdir <nombre>`    | Crea un nuevo directorio.                                                  | `mkdir mi_carpeta`         |
| `touch <archivo>`   | Crea un archivo vacío o actualiza la fecha de modificación si ya existe.   | `touch mi_archivo.txt`     |
| `cat <archivo>`     | Muestra el contenido de un archivo.                                        | `cat mi_archivo.txt`       |
| `tree`              | Muestra la estructura de directorios en forma de árbol.                    | `tree`                     |
| `clear`             | Limpia la pantalla del terminal.                                           | `clear`                    |

---

## 📦 Gestión de Paquetes

| Comando                         | Descripción                                                               | Ejemplo                          |
|---------------------------------|---------------------------------------------------------------------------|----------------------------------|
| `sudo`                          | Ejecuta un comando con privilegios de administrador.                      | `sudo apt update`                |
| `sudo apt update`               | Actualiza la lista de paquetes disponibles.                               | `sudo apt update`                |
| `sudo apt upgrade`              | Instala las últimas versiones de los paquetes instalados.                 | `sudo apt upgrade`               |
| `sudo apt install <paquete>`    | Instala un paquete especificado.                                          | `sudo apt install htop`          |
| `sudo apt install docker.io`    | Instala el motor de Docker en sistemas basados en Debian.                 | `sudo apt install docker.io`     |

---

## 📟 Gestión de Procesos

| Comando                     | Descripción                                                                 | Ejemplo                          |
|-----------------------------|-----------------------------------------------------------------------------|----------------------------------|
| `htop`                      | Muestra una vista interactiva de procesos para monitoreo del sistema.       | `htop`                           |
| `sudo apt install htop`     | Instala el programa `htop`.                                                 | `sudo apt install htop`          |
| `ifconfig`                  | Muestra la configuración de las interfaces de red (obsoleto en algunas distros). | `ifconfig`                  |

---

## 📝 Notas

- **Autocompletado con Tab:** Pulsa la tecla `Tab` para autocompletar nombres de archivos o directorios al usar comandos como `cd`.

- **Ayuda de Comandos:** Usamos `man <comando>` para ver la página del manual de cualquier comando (por ejemplo: `man ls`).

- **Información de Red:** En sistemas Linux modernos, se recomienda usar `ip addr` en lugar de `ifconfig` para obtener información de red.

---
