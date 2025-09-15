
Reto:

Descripción:
-How to automate tasks to run at intervals on linux servers?
  Use ssh to connect to this server:
```
Server: saturn.picoctf.net
Port: 50634
Username: picoplayer 
Password: ENAFb6zfzn
```

Solución:
Ingresar a la instancia y los archivos de ciertas carpetas para encontrar la bandera.
-Ingresar a la instancia con un comando de shell.
```
$ ssh -p 50634 picoplayer@saturn.picoctf.net
```
-Una vez dentro del servidor, ingresar a la carpeta 'etc' con el siguiente comando.
```
$ cd /etc/
```
-Ejecutar una busqueda por la bandera usando el comando 'grep', de forma recursiva por todas los archivos de la carpeta.
```
$ grep -r 'pico' * 
```
-El archivo que tenga la bandera se mostrara en la terminal junto con la bandera.

El resultado es: **picoCTF{Sch3DUL7NG_T45K3_L1NUX_1d781160}**.

Notas adicionales:
-El prefijo '-r' indica que se quiere buscar el los archivos de una carpeta de forma recursiva, es decir, buscar en los archivos dentro de otras carpetas. 

Referencias:
https://www.freecodecamp.org/espanol/news/grep-command-tutorial-how-to-search-for-a-file-in-linux-and-unix-with-recursive-find/