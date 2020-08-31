# Imagen del contenedor que ejecuta tu código
FROM ubuntu:18.04

# Copias tu archivo de código de tu repositorio de acción a la ruta `/`del contenedor
COPY entrypoint.sh /entrypoint.sh

RUN apt-get update && apt-get install -y apache2-utils
RUN chmod +x /entrypoint.sh

# Archivo del código a ejecutar cuando comienza el contedor del docker (`entrypoint.sh`)
ENTRYPOINT ["/entrypoint.sh"]