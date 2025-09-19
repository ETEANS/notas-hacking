
**Reto:**
Encontrar la dirección que contiene la bandera.

**Descripción:**
-Can you find the robots? `https://jupiter.challenges.picoctf.org/problem/60915/`or http://jupiter.challenges.picoctf.org:60915

**Solución:**
Buscar en el archivo "robots.txt" la dirección que contiene la bandera.
-Abrir la página.
-Escribir al final de la dirección de la página el texto "robots.txt".
-Una vez dentro del archivo, copiar el texto que termina en ".html".
-Borrar "robots.txt" de la dirección y pegar el texto copiado.
-Una vez ingresada la nueva dirección, la bandera aparecerá en la página.

El resultado es: **picoCTF{ca1cu1at1ng_Mach1n3s_8028f}**.

**Notas adicionales:**
-Un archivo "robots.txt" indica a los rastreadores los URLs accesibles de la pagina.

**Referencias:**
http://jupiter.challenges.picoctf.org:60915
https://developers.google.com/search/docs/crawling-indexing/robots/intro?hl=es#what-is-a-robots.txt-file-used-for
https://developers.google.com/search/docs/crawling-indexing/robots/create-robots-txt?hl=es