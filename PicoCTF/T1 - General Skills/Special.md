
Reto:
Encontrar la bandera estropeando un auto corrector.

Descripción:
Don't power users get tired of making spelling mistakes in the shell? Not anymore! Enter Special, the Spell Checked Interface for Affecting Linux. Now, every word is properly spelled and capitalized... automatically and behind-the-scenes! Be the first to test Special in beta, and feel free to tell us all about how Special streamlines every development process that you face. When your co-workers see your amazing shell interface, just tell them: That's Special (TM)
Start your instance to see connection details.`ssh -p 56150 ctf-player@saturn.picoctf.net`
The password is `3f39b042`

Solución:
Utilizar un `$` para ejecutar el comando sin ser afectado.
-Ingresar al servidor que contiene el programa.
```
$ ssh -p 56150 ctf-player@saturn.picoctf.net
```
-Una vez adentro ingresar el siguiente comando para evitar el auto corrector.
```
$ $(grep '-r' ''pico'' * )
```
-Una vez ingresado este comando, la bandera aparecerá en la terminal.

El resultado es: **picoCTF{5p311ch3ck_15_7h3_w0r57_f906e25a}**.

Notas adicionales:
-El simbolo $ permite ejecutar comandos en la terminal dentro de un script de bash.

Referencias:
https://man7.org/linux/man-pages/man1/grep.1.html
https://www.w3schools.com/bash/bash_script.php