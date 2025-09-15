
Reto:
Encontrar la bandera utilizando Git.

Descripción:
-Someone's commits seems to be preventing the program from working. Who is it?

Solución:
Acceder al registro de commits a traves de Git para encontrar la bandera.
-Accede a la carpeta que contiene la carpeta '.git'
-Crear un archivo que guarda los commits registrados.
-Consulta los commits con 'git log' y envía la salida a un archivo.
```
$ git log > commits.txt
```
-Revisa el archivo creado para obtener la bandera.
```
$ grep 'pico' commits.txt
```

El resultado es: **picoCTF{@sk_th3_1nt3rn_2c6bf174}**.

Notas adicionales:
-La salida del texto puede que no tenga formato, es asignarle un formato al nuevo archivo.

Referencias:
https://primer.picoctf.org/#_git_version_control