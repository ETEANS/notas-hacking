
Reto:
Utilizar la etiqueta de ayuda para obtener la bandera

Descripción:
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm) has extraordinarily helpful information...

Solución:
Obtener el archivo y ejecutar el programa con la etiqueta de ayuda, la cual debería tener la bandera.
-Obtener el archivo con el comando 'wget'.
```
$ wget https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm
```
-Otorgar permisos al archivo para que sea ejecutable, usando el comando 'chmod'.
```
$ chmod +x warm
```
-Ejecutar el archivo con el siguiente.
```
$ ./warm
```
-La ejecución del programa muestra un texto en la terminal que sugiere utilizar la etiqueta '-h'.
```
$ ./warm -h
```
-Tras ejecutar este comando, la salida en la terminal muestra la bandera.

El resultado es: **picoCTF{b1scu1ts_4nd_gr4vy_616f7182}**.

Notas adicionales:
-Al ejecutar el comando 'chmod', las etiquetas van a otorgar diferentes permisos al archivo, '-x' 
 otorga permisos para ejecutar el archivo, '-w' otorga permisos para escribir en el archivo y '-r' otorga permisos para leer el archivo.

Referencias:
https://www.freecodecamp.org/espanol/news/comando-chmod-como-cambiar-permisos-de-archivo-en-linux/