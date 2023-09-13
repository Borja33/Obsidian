--------------------
- Tags: #cmd #comandos #filtrar
-----------------------------
# Definición

> Para seleccionar una columna, línea, etc. Para quedarnos con la parte que nos interesa de una salida.

## Comandos

```bash
awk 'NF{print $NF}'
```
- Muestra la ultima columna

```bash
awk 'NR==2'
```
- Muestra la segunda fila