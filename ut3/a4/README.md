**UT3-A4. Hackeo de Windows, ejecución del modo comando desde Kali Linux**

En está práctica vamos a acceder en remoto a una máquina con windows7 aprovechando las vulnerabilidades del servidor instalado.

Para ello descargamos y arrancamos el servidor en cuestión.

![](./img/1.JPG)

![](./img/2.JPG)

Ahora desde nuestra máquina ***kali-linux***
vamos a hacer uso de ***nmap*** para escanear la ip de windows y comprobar si tienes servicios con puertos abiertos.  

![](./img/3.JPG)

Podemos ver que el puerto 8080 está abierto. Vamos a iniciar un navegador para ver si podemos encontrar más información del servicio.

![](./img/4.JPG)

Una vez identificado el servicio y el puerto, iniciamos ***msfconsole*** y realizamos una busqueda con el nombre del servidor que obtuvimos para comprobar si hay vulnerabilidades que podamos explotar.

![](./img/5.JPG)

Como podemos comprobar existe una vulneravilidad para ese servicio. Vamos a utilizarla con el comando ***use*** y el nombre de la vulnerabilidad.    
Con ***show options*** podemos ver las variables que nos brinda el exploit.

![](./img/6.JPG)

Vamos a definir la ip y puerto de nuestra víctima.

![](./img/20.JPG)

Y lo activamos.

![](./img/21.JPG)

Si miramos los regsitros del servidor en nuestra máquina Windows, podemos ver la intrusión.

![](./img/7.JPG)

De nuevo en la consola de kali podemos utilizar comandos para listar directorios o incluso hacer capturas de pantalla.

![](./img/9.JPG)

![](./img/10.JPG)

Con el comando ***download*** podremos descargarnos archivos en nuestra máquina.

![](./img/11.JPG)

![](./img/12.JPG)

Con el comando ***shell*** podemos abrir una terminal en nuestra víctima.

![](./img/13.JPG)

CON ***sysinfo*** podemos ver la información del sistema.

![](./img/14.JPG)

Con ***idletime*** podemos ver la última conexión de la víctima.

![](./img/15.JPG)

Con el comando ***upload*** podremos subir archivos desde nuestra máquina a la víctima.

![](./img/16.JPG)

Con el comando ***search*** podremos buscar archivos dentro de su disco duro.

![](./img/17.JPG)

Y con el comando ***route*** podremos ver e incluso modificar su tabla de rutas.

![](./img/18.JPG)
