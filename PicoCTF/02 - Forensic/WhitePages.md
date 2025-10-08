
**Reto:**
-Encontrar el significado de un archivo aparentemente en blanco para encontrar la bandera.

**Descripción:**
-I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://jupiter.challenges.picoctf.org/static/fa4a277cfa846e07a5981d8a19288a2e/whitepages.txt) is all blank!

**Solución:**
Utilizar un programa para extraer la información y manipularla hasta obtener la bandera.
-Descargar el archivo.
-Crear el siguiente programa:
```
from pwn import *

file = open("whitepages.txt", "rb")
data = bytearray(file.read())
data = data.replace(b'\xe2\x80\x83',b'0')
data = data.replace(b'\x20',b'1')
data = data.decode('ascii')
data = unbits(data)
print(data)
```
-Guardar el programa en el mismo directorio donde se encuentra el archivo descargado.
-Ejecutar el programa.
```
$ python exp.py
```
-El programa va a mostrar un texto que contiene la bandera.

El resultado es: **picoCTF{not_all_spaces_are_created_equal_3e2423081df9adab2a9d96afda4cfad6}**

**Notas adicionales:**
-Es necesario tener la librería de `pwntools` para ejecutar el programa, se puede instalar con el siguiente comando:
```
$ pip install pwntools
```
**Referencias:**
https://docs.pwntools.com/en/stable/