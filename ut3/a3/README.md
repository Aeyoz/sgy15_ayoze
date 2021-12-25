# Explotar vulnerabiidades.

### Explotando vulnerabilidades con Metasploit Framework MYSQL.

Comprobamos que la máquina tiene el puerto 3306 abierto con la utilidad msfconsole ejecutando el comando db_nmap.

![](./parte1/img/001.png)

Buscamos información del puerto y entramos.

![](./parte1/img/002.png)

Entramos a la base de datos con la línea mysql -u root -p --host=10.0.2.5 --port=3306

![](./parte1/img/004.png)

Extraemos la información de los usuarios con tarjetas de crédito.

![](./parte1/img/003.png)

### Explotando vulnerabilidades con Metasploit Framework VSFTPD.

Consultamos el estado e iniciamos el servicio de postgresql.

![](./parte2/img/001.png)

Iniciamos la herramieta msfconsole.

![](./parte2/img/002.png)

Hacemos un **db_nmap 10.0.2.5 -p 1-65535** para hacer un escaneo de todos los puertos de la máquina víctima.

![](./parte2/img/003.png)

mostramos un lstado de los hosts que se han escaneado recientemente, aparece, además de la máquina Metasploit de Windows (HERNANDEZ28WSGY) y la máquina del profesor (AMARZAR-PC), aparece la máquina victima con una ip=10.0.2.5.

![](./parte2/img/004.png)

Vemos los servicios de la máquina víctima con services 10.0.2.5.

![](./parte2/img/005.png)

Ejecutamos vulns para ver las vulnerabilidades que se han detectado en la máquina.

![](./parte2/img/006.png)

Ahora hacemos un db_nmap -sV 10.0.2.5 -p 21 para revelar más información sobre los servicios relacionados con los puertos abirtos, vemos que se nos proporciona más información sobre el puerto 21 que está abierto para conexiones ftp.

![](./parte2/img/007.png)

![](./parte2/img/008.png)

Buscamos exploits relacionados con la información proporcionada por el puerto.

![](./parte2/img/009.png)

Usamos el exploit y cambiamos el RHOST a 10.0.2.5 y lo ejecutamos.

![](./parte2/img/010.png)

Ahora nos encontramos dentro de la máquina, ahora podemos apagarla si queremos.

![](./parte2/img/011.png)

Vemos que se apaga la máquina víctima.

![](./parte2/img/012.png)
