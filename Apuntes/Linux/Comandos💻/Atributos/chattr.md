--------------------
- Tags: #cmd #comandos #cambiar #directorios #archivos #atributos
-----------------------------
# Definición

> Comando del sistema de archivos que se utiliza para cambiar los atributos de un archivo en un directorio. El uso principal de este comando es hacer que varios archivos no puedan modificarse para usuarios que no sean el superusuario. En resumen, **`chattr`** puede hacer que un archivo sea inmutable, no se pueda eliminar.

## Comando

```bash
sudo chattr +i nombredirectorio/archivo
```

## Atributos

- **a** Cuando se establece este atributo, el archivo solo se puede abrir en modo adjunto para escritura.
- **A** Cuando un archivo con este conjunto de atributos está abierto, su registro de hora no cambia. atime (tiempo de acceso) es la última vez que se accedió / abrió el archivo mediante algún comando o aplicación.
- **e** Este atributo indica que el archivo está usando extensiones para mapear los bloques en el disco. El atributo **e** no se puede modificar con **`chattr`**.
- **i**  Este atributo indica que el archivo es inmutable, lo que significa que el archivo no se puede eliminar ni cambiar de nombre.