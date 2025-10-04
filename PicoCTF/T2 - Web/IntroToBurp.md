
**Reto:**
-Modificar el request para obtener la bandera.

**Descripción:**
-Try [here](http://titan.picoctf.net:52272/) to find the flag

**Solución:**
Utilizar Burp Suite para modificar el request y pasar el OTP para obtener la bandera.
-Abrir la página con Burp Suite.
-Registrarse en la página.
-Activar el proxy de Burp Suite.
-Ingresar un OTP en la entrada.
-Cambiar el atributo de OTP en el request a 000000.
-Cuando se ingresa al sitio, la bandera aparece en pantalla.

El resultado es: **picoCTF{#0TP_Bypvss_SuCc3$S_6bffad21}**.

**Notas adicionales:**
-Cuando se captura un request en proxy, se hacen las modificaciones al request y liberar las petición de forma manual. 

**Referencias:**
http://titan.picoctf.net:59587/
https://portswigger.net/burp