# Clonación de discos con clonezila

#### Clonacion desde un disco a otro o una partición del mismo.

##### Preparativos.

Empezamos creando una partición a un disco nuevo en el particionador de Yast de OpenSUSE.

![](./img/001.png)

Elegimos que la particion sea para datos y aplicaciones

![](./img/002.png)

Formateamos el disco con un formato adecuado

![](./img/003.png)

Elegimos el tamaño de las particiones y una vez echo esto apagamos la máquina.

![](./img/004.png)

##### Clonación de discos

Ahora encendemos la propia máquina, pero le añadimos la ISO de clonezila.

![](./img/007.png)

Empezamos a elegir las opciones de nuestro teclado, en mi caso lo puse en español y no toqué nada del mapeado del mismo.

![](./img/008.png)

Aquí, como queremos clonar de un disco a otro debemos de elegir la segunda opción **"device-device"**.

![](./img/009.png)

Elegimos el modo principiante.

![](./img/010.png)

Elegimos la opción de disco local a disco local.

![](./img/011.png)

Elegimos el segundo disco.

![](./img/012.png)

Siguiente.

![](./img/013.png)

Elegimos la opción del medio si queremos comprobar que realmente se ha creado la copia.

![](./img/014.png)

Elegimos que reinicie después de realizar el clonado de disco.

![](./img/015.png)

Al realizar el paso anterior nos devuelve el siguiente texto que deberemos de aceptar.

![](./img/016.png)

Ahora nos devuelve información de como va la clonación de discos.

![](./img/017.png)

## Clonacion de discos: SSH

Empezamos desde el principio eligiendo la opción device-image.

![](./img/018.png)

Selecionamos la opcion ssh_server para clonar el disco desde la maquina a un servidor **ssh**.

![](./img/019.png)

Seleccionamos la opción de dhcp para que nuestra maquina adopte una ip de manera automática.

![](./img/020.png)

Elegimos la ip de la maquina que vamos a usar como servidor ssh.

![](./img/21.png)

Aquí nos pregunta por el puerto por el que realizará la conexión ssh para enviar la copia de nuestros datos a la máquina servidor.

![](./img/22.png)

Ahora elegimos un usuario al que se accederá a la máquina servidor remota.

![](./img/026.png)

Elegimos una ruta para la clonación de nuesto disco. Después de esta ventana nos aparece una ventana de confirmación.

![](./img/024.png)

Ahora introducimos la contraseña de root.

~~~

Como no hemos creado la carpeta /home/partimag nos
devuelve 2 errores, después del segundo me di cuenta y cree la carpeta

~~~

![](./img/027.png)

Vemos la creación de la carpeta partimag en **/home**.

![](./img/028.png)

Ahora debemos de introducir el nombre de nuestra imagen.

![](./img/029.png)

Seleccionamos el segundo disco como punto de origen de la copia.

![](./img/030.png)

Guardamos la imagen clonada.

![](./img/031.png)

Ahora nos devuelve información sobre el proceso de la clonación de la imagen.

![](./img/032.png)

![](./img/033.png)
