
Reto:
Adivinar el número correcto para obtener la bandera.

Descripción:
Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!You can download the challenge files here:
- [challenge.zip](https://artifacts.picoctf.net/c_atlas/5/challenge.zip)
`ssh -p 57408 ctf-player@atlas.picoctf.net`Using the password `1ad5be0d`. Accept the fingerprint with `yes`, and `ls` once connected to begin. Remember, in a shell, passwords are hidden!

Solución:
Ejecutar el comando shell para acceder a la instancia y realizar una busqueda binaria para encontrar el número correcto.
-Abrir la instancia con shell e ingresar la contraseña.
```
$ ssh -p 57408 ctf-player@atlas.picoctf.net
```
-Una vez dentro de la instancia, en la terminal aparece un mensaje indicando adivinar un número entre 1 y 1000, ingresar 500.
-Si el número incorrecto es ingresado, la terminal va indicar si el número es mayor o menor del numero ingresado.
-Dependiendo del resultado, ingresar un número mayor o menor utilizando busqueda binaria.
500>250>375>442>475>458>450>446>444>445
-Una ingresado el número correcto, la bandera aprecera en la terminal.

-El resultado es: **picoCTF{g00d_gu355_3af33d18}**

Notas adicionales:
-La busqueda binaria es utilizada para buscar datos en una lista de datos ordenada.

Referencias:
https://www.w3schools.com/dsa/dsa_algo_binarysearch.php