
**Reto:**
-Obtener la bandera de una captura de paquete usando una contraseña.

**Descripción:**
-We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.

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

El resultado es: **picoCTF{honey.roasted.peanuts}**.

**Notas adicionales:**
-Existe una bandera engañosa, la verdadera bandera se encuentra debajo de las especificaciones de la secuencia.

**Referencias:**
https://blog.didierstevens.com/2020/12/14/decrypting-tls-streams-with-wireshark-part-1/
