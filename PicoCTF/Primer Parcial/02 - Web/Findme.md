
**Reto:**
-Encontrar la bandera dentro de la redirección.

**Descripción:**
Help us test the form by submiting the username as `test` and password as `test!`The website running [here](http://saturn.picoctf.net:57302/).

**Solución:**
Utilizar BurpSuite para interceptar las peticiones de redirección y obtener la bandera dentro de las peticiones.
-Abrir la pagina con BurpSuite.
-Encender el proxy de BurpSuite.
-Iniciar sesión en la pagina con `test` y `test!` en usuario y contraseña respectivamente.
-Enviar la petición desde el proxy.
-Copiar el `id` de la petición y continua
-Copiar el `id` de la segunda petición.
-Desencriptar ambos `id`s en base 64.
-Los dos ids desencriptados juntos son la bandera.

El resultado es: **picoCTF{proxies_all_the_way_a0fe074f}**.

**Notas adicionales:**
-Se requiere tener BurpSuite para hacer el proceso.

**Referencias:**
https://www.site24x7.com/es/tools/comprobador-de-redireccion.html