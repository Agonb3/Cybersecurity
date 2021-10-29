**UT2-A6. Encriptado de información con Windows 7 y Windows 10.**

**Windows7**

Vamos a encriptar archivos con ***EFS*** en Windows7 y Windows10.

Iniciamos Windows7 y lo primero que haremos es entrar en el centro de cuentas y crearemos 2 perfiles nuevos "encriptado" y "normal", ambos con rol de administrador del sistema.

![](./img/1.JPG)

![](./img/2.JPG)

![](./img/3.JPG)

Una vez creados los perfiles, iniciamos sesión con el perfil de encriptado.

![](./img/4.JPG)

Una vez en el perfil, ejecutamos tecla windows + r para abrir la consola de busqueda, y dentro buscamos ***services.msc***.

![](./img/0.JPG)

Dentro de servcios buscamos sistema de cifrado de archivos y con el botón derecho del ratón seleccionamos ***activar***.

![](./img/6.JPG)

Ahora crearemos una carpeta en la ruta C:// con el nombre de ***Encriptar*** y luego en las propiedades de la carpeta, entraremos en ajustes avanzados y activaremos el cifrado.

![](./img/8.JPG)

![](./img/9.JPG)

Nos dará la oportunidad de hacer una copia de seguridad con contraseña.

![](./img/10.JPG)

![](./img/11.JPG)

Una vez finalizado el asistente, vamos a crear un fichero de texto dentro de la carpeta para comprobar que nuestro usuario sigue teniendo acceso a la misma.

![](./img/12.JPG)

Vamos a cambiar de usuario y a intentar acceder al fichero que hemos creado.

![](./img/13.JPG)

![](./img/15.JPG)

Al hacer doble click sobre el archivo, nos aparece un mensaje avisandonos que no tenemos permiso para acceder.

![](./img/14.JPG)

Al intentar desactivar el ***EFS*** vemos que el menú no esta habilitado para este usuario.

![](./img/16.JPG)

**Windows10**

Vamos a hacer la misma práctica con Windows10.
Comenzamos creando los usuarios.

![](./img/20.JPG)

![](./img/21.JPG)

![](./img/22.JPG)

Una vez creados, les damos rol de administradores del sistema.

![](./img/23.JPG)

Cerramos sesión e iniciamos con la cuenta encriptado.

![](./img/24.JPG)

Con las teclas ***windows+r*** iniciamos el buscador y buscamos ***services.msc***

![](./img/25.JPG)

volvemos a buscar ***sistema de cifrado de archivos*** y lo activamos.

![](./img/26.JPG)

![](./img/27.JPG)

En el disco local C creamos de nuevo una carpeta con nombre ***Encriptar*** y ciframos el contenido.

![](./img/28.JPG)

Creamos un nuevo fichero

![](./img/29.JPG)

Cambiamos de nuevo de usuario e intamos acceder al fichero.

![](./img/30.JPG)

Una vez más nos sale el mensaje denegando el acceso.

![](./img/31.JPG)

Entramos en servicios para intentar desactivar el ***EFS*** pero al igual que en Windows7 las opciones no estan habilitadas para este usuario.
