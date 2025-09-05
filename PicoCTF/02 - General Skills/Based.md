
Reto:
Concetarse a una red y resolver problemas de desencriptar cadenas de números con tiempo limite.

Descripción:
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with `nc jupiter.challenges.picoctf.org 29956`.

Solución:
Conectarse a una red desde la terminal y resolver los problemas utilizando programas para desencriptar los números de forma rápida.
-Crear múltiples programas que desencriptan cadenas de números en diferentes bases.
  a) Programa que desencripta números binarios.
```
binaryChain = "01110011 01101100 01110101"  
binaryStrings = binaryChain.split()  
for i in range (0,len(binaryStrings)):  
    a = int(binaryStrings[i],2)  
    print(chr(a), end="")
```
  b) Programa que desencripta números en base 8.
```
intChain = "148 152 129"  
intStrings = intChain.split()  
for i in range (0,len(intStrings)):  
    a = int(intStrings[i],8)  
    print(chr(a), end="")
```
  c) Programa que desencripta números en hexadecimal.
```
intChain = "73 6f 63 74"  
intStrings = intChain.split()  
for i in range (0,len(intStrings)):  
    a = int(intStrings[i],16)  
    print(chr(a), end="")
```
-Iniciar la conexión usando el comando 'nc'.
```
$ nc jupiter.challenges.picoctf.org 29956
```
-Responder las preguntas utilizando los programas creados, cada pregunta dura 45 segundos (los números son diferentes cada vez que se inicia la conexión).
-Una vez resueltos los problemas, la terminal otorga la bandera.

El resultado es: **picoCTF{learning_about_converting_values_b375bb16}**

Notas adicionales:
-La función 'split' separa una cadena a partir de una serie de caracteres, si la función esta vacía, va a separar a partir de los espacios
-Al convertir una cadena a un entero, el segundo argumento indica la base de la cadena, si no lo tiene, utiliza la base 10.

Referencias:
https://www.geeksforgeeks.org/python/python-binary-list-to-integer/
https://www.geeksforgeeks.org/python/convert-string-to-integer-in-python/
