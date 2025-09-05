Reto:
Conectarse a un sistema remoto y extraer la bandera de distintos archivos

Descripción:
-Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin. Login via `ssh` as `ctf-player` with the password, `b60940ca`
Additional details will be available after launching your challenge instance.

Solución:
Conectarse a la red y leer los archivos que contienen la bandera.
-Conectarse a la instancia creada e ingresar la contraseña.
```
$ ssh ctf-player@venus.picoctf.net -p 55416
```
-Buscar los archivos y consultar el archivo de la bandera
```
$ ls
$ cat 1of3.flag.txt
```
-Una vez obtenida la primera parte de la bandera (picoCTF{xxsh_), consultar el archivo de instrucciones y dirigirse al directorio que indica
```
$ cat instructions-to-2of3.txt
$ cd /
```
-Las instrucciones indican que la siguiente parte de la bandera se encuentra en la carpeta 'root', una vez en ella, consultar los archivos y obtener la siguiente parte de la bandera.
```
$ ls
$ cat 2of3.flag.txt
```
-Ahora que la segunda parte de la bandera (0ut_0f_\/\/4t3r_) fue conseguida, consultar el archivo de instrucciones y dirigirse al directorio que indica.
```
$ cat instructions-to-3of3.txt
$ cd ~
```
-Las instrucciones indican que la última parte de la bandera se encuentra en la carpeta 'home', una vez en ella, consultar los archivos y obtener la siguiente parte de la bandera.
```
$ ls
$ cat 3of3.flag.txt
```

El resultado es: **picoCTF{xxsh_0ut_0f_\/\/4t3r_c1754242}**

Notas adicionales:
-Los comandos 'cd /' y 'cd ~' siven para acceder a las carpetas 'root' y 'home' respectivamente.
-Hay directorios en la carpeta 'root' que tienen el acceso prohibido, lo que dificulta la navegación con el comando 'grep'

Referencias
https://www.hostinger.com/mx/tutoriales/comando-cat-linux
https://www.ionos.mx/digitalguide/servidores/configuracion/comando-cd-de-linux/