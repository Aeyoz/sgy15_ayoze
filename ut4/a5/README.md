
<center>

# OpenVPN en Pfsense.

</center>

***Nombre:*** Ayoze Hernández Díaz
***Curso:*** 2º de Ciclo Superior de Administración de Sistemas Informáticos en Red.

### ÍNDICE

+ [Introducción](#id1)
+ [Objetivos](#id2)
+ [Instalación del paquete OpenVPN](#id3)
+ [Creación de usuarios](#id4)
+ [Conexión VPN](#id5)


#### ***Introducción***. <a name="id1"></a>

Pfsense es una distribución de linux diseñada para actuar como Firwall o enrutador.

#### ***Objetivos***. <a name="id2"></a>

El objetivo es instalar el paquete de OpenVPN en nuestro servidor Pfsense para crear una conexión segura entre nuestros usuarios e internet mediante un túnel.

#### ***Instalación del paquete OpenVPN***. <a name="id3"></a>

Para poder instalar el servicio/paquete debemos generar un certificado dedicado para el servicio de OpenVPN.

![](./img/001.png)

Rellenamos los datos del certificado.

![](./img/002.png)

Indicamos el tipo de acceso que queramos dar a los usuarios para la VPN.

![](./img/003.png)

Indicamos la entidad emisora para el certificado.

![](./img/004.png)

Se completan los siguientes por defecto y nos aparece lo siguiente, especificamos que la Interfaz sea de tipo WAN.

![](./img/005.png)

![](./img/006.png)

Añadimos una ip para el túnel y marcamos el recuadro para redireccionar la puerta de enlace y en local network lo podemos dejar en blanco para que tome valores por defecto.

![](./img/007.png)

Aceptamos y avanzamos.

![](./img/008.png)

Accedemos al apartado **System>Package Manage>Package Installer**.

![](./img/009.png)

![](./img/010.png)

#### ***Creación de usuarios***. <a name="id4"></a>

Creamos el usuario VPN para las conexiones VPN y configuramos alguna que otra opción.

![](./img/011.png)


#### ***Conexión VPN***. <a name="id5"></a>

Editamos las opciones de conexión de los clientes haciendo que accedan mediante la interfaz WAN y especificamos el host de la máquina servidor

![](./img/012.png)

Especificamos que usuario es el que se va a conectar mediante el uso de la pasarela/túnel.

![](./img/013.png)

Configuramos algunos áspectos más como el certificado usado para el servicio.

![](./img/014.png)

Aquí cambiamos la opción de gateway a IPv4 only.

![](./img/015.png)

En el apartado de **Services>OpenVPN>Open-VPN-Clientexport** descargamos el ejecutable para windows de 64 bits y lo ejecutamos en la máquina cliente y lo ejecutamos de todas formas.

![](./img/016.png)

Instalamos

![](./img/017.png)

Instalamos los paquetes adicionales.

![](./img/018.png)

Nos sale el siguiente cuadro de inicio de sesión.

![](./img/019.png)
