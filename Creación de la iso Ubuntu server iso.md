# Ubuntu Server indicaciones
## Paso 1

1. Seleccionamos la aplicación VirtualBox
2. Despues en Nova, rellenar con cualquier nombre, por ejemplo Ubuntututu,
3. Despues seleccionar la ISO de, en este caso, de Ubuntu server (Desselecionar la casilla de Proceed witn Unattended installation.)
4. Despues colocar la RAM necesarria y lo demas para el sistema, recomendable 2Gb ram , 2 procesadores y 25 Gb de almacenamiento.

¡¡Algunos Usuarios Tienen Que Reinstalar Ultima Version VirtualBox!!

5. Durante la instalación de Ubuntu Server seleccionaremos el idioma del sistema y del teclado
6. Elegiremos nombre y usuario a nuestro gusto (simepre algo que recordemos con facilidad)
7. En el apartado de "perfil de usuario" pondremos el nombre del servidor, del host y la contraseña
10. Seguimos los pasos para su instalación en español (Seleccionar la casilla SSH para instalar) y reiniciar la maquina virtual
11. Una vex instalada, en configuración de redes de VirtualBox ,configuraremos los adaptadores en el 2 de solo anfitrión.
12. Con el comando ls a veremos que en enpos0s8 no tendra ninguna Ip, para despues con el fichero de localización /etc/netplan, utilizaremos el comando sudo nano /etc/netplan/50-clou-init.yaml
13. Escribiremos una direccion Ip, colocando antes False en dhcp :.
14. Con el comando sudo netplan apply aplicaremos los cambios y verificaremos con ip a "comando".
15. 
