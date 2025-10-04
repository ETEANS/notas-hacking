
**Reto:**
-Resolver los problemas de las conexión para obtener la bandera.

**Descripción:**
-Play this short game to get familiar with terminal applications and some of the most important rules in scope for picoCTF.
-Connect to the program with netcat:`$ nc verbal-sleep.picoctf.net 61760`

**Solución:**
Ingresar a la conexión y resolver las situaciones para obtener la bandera.
-Entrar a la conexión con el comando nc.
-Leer el texto mostrado y seleccionar una opción.
-En caso de tomar una decisión incorrecta, se puede volver a intentar la selección después.
-Una vez resueltas las consignas, la bandera aparecera en pantalla.

El resultado es: **picoCTF{m1113n1um_3d1710n_3b6c6fab}**.

**Notas adicionales:**
-La secuencia es cargada desde una instancia, así que es necesario responder las cuestiones antes de que termine el tiempo.

**Referencias:**
https://www.ochobitshacenunbyte.com/2021/11/04/uso-del-comando-ncat-nc-en-linux-con-ejemplos/