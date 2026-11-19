# APACHE 2 #
## Instalación y uso paso a paso ##
1. Instalamos apache 2 entrando desde nuestra terminal a nuestro servidor Ubuntu con nuestro usuario y contraseña

2. Con el comando sudo apt-get install apache2 instalaremos apache2 para su posterior uso (antes actualizaremos el sistema con sudo apt update)

3. Comprobamos que esta funcionando con el comando Systemctl status apache2

4. Una vez este Active estara funcionando correctamente y podremos ver sus contenidos

5. Entramos a /etc/apache2 para despues ver sus archivos improtantes con el comando ls.Podremos ver archivos como sites-available (Sitios web disponibles para activar), sites-enables (Sitios web activados), ports.conf (numeros de puertos )

6. Prestaremos antención a sites-available para editar con sudo nano el archivo /var/www/html/index.html para editar el contenido de este html. Como por ejemplo que va a salir, por que puerto va a salir etc..

7. LISTA COMANDOS A TENER EN CUENTA:
- sudo apachectl configtest # valida sintaxis ANTES de recargar
- sudo systemctl reload apache2 # aplica cambios de configuración
- sudo systemctl restart apache2 # para casos de cambios de red/puertos
- sudo journalctl -u apache2 -f # log del servicio en vivo

8.LISTA DE DIRECTORIOS A TENER EN CUENTA:
- /etc/apache2/apache2.conf → configuración principal
- /etc/apache2/sites-available/ → vhosts definidos
- /etc/apache2/sites-enabled/ → vhosts activos (enlaces simbólicos)
- /etc/apache2/mods-available/ → módulos instalados
- /etc/apache2/mods-enabled/ → módulos activos (enlaces simbólicos)
- /var/www/html/ → raíz de documentos por defecto
- /var/log/apache2/ → access.log y error.log
  
