--------------------
- Tags: #protocolo #dhcp #red #udp 
-----------------------------
# Definición

> **`DHCP:67/68 (Dynamic Host Configuration Protocol`** un [protocolo](Protocolos%20Comunes) utilizado para asignar direcciones IP y otros parámetros de configuración a los dispositivos en una red.
> 
> Es uno de los más utilizados por los routers, tanto domésticos como también profesionales, además, de forma predeterminada cualquier cliente cableado o por WiFi está configurado para obtener una dirección IP por **`DHCP`**. 
> 
> Es un [protocolo](Protocolos%20Comunes) de red que utiliza una arquitectura cliente-servidor. Por tanto, tendremos uno o varios servidores **`DHCP`** y también uno o varios clientes, que se deberán comunicar entre ellos correctamente para que el servidor **`DHCP`** brinde información a los diferentes clientes conectados. Este [protocolo](Protocolos%20Comunes) se encarga de asignar de manera dinámica y automática una dirección IP, ya sea una dirección IP privada desde el router hacia los equipos de la red local, o también una IP pública por parte de un operador que utilice este tipo de protocolo para el establecimiento de la conexión.
> 
> Cuando tenemos un servidor **`DHCP`** en funcionamiento, todas las direcciones IP que ha proporcionado a diferentes clientes se guardan en un listado donde se relaciona la IP que se le ha proporcionado (dirección lógica) y la dirección MAC (dirección física de la tarjeta de red). Gracias a este listado, el servidor **`DHCP`** se asegura de no proporcionar a dos equipos diferentes la misma dirección IP, lo que ocasiona un caos en la red local. A medida que el servidor va asignando direcciones IP, también tiene en cuenta cuándo pasa un determinado tiempo y caducan, quedando libres para que otro cliente pueda obtener esta misma dirección IP. El servidor **`DHCP`** sabrá en todo momento quién ha estado en posesión de una dirección IP, cuánto tiempo ha estado, y cuándo se ha asignado a otro cliente.

