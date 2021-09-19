# Ejemplo de curl.h

Este es un archivo de ejemplo del uso de curl.h para extraer todos los enlaces dentro de una página web. Su funcionamiento toma en cuenta los siguientes supuestos.

- Todos los enlaces relevantes estarán dentro de una propiedad **href**, sin importar el tag que sea.

- Los errores de memoria (o casos donde el retorno de la solicitud sea distinto a 200) son verificados, pero no manejados de ninguna otra manera.

## Instalación y ejecución

Para la compilación es necesario estar en un sistema POSIX, con gcc y glibc-dev instalados. ((1) sólo en caso de que libcurl-dev no se pueda instalar, (2) en caso de que (1) no se pueda instalar.)

Si se necesita instalar, se puede hacer con:

    sudo apt-get install build-essential
    sudo apt-get install libcurl-dev
    sudo apt-get install libcurl4-openssl-dev (1)
    sudo apt-get install libcurl4-gnutls-dev  (2)


Finalmente, para compilarlo se hace se la siguiente manera:

    gcc main.c -l curl -o main.o
