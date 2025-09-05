Reto:
Descomprimir una carpeta y encontrar la bandera en los archivos de la carpeta.

Descripción:
Unzip this archive and find the flag.

Solución:
Descomprimir la carpeta a otra carpeta y extraer la bandera usando el comando 'grep'.
-Descomprimir la carpeta usando el comando 'unzip'.
```
$ unzip big-zip-files.zip
```
-Buscar la bandera en los archivos descomprimidos utilizando el comando 'grep' de forma recursiva.
```
$ grep -r 'pico' big-zip-files/*
```

-El resultado es: **picoCTF{gr3p_15_m4g1c_ef8790dc}**

Notas adicionales:
-La letra '-r' en el comando grep es usado para indicar que la busqueda se va a hacer de forma recursiva en un directorio, incluyendo los subdirectorios.

Referencias
https://askubuntu.com/questions/86849/how-to-unzip-a-zip-file-from-the-terminal
https://askubuntu.com/questions/55325/how-to-use-grep-command-to-find-text-including-subdirectories