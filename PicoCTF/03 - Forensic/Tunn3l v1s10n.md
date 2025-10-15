
**Reto:**
-Obtener la bandera de una imagen corrupta.

**Descripción:**
-We found this [file](https://mercury.picoctf.net/static/01be2b38ba97802285a451b94505ea75/tunn3l_v1s10n). Recover the flag.

**Solución:**
Abrir la imagen con un editor hexadecimal y corregir los bytes necesarios para abrir la imagen y obtener la bandera.
-Descargar la imagen.
-Abrir el archivo con un editor hexadecimal.
-Cambiar el offset 0E a 28 y 0F a 00 para arreglar el archivo.
-Cambiar el offset 17 a 03.
-Guardar la imagen con extensión .bmp
-Abrir la imagen.
-La bandera aparecerá en la parte de arriba de la bandera.

El resultado es **picoCTF{qu1t3_a_v13w_2020}**.

**Notas adicionales:**
-Si los primeros 2 bytes del archivo son 'BM', significa que el archivo es un bitmap.
-Los 8 bytes en los offsets de 12 a 19 representan el ancho y alto de la imagen respectivamente (4 bytes para cadafimrndión).

**Referencias:**
https://en.wikipedia.org/wiki/BMP_file_format