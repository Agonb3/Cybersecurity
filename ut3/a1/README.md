**UT3-A1. Phishing con SET (Social Engineering Toolkit)**

La finalidad de está práctica es interceptar los datos de login de facebook de la victima.
Para ello utilizaremos la herramienta ***Social Engineering Toolkit*** integrada en nuestra máquina ***kali linux***.

Al iniciar la herramienta nos pedirá que seleccionemos entre las distintas opciones disponibles.
En el primer menú elegiremos actualizar la herramienta.

![](./img/2.JPG)

Ahora iniciamos el programa.

![](./img/3.JPG)

En el siguiente menú selccionamos atacar una página web.

![](./img/4.JPG)

En la siguiente ventana seleccionamos el ataque de credenciales y luego clonar sitio.

![](./img/50.JPG)
![](./img/51.JPG)

Nos pedirá que declaremos nuestra ip y el puerto de escucha y, a continuación la url a clonar, donde podremos la página web de facebook.

![](./img/90.JPG)

Hecho estó, deberia crearnos una copia en ***/var/www/*** pero como podemos comprobar la carpeta esta vacía.

![](./img/101.JPG)

intente reiniciar ***apache*** pero me da error y no levanta el servicio.

![](./img/100.JPG)
