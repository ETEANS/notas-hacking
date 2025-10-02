
**Reto:**
-Encontrar la bandera en un paquete de capturas.

**Descripción:**
-We found this [packet capture](https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap). Recover the flag.

**Solución:**
Abrir el archivo con WireShark y buscar la bandera dentro de las secuencias filtradas.
-Descargar el archivo.
-Abrir el archivo con WireShark.
-Seguir un canal UDP.
-Buscar por las secuencias hasta encontrar la bandera.
-La bandera se encuentra en la secuencia 6.

El resultado es: **picoCTF{StaT31355_636f6e6e}**.

**Notas adicionales:**
-Para seguir un paquete, hay que hacer click derecho en el paquete y elegir 'seguir'.

**Referencias:**
https://www.wireshark.org/
https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap