
Reto:
Ejecutar el programa e introducir la contraseña para obtener la bandera.

Descripción:
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/12/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/12/level1.flag.txt.enc) in the same directory too.

Solución:
Abrir el código con un editor de texto, ver la contraseña y ejecutar el programa con la contraseña memorizada.
-Abrir el programa con un editor de texto
-Copiar la contraseña del programa (la contraseña esta en hexadecimal).
-Crear un programa para obtener la contraseña
```
print(chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36))
```
-Una vez obtenida la contraseña, ejecutar el programa e ingresar la contraseña.
```
$ python level2.py
```
-Una vez ejecutado el programa correctamente, la bandera se mostrara en pantalla.

El resultado es: **picoCTF{tr45h_51ng1ng_489dea9a}**

Notas adicionales:
-La función 'chr' convierte un número a su letra asociada en ASCII.

Referencias:
https://www.arsys.es/blog/comandos-nano