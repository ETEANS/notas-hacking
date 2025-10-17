
**Reto:**
-Buscar la llave dentro de un archivo de imagen de disco para obtener la bandera. 

**Descripción:**
-Download this disk image, find the key and log into the remote machine.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.
- [Download disk image](https://artifacts.picoctf.net/c/69/disk.img.gz)
- Remote machine: `ssh -i key_file -p 50479 ctf-player@saturn.picoctf.net`

**Solución:**
Buscar el archivo que contiene la llave de acceso usando Sleuthkit, copiar la llave a un archivo, entrar a la conexión con el archivo y consultar la bandera.
-Descargar el archivo y descomprimirlo.
-Usar el siguiente comando para mostrar las particiones de la imagen.
```
$ ./mmls disks/disk.flag.img
```
-Copiar el número de inicio de la última partición.
-Ejecutar el siguiente comando.
```
$ ./icat -o <número inicio> disks/disk1.img 2345 > key_file
```
-Reasigna los permisos del archivo con el siguiente comando:
```
$ chmod 400 key_file
```
-Ingresa a la conexión.
```
$ ssh -i key_file -p 50479 ctf-player@saturn.picoctf.net
```
-Una vez que el `key_file` es aceptado, ingresa el siguiente comando:
```
$ cat flag.txt
```
-El contenido del archivo es la bandera.

El resultado es: **picoCTF{k3y_5l3u7h_339601ed}**.

**Notas adicionales:**
-El archivo que contiene la llave esta en la carpeta root, es necesario buscarlo de forma manual.
-El archivo llave empieza con el texto `-----BEGIN OPENSSH PRIVATE KEY-----`

**Referencias:**
https://www.sleuthkit.org/index.php
https://www.autopsy.com/download/