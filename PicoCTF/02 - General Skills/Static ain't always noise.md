Reto:
Desencriptar un archivo binario y obtener la bandera.

Descripción:
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/7495259e963bd5b67d0fb8b616652618/static)? This [BASH script](https://mercury.picoctf.net/static/7495259e963bd5b67d0fb8b616652618/ltdis.sh) might help!

Solución:
Ejecutar el script de BASH para desencriptar el archivo y extraer la bandera de este.
-Ejecutar el archivo 'ltdis.sh' referenciando al archivo 'static'.
```
$ bash .\ltdis.sh .\static
```
-Este comando crea un archivo desencriptado, en el cuál se va a buscar la bandera utilizando el comando 'grep'.
```
$ grep -n 'pico' .\static.ltdis.strings.txt
```

-El resultado es: **picoCTF{d15a5m_t34s3r_f6c48608}**.

Notas adicionales:
-Al momento de consultar el archivo bash, se puede ver las instrucciones y comentarios indicando las peticiones del script.

Referencias:
https://www.hostinger.com/tutorials/how-to-run-sh-file-in-linux?utm_campaign=Generic-Tutorials-DSA|NT:Se|LO:MX-EN&utm_medium=ppc&gad_source=1&gad_campaignid=20980195875&gbraid=0AAAAADMy-hYhk4s6OE3GLtMaD7ehYNNGd&gclid=Cj0KCQjw8eTFBhCXARIsAIkiuOxQkh2l7NuE5Xi5RFFzd1NJm1iM9dqfK_itiK0fYe8bmZXneIyNuCEaAm_WEALw_wcB