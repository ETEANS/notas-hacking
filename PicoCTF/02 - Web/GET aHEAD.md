
**Reto:**
Obtener la bandera cambiando el método de la pagina.

**Descripción:**
Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:21939/](http://mercury.picoctf.net:21939/)

**Solución:**
Cambiar el método de solicitud de POST a HEAD para conseguir la bandera.
-Abrir la página.
-Obtener el tipo de método usado.
-Ejecutar un cómando en la terminal que cambia el método a HEAD.
```
$ curl -I http://mercury.picoctf.net:21939/index.php
```
-Una vez presionado enter, la bandera aparecerá en pantalla.

El resultado es: **picoCTF{r3j3ct_th3_du4l1ty_6ef27873}**.

**Notas adicionales:**
-Es posible cambiar los métodos desde el navegador utilizando la herramienta Burp Suite.

**Referencias:**
[http://mercury.picoctf.net:21939/](http://mercury.picoctf.net:21939/)
https://developer.mozilla.org/es/docs/Web/HTTP/Reference/Methods