
**Reto:**
-Moverse por la terminal usando solamente números y símbolos.

**Descripción:**
-The Multiverse is within your grasp! Unfortunately, the server that contains the secrets of the multiverse is in a universe where keyboards only have numbers and (most) symbols.`ssh -p 49415 ctf-player@mimas.picoctf.net`Use password: `f3b61b38`

**Solución:**
Utilizar wildcards para leer el archivo flag.txt con un programa de la terminal y obtener la bandera.
-Entrar al ssh e ingresar la contraseña.
```
ssh -p 49415 ctf-player@mimas.picoctf.net
```
-Obtener la localización de la bandera con el siguiente comando:
```
$ */*
```
-Utilizar el script de base64 para leer el contenido del archivo en base64 con el siguiente comando:
```
$ /???/???[!_]64 /????/??????????/??????/????????
```
-El contenido del archivo va a aparecer en la terminal encriptado en base64.
-Desencripta el texto en base64.
-El texto desencriptado es la bandera.

El resultado es **picoCTF{7h15_mu171v3r53_15_m4dn355_640b6add}**.

**Notas adicionales:**
-Es necesario revisar los archivos de la terminal para averiguar donde se encuentran las carpetas y archivos.
-Los wildcards son simbolos que son representados por unidades de información.

**Referencias:**
https://rsg-ecuador.github.io/unix.bioinfo.rsgecuador/content/Curso_basico/03_Manejo_terminal/5_wildcards.html
https://tldp.org/LDP/abs/html/globbingref.html
https://tldp.org/LDP/GNU-Linux-Tools-Summary/html/x11655.htm
