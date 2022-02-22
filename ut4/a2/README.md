<center>

# TÍTULO DE LA PRÁCTICA

</center>

***Nombre:*** Ayoze Hernández Díaz
***Curso:*** 2º de Ciclo Superior de Administración de Sistemas Informáticos en Red.

### ÍNDICE

+ [Introducción](#id1)
+ [Objetivos](#id2)
+ [](#id3)
+ [](#id4)
+ [](#id5)

#### ***Introducción***. <a name="id1"></a>

#### ***Objetivos***. <a name="id2"></a>

#### ***Instalación***. <a name="id3"></a>

Para empezar debemos tener una máquina de windows server 2016 arrancada y crear un usuario que se usará unicamente par las conexiones VPN.

![](./img/001.png)

En la sección de marcado permitimos acceso a las redes y el otorgamos permiso de devolución de llamada.

![](./img/004.png)

Instalamos el rol de **Acceso remoto** y sus características.

![](./img/002.png)

![](./img/003.png)

Accedemos a la herramienta de acceso remoto y la configuramos a nuestro gusto.

![](./img/005.png)

Aquí vamos a la sección de Configurar y habilitar Enrutamiento y acceso remoto.

![](./img/006.png)

Aquí elegimos la opción de configuración personalizada.

![](./img/007.png)

Queremos el acceso a VPN y el NAT.

![](./img/008.png)

Finalizamos.

![](./img/009.png)

Iniciamos el servicio.

![](./img/010.png)

#### ***Configuración del firewall de windows***. <a name="id4"></a>

Debemos de añadir las siguientes reglas relacionadas con los puertos asociados a los protocolos GRE, L2TP, TCP y UDP tanto en las reglas de salida como en las de entrada.

![](./img/012.png)

![](./img/013.png)

![](./img/014.png)

![](./img/015.png)

![](./img/016.png)

![](./img/017.png)

![](./img/018.png)

![](./img/019.png)



Iniciamos el NPS (Network Policy Server).

![](./img/022.png)

Vamos al apartado de **configurar cuentas**.

![](./img/023.png)

Se nos abre un cuadro adicional vamos con opciones por defecto.

![](./img/024.png)

![](./img/025.png)

![](./img/026.png)

![](./img/027.png)

Habilitamos esas directivas.

![](./img/028.png)

Añadimos más directivas de red especificando que son para servidores de acceso **remoto/vpn**.

![](./img/029.png)

Hacemos que la condición se pertenecer al grupo vpnusers.

![](./img/030.png)

Concedemos permiso para acceder.

![](./img/031.png)

En las siguientes imágenes se muestran campos adicionales que se pueden configurar.

![](./img/032.png)

![](./img/033.png)

![](./img/034.png)

![](./img/035.png)

![](./img/036.png)

Agregamos un atributo que permita el protocoo PPTP (Point-to-Point Tunneling Protocol)

![](./img/037.png)

Vemos un resumen de la directiva.

![](./img/038.png)

Vamos a la configuración del windows cliente al apartado de VPN y agregamos una nueva.

![](./img/039.png)

Se nos abre un cuadro que hay que rellenar de la siguiente manera:

![](./img/040.png)

Configuramos una nueva red.

![](./img/042.png)

Especificamos que queremos la Ip del servidor y le damos un nombre a la conexión.

![](./img/043.png)

El usuario vpn es el que tiene acceso por lo que lo ponemos aquí.

![](./img/045.png)

Nos conectamos a la vpn y hacemos un tracert a 1.1.1.1 y vemos que sale por la maquina servidor y luego a la red.

![](./img/046.png)

Ahora en **ubuntu** añadimos una vpn con el protocolo Layer 2 Tunneling Protocol (L2TP).

![](./img/041.png)

Añadimos los datos de la red a la que nos queremos conectar.

![](./img/047.png)

En opciones avanzadas usamos el cifrado punto a punto (MPPE).

![](./img/048.png)

Hacemos un traceroute a www.google.es

![](./img/050.png)
#### ***Conclusiones***. <a name="id5"></a>
