Reto:
Obtener la bandera copiando la salida en un archivo.

Descripción:
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 14291`.

Solución:
Extraer la información del link y copiar la información a un archivo para hacer la busqueda.
-Obtener la información y colocarla en un archivo.
```
$ nc jupiter.challenges.picoctf.org 14291 > out.txt
```
-Buscar la bandera en el archivo usando el comando **egrep**
```
$ egrep -n 'pico' out.txt
```

-El resultado fue: **picoCTF{digital_plumb3r_ea8bfec7}**

Notas adicionales:
-El símbolo '>' es usado para indicar a donde copiar la salida de un comando.

Referencias:
https://atareao.es/como/guardar-la-salida-de-un-comando-en-un-archivo-con-logsave/
