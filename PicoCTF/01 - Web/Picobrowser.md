
**Reto:**
-Obtener la bandera de una página sin tener que utilizar un buscador especifico.

**Descripción:**
-This website can be rendered only by **picobrowser**, go and catch the flag! `https://jupiter.challenges.picoctf.org/problem/26704/` or http://jupiter.challenges.picoctf.org:26704

**Solución:**
Cambiar el agente de usuario al nombre del agente pedido para cumplir las condiciones y obtener la bandera.
-Abrir la página.
-Presiona las teclas "Ctrl+Shift+i" para abrir las herramientas de desarrollador.
-Acceder a la pestaña de Condiciones de Red (Network conditions).
-En esta pestaña, desactivar el uso del navegador por determinado.
-En la sección de "user agent", cambiar el nombre del buscador a "picobrowser", dejando el esquema en "Custom...".
-Finalmente hacer click en la página en el botón "flag" y la bandera aparecera en la terminal.

El resultado es: **picoCTF{p1c0_s3cr3t_ag3nt_e9b160d0}**.

**Notas adicionales:**
-La pestaña de "Network conditions" se encuentra en los tres puntos de la herramientas, dentro de la sección "more tools".

**Referencias:**
https://developer.chrome.com/docs/devtools/device-mode/override-user-agent?hl=es-419
http://jupiter.challenges.picoctf.org:26704
