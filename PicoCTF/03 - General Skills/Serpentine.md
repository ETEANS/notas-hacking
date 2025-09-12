
Reto:
-Modificar un programa para encontrar la bandera.

Descripción:
-Find the flag in the Python script![Download Python script](https://artifacts.picoctf.net/c/37/serpentine.py)

Solución:
Abrir el código con un editor de texto, asignar la función al comando, guardar y ejecutar el programa.
-Abrir el programa con un editor de texto
-Colocar la función para desencriptar la bandera dentro de la acción que supuestamente muestra la bandera.
-Guarda el programa y ejecuta el programa.
```
$ python serpentine.py
```
-Una vez ejecutado el programa correctamente, selecciona la opción correcta y la bandera se mostrara en pantalla.

El resultado es: **picoCTF{7h3_r04d_l355_7r4v3l3d_8e47d128}**

Notas adicionales:
-Al ejecutar antes de modificarlo, la opción para mostrar la bandera no realiza la acción.

Referencias:
https://www.arsys.es/blog/comandos-nano