
**Reto:**
-Encontrar la cookie y obtener la bandera con esta.

**Descripción:**
-Cookie Monster has hidden his top-secret cookie recipe somewhere on his website. As an aspiring cookie detective, your mission is to uncover this delectable secret. Can you outsmart Cookie Monster and find the hidden recipe?
-You can access the Cookie Monster [here](http://verbal-sleep.picoctf.net:62486/) and good luck

**Solución:**
Iniciar sesión en la pagina, copiar la cookie y desencriptarla para obtener la bandera.
-Abrir la página.
-Iniciar sesión.
-Presiona las teclas "Ctrl+Shift+i" para abrir las herramientas de desarrollador.
-Buscar la cookie en Network y copiar su valor.
-Desencriptar la cookie a base 64.
-La cookie desencriptada es la bandera.

El resultado es: **picoCTF{c00k1e_m0nster_l0ves_c00kies_78B4C390}**.

**Notas adicionales:**
-La cookie puede ser encontrada en los métodos de petición o en la pestaña de aplicación.

**Referencias:**
http://verbal-sleep.picoctf.net:62486/
https://www.base64decode.org/
