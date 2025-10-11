
**Reto:**
-Conectarse a una base de datos y extraer la bandera de las tablas.

**Descripción:**
-Connect to this PostgreSQL server and find the flag!`psql -h saturn.picoctf.net -p 54747 -U postgres pico`Password is `postgres`.

**Solución:**
Entrar al sistema, consultar las bases de datos accesibles y hacer una consulta a los datos de la tabla.
-Ingresar a la base de datos con el comando e ingresar la contraseña.
```
$ psql -h saturn.picoctf.net -p 54747 -U postgres pico
```
-Ingresar el comando `\d+` para mostrar las relaciones.
-Mostrar las tablas del esquema y sus columnas encontrada con el siguiente comando:
```
$ \d public.*
```
-Utilizar el siguiente comando para hacer una consulta a los datos de la tabla FLAGS.
```
$ public
$ SELECT * FROM FLAGS;
```

El resultado es: **picoCTF{L3arN_S0m3_5qL_t0d4Y_21c94904}**.

**Notas adicionales:**
-Es posible filtrar el resultado deseado usando la siguiente cláusula.
```
$ SELECT * FROM FLAGS WHERE SUBSTR(ADDRESS,4) == 'pico';
```

**Referencias:**
https://www.postgresql.org/

