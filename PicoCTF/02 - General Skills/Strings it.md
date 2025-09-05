
Reto:
Obtener la bandera de un archivo encriptado a partir de cadenas

Descripción:
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings) without running it?

Solución:
Obtener las cadenas del archivo ejecutando el comando 'strings' en el archivo encriptado y consultar la bandera.
-Ejecutar el comando 'strings' referenciando el archivo y el archivo donde guardar la salida.
```
$ strings strings > out.txt
```
-Consultar el archivo para buscar la bandera (el siguiente comando es de PowerShell).
```
$ Select-String -Path out.txt -Pattern "pico"
```

El resultado es: **picoCTF{5tRIng5_1T_7f766a23}**

Notas adicionales:
-La salida del archivo es en formato UTF-16 LE, el cuál no es reconocido por el comando 'grep', 
 para escanear este formato con 'grep', es necesario utilizar el comando 'iconv' para convertir el formato del texto.
 Ejemplo:
```
 iconv -f UTF-16LE -t UTF-8 out.txt | grep "pico"
```

Referencias:
https://linux.die.net/man/1/strings
https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1702770#:~:text=*Esta%20opci%C3%B3n%20se%20agreg%C3%B3%20en,Codifica%20en%20formato%20UTF%2D8.&text=utf32:%20Codifica%20en%20formato%20UTF%2D32.