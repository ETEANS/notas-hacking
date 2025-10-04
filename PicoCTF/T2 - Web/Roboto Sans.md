
**Reto:**
-Obtener la bandera en los archivos ocultos de la página.

**Descripción:**
-The flag is somewhere on this web application not necessarily on the website. Find it.
-Check [this](http://saturn.picoctf.net:60563/) out.

**Solución:**
Buscar en el archivo `robots.txt` y utilizar las pistas del archivo para obtener la bandera.
-Abrir la página.
-Escribir al final de la dirección de la página el texto "robots.txt".
-Dentro del archivo, copiar la segunda línea encriptada en base64.
-Una vez desencriptada, esta linea revela la ubicación de la bandera.
-Escribir la dirección en la página.
-Una vez dentro del archivo, la bandera aparecerá en la página.

El resultado es: **picoCTF{Who_D03sN7_L1k5_90B0T5_22ce1f22}**.

**Notas adicionales:**
-Las otras cadenas encriptadas son distracciones.

**Referencias:**
http://saturn.picoctf.net:60563/
https://developers.google.com/search/docs/crawling-indexing/robots/intro?hl=es#what-is-a-robots.txt-file-used-for