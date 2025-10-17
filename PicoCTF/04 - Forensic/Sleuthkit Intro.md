
**Reto:**
-Encontrar el tamaño de una partición de una imagen de disco.

**Descripción:**
-Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.[Download disk image](https://artifacts.picoctf.net/c/164/disk.img.gz)Access checker program: `nc saturn.picoctf.net 60747`.

**Solución:**
Utilizar Sleuthkit para analizar las particiones de la imagen, de ahí, entrar a la conexión e ingresar el tamaño de la partición.
-Descargar el archivo y descomprimirlo.
-Usar el siguiente comando para mostrar las particiones de la imagen.
```
$ ./mmls disks/disk.img
```
-Copiar la longitud de la última línea.
-Entrar a la conexión con el siguiente comando:
```
$ nc saturn.picoctf.net 60747
```
-Ingresar la longitud de la partición.
-Si la longitud ingresada es correcta, la bandera aparece en pantalla.

El resultado es: **picoCTF{mm15_f7w!}**.

**Notas adicionales:**
-Es necesario instalar el Sleuthkit para ejecutar los comandos.

**Referencias:**
https://www.sleuthkit.org/index.php