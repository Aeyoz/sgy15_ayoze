
<center>

# Hack Windows usando TCP reverse.


</center>

***Nombre:*** Ayoze Hernández Díaz

***Curso:*** 2º de Ciclo Superior de Administración de Sistemas Informáticos en Red.

### ÍNDICE

+ [Introducción](#id1)
+ [Objetivos](#id2)
+ [Uso de msfvenom](#id3)
+ [Sesión meterpreter](#id4)
+ [Conexión](#id5)

#### ***Introducción***. <a name="id1"></a>

En esta práctica se van a usar las herramientas de Kali Linux para intentar colar un troyano en Windows 7/10.

#### ***Objetivos***. <a name="id2"></a>

El objetivo es que, mediante el uso de msfvenom y msfconsole podamos abrir una sesión de meterpreter en la máquina de Windows y tener acceso desde Kali.

#### ***Uso de msfvenom***. <a name="id3"></a>

Con msfvenom podemos generar un archivo **install_adobe.exe** que será el detonante de la sesión meterpreter, para ello debemos de ejecutar el siguiente comando mostrado en la imagen.

![](./img/001.png)

Vemos que el archivo se ha generado el la ruta **/root**.

![](./img/002.png)

Podemos hacer que el archivo sea menos detectable por páginas como [**Virus Total**](https://www.virustotal.com/gui/home/upload) con la siguiente linea de comando.

![](./img/003.png)

Vemos que se ha generado un **install_adobe2.exe**.

![](./img/004.png)

#### ***Sesión meterpreter***. <a name="id4"></a>

Para poder abrir la sesión meterpreter debemos de encontrar alguna manera de pasar el archivo "bichado" a la máquina target/objetivo/víctima. Para ello haremos uso del programa **hfs** (HTTP File Server) usado en la práctica anterior de la misma manera.

En las siguientes imagenes se puede ver el proceso a seguir para que se pueda pasar el archivo mediante este tipo de servicio. Para ello debemos de usar el multi/handler y usar el payload adecuado (**windows/meterpreter/reverse_tcp**) además debemos de especificar la Ip (LHOST) como el puerto de escucha de la máquina atacante.  

![](./img/005.png)

Además de lo ya mencionado debemos de especificar la Ip de la máquina target/objetivo/víctima como el puerto por el que escucha el servicio de hfs. Una vez configurado todo debemos de **"explotar"** la máquina atacada.

![](./img/006.png)

Ahora nos interesa subir el archivo install_adobe2.exe, por lo que hacemos un upload del archivo a la máquina target/objetivo/víctima.

![](./img/007.png)

Vemos que dentro de la ruta de la herramienta hfs se encuentra el ejecutable de **install_adobe2.exe**.

![](./img/008.png)

#### ***Conexión***. <a name="id5"></a>

Para poder conectar con la máquina que queremos atacar debemos de ejecutar el programa install_adobe2 en la máquina de Windows.

![](./img/009.png)

Usamos una sesión meterpreter como la anteriormente usada para subir el archivo, pero no especificamos parametros del lado de la víctima. Vemos que nos conectamos con éxito.

![](./img/010.png)

Podemos ver que hay unos cuantos comandos que podemos ejecutar, yo me informé quien era dentro de la máquina de Windows, es decir, de quién era la sesión con la que se abrió el archivo de install_adobe2.exe, miré además información del ordenador desde el que se había ejecutado y finalmente apagué la máquina de windows mediante meterpreter.

![](./img/011.png)

![](./img/012.png)

![](./img/013.png)
