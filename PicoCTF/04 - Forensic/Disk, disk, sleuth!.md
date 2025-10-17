
**Reto:**
-Buscar dentro de un archivo de imagen de disco la bandera.

**Descripción:**
-Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image: [dds1-alpine.flag.img.gz](https://mercury.picoctf.net/static/920731987787c93839776ce457d5ecd6/dds1-alpine.flag.img.gz)

**Solución:**
Utilizar el comando `srch_strings` en el archivo y buscar en la salida la bandera con un comando.
-Descargar y descomprimir el archivo.
-Ejecutar el siguiente comando:
```
$ srch_strings dds1-alpine.flag.img | grep 'pico'
```
-En una de las lineas se encuentra la bandera.

El resultado es **picoCTF{f0r3ns1c4t0r_n30phyt3_564ff1a0}**.

**Notas adicionales:**
-Es preferible usar en Linux, descarga los comandos de sleuthkit con el siguiente comando:
```
$ sudo apt install sleuthkit
```

**Referencias:**
https://www.sleuthkit.org/index.php