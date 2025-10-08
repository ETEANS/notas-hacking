
**Reto:**
-Arreglar un archivo corrupto para obtener la bandera.

**Descripción:**
.We found this [file](https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery). Recover the flag.

**Solución:**
Utilizar un editor en hexadecimal para editar el archivo hasta arreglar sus problemas y ver la bandera en la imagen.
-Descargar el archivo.
-Abrir el archivo con un editor de texto en hexadecimal.
-Utilizando documentación de un archivo PNG, cambiar datos del archivo hasta tener un archivo funcional.
-Subir la imagen a un inspector de chunks PNG para evaluar los problemas.
-Corregir los chunks dañados a partir de la información ofrecida por el inspector.
-Una vez corregida la imagen, exportar el archivo.
-Al abrir la imagen arreglada, la bandera aparece en la imagen.

El resultado es: **picoCTF{c0rrupt10n_1847995}**.

**Notas adicionales:**
-Los chunks de una imagen PNG suelen ser de 4 bytes.

**Referencias:**
https://medium.com/@0xwan/png-structure-for-beginner-8363ce2a9f73
https://www.nayuki.io/page/png-file-chunk-inspector
