
**Reto:**
-Iniciar sesión alterando el Query para obtener la bandera.

**Descripción:**
-There is a website running at `https://jupiter.challenges.picoctf.org/problem/33850/` 
  ([link](https://jupiter.challenges.picoctf.org/problem/33850/)). Do you think you can log us in? Try to see if you can login!

**Solución:**
Obtener la declaración de consulta y utilizar uno de los campos para ingresar al sistema y obtener la bandera.
-Abrir la página.
-Presiona las teclas "Ctrl+Shift+i" para abrir las herramientas de desarrollador.
-Buscar la entrada con el nombre "debug" y cambiar el valor a "1".
-Ingresar al sistema y ver la declaración SQL para ingresar.
-Regresar a la pantalla de inicio de sesión y escribir en el campo de la contraseña:
`' OR '1' = '1`
-Una vez ingresada esta contraseña, iniciar sesión.
-En la pagina va a aparecer la bandera.

El resultado es **picoCTF{s0m3_SQL_f8adf3fb}**.

**Notas adicionales:**
-La declaración `'1' = '1'` es una sentencia que siempre regresa 'true'.

**Referencias:**
https://jupiter.challenges.picoctf.org/problem/33850/
[Uso de los operadores AND, OR y NOT en SQL | LearnSQL.es](https://learnsql.es/blog/uso-de-los-operadores-and-or-y-not-en-sql/)