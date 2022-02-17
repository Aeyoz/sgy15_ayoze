
<center>

# Instalación y configuración de un servidor Pfsense


</center>

***Nombre:*** Ayoze Hernández Díaz
***Curso:*** 2º de Ciclo Superior de Administración de Sistemas Informáticos en Red.

### ÍNDICE

+ [Introducción](#id1)
+ [Objetivos](#id2)
+ [Material empleado](#id3)
+ [](#id4)
+ [](#id5)


#### ***Introducción***. <a name="id1"></a>

En esta práctica lo que se pretende es realizar la instalación y configuración de un servidor Pfsense para que tengamos que registrarnos en la red para acceder a ella.

#### ***Objetivos***. <a name="id2"></a>

Con esta práctica se pretende controlar el acceso de los clientes a la red.

#### ***Material empleado***. <a name="id3"></a>

Usaremos 3 máquinas:

* Servidor Pfsense
* Cliente Windows 10
* Cliente Ubuntu 20.4

#### ***Instalación del servidor Pfsense***. <a name="id4"></a>

Empezamos la instalación del servidor Pfsense y para ello debemos de aceptar los terminos de distribución.

![](./img/001.png)

Queremos instalar Pfsense.

![](./img/002.png)

Escogemos el teclado español con los acentos.

![](./img/003.png)

Queremos que las particiones sean por defecto.

![](./img/004.png)

Cuando terminamos nos aparece la siguiente pantalla con menú.

![](./img/006.png)

#### ***Configuración***. <a name="id5"></a>

En el cliente Windows usaremos la siguiente configuración de red en la que tenemos tanto en gateway como en DNS la ip LAN del servidor Pfsense.

![](./img/007.png)

Accedemos a la dirección web 192.168.1.1 con las siguientes credenciales:

* User = admin
* Passwd = pfsense

![](./img/008.png)

Empezamos a configurar el FQDN (Fully Qualified Domain Name) del server que será pfsense.asir.test

> **NOTA:** La parte de pfsense en pfsense.asir.test se añade automáticamente.

![](./img/009.png)

Establecemos la zona horaria

![](./img/010.png)

![](./img/011.png)

![](./img/012.png)

![](./img/013.png)

![](./img/014.png)

![](./img/015.png)

![](./img/016.png)

![](./img/017.png)

![](./img/018.png)

![](./img/019.png)

![](./img/020.png)

![](./img/021.png)

![](./img/022.png)

![](./img/023.png)

![](./img/024.png)

![](./img/025.png)

![](./img/026.png)

![](./img/027.png)

![](./img/028.png)

![](./img/029.png)

![](./img/030.png)

![](./img/031.png)

![](./img/032.png)

![](./img/033.png)

![](./img/034.png)

![](./img/035.png)
