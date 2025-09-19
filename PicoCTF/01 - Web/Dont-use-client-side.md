
**Reto:**
-Descubrir la bandera de un portal seguro.

**Descripción:**
-Can you break into this super secure portal? `https://jupiter.challenges.picoctf.org/problem/17682/` or http://jupiter.challenges.picoctf.org:17682

**Solución:**
Utilizar las herramientas para desarrollador para obtener la contraseña o algo que se asemeja a la bandera.
-Abrir la página.
-Presiona las teclas "Ctrl+Shift+i" para abrir las herramientas de desarrollador.
-Abrir el script que verifica la contraseña.
```
function verify() {
    checkpass = document.getElementById("pass").value;
    split = 4;
    if (checkpass.substring(0, split) == 'pico') {
      if (checkpass.substring(split*6, split*7) == '706c') {
        if (checkpass.substring(split, split*2) == 'CTF{') {
         if (checkpass.substring(split*4, split*5) == 'ts_p') {
          if (checkpass.substring(split*3, split*4) == 'lien') {
            if (checkpass.substring(split*5, split*6) == 'lz_b') {
              if (checkpass.substring(split*2, split*3) == 'no_c') {
                if (checkpass.substring(split*7, split*8) == '5}') {
                  alert("Password Verified")
                  }
                }
              }
      
            }
          }
        }
      }
    }
    else {
      alert("Incorrect password");
    }
    
  }
```
-A partir de la función, construir la contraseña.
-Una vez construida la contraseña, esta claramente es la bandera.

El resultado es: **picoCTF{no_clients_plz_b706c5}**

**Notas adicionales:**
-Al ser una función escrita en JavaScript, es posible armar la contraseña copiando los verificadores 
  y pegándolos en una función que regresa la bandera.

**Referencias:**
https://developer.chrome.com/docs/devtools?hl=es-419
http://jupiter.challenges.picoctf.org:17682