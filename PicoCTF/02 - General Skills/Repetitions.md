Reto:
Decodificar un archivo múltiples veces.

Descripción:
Can you make sense of this file?

Solución:
Utilizar un decodificador web de base 64, copiar el resultado y decodificar el resultado de nuevo hasta encontrar la bandera.
-Consultar la información del archivo.
```
$ cat enc_flag
```
-Desencriptar la información del archivo y obtener el resultado.
-Desencriptar el resultado hasta encontrar la bandera (repetir este paso)
-En total se hicieron 6 recursiones para encontrar la bandera.

El resultado es: **picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_de523f49}**

Notas adicionales:
-Es posible decodificar en base 64 desde la terminal usando el siguiente comando.
```
$ echo "<insertar cadena encriptada>" | base64 -d
```

Referencias:
https://www.base64decode.org/
https://askubuntu.com/questions/178521/how-can-i-decode-a-base64-string-from-the-command-line