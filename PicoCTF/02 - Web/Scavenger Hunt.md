
**Reto:**
-Buscar en los archivos de la página las partes de la bandera.

**Descripción:**
-There is some interesting information hidden around this site [http://mercury.picoctf.net:44070/](http://mercury.picoctf.net:44070/). 
  Can you find it?

**Solución:**
Examinar los archivos que indican los comentarios de las banderas.
-Abrir la página.
-Presiona las teclas "Ctrl+Shift+i" para abrir las herramientas de desarrollador.
-Copiar la primera parte de la bandera que aparece en un comentario en el archivo html.
-Revisar el archivo css y copiar la segunda parte de la bandera en el archivo.
-Con la pista del archivo js, ingresar "robots.txt" para ingresar al archivo y copiar la tercera parte de la bandera.
-Con la pista del archivo robots, ingresar ".htaccess" en la dirección para ingresar al archivo y copiar la cuarta parte de la bandera.
-Con la pista del archivo .htaccess, ingresar "DS_Store" en la dirección para ingresar al archivo y copiar la última parte de la bandera.

El resultado es: **picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_7a46d25d}**.

**Notas adicionales:**
-Una página puede contener múltiples archivos ocultos.

**Referencias:**
[http://mercury.picoctf.net:44070/](http://mercury.picoctf.net:44070/)
https://developers.google.com/search/docs/crawling-indexing/robots/intro?hl=es
https://httpd.apache.org/docs/2.4/howto/htaccess.html 
https://www.vozidea.com/archivos-ds_store