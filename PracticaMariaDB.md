# MARIADB PRACTICA KEVIN DANIEL QUIZHPE INGA #

## ¿Qué es una base de datos? ##
Es como un archivador muy ordenado donde un programa guarda su información para
poder encontrarla y usarla rápido, organizada en tablas, columnas y filas

## ¿Para qué la necesita WordPress? ##
WordPress guarda en la base de datos todo lo que no son ficheros:
entradas, las páginas, los comentarios, los usuarios y la configuración del sitio. Cada vez que alguien visita la
web, WordPress le pide los datos a la base de datos.

## ¿Qué es MariaDB? ##
Es el programa que gestiona la base de datos: la guarda, la protege y responde a las
peticiones. Es la que viene en los repositorios de Ubuntu y funciona muy bien con WordPress.

# CAPTURA ACTIVE APACHE2 #
<img width="593" height="116" alt="image" src="https://github.com/user-attachments/assets/a4a8ffbc-112d-45a3-83e6-2596ea8edcab" />

# CAPTURA VERSION MARIADB #
<img width="819" height="37" alt="image" src="https://github.com/user-attachments/assets/6cb52bc0-c177-4a3c-aad6-b54d864f80ca" />

## ¿Qué diferencia hay entre el paquete mariadb-server y el paquete mariadb-client? ¿Cuál de los dos has instalado? ##
La diferencia principal es que mariadb-server es el motor de la base de datos (el programa que guarda y gestiona los datos), 
y mariadb-client es la herramienta para conectarse a ese motor con comandos.

# CAPTURA MARIADB ESTADO Y ENTRADA #
<img width="956" height="454" alt="image" src="https://github.com/user-attachments/assets/3d46268d-b8cd-4ed3-8ba4-9138bec1a63b" />

<img width="647" height="200" alt="image" src="https://github.com/user-attachments/assets/841bf555-aa7a-4580-ac63-72df155ad657" />

## ¿Qué diferencia hay entre active (running) y enabled? ¿Qué pasaría con la web de WordPress si MariaDB estuviera active pero no enabled y se reiniciara el servidor? ##
Cuando esta en active significa que el programa está encendido ahora mismo.
Cuando sale enabled significa que el programa tiene permiso para encenderse solo cuando reinicias el ordenador.
Si MariaDB no esta en active pero no enabled tu web se va a romper y mostrará el famoso cartel de "Error al establecer una conexión con la base de datos".
Al reiniciar el servidor, MariaDB se apaga. Como no lo dejaste en enabled, el servidor arranca pero la base de datos se queda durmiendo. WordPress intentará cargar, no encontrará tus datos y fallará.

# Error y recuperación MARIADB #
<img width="795" height="149" alt="image" src="https://github.com/user-attachments/assets/2c440780-43ec-4c7b-8862-fa571cb35577" />

## Si WordPress no pudiera conectar con la base de datos, ¿qué dos comandos de este apartado usarías para saber si el problema es que MariaDB está parado? ##
Para saber si MariaDB está parado, usarías estos dos comandos:
1. systemctl is-active mariadb Te dirá directamente con una palabra (active o inactive) si la base de datos está funcionando ahora mismo.
2. sudo systemctl status mariadb Te dará el informe completo del servicio para ver si está apagado, encendido o si muestra algún mensaje de error en rojo.

# CAPTURA PAGINA WEB CON MI IP Y PHP V #
<img width="1733" height="826" alt="image" src="https://github.com/user-attachments/assets/638430f9-69a5-4096-8927-0d2ad29c3a83" />

<img width="551" height="101" alt="image" src="https://github.com/user-attachments/assets/290b202b-3047-4051-88fb-d17759f12ec4" />

# Errores encontrados, soluciones #
En este ejercicio no he encontrado ningun error de comando ni nada todo estaba bien explicado los unicos problemas han sido por escribir mal un comando simplemente

