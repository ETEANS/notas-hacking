
**Reto:**
-Encontrar la bandera del archivo de imagen y la forma de desencriptarlo.

**Descripción:**
-Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.
- [Download compressed disk image](https://artifacts.picoctf.net/c/214/disk.flag.img.gz)

**Solución:**

-Descargar el archivo y descomprimirlo.
-Usar el siguiente comando para mostrar las particiones de la imagen.
```
$ ./mmls disks/disk.flag.img
```
-Copiar el número de inicio de la última partición.
-Ejecutar el siguiente comando para extraer la llave encriptada.
```
$ ./icat -o <numero_inicio> disk.flag.img 1782 > flag.txt.enc
```
-Ejecutar el comando `strings` para buscar una cadenas.
```
$ strings -t d disk.flag.img | grep flag.txt
```
-Copiar el comando `openssl` y modificarlo para hacer el proceso inverso:
```
$ openssl aes256 -d -salt -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567
```
-Una vez que el comando es ejecutado correctamente, ingresa el siguiente comando:
```
$ cat flag.txt
```
-El contenido del archivo es la bandera.

El resultado es: **picoCTF{h4un71ng_p457_1d02081e}**.

**Notas adicionales:**
-El archivo que contiene la llave esta en la carpeta root, es necesario buscarlo de forma manual.
-El comando `openssl` se cambia el orden de los parámetros y se agrega la instrucción `-d` para indicar desencriptación.

**Referencias:**
https://www.sleuthkit.org/index.php
https://www.autopsy.com/download/