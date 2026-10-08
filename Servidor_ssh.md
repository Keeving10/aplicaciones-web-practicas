<h1>¿Que es un servidor ssh?</h1>
Son las siglas de Secure Shell y es un protocolo de red destinado principalmente a la conexión con máquinas a las que accedemos por línea de comandos. Resumiendo, con SSH podemos conectarnos con servidores usando la red Internet como vía para las comunicaciones.

Su configuración consta de dos partes:
- Marcar casilla SSH durante la instalación de UbuntuServer

O seguir los siguientes pasos con comandos:
-Abrimos el terminal de nuestro sistema
-Instalamos el servidor ejecutando el comando sudo apt update y despues sudo apt install openssh-server (comandos son para tener el equipo actualizado y instalar el paquete openssh)
-Comprobamos que el servicio esta funcionando con sudo systemctl status ssh.
