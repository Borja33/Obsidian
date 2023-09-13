--------------------
- Tags: #cmd #comandos #redireccionamiento #archivos 
-----------------------------
# Definición

>  Su uso básico es absorber la entrada estándar y escribirla en un archivo. Para redirigir al mismo archivo que estamos manipulando.

## Comando

```bash
sponge archivo
```
- Crea el archivo y recibe la entrada por consola (Ctrl + d para señalar el fin)

```bash
echo "Put this text in a file" | sponge file1.txt
```
- Redirige el comando echo al archivo indicado por sponge. una redirección abrirá el archivo para escribirlo y luego leerá la "transmisión" en él. Si intenta leer y escribir en el mismo archivo con una redirección, corre un riesgo real de dañarlo.
