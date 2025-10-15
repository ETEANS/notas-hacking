
**Reto:**
-Obtener la bandera de una captura de paquete usando una contraseña.

**Descripción:**
-We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.

**Solución:**
Utilizar Wireshark para abrir el paquete de capturas, seguir el stream de TLS, desencriptar los canales con con la llave y obtener la bandera.
-Descargar el archivo.
-Abrir el archivo con WireShark.
-Seguir un canal TLS.
-Entrar a la pestaña 'edición' y la opción de preferencias.
-Buscar el protocolo TLS.
-Editar la lista de llaves y agregar el archivo key.
-Aceptar y salir de la ventana.
-Cambiar la secuencia a 0.
-Buscar la bandera dentro de la secuencia.

El resultado es: **picoCTF{nongshim.shrimp.crackers}**.

**Notas adicionales:**
-Al editar la lista de llaves, solo es necesario hacer click en la pestaña de key file y escoger el archivo KEY.

**Referencias:**
https://blog.didierstevens.com/2020/12/14/decrypting-tls-streams-with-wireshark-part-1/