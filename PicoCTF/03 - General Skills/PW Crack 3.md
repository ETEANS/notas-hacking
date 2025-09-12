
Reto:
Desencriptar la contraseña correcta para obtener la bandera del programa.

Descripción:
Can you crack the password to get the flag?
Download the password checker [here](https://artifacts.picoctf.net/c/16/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/16/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/16/level3.hash.bin) in the same directory too.
There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.

Solución:
Abrir el código con un editor de texto binario, ver la contraseña y ejecutar el programa con la contraseña memorizada.
-Abrir el archivo "level3.hash.bin" con bvi.
```
$ bvi level3.hash.bin
```
-Obtener la contraseña con los valores hexadecimales del archivo.
-Abrir el archivo del código.
-Comparar los valores del archivo hash con los valores comentados del código.
-Una vez obtenida la contraseña, ejecutar el programa e ingresar la contraseña.
```
$ python level3.py
```
-Una vez ejecutado el programa correctamente, la bandera se mostrara en pantalla.

El resultado es: **picoCTF{m45h_fl1ng1ng_2b072a90}**

Notas adicionales:
-El comando "bvi" se diferencia de "vi" por el hecho de que muestra los caracteres del archivo en diferentes bases.

Referencias:
https://linux.die.net/man/1/bvi