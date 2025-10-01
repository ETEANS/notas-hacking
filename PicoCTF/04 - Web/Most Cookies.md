
**Reto:**
-Desencriptar y encriptar una flask cookie para obtener la bandera.

**Descripción:**
-Alright, enough of using my own encryption. Flask session cookies should be plenty secure! [server.py](https://mercury.picoctf.net/static/c135543530f7dc24c3a6ecaeb44a81b8/server.py) [http://mercury.picoctf.net:65344/](http://mercury.picoctf.net:65344/)

**Solución:**
Desencriptar la cookie y obtener la llave secreta para crear la cookie necesaria para ingresar y obtener la bandera.
-Revisar el código de "server.py".
-Copiar la lista de nombres de cookies y pegarlas en un archivo de texto.
-Abrir la página.
-Ingresar la cookie que indica el sitio.
-Presiona las teclas "Ctrl+Shift+i" para abrir las herramientas de desarrollador.
-Copia la cookie asosiada con tu sesión.
-Desencripta la sesión usando un entorno virtual y el comando `flask-unsigned` con el archivo de cookies.
```
$ flask-unsign --unsign --cookie "eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.aNyMfg.UCSdORCKYOI8WJSmZvV74rt6Qc4" --wordlist cookies.txt
```
-Una vez desencriptada la cookie, crear una nueva cookie con la llave secreta.
```
$ flask-unsign --sign --cookie "{'very_auth':'admin'}" --secret "fortune"
```
-Cuando este comando se ejecuta, aparece la cookie encriptada en la terminal.
-Copiar la cookie y cambiar la cookie de la pagina por la nueva.
-Recargar la página y la bandera aparecerá en la página.

El resultado es: **picoCTF{pwn_4ll_th3_cook1E5_25bdb6f6}**.

**Notas adicionales:**
-Es necesario instalar el comando 'flask-unsign' es necesario ejecutar el siguiente comando:
```
python3 -m pip install flask-unsign
```

**Referencias:**
https://www.geeksforgeeks.org/python/flask-cookies/
[http://mercury.picoctf.net:65344/](http://mercury.picoctf.net:65344/)
https://gist.github.com/aescalana/7e0bc39b95baa334074707f73bc64bfe