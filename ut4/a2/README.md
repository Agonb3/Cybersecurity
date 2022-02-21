
<center>

# UT4-A2 VPN en Windows Server


</center>

***Ayoze Glez. Bello***

*** 2º de Ciclo Superior de Administración de Sistemas Informáticos en Red.***

### ÍNDICE

+ [Introducción](#id1)
+ [Objetivos](#id2)
+ [Material empleado](#id3)
+ [Desarrollo](#id4)
+ [Conclusiones](#id5)


#### ***Introducción***. <a name="id1"></a>

Vamos a configurar un servidor vpn en Windows Server 2016.

#### ***Objetivos***. <a name="id2"></a>

Vamos a crear una vpn y conectar un cliente con Windows 10.

#### ***Material empleado***. <a name="id3"></a>

- Windows Server 2016
- Windows 10

#### ***Desarrollo***. <a name="id4"></a>

Lo primero que debemos hacer es asignar una ip estática a nuestro servidor.

![](./img/14.JPG)

Ahora iniciamos nuestro panel administrador y agregamos los roles de ***active directory***, ***acceso remoto*** y ***enrrutamiento*** y aceptamos las caracteristicas que nos indique el asistente que necesitas instalar para el correcto funcionamiento de los servicios.

![](./img/2.JPG)

![](./img/3.JPG)

![](./img/12.JPG)

Ahora tendremos una nueva pestaña para gestionar el enrrutamiento y acceso remoto a nuestro servidor.

![](./img/15.JPG)

![](./img/13.JPG)

Haciendo click derecho sobre el nombre de nuestro servidor podremos acceder a la configuración.

![](./img/16.JPG)

Seleccionamos la opción de ***Acceso a red privada virtual***

![](./img/17.JPG)

Seleccionamos la interfaz de red.

![](./img/18.JPG)

y siguiendo las indicaciones del asistente, seleccionamos agregar un intervalo de direcciones.

![](./img/19.JPG)

![](./img/300.JPG)

Seleccionamos la opción de usar enrrutamiento acceso remoto.

![](./img/21.JPG)

![](./img/22.JPG)

Una vez configurado volvemos a la pestaña inicial y desplegamos las subcategorias del servidor, para hacer click derecho en ***puertos*** y seleccionamos ***propiedades***

![](./img/23.JPG)

aquí reducimos el numero de puertos disponibles para los diferentes protocolos, priorizando los ***L2PT*** y marcando las casillas para permitir las conexiones, como se muestra en la imagen.

![](./img/101.JPG)

![](./img/25.JPG)

Ahora otra vez clicando sobre el nombre de nuestro servidor seleccionamos ***propiedades*** y nos vamos a la pestaña de ***seguridad*** para asignar la contraseña del servicio.

![](./img/28.JPG)

Una vez configurada la VPN nos dirigimos a ***active directory*** para crear un usuario autorizado para usar el servicio.

![](./img/29.JPG)

Creamos una nueva unidad organizativa a la que llamaremos ***vpn-users***

![](./img/30.JPG)

dentro de ella crearemos un nuevo usuario para nuestro servicio.

![](./img/32.JPG)

Le asignamos una contraseña y marcamos las pestañas que se muestran en la imagen.

![](./img/33.JPG)

Una vez creado el usuario debemos hacer click derecho sobre el y abrir las propiedades. Dentro de estas buscamos la pestaña de ***marcado*** y marcamos ***permitir acceso***

![](./img/x.JPG)

Ya tenemos listo el servidor, ahora abrimos el cliente y creamos la conexión.
Para ello abrimos el centro de recursos y redes y marcamos en la opción de VPN. Para crear la conexión simplemente introducimos la dirección ip del servidor, el nombre de usuario y la contreseña.

![](./img/202.JPG)

Como podemos ver en la imagen, ya estamos conectados y se nos a asignado una ip del rango que habiamos definido anteriormente.

![](./img/500.JPG)

#### ***Conclusiones***. <a name="id5"></a>

La implementación de este tipo de servidores es sencilla, pero es necesario conocer cada uno de los pasos correctamente porque el hecho de no marcar una sola casilla durante el proceso, hace que el servicio no pueda iniciarse correctamente.
