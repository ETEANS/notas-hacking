
**Reto:**
-Buscar el archivo que contiene la bandera dentro de una imagen de disco.

**Descripción:**
-Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.
- [Download compressed disk image](https://artifacts.picoctf.net/c/136/disk.flag.img.gz)

**Solución:**
Buscar el archivo flag dentro del archivo de imagen de disco y leer el archivo.
-Descargar el archivo y descomprimirlo.
-Usar el siguiente comando para mostrar las particiones de la imagen.
```
$ ./mmls disks/disk.flag.img
```
-Copiar el número de inicio de la última partición.
-Ejecutar el siguiente comando con el número copiado para buscar el número del archivo.
```
$ .\fls -o <numero_inicio> -r disks/disk.flag.img | grep 'flag'
```
-Busca el número que contiene el archivo "flag.uni.txt".
-Leer el archivo con el siguiente comando:
```
$ .\icat -o <numero_inicio> disks/disk.flag.img <numero_archivo>
```
-La bandera aparecerá en pantalla.

El resultado es: **picoCTF{by73_5urf3r_3497ae6b}**.

**Notas adicionales:**
-Para ver los inodos de las particiones, utiliza el siguiente comando.
```
$ .\fsstat -o <numero_inicio> <nombre_imagen>
```

**Referencias:**
https://www.sleuthkit.org/index.php