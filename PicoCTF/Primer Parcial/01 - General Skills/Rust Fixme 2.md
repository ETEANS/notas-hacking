
**Reto:**
-Arreglar el código de Rust para obtener la bandera.

**Descripción:**
-The Rust saga continues? I ask you, can I borrow that, pleeeeeaaaasseeeee?
-Download the Rust code [here](https://challenge-files.picoctf.net/c_verbal_sleep/babfbee79718a6363826ba86300173ffde6d81577e9dd07d4130c53a7eecf6c3/fixme2.tar.gz).

**Solución:**
Ingresar al código para hacer modificaciones a las variables y funciones, una vez arreglado, ejecutar el programa y obtener la bandera.
-Descargar el archivo y descomprimirlo.
-Buscar el archivo `main.rs` dentro de la carpeta descomprimida.
-Editar el archivo con un editor de texto, agregando 'mut' a las variables mutables.
-Una vez corregido el archivo, en el directorio anterior, escribir el siguiente comando:
```
$ cargo build
```
-Cuando el programa haya sido compilado, ejecutarlo con el siguiente comando:
```
$ cargo run
```

El resultado es: **picoCTF{4r3_y0u_h4v1n5_fun_y31?}**.

**Notas adicionales:**
-Para marcar a una variable en Rust como mutable, se coloca la palabar 'mut' despues de declarar la variable.

**Referencias:**
https://rust-lang.org/tools/install/
https://doc.rust-lang.org/book/ch01-03-hello-cargo.html