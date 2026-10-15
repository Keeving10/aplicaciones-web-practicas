# VirtualHost #
## Caracteristicas Definición ##

Podemos decir que VirtualHost es es una característica que permite alojar múltiples sitios web en un único servidor físico (o máquina virtual).
racias a los VirtualHosts, Apache diferencia a qué sitio web debe dirigir a un visitante cuando este llega al servidor,
ya sea basándose en la dirección IP, el nombre de dominio o el número de puerto.

Todos los VirtualHosts se crean en /etc/apache2/sites-available/.
Podemos añadir que puertos queremos que escuche el VirtualHost ejemplo:
1. Añadiermos 'Listen 8080' en /etc/apache2/ports.conf
1. Creariamos /etc/apache2/sites-available/puerto8080.conf
3. Pondriamos su IP deseada en /etc/apache2/sites-available/sitio-ip.conf
4. Finalmente habilitariamos el sitio con sudo a2ensite mi-sitio.conf (revisando si no hay
   ningún sitio habilitado antes, si fuese el caso lo deshabilitariamos con sudo a2dissite "nombre del servidor")
