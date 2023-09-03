-----------------
- Tags: #cmd #busqueda #comandos
--------------------------------
# Definición

> Se puede utilizar para buscar archivos y directorios y realizar operaciones posteriores con ellos. Admite búsqueda por archivo, carpeta, nombre, fecha de creación, fecha de modificación, propietario y permisos.

## Comando

```bash
find / -name "nombrearchivo"
```
- Buscar un solo archivo por nombre

```bash
find / -iname "*foo*txt"
```
- Buscar un solo archivo por nombre aproximado

```bash
find / -ls
```
- Encontrar toda a partir de una ruta

```bash
find / -type f
```
- Encontrar archivos por tipo

```bash
find / -type d -ipath "*public_html/example.com*"
```
- Busca un camino