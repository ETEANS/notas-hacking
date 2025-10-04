
**Reto:**
-Ejecutar un programa con la encriptación adecuada para obtener la bandera.

**Descripción:**
-Python scripts are invoked kind of like programs in the Terminal... Can you run [this Python script](https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/ende.py) using [this password](https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/pw.txt) to get [the flag](https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/flag.txt.en)?

**Solución:**
Ejecutar el programa con el modo de desencriptar y junto el nombre del archivo a desencriptar, y dentro del programa ingresar la contraseña.
-Descargar los archivos y tenerlos en el mismo directorio.
-Ejecutar el programa con el siguiente comando:
```
$ python ende.py -d flag.txt.en
```
-Dentro del programa, ingresar la contraseña que se encuentra en el archivo de texto `pw.txt`.
-Si la contraseña es correcta, el programa va a mostrar la bandera desencriptada.

El resultado es: **picoCTF{4p0110_1n_7h3_h0us3_67c6cc96}**.

**Notas adicionales:**
-Es necesario tener el paquete de `cryptography` para ejecutar el programa, si no se tiene, es necesario instalarlo con el siguiente comando:
```
$ pip install cryptography
```

**Referencias:**
https://www-geeksforgeeks-org.translate.goog/python/command-line-arguments-in-python/?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=tc