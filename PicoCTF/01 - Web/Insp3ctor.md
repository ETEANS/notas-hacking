
**Reto:**
-Encontrar la bandera en el código de la pagina.

**Descripción:**
-Kishor Balan tipped us off that the following code may need inspection: `https://jupiter.challenges.picoctf.org/problem/9670/` ([link](https://jupiter.challenges.picoctf.org/problem/9670/)) or http://jupiter.challenges.picoctf.org:9670

**Solución:**
Utilizar las herramientas de desarrollador para obtener el código de la pagina y obtener la bandera dividida.
-Abrir la página.
-Presiona las teclas "Ctrl+Shift+i" para abrir las herramientas de desarrollador.
-En el código de HTML, buscar un comentario que indica la primera parte de la bandera.
```
<!-- Html is neat. Anyways have 1/3 of the flag: picoCTF{tru3_d3 -->
```
-Moverse a la pestaña de recursos para ver los archivos.
-En la pestaña de recursos, buscar en el archivo CSS la segunda parte de la bandera.
```
/* 
You need CSS to make pretty pages. Here's part 2/3 of the flag: t3ct1ve_0r_ju5t 
*/
```
-En la pestaña de recursos, buscar en el archivo JS (código de JavaScript) la tercera parte de la bandera.
```
/* Javascript sure is neat. Anyways part 3/3 of the flag: _lucky?2e7b23e3} */
```
-Una vez juntadas las banderas, se tiene la bandera completa.

El resultado es: **picoCTF{tru3_d3t3ct1ve_0r_ju5t_lucky?2e7b23e3}**

**Notas adicionales:**
-Los comentarios en HTML se hacen con la notación: <!-- comentario -->

**Referencias:**
https://developer.chrome.com/docs/devtools?hl=es-419
https://jupiter.challenges.picoctf.org/problem/9670/