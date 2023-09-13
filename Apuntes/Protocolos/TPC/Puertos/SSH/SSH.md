--------------------
- Tags: #protocolo #ssh #red #tcp 
-----------------------------
# Definición

> **`22:SSH`** son las siglas de **Secure SHell** y es un protocolo de red destinado principalmente a la conexión con máquinas a las que accedemos por línea de comandos. En otras palabras, con **`SSH`** podemos conectarnos con servidores, usando la red Internet como vía para las comunicaciones.

## Comando

```bash
ssh root@1.2.3.4
```
- Para realizar una conexión en este caso como root a la ip indicada
### sshpass

> **`Sshpass`** es una herramienta que vienen todas las distros Linux pero no viene instalada por defecto y te permite el poder añadir en una única línea de terminal la dirección del servidor y la contraseña. Para introducir la contraseña del [[SSH]] antes de la conexión

## Comando

```bash
sudo apt install sshpass
```
- Para instalar 

```bash
sshpass -p `contraseña` ssh nombre@IP
```
- Conectarnos por ssh, medina IP y nombre, con la contraseña en una misma línea
