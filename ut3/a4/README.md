# Hackeo de Windows, ejecución del modo comando desde Kali Linux

En la máquina Windows victima abrimos un servidor de ficheros http por el puerto 8080.

![](./img/001.png)

Comprobamos con un nmap que está abierto.

![](./img/002.png)

Accedemos al servidor HTTP mediante un navegador con la ip de la máquina victima y con el puerto anterior, es decir, buscamos 10.0.2.4:8080 en el navegador.

![](./img/003.png)

Vemos la version del server en la parte de abajo a la izquierda.

![](./img/004.png)

Ejecutamos la herramienta **msfconsole** y buscamos sobre el httpfileserver para comprobar si hay vulnerabilidades que podamos usar, y vemos que hay una.

![](./img/005.png)

Usamos esa debilidad.

![](./img/006.png)

Cambiamos el puerto y el RHOST de la máquina atacante y ejecutamos el exploit.

![](./img/007.png)

Vemos en el servidor HTTP que alguien ha entrado.

![](./img/008.png)

Obtenemos el id de usuario actual y vemos que hay en el directorio en el que estamos.

![](./img/009.png)

Ahora sacamos una captura de pantalla del escritorio de la victima con el comando screenshot.

![](./img/011.png)

![](./img/010.png)

Desde el equipo vulnerable subimos un archivo **prueba.txt**.

![](./img/012.png)

Desde la máquina kali descargamos ese fichero.

![](./img/013.png)

Vemos el contenido del fichero.

![](./img/014.png)

Abrimos el cmd con **shell** y ejecutamos comandos de Windows, por ejemplo dir para visionar el contenido del directorio.

![](./img/015.png)

Desde la máquina kali, fuera de la shell, ejecutamos **idletime** para ver el tiempo que lleva iniciada la sesión del usuario. Con **sysinfo** vemos información del sistema. Y con **upload** podemos subir un fichero o carpeta a la víctima.

![](./img/016.png)

Buscamos el fichero prueba.txt desde meterpreter, ejecutamos el notepad de windwos y buscamos la tabla de rutas.

![](./img/017.png)

Ahora apagamos la máquina en 10 segundos.

![](./img/018.png)
