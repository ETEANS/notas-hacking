
Reto:
-resolver los problemas de números binarios.

Descripción:
-How well can you perfom basic binary operations?
 Start searching for the flag here 
 `nc titan.picoctf.net 63996`

Solución:
Ingresar a la conexión y resolver los problemas con un programa.
-Conectarse a la conexión con el comando 'nc',
```
$ nc titan.picoctf.net 63996
```
-Una vez inicia la conexión, resolver los 6 problemas utilizando un programa.
```
a = (0b00110100 * 0b10100100)
b = (0b10100100 >> 1)
c = (0b00110100 | 0b10100100)
d = (0b00110100 + 0b10100100)
e = (0b00110100 << 1)
f = (0b00110100 & 0b10100100)
print(bin(a))
print(bin(b))
print(bin(c))
print(bin(d))
print(bin(e))
print(bin(f))
print(hex(f))
```
-Cuando se resuelven los 6 problemas y el último resultado en hexadecimal, la bandera aparecera en la terminal.

Es resultado es: **picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_1367e2c6}**.

Notas adicionales:
-la función `bin` convierte cualquier número a binario.

Referencias:
https://www.geeksforgeeks.org/dsa/binary-operators-in-programming/