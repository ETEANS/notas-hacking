
**Reto:**
-Utilizar un defecto dentro del programa para generar un bug y obtener la bandera

**Descripción:**
-There's a flag shop selling stuff, can you buy a flag? [Source](https://jupiter.challenges.picoctf.org/static/dd28f0987f28c894f35d5d48564c3402/store.c). Connect with `nc jupiter.challenges.picoctf.org 44566`.

**Solución:**
Ingresar un número lo suficientemente alto para desbordar el resultado de la operación y obtener los fondos necesarios para obtener la bandera dentro del programa.
-Entrar a la instancia.
```
$ nc jupiter.challenges.picoctf.org 44566
```
-Seleccionar la opción para comprar banderas.
-Seleccionar la opción de bandera falsa.
-Ingresar la cantidad de 2386093,
-Realizar el proceso tres veces hasta tener una cantidad mayor de 100000.
-Seleccionar la opción para comprar banderas.
-Seleccionar la opción de `1337`.
-Ingresar la cantidad de 1.
-La bandera será revelada al usuario

El resultado es: **picoCTF{m0n3y_bag5_68d16363}**.

**Notas adicionales:**
-Un `int` en C utiliza 4 bytes o 32 bits, lo que significa que el valor máximo es 2147483647 (uno de los bits es utilizado para el signo negativo).
-El número de 2386093 es utilizado debido a que este número multiplicado por 900 es suficiente para desbordar un  `int`.

**Referencias:**
https://en.wikipedia.org/wiki/Integer_overflow