--------------------
- Tags: #protocolo #smb #red #tcp 
-----------------------------
# Definición

> **`139,445:SMB (Server Message Block)`** Es un protocolo de uso compartido de archivos de red.
> 
> Es un [protocolo](Protocolos%20Comunes) cliente/servidor que gobierna el acceso a archivos y directorios completos, así como a otros recursos de red como impresoras, enrutadores o interfaces abiertas a la red. El intercambio de información entre los diferentes procesos de un sistema se puede manejar en base al protocolo **`SMB`**.


### Funciones

> Permite al cliente comunicarse con otros participantes en la misma red, lo que le permite acceder a archivos o servicios abiertos a él en la red. Para que esto funcione, el otro sistema también debe haber implementado el protocolo de red y recibir y procesar la solicitud del cliente respectivo utilizando una aplicación de servidor **`SMB`**.
>
> Pero ambas partes deben establecer primero una conexión, por lo que primero intercambian los mensajes correspondientes. En las redes IP, **`SMB`** utiliza el [[TCP]] que proporciona un protocolo de enlace de tres vías entre el cliente y el servidor, antes de finalmente establecer una conexión. Transporte de datos posterior está regulado por las disposiciones del protocolo [[TCP]].
> 
> El protocolo **`SMB`** crea una conexión entre el servidor y el cliente enviando múltiples mensajes de solicitud y respuesta de un lado a otro.