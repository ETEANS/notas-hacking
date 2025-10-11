
**Reto:**
-Obtener la bandera desde una terminal con comandos reducidos.

**Descripción:**
-Reception of Special has been cool to say the least. That's why we made an exclusive version of Special, called Secure Comprehensive Interface for Affecting Linux Empirically Rad, or just 'Specialer'. With Specialer, we really tried to remove the distractions from using a shell. Yes, we took out spell checker because of everybody's complaining. But we think you will be excited about our new, reduced feature set for keeping you focused on what needs it the most. Please start an instance to test your very own copy of Specialer.`ssh -p 59123 ctf-player@saturn.picoctf.net`. The password is `fd7746b4`

**Solución:**
Utilizar el comando echo para mostrar la salida de los archivos de texto en la terminal.
-Entrar al programa con el siguiente comando e ingresar la contraseña.
```
$ ssh -p 59123 ctf-player@saturn.picoctf.net
```
-Buscar los archivos y carpetas con el comando `echo`.
```
$ echo *
```
-Leer los archivos de los directorios disponibles con el siguiente comando:
```
$ echo $(<[nombre_del_archivo])
```
-Al examinar el archivo 'kazam.txt', la bandera aparecerá en pantalla

El resultado es: **picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_38f5cc78}**.

**Notas adicionales:**
-Al presionar la tecla `tab` dos veces, aparecen los comandos disponibles.
-Para hacer esto, fue necesario revisar cada uno de los archivos uno por uno...

**Referencias:**
https://www.baeldung.com/linux/echo-file-input
https://josephkimiri.github.io/posts/Specialer/