
Reto:
Descomprimir una carpeta y encontrar el archivo indicado.

Descripción:
Unzip this archive and find the file named 'uber-secret.txt'

Solución:
Descomprimir la carpeta a otra carpeta y extraer la bandera usando el comando 'grep' en el archivo que se busca.
-Descomprimir la carpeta usando el comando 'unzip'.
```
$ unzip files.zip
```
-Buscar la bandera en el archivo especifico.
```
$ grep -n 'pico' files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
```

-El resultado es: **picoCTF{f1nd_15_f457_ab443fd1}**

Notas adicionales:
-Se puede referenciar el directorio que se quiere excanear aún si el comando no se ejecuta en em mismo directorio

Referencias:
https://askubuntu.com/questions/86849/how-to-unzip-a-zip-file-from-the-terminal
https://askubuntu.com/questions/55325/how-to-use-grep-command-to-find-text-including-subdirectories