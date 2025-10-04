
**Reto:**
-Obtener la bandera manipulando la declaración SQL. 

**Descripción:**
-Can you login to this website?Try to login [here](http://saturn.picoctf.net:57444/).

**Solución:**
Ingresar un texto que regresa un valor verdadero en una consulta de SQL y buscar la bandera dentro del sitio.
-Abrir la página.
-Ingresar en los campos de usuario y contraseña el siguiente texto: `' OR 1=1 --'`.
-Presiona las teclas "Ctrl+Shift+i" para abrir las herramientas de desarrollador.
-La bandera se encuentra en una etiqueta en el html de la pagina.

El resultado es: **picoCTF{L00k5_l1k3_y0u_solv3d_it_d3c660ac}**.

**Notas adicionales:**
-Si se ingresa a la página con los datos erroneos, es posible ver la consulta realizada.

**Referencias:**
http://saturn.picoctf.net:57444/
https://pushmetrics.io/blog/why-use-where-1-1-in-sql-queries-exploring-the-surprising-benefits-of-a-seemingly-redundant-clause/