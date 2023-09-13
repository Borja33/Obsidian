--------------------
- Tags: #cmd #comandos #redireccionamiento #concatenar #tuberia
-----------------------------
# Definición

> Permite redireccionar la ejecución de un comando mediante una [tubería](tuberia), hacia otro comando. Posibilita que comandos como [rm](rm.md) o [mkdir](mkdir.md) acepten la entrada estándar como argumentos.

## Comando

```bash
echo 'archivo1 archivo2 archivo3' | xargs mkdir
```

