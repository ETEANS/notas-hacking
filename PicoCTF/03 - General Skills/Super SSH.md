
Reto:
-Obtener la bandera usando Secure Shell

Descripción:
-Using a Secure Shell (SSH) is going to be pretty important.
  Can you `ssh` as `ctf-player` to `titan.picoctf.net` at port `59072` to get the flag?
  You'll also need the password `84b12bae`. If asked, accept the fingerprint with `yes`.
  If your device doesn't have a shell, you can use: [https://webshell.picoctf.org](https://webshell.picoctf.org/)
  If you're not sure what a shell is, check out our Primer: [https://primer.picoctf.com/#_the_shell](https://primer.picoctf.com/#_the_shell)

Solución:
Ejecutar el comando 'ssh' para conectarse al servidor y obtener la bandera dentro del shell.
-Ejecutar el comando 'ssh' con los datos necesarios.
```
$ ssh ctf-player@titan.picoctf.net -p 59072
```
-Ingresar la contraseña.
-Una vez ingresada la contraseña, la bandera va a aparecer en la terminal

El resultado es: **picoCTF{s3cur3_c0nn3ct10n_07a987ac}**

Notas adicionales:
-Los argumentos para ingresar son los siguientes: 
```
$ ssh [nombre de usuario]@[nombre de conexión] -p [número del puerto]
```

Referencias:
https://linux.die.net/man/1/ssh
[https://primer.picoctf.com/#_the_shell](https://primer.picoctf.com/#_the_shell)
[https://webshell.picoctf.org](https://webshell.picoctf.org/)