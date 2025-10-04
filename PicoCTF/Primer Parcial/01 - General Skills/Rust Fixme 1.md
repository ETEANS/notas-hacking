
**Reto:**
-Arreglar el código de Rust para obtener la bandera.

**Descripción:**
-Have you heard of Rust? Fix the syntax errors in this Rust file to print the flag!Download the Rust code [here](https://challenge-files.picoctf.net/c_verbal_sleep/3f0e13f541928f420d9c8c96b06d4dbf7b2fa18b15adbd457108e8c80a1f5883/fixme1.tar.gz).

**Solución:**
Ingresar al código para hacer modificaciones, una vez arreglado, ejecutar el programa y obtener la bandera.
-Descargar el archivo y descomprimirlo.
-Buscar el archivo `main.rs` dentro de la carpeta descomprimida.
-Editar el archivo con un editor de texto.
-Una vez corregido el archivo, en el directorio anterior, escribir el siguiente comando:
```
$ cargo build
```
-Cuando el programa haya sido compilado, ejecutarlo con el siguiente comando:
```
$ cargo run
```

El resultado es: **picoCTF{4r3_y0u_4_ru$t4c30n_n0w?}**.

**Notas adicionales:**
-Es necesario tener un compilador de Rust para ejecutar el programa.
-Cargo es un empaquetador de Rust.

**Referencias:**
https://rust-lang.org/tools/install/
https://doc.rust-lang.org/book/ch01-03-hello-cargo.html