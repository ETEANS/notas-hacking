
**Reto:**
-Descifrar el token correcto para obtener la bandera.

**Descripción:**
-Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/58210/` or http://jupiter.challenges.picoctf.org:58210

**Solución:**
Cambiar el atributo de jwt de la 'cookie' para ingresar como admin.
-Abrir la página.
-Presiona las teclas "Ctrl+Shift+i" para abrir las herramientas de desarrollador.
-Copiar el valor de la cookie.
-Descargar los archivos que muestra el repositorio de la pagina.
-Coloca la cookie en un archivo.
-Lee el archivo con `john` para obtener la llave.
```
$ john ~/hash -w=/usr/share/wordlists/rockyou.txt
```
-Coloca la cookie en un desencriptador de JWT y la llave.
-Una vez desencriptada el JWT, cambiar el nombre del usuario a "admin" y codificar la cookie.
-Cambiar la cookie vieja por la nueva y volver a cargar la página. 
-Una vez cargada la página, la llave aparecerá en el bloque de texto.

El resultado es: **picoCTF{jawt_was_just_what_you_thought_44c752f5}**.

**Notas adicionales:**
-John es utilizado para desencriptar contraseñas o archivos encriptados.

**Referencias:**
http://jupiter.challenges.picoctf.org:58210
https://github.com/openwall/john?tab=readme-ov-file
https://www.jwt.io/