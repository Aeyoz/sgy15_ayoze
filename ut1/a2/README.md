# Duplicati

### Proceso de instalación

Descargamos Duplicati y ejecutamos el comando ```dpkg -i``` para poder instalar este paquete.

Pero nos da un error, para solucionarlo deberemos de arreglar las licencias que hayan sido incumplidas.


Para esto utilizamos los siguientes comandos.

![imagen](./img/016.png)

![imagen](./img/017.png)

![imagen](./img/018.png)

![imagen](./img/020.png)

### Configuracion de Duplicati

Al abrir Duplicati nos encontramos con la siguiente pantalla, en la que deberemos de acceder arriba a la izquierda al apartado de añadir copia de seguridad.

![imagen](./img/001.png)

Configuramos nuestra nueva copia de seguridad.

![imagen](./img/002.png)

Especificamos el nombre de nuestra copia de seguridad, e cifrado que queremos para esta y una frase o contraseña de seguridad.

![imagen](./img/003.png)

Ahora debemos de elegir nuestro servicio deslocalizado para hacer la copia de seguridad de nuestros archivos.

![imagen](./img/004.png)

Nos pedirá la creación de una nueva carpeta, la creamos.

![imagen](./img/005.png) ![imagen](./img/006.png)

Ahora debemos de elegir los archivos que queremos asegurar.

![imagen](./img/007.png)

Elegimos un horario en el que se realizaran nuestras copias de seguridad.

![imagen](./img/008.png)

Elegimos el tiempo de vida de nuestras BackUps.

![imagen](./img/009.png)

### Backup

Ahora es turno de ejecutar Duplicati y comprobar que nuestra backup está en Google Drive.

![imagen](./img/010.png)

![imagen](./img/011.png)

### Restaurar Backup

Vemos que ha sido todo un exito, ahora debemos comprobar que nuestra backup funciona, para ello eliminamos nuestros archivos y los restauramos de nuevo

![imagen](./img/012.png)

Nos vamos a Duplicati a la seccion de Restaurar

![imagen](./img/001.png)

Elegimos los 2 ficheros a restaurar.

![imagen](./img/013.png)

Especificamos la ubicacion que queremos para ellos.

![imagen](./img/014.png)

Vemos que han sido restaurados con éxito.

![imagen](./img/015.png)
