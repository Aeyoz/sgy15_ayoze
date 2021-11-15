# Phishing con SET (Social Engineering Toolkit)

## Introducción

La herramienta que vamos a usar en esta practica se llama SET o Social Engineering Toolkit. Con ella podemos realizar una gran cantidad de ataques a la máquina cliente de windows 7 que tenemos preparada, pero en esta nos centraremos en el phishing, es decir capturar contraseñas y usuarios en sitios como facebook, reddit, ultimainformatica...


## Herramienta

Empezamos abriendo la herramienta.

![](./img/001.png)

Este es el panel inicial de la herramienta, elegimos las opciones 4 y 5 para actualizar la herramienta.

![](./img/002.png)

![](./img/003.png)

![](./img/004.png)

Ahora que está actualizada la herramienta, elegimos la opción 1 (Social-Engineering Attacks)

![](./img/005.png)

Dentro de la opción 1 se nos presentan aún más opciones, pero solo vamos a usar la segunda, es decir Website Attack Vectors.

![](./img/006.png)

Elegimos la opción 5 para atacar a los sitios web.

![](./img/007.png)

Elegimos la segunda opción 2 para clonar los sitios web.

![](./img/008.png)

La primera vez nos sale el siguiente aviso. Después de este nos solicita una IP, podemos dejar este espacio en blanco, ya que queremos nuestra que nuestra máquina almacene los ficheros de configuración de las páginas clonadas o bien podemos poner una ip de destino.

![](./img/009.png)

Elegimos la página de login de Facebook.

![](./img/012.png)

## Facebook

Una vez le demos enter a la url, debemos de ir a un navegador y poner la ip 127.0.0.1 en la barra de busqueda y nos saldrá lo siguiente, debemos de acceder a esa url nueva para ver la página clonada.

![](./img/018.png)

Vemos que nos muestra en pantalla una copia exacta de la página de Facebook. Introducimos tanto usuario como contraseña falsos.

![](./img/019.png)

Vemos que nos salen el usuario y contraseña falsos.

![](./img/021.png)

Vemos que el archivo con esta información se guarda en **/root/.set/reports**.

![](./img/022.png)

### Facebook desde el víctima.

Hacemos lo mismo desde la máquina víctima para comprobar que funciona.

![](./img/023.png)

![](./img/024.png)

La página se ve media extraña en el navegador, pero es porque el navegador es antiguo.

![](./img/025.png)

Vemos que nos sale la contraseña y usuario en el reporte que nos da al ejecutar la herramienta.

![](./img/026.png)

Vemos que nos salen la contraseña y el usuario en el archivo.

![](./img/027.png)

## Reddit

Repetimos el mismo proceso con la página de reddit.

![](./img/028.png)

Vemos que la página de reddit luce extraña (letras que tengan tildes).

![](./img/029.png)

Vemos que nos pilla la contraseña y el usuario.

![](./img/030.png)

![](./img/031.png)

## Ultima Informática.

La página de login de Ultima Informática luce así.

![](./img/032.png)

![](./img/033.png)

Repetimos el proceso aquí y vemos que nuestra página luce exactamente igual a la página real. Introducimos usuario y contraseña.

![](./img/035.png)

Vemos que en el reporte nos sale tanto el usuario y contraseña.

![](./img/034.png)
