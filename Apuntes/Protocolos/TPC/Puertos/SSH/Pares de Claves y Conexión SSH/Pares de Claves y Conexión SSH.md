--------------------
- Tags: #protocolo #ssh #red #tcp #claves #conexion
-----------------------------
# Definición

> Los **`Pares de Claves SSH`** son dos claves criptográficamente seguras que pueden usarse para autenticar a un cliente a un servidor [[SSH]]. Cada par de clave esta compuesto por una clave pública y una privada.
> 
> El cliente mantiene la clave privada y debe mantenerla en absoluto secreto. Poner en riesgo la clave privada puede permitir a un atacante no autorizado iniciar sesión en los servidores que están configurados con la clave pública asociada sin autenticación adicional. Como medida de precaución adicional, es recomendable cifrar la clave en el disco con una frase de contraseña.
> 
> La clave pública asociada puede compartirse libremente sin ninguna consecuencia negativa. La clave pública puede usarse para cifrar mensajes que solo la clave privada puede descifrar. Esta propiedad se emplea como forma de autenticación mediante el uso del par de claves.
### Comandos
- **systemctl start sshd** para habilitar el servidor

- **ssh-keygen** para crear un par de claves (pública y privada)

- **systemctl stop sshd**  para parar el servidor

- **ssh -i claveprivada usuario@ip** para conectarse con una clave privada