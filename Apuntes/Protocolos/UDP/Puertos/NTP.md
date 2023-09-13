--------------------
- Tags: #protocolo #ntp #red #udp 
-----------------------------
# Definición

> **`NTP:123 (Network Time Protocol)`** un [protocolo](Protocolos%20Comunes) utilizado para sincronizar los relojes de los dispositivos en una red.
> 
> Su función principal es la de sincronizar los relojes de los sistemas informáticos. Para ello utiliza el enrutamiento de paquetes en redes con latencia variable. Estamos ante uno de los [protocolo](Protocolos%20Comunes) de red más antiguos y sigue siendo importante para mantener el funcionamiento correcto de las conexiones.
> 
> Como capa de transporte utiliza [[UDP]] a través del puerto 123. **`NTP`** va a servir para lanzar una petición de sincronización. En primer lugar se envía un mensaje por parte del cliente y comprueba y si el desfase de tiempo entre el servidor y el solicitante supera los 17 minutos. Posteriormente ese mensaje llega al servidor de destino. En caso de que efectivamente supere los 17 minutos, el proceso se pararía y no continuaría adelante.