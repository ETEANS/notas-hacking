
**Reto:**
Entrar como administrador para obtener la bandera.

**Descripción:**
-Can you get the flag?
-Go to this [website](http://saturn.picoctf.net:57625/) and see what you can discover.

**Solución:**
Modificar la cookie del sitio para entrar como administrador y obtener la bandera.
-Abrir la página.
-Entrar como invitado.
-Inspeccionar la página y dirigirse a la pestaña de aplicación.
-Buscar la característica de Admin y cambiar su valor asociado a '1'.
-Vuelve a cargar la página y la bandera va a aparecer en la página.

El resultado es: **picoCTF{gr4d3_A_c00k13_65fd1e1a}**.

**Notas adicionales:**
-Es necesario un editor de cookies.

**Referencias:**
http://saturn.picoctf.net:57625/
https://chromewebstore.google.com/detail/cookie-editor/hlkenndednhfkekhgcdicdfddnkalmdm?pli=1