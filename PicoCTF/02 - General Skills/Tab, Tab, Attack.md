Reto:
Recorrer directorios hasta encontrar el archivo y desencriptarlo.

Descripción:
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/9689f2b453ad5daeb73ca7534e4d1521/Addadshashanammu.zip)

Solución:
Recorrer los directorios usando el comando 'cd' para entrar a los directorios, una vez encontrado el archivo, desencriptarlo y obtener la bandera.
-Descomprimir la carpeta con el comando 'unzip'.
```
unzip .\Addadshashanammu.zip
```
-Recorrer los directorios hasta llegar al archivo.
```
$ cd .\Addadshashanammu\
$ cd .\Almurbalarammi\
$ cd .\Ashalmimilkala\
$ cd .\Assurnabitashpi\
$ cd .\Maelkashishi\
$ cd .\Onnissiralis\
$ cd .\Ularradallaku\
```
-Una vez encontrado el archivo, es necesario obtener las cadenas con el comando 'strings' y consultando la bandera con el comando 'grep'
```
$ strings .\fang-of-haynekhtnamet | grep 'pico'
```

El resultado es: **picoCTF{l3v3l_up!_t4k3_4_r35t!_2bcfb2ab}**

Notas adicionales:
-El uso de la tecla 'tab' permite  recorrer los archivos y/o subdirectorios existentes dentro de un directorio.
-Es posible concatenar comandos en la terminal con el símbolo '|'.

Referencias:
https://askubuntu.com/questions/334941/how-to-combine-multiple-commands-in-terminal