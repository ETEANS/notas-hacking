
**Reto:**
-Arreglar el código de Rust para obtener la bandera.

**Descripción:**
-Have you heard of Rust? Fix the syntax errors in this Rust file to print the flag!
-Download the Rust code [here](https://challenge-files.picoctf.net/c_verbal_sleep/dcdaf491b35c1d0f5075e9583edbbb7aaea1dffb6ad32bc000e4d87b5200ff7b/fixme3.tar.gz).

**Solución:**
Ingresar al código para hacer modificaciones, una vez arreglado, ejecutar el programa y obtener la bandera.
-Descargar el archivo y descomprimirlo.
-Buscar el archivo `main.rs` dentro de la carpeta descomprimida.
-Editar el archivo con un editor de texto, quita los commentarios de la parte 'unsafe'.
-Una vez corregido el archivo, en el directorio anterior, escribir el siguiente comando:
```
$ cargo build
```
-Cuando el programa haya sido compilado, ejecutarlo con el siguiente comando:
```
$ cargo run
```

El resultado es: **picoCTF{n0w_y0uv3_f1x3d_1h3m_411}**.

**Notas adicionales:**
-La operación 'unsafe' se encarga de controlar comandos que no son seguros.

**Referencias:**
https://rust-lang.org/tools/install/
https://doc.rust-lang.org/book/ch01-03-hello-cargo.html