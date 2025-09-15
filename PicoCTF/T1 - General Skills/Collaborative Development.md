
Reto:
-Cambiar de ramas en git para obtener la bandera completa.

Descripción:
-My team has been working very hard on new features for our flag printing program! I wonder 
  how they'll work together?You can download the challenge files here:

Solución:
Cambiar las ramas del repositorio para acceder a todos los archivos que contienen la bandera.
-Accede a la carpeta que contiene la carpeta '.git'.
-Cambia la rama con el prefijo 'switch'.
```
$ git switch feature/part-1
```
-Accede la archivo 'flag.py' y busca la parte de la bandera dividida.
-Accede a las otras ramas para revisar el mismo archivo hasta obtener la bandera completa.

El resultado es: **picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_6c06cec1}**.

Notas adicionales:
-Para revisar las ramas disponibles de un repositorio, utiliza el siguiente comando.
```
$git branch -a
```

Referencias:
https://git-scm.com/docs/git-switch