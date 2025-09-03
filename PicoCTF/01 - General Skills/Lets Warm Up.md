Reto: 
-Convertir un número hexadecimal a un caracter en ASCII.

Descripción:
-If I told you a word started with 0x70 in hexadecimal, what would it start with in ASCII?

Solución:
Convertir el número hexadecimal a entero y asociarlo con su caracter ASCII
-Convertir un número entero representado con hex y convertirlo en un caracter.
```
int hex = 0x70;
System.out.println((char)hex);
```
-Utilizar un convertidor web para decriptar el número y buscar su valor ASCII.

-El resultado fue: picoCTF{p}

Notas adicionales:
-Puede funcionar si se representa el número de forma decimal

Referencias
https://www.geeksforgeeks.org/java/java-int-to-char-conversion/