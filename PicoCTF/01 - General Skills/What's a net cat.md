
Reto:

Descripción:
Using netcat (nc) is going to be pretty important. Can you connect to `jupiter.challenges.picoctf.org` at port `64287` to get the flag?

Solución:
Obtener la bandera ejecutando el comando nc con la pagina de la solución
-Ejecutar el comando junto con el link y el puerto en una terminal de Linux y copiar la salida.
```
$ nc jupiter.challenges.picoctf.org 64287
```

-El resultado es: **picoCTF{nEtCat_Mast3ry_284be8f7}**

Notas adicionales
-Es posible ejecutar el comando en Windows, pero requiere una instalacion

Referencias
https://linux.die.net/man/1/nc