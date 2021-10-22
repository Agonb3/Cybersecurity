**UT2-A4. Clonación de discos mediante CLONEZILLA**

Vamos a realizar una copia de un disco duro, alojandola en un servidor remoto mediante ssh.  
Para ello lo primero que haremos será instalar el servicio ***openssh-server*** en nuestro servidor.

![](./img/50.JPG)

Ahora crearemos nuestro usuario del sistema.

![](./img/51.JPG)

Y crearemos la carpeta donde alojaremos las copias de seguridad.

![](./img/200.JPG)

Sin apagar nuestro servidor, conectamos la máquina desde la cual realizaremos la copia.  
En la configuración de la máquina añadimos un nuevo disco duro y le damos formato.

![](./img/52.JPG)

![](./img/55.JPG)

En la pestaña dispositivos añadimos el disco de ***clonezilla-live*** que previamente debemos tener descargado en le pc, y reiniciamos para que se inicie el asistente.
A cada paso, nos dará varias opciones, he iremos marcandolas como en las imagenes.

![](./img/60.JPG)

![](./img/61.JPG)

![](./img/63.JPG)

![](./img/64.JPG)

![](./img/65.JPG)

En esté paso nos pide la direcci
on ip del servidor.

![](./img/66.JPG)

![](./img/67.JPG)

![](./img/68.JPG)

![](./img/70.JPG)

Ahora introducimos nuestra contraseña y seguimos las instrucciones del asistente.

![](./img/71.JPG)

![](./img/80.JPG)

![](./img/82.JPG)

![](./img/83.JPG)

Seleccionamos el disco que queremos copiar.

![](./img/84.JPG)

![](./img/85.JPG)

![](./img/86.JPG)

Y con está instrucción del asistente ya terminamos el proceso de copia.

![](./img/87.JPG)
