
<center>

# UT4-A4 Instalación y configuración den servidor WifiRadius con PFSENSE


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

El estándar 802.1X nos permite realizar una conexión segura a puntos de acceso de red inalámbrica, centralizando la seguridad de todos los dispositivos de una red sobre una única base de datos de usuarios y contraseñas (servidor RADIUS).

#### ***Objetivos***. <a name="id2"></a>

Vamos a implementar un sistema de autentificación y autorización de usuarios en la red, mediante ***RADIUS  (Remote Authentication Dial-In User Server*** instalado en nuetro firewall ***Pfsense***.

#### ***Material empleado***. <a name="id3"></a>

- Servidor Pfsense
- Cliente Ubuntu

#### ***Desarrollo***. <a name="id4"></a>

Lo primero que debemos hacer es configurar nuestro servidor de Pfsense (en caso de no haberlo configurado antes). Para ello, pondremos 2 adaptadores de red uno con el rol de ***WAN*** y ***LAN***.

![](./img/1.JPG)

Ahora desde otro host accederemos al administrador de pfsense mediante su ip y los datos de acceso por defecto del sistema.

![](./img/2.JPG)

Antes de configurar nuestro RADIUS vamos a realizar algunos ajustes generales en el servidor, como el nombre de host, dominio, ip de la interfaz LAN, puerto asignado para las conexiones, etc ...

![](./img/3.JPG)

![](./img/4.JPG)

![](./img/5.JPG)

En la pestaña ***Servicios/servidor DHCP/LAN*** marcamos la pestaña habilitar y elegimos un rango de direcciones para asignar a nuestros clientes.

![](./img/Captura.JPG)

Ahora vamos a conectarnos desde nuestro cliente mediante red interna a la ip LAN de nuestro servidor, y como podemos ver nos asigna una de las ip's que habiamos definido en el rango disponible.

![](./img/7.JPG)

Una vez acabadas las configuraciones iniciales, volvemos a nuestro servidor y nos vamos al gestor de paquetes para instalar ***RADIUS***.

![](./img/8.JPG)

![](./img/9.JPG)

Ya podemos configurar el servcio desde la pestaña ***Servicios/FreeRADIUS***

![](./img/10.JPG)

Seleccionamos la opción de ***NAS/Clients*** y rellenamos las casillas con los datos del servicio y una contraseña para el mismo.

![](./img/11.JPG)

En la pestaña interfaces asignamos la LAN, el puerto que usaremos, y dejaremos el resto por defecto.

![](./img/12.JPG)

Asignaremos un segundo puerto al servcio esta vez con la opción de ***Contabilidad*** en el tipo de interfaz.
![](./img/13.JPG)

Ahora vamos a crear los usuarios autorizados para el servicio, dandoles unicamente nombre y contraseña.

![](./img/14.JPG)

Vamos a activar el ***Portal Cautivo***, para ello nos dirijimos a ***Servicios/Portal Cautivo/portalasir/Configuración*** y marcamos la pestaña ***Habilitar***.

![](./img/16.JPG)

Por último nos dirigimos a ***Sistema/Gestión de Usuarios/Servidores de Autentificación/Editar*** y rellenamo las casillas con los datos que hemos habilitado para el servicio.

![](./img/17.JPG)

![](./img/19.JPG)

También dejaremos marcadas las siguientes pestañas y guardamos.

![](./img/15.JPG)

Ya hemos terminado la configuración del servicio. Ahora desde el cliente intentamos navegar a alguna página y vemos que nos pide autenticarnos en el servicio para continuar.

![](./img/21.JPG)

#### ***Conclusiones***. <a name="id5"></a>

Implementar este tipo de servicios puede ser muy util para proteger tu red de una forma efectiva. Ademas el hecho de poder gestionar el servicio desde una interfaz gráfica hace sumamente sencillo su uso.
