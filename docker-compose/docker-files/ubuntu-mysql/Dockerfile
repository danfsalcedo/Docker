FROM ubuntu:latest

ENV DEBIAN_FRONTEND=noninteractive

# Actualizar el sistema e instalar MySQL
RUN apt-get update && \
    apt-get install -y mysql-server && \
    apt-get clean

# Exponer el puerto de MySQL
EXPOSE 3306

# Comando para iniciar MySQL
CMD ["mysqld"]
