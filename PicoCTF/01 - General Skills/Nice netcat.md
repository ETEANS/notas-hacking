Reto:
Obtener y traducir la bandera

Descripción:
-There is a nice program that you can talk to by using this command in a shell: 
 `$ nc  mercury.picoctf.net 22342`, but it doesn't speak English...

Solución:
Obtener los números ejecutando el comando y convertir los números en ASCII.
-Ejecutar el comando nc en la terminal
```
$ nc  mercury.picoctf.net 22342
```
-Copiar los números obtenidos y convertirlos con ASCII usando Python.
```
A = [112,105,99,111,67,84,70,123,103,48,48,100,95,107,49,116,116,121,33,95,
     110,49,99,51,95,107,49,116,116,121,33,95,53,102,98,53,101,53,49,100,125,10]
for i in range(0,len(A)):
	print(chr(A[i]), end="")
```

-El resultado es: **picoCTF{g00d_k1tty!_n1c3_k1tty!_5fb5e51d}**

Notas adicionales:
-Los números aparecen en cada línea cuando se ejecuta el comando.

Referencias:
https://www.w3schools.com/python/python_lists.asp