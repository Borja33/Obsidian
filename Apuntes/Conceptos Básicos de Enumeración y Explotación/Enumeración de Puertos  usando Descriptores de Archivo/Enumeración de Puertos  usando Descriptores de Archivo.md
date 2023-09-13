--------------------
- Tags: #enumeracion #puertos #descriptores #archivos  
-----------------------------
# Definición

> Una alternativa a [[Nmap]] para la enumeración de puertos, es utilizando herramientas como los descriptores de archivo en sistema Unix. Los descriptores de archivo son una forma de acceder y manipular archivos y dispositivos en sistemas Unix. En particular, la utilización de [[dev]]/[[TCP]] permite la conexión a un host y puerto específicos como si se tratara de un archivo en el sistema.
> 
> Para realizar la enumeración de puertos utilizando [[dev]]/[[TCP]] en Bash, es posible crear un script que realice una conexión a cada puerto de interés y compruebe si el puerto esta abierto o cerrado en función de si se puede enviar o recibir datos. Una forma de hacer esto es mediante el uso de comandos como [[echo]] o [[cat]], aplicando redireccionamientos al [[dev]]/[[TCP]]. El código de estado devuelto por el comando se puede utilizar para determinar si esta abierto o cerrado.
