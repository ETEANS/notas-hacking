
**Reto:**
-Ingresar como administrador para obtener la bandera.

**Descripción:**
-Can you get the flag?Go to this [website](http://saturn.picoctf.net:57269/) and see what you can discover.

**Solución:**
Buscar el nombre de usuario y contraseña en los archivos de la pagina e ingresar con estos datos para obtener la bandera.
-Abrir la página.
-Iniciar sesión con datos genéricos.
-Presiona las teclas "Ctrl+Shift+i" para abrir las herramientas de desarrollador.
-Ver el archivo 'secure.js' y copiar el nombre de usuario y contraseña del administrador.
-Regresar al inicio de sesión e ingresar los datos obtenidos.
-Una vez ingresado como administrador, la bandera aparecerá en la página.

El resultado es: **picoCTF{j5_15_7r4n5p4r3n7_a8788e61}**.

**Notas adicionales:**
-El código html de la página tiene el método usado para verificar la contraseña y usuario.

**Referencias:**
http://saturn.picoctf.net:57269/