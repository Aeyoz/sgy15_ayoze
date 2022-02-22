<center>

# Evasión con msfvenom y Veil.


</center>

***Nombre:*** Ayoze Hernández Díaz
***Curso:*** 2º de Ciclo Superior de Administración de Sistemas Informáticos en Red.

### ÍNDICE

+ [Introducción](#id1)
+ [Objetivos](#id2)
+ [Msfvenom](#id3)
+ [Veil](#id4)



#### ***Introducción***. <a name="id1"></a>

En esta práctica se van a usar las herramientas de Kali Linux para generar archivos maliciosos para que Virus Total los analice.

#### ***Objetivos***. <a name="id2"></a>

El objetivo de esta práctica es el visionado de diferentes técnicas de evasión, para ello generaremos varios archivos con varias herramientas o utilidades.

#### ***Msfvenom***. <a name="id3"></a>

Con la herramienta de **msfvenom** listaremos la gran variedad de encoders o codificadores que podemos usar para generar archivos.

![](./img/001.png)

Primero generamos un archivo llamado meterpreter.exe que nos permitirá acceder mediante una sesión meterpreter con un payload basado en reverse_tcp siendo nuestra ip la 10.0.2.15.

![](./img/003.png)

Volvemos a generar un archivo meterpreter2.exe que se camufla más que el anterior debido al uso de un encoder.

![](./img/004.png)

Subiremos estos 2 archivos a Virus Total.

**meterpreter.exe**:

![](./img/007.png)

**meterpreter2.exe**:

![](./img/009.png)

Ahora veremos un ejemplo más práctico para esta herramienta, para ello necesitaremos la aplicación de **putty** como paquete víctima.

![](./img/010.png)

Volvemos a usar la herramienta de msfvenom, con la diferencia de que esta vez no vamos a crear un paquete, sino que vamos a infectar uno ya existente.

Como con las 2 prácticas anteriores, usamos el método de entrar por la herramienta de hfs (HTTP File Server).

![](./img/015.png)

Ahora debemos de ejecutar el programa y abrir una sesión meterpreter.

![](./img/012.png)

Ahora debemos de ejecutar el programa y abrir una sesión meterpreter y vemos que con exito se abrió.

![](./img/014.png)


#### ***Veil***. <a name="id4"></a>

Ahora el otro método que usaremos para intentar evadir el escaner de Virus Total es el uso de la herramienta **veil**, si intentamos ejecutar veil vemos que no lo tenemos instalado, por lo que accedemos a ello.

![](./img/016.png)

Una vez realizado el proceso de instalación debemos de instalar componentes adicionales mediante la interfaz del propio veil.

![](./img/017.png)

![](./img/021.png)

Cuando esta instalación termina somos capaces de usar el veil.

![](./img/022.png)

Usamos la herramienta de evasión.

![](./img/023.png)

Seleccionamos el payload **cs/meterpreter/rev_tcp.py**.

![](./img/024.png)

Ahora especificamos que el puerto que escuchará es el **444** y que la ip que tiene la máquina atacante es la **172.19.0.6** y generamos el fichero **prueba.exe**.

![](./img/025.png)

Subimos el fichero a Virus Total y comprobamos que es funcional.

![](./img/026.png)

![](./img/027.png)

Abrimos una sesión meterpreter y entramos a la máquina.

![](./img/028.png)

![](./img/029.png)
