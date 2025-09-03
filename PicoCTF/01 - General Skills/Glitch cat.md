Reto:
-Obtener y reparar la bandera.

Descripción:
-Our flag printing service has started glitching!
 Additional details will be available after launching your challenge instance.

Solución:
Activar el servicio para obtener la cuenta y arreglar la bandera.
-Inicializar el servicio para obtener la bandera
-Obtener la bandera mediante la terminal de Linux
```
$ nc saturn.picoctf.net 61253
```
-Convertir los números separados de la bandera a caracteres en Python
```
my_string = 'picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'

print(my_string)
```

-El resultado fue: **picoCTF{gl17ch_m3_n07_a4392d2e}**

Notas adicionales:
-Fue necesario iniciar una instancia en picoCTF para obtener la bandera.

Referencias
https://www.geeksforgeeks.org/linux-unix/practical-uses-of-ncnetcat-command-in-linux/
