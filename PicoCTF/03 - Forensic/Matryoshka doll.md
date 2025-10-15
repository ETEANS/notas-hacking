
**Reto:**
-Encontrar los archivos ocultos dentro de una imagen para obtener la bandera.

**Descripción:**
-Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/1b70cffdd2f05427fff97d13c496963f/dolls.jpg)

**Solución:**
Ejecutar el comando 'binwalk' con la imagen para obtener sus archivos ocultos, y realizar el mismo proceso hasta encontrar la bandera.
-Descargar la imagen.
-Usar el comando 'binwalk' con la imagen y extraer la carpeta oculta.
```
$ binwalk -e 1_c.jpg
```
-Entrar a la carpeta descubierta.
-Realizar el mismo proceso hasta encontrar la bandera.
-Una vez encontrado el archivo 'flag.txt', abrirlo.
-Dentro del archivo se encuentra la bandera.

El resultado es: **picoCTF{bf6acf878dcbd752f4721e41b1b1b66b} **.

**Notas adicionales:**
-El comando binwalk busca imágenes binarias y código encriptado dentro de archivos.

**Referencias:**
https://www.kali.org/tools/binwalk/