
**Reto:**
-Buscar un archivo dentro de un archivo .pptm que contiene la bandera.

**Descripción:**
-I've hidden a flag in this file. Can you find it? [Forensics is fun.pptm](https://mercury.picoctf.net/static/3944a59474f9f676942282c50b9c3675/Forensics%20is%20fun.pptm)

**Solución:**
Descomprimir el archivo .pptm y buscar el archivo oculto que contiene la bandera.
-Descargar el archivo.
-Cambiar la extensión del archivo a .zip.
-Descomprimir el archivo
-Buscar el archivo llamado 'hidden'.
-Abrir el archivo y copiar el contenido.
-Desencriptar el contenido en base64.
-El contenido desencriptado es la bandera.

El resultado es: **picoCTF{D1d_u_kn0w_ppts_r_z1p5}**.

**Notas adicionales:**
-Es necesario tener activada la opción de ver archivos ocultos para ver el archivo.

**Referencias:**
https://www.converter365.com/presentation-converter/pptm/pptm-to-zip