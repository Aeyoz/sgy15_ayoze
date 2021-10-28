# Cifrado de archivos en Windows 7 y Windows 10

## Cifrado de archivos en Windows 7.

### Creación de usuarios.

Nos dirigimos a Panel de control → Cuentas de usuario y protección infantil → Control parental → Crear nueva cuenta de usuario.

![win7](./img/win7/001.png)

Creamos los usuarios normal y encriptado

![win7](./img/win7/002.png)

![win7](./img/win7/003.png)

Ahora con los usuarios creados debemos de otorgarles permisos de administrador.

![win7](./img/win7/004.png)

Iniciamos sesión con cada uno de ellos y cambiamos el tipo de cuenta de **Usuario estándar** a **Administrador**.

![win7](./img/win7/025.png)



### Activación del servicio de "Sistema de cifrado de archivos (EFS)"

Debemos de teclear el "Shortcut" **Win + R** y escribir services.msc y buscamos el servicio llamado **"Sistema de cifrado de archivos EFS"** y lo activamos e iniciamos.

![win7](./img/win7/023.png)

### Cifrado de archivos.

Para crear certificados de cifrado debemos de acceder a la utilidad de cifrado de archivos y seguir los pasos guiados por la interfaz.

![win7](./img/win7/098.png)

![win7](./img/win7/012.png)

![win7](./img/win7/013.png)

![win7](./img/win7/014.png)

![win7](./img/win7/015.png)

Guardaremos el certificado dentro de la carpeta certs dentro del disco duro C.

![win7](./img/win7/016.png)

Seleccionamos la opción de actualizar los archivos de cifrado más tarde.

![win7](./img/win7/017.png)

Vemos un resumen del certificado de cifrado para archivos.

![win7](./img/win7/018.png)

Ahora debemos de entrar como usuario **enciptado** y debemos de crear una carpeta de nombre **encriptar** y añadimos un fichero de nombre **hola** dentro de esta para que tenga algo de contenido.

![win7](./img/win7/005.png)

![win7](./img/win7/006.png)

![win7](./img/win7/009.png)

![win7](./img/win7/010.png)

Vemos que tanto los archivos dentro de la carpeta como esta misma nos tienen las letras de color verde.

![win7](./img/win7/011.png)

Si intentamos quitar el cifrado de esta carpeta no podemos aunque seamos administradores.

![win7](./img/win7/022.png)

Vemos que tampoco podemos deneter el servicio de Sistema de cifrado de archivos (EFS)

![win7](./img/win7/023.png)

![win7](./img/win7/024.png)

Vemos que si intentamos editar el fichero tampoco nos lo permite.

![win7](./img/win7/020.png)

## Cifrado de archivos en Windows 10.

### Creación de usuarios.

Empezamos creando los usuarios **encriptado** y **normal** con sus contraseñas respectivas.

![win10](./img/win10/001.png)

![win10](./img/win10/002.png)

Les damos permisos de administrador a estos.

![win10](./img/win10/003.png)

### Activación del servicio de "Sistema de cifrado de archivos (EFS)"

Para activar el cifrado de archivos EFS de otra manera se puede ir a **Directivas d egrupo local** y activarla siguiendo las siguientes 5 imágenes.

![win10](./img/win10/004.png)

![win10](./img/win10/005.png)

![win10](./img/win10/006.png)

![win10](./img/win10/007.png)

![win10](./img/win10/008.png)

### Cifrado de archivos.

Ahora creamos en C la carpeta encripar y le añadimos dentro un archivo llamado hola.

![win10](./img/win10/009.png)

![win10](./img/win10/010.png)

![win10](./img/win10/011.png)

Al aceptar el cifrado se nos genera un certificado de cifrado. Seguimos los pasos por defecto.

![win10](./img/win10/012.png)

![win10](./img/win10/013.png)

![win10](./img/win10/014.png)

![win10](./img/win10/015.png)

Seleccionamos una ruta para guardar el certificado.

![win10](./img/win10/016.png)

Vemos un resumen de la exportacion del certificado.

![win10](./img/win10/017.png)

Vemos que ahora si está cifrada la carpeta.

![win10](./img/win10/019.png)

![win10](./img/win10/022.png)

Vemos que al intentar acceder a este y vemos que nos niega el acceso.

![win10](./img/win10/023.png)

Si intentamos desactivar el servicio vemos que no podemos.

![win10](./img/win10/024.png)

![win10](./img/win10/025.png)
