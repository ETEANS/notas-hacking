
**Reto:**
Ingresar a una página como administrador para obtener la bandera.

**Descripción:**
-The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? `https://jupiter.challenges.picoctf.org/problem/13594/` or http://jupiter.challenges.picoctf.org:13594

**Solución:**
Modificar la cookie de la sesión para recibir permisos de administrador y acceder a la bandera.
-Abrir la página.
-Inspeccionar la página y dirigirse a la pestaña de aplicación.
-Buscar la característica de Admin y cambiar su valor asociado a 'True'.
-Vuelve a cargar la página y la bandera va a aparecer en la página.

El resultado es: **picoCTF{th3_c0nsp1r4cy_l1v3s_d1c24fef}**.

**Notas adicionales:**
-En algunos casos, es necesario una extensión llamada 'cokie editor'

**Referencias:**
http://jupiter.challenges.picoctf.org:13594
https://chromewebstore.google.com/detail/cookie-editor/hlkenndednhfkekhgcdicdfddnkalmdm?pli=1