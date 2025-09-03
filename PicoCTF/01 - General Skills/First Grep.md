Reto:
Encontrar la bandera en un archivo.

Descripción:
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/315d3325dc668ab7f1af9194f2de7e7a/file)? This would be really tedious to look through manually, something tells me there is a better way.

Solución:
Buscar la bandera en el archivo mediante comandos
-Ejecutar el comando 'grep' para buscar la bandera en el archivo.
```
grep 'picoCTF' file
```

-El resultado fue: **picoCTF{grep_is_good_to_find_things_f77e0797}**

Notas adicionales:
-Al usar "-n" en el comando, la salida va a mostrar el número o los números donde esta presente la sentencia

Referencias:
https://ryanstutorials.net/linuxtutorial/grep.php
