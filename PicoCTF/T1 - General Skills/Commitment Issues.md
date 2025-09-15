
Reto:
Revertir un commit para obtener la bandera.

Descripción:
I accidentally wrote the flag down. Good thing I deleted it!

Solución:
Regresar hasta el commit donde se ingreso la bandera.
-Accede a la carpeta que contiene la carpeta '.git'.
-Revisa los commits del repositorio con el siguiente comando.
```
$ git log
```
-Busca el registro que menciona la bandera, copia el id del commit y revierte al commit con el siguiente comando.
```
$ git reset --hard <id del commit>
```
-Una vez ejecutada la regresión, accede al archivo 'message.txt'.
```
$ cat message.txt
```
-En el archivo se encuentra la bandera.

El resultado es: **picoCTF{s@n1t1z3_30e86d36}**.

Notas adicionales:
-Existen dos formas de revertir commits, 'git reset' y 'git revert'.

Referencias:
https://primer.picoctf.org/#_git_version_control