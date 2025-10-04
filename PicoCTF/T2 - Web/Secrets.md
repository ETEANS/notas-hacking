
**Reto:**
-Encontrar las carpetas ocultas de la página para obtener la bandera.

**Descripción:**
-We have several pages hidden. Can you find the one with the flag?
-The website is running [here](http://saturn.picoctf.net:52664/).

**Solución:**
Buscar por las carpetas mencionadas y dirigirse a los índices de las carpetas hasta encontrar la bandera.
-Abrir la pagina.
-Presiona las teclas "Ctrl+Shift+i" para abrir las herramientas de desarrollador.
-Buscar la carpeta 'secret' e ingresa la carpeta a la dirección.
-Dentro de la carpeta 'secret', ingresar a la carpeta 'hidden'.
-Dentro de la carpeta 'hidden', buscar una referencia en el código.
-Entrar a la carpeta superhidden.
-Dentro de esta carpeta, revisar el código de la pagina y encontrar la bandera

El resultado es: **picoCTF{succ3ss_@h3n1c@10n_51b260fe}**.

**Notas adicionales:**
-Una forma de deducir las carpetas de una página es con el comando `gobuster`.
```
$ gobuster dir -u http://saturn.picoctf.net:57151/  -w /usr/share/wordlists/dirb/common.txt -x css,js,txt,php
```

**Referencias:**
http://saturn.picoctf.net:52664/
https://rinku.tech/curso-kali-linux/utilizar-gobuster/