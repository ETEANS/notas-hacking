
**Reto:**
-Encontrar la bandera en la página y desencriptarla. 

**Descripción:**
-Do you know how to use the web inspector?Start searching [here](http://titan.picoctf.net:60108/) to find the flag

**Solución:**
Utilizar las herramientas de desarrollador para buscar una cadena encriptada y desencriptarla para obtener la bandera.
-Abrir la página.
-Hacer click en la sección de 'about'.
-Presiona las teclas "Ctrl+Shift+i" para abrir las herramientas de desarrollador.
-Buscar en el código de la pagina hasta encontrar la sección con la clase 'about' y copiar la propiedad 'notify_true'.
-Copiar la propiedad y desencriptarla en base64.
-La propiedad desencriptada es la bandera.

El resultado es: **picoCTF{web_succ3ssfully_d3c0ded_02cdcb59}**.

**Notas adicionales:**
-Un valor encriptado en base64 es más largo que su cádena desencriptada.

**Referencias:**
http://titan.picoctf.net:60108/about.html
https://www.base64decode.org/
