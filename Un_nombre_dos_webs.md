# ACTIVIDAD 1 NOMBRE 2 WEBS #
## Guia paso a paso ##

1. Primer paso: creación de las páginas y carpetas con los siguientes comandos en apache2 
sudo mkdir -p /var/www/smr/web /var/www/smr/intranet
echo "<h1>Bienvenidos a SMR</h1>" | sudo tee /var/www/smr/web/index.html
echo "<h1>Intranet de SMR</h1>" | sudo tee /var/www/smr/intranet/intranet.html

2. Crearemos el usuario de la intranet instalando el apache2-utils con el comando
   sudo apt apache2-utils -y
   y colocaremos contraseña con
   sudo htpasswd -c /etc/apache2/.htpasswd alumno
3. En este paso diremos a apache que escuche en el puerto deseado, en este caso el 9999 con el siguiente comando:
   sudo nano /etc/apache2/ports.conf
   y en la parte de la línea Listen 80 añadiremos la linea con el puerto deseado, ejemplo:
   Listen 9999
4. 
