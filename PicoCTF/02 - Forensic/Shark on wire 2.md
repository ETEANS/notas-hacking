
**Reto:**
-Encontrar la bandera en un paquete de capturas.

**Descripción:**
-We found this [packet capture](https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap). Recover the flag that was pilfered from the network.

**Solución:**
Abrir el archivo con WireShark y buscar la bandera dentro de los puertos filtrados.
-Descargar el archivo.
-Abrir el archivo con WireShark.
-Filtar los paquetes con `udp.dstport == 22`.
-Copia los últimos 3 dígitos de los puertos filtrados.  
-Pega los puestos en un programa de Python:
```
print(chr(0) + chr(112) + chr(105) + chr(99) + chr(111) + chr(67) + chr(84) + chr(70) + chr(123) + chr(112) +  chr(49) + chr(76) + chr(76) + chr(102) + chr(51) + chr(114) + chr(51) + chr(100) + chr(95) + chr(100) + chr(97) + chr(116) + chr(97) + chr(95) + chr(118) + chr(49) + chr(97) + chr(95) + chr(115) + chr(116) + chr(51) + chr(103) + chr(48) + chr(125) + chr(0))
```
-Guarda y ejecuta el programa.
-Una vez ejecutado el programa, ña bandera aparece en la terminal.

El resultado es: **picoCTF{p1LLf3r3d_data_v1a_st3g0}**.

**Notas adicionales:**
-Es posible filtrar los puestos de forma directa usando Scapy en Python 2,

**Referencias:**
https://www.wireshark.org/
https://scapy.net/