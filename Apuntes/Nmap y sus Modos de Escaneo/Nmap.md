--------------------
- Tags: #herramienta #escaneo #red #penetracion #explotar #pentesting
-----------------------------
# Definición

> **`Nmap`** es una herramienta de escaneo de red gratuita y de código abierto que se emplea en pruebas de penetración(pentesting) para explotar y auditar redes y sistemas informáticos. 

- **tcpdump -i ens33 -w Captura.cap** Permite al usuario capturar y mostrar en tiempo real los paquetes transmitidos y recibidos por la red a la cual el ordenador esta conectado.
### Comandos

- **-p** puestos a escanear
	- *-p 22* puerto 22
	- *-p1-65535* rango de puertos
	- *-p-* todos los puertos
- **--top-ports 500** escanea los 500 puertos más comunes
- **--open** devuelve solo puertos abiertos
- **-n** quitar resolución DNS
- **-T** seleccionar plantilla de temporizado
- **-sT** para establecer ThreeHandshake (SYN->SYN-ACK->ACK)
- **-Pn** sirve para dar por sentado que el host esta activo
- **-sU** para escanear por [[UDP]]
- **-sn** aplica un barrido por ping
- **-sV** muestra más información del puerto (versión, protocolo...)

> Cuando se realizan pruebas de penetración, uno de los mayores desafíos es evadir la detección de los Firewalls, que son diseñados para proteger las redes y sistemas de posibles amenazas. Para superar este obstáculo, **`Nmap`** ofrece una variedad de técnicas de evasión que permiten a los profesionales de seguridad realizar escaneos sigilosos y evitar así la detección de los mismos.
### Comandos para evitar el Firewall

- **MTU (-mtu)** La técnica de evasión **`MTU o (Maximum Transmission Unit)`** implica ajustar el tamaño de los paquetes que se envían para evitar la detección por parte del Firewall. **`Nmap`** permite configurar manualmente el tamaño máximo de los paquetes para garantizar que sean lo suficientemente pequeños para pasar por el Firewall sin ser detectados.

- **Data Length (-data-length)** Esta técnica se basa en ajustar la longitud de los datos enviados para que sean lo suficientemente cortos como para pasar por el Firewall sin ser detectados. **`Nmap`** permite a los usuarios configurar manualmente la longitud.

- **Source Port (-source-port)** Esta técnica consiste en configurar manualmente el número de puerto de origen de los paquetes enviados para evitar la detección por parte del Firewall. **`Nmap`** permite a los usuarios especificar manualmente un puerto de origen aleatorio o un puerto especifico para evadir la detección del Firewall.

- **Decoy (-D)** Esta técnica de evasión en **`Nmap`** permite al usuario enviar paquetes falsos a la red para confundir a los sistemas de detección de intrusos y evitar la detección de Firewall. El comando **`-D`** permite al usuario enviar paquetes falsos junto con los paquetes reales de escaneo para ocultar su actividad.

- **Fragmented (-f)** Esta técnica se basa en fragmentar los paquetes enviados para que el Firewall no pueda reconocer el tráfico como un escaneo.

- **Spoof-Mac (-spoof-mac)** Esta técnica de evasión consiste en cambiar la dirección MAC del paquete para evitar la detección del Firewall.

- **Stealth Scan (-sS)** Esta técnica es una de las más utilizadas para realizar escaneos sigilosos y evitar la detección del Firewall. El comando **`-sS`** permite al usuario realizar un escaneo de tipo SYN sin establecer una conexión completa, lo que permite evitar el Firewall.

- **min-rate (-min-rate)** Esta técnica permite al usuario controlar la velocidad de los paquetes enviados para evitar la detección del Firewall. El comando **`-min-rate`** permite al usuario reducir la velocidad de los paquetes enviados.

> Una de las características más poderosas de **`Nmap`** es su capacidad para automatizar tareas utilizando scripts personalizados. El parámetro **-script** de **`Nmap`** permite al usuario seleccionar un conjunto de scripts para ejecutar en un objetivo d escaneo especifico.
> 
> Existen diferentes categorías de scripts disponibles en **`Nmap`**, cada una diseñada para realizar una tarea especifica.

### Categorías de Scripts

- **default** Esta es la categoría predeterminada en **`Nmap`**, que incluye una gran cantidad de scripts de reconocimiento básicos y útiles para la mayoría de los escaneos. 

- **discovery** Esta categoría se enfoca en descubrir información sobre la red, como la detección de hosts y dispositivos activos, y la resolución de nombre de dominio.

- **safe** Esta categoría incluye scripts que son considerados seguros y que no realizan actividades invasivas que puedan desencadenar una alerta de seguridad en la red.

- **intrusive** Esta categoría incluye scripts más invasivos que pueden ser detectados fácilmente por un sistema de detección de intrusos o Firewall, pero que pueden proporcionar información valiosa.

- **vuln** Esta categoría se enfoca especialmente en la detección de vulnerabilidades y debilidades en los sistemas y servicios que se están ejecutando en la red.

- **-sV** escaneo de Versiones,SO
- **-A** escaneo agresivo
- **-sS** escaneo sigiloso
- **-iL** escaneo desde un archivo
- **zenmap** interfaz grafica de **`Nmap`**
- **--script="vuln and safe"** combinar dos categorías de scripts y ejecutarlos. 
- **script nombre script** ejecutar un scripts concreto.
- **-sC** equivalente a **-script=predeterminado**

>**`Nmap`** permite la creación y uso de scripts personalizados en el lenguaje **Lua**. La estructura básica de un script de **Lua** en **`Nmap`** incluye la definición de una tabla.

### Campos Comunes Script Lua

- **description** Este campo se utiliza para proporcionar una descripción corta del script y su funcionalidad.

- **categories** Este campo se utiliza para especificar las categorías a las que pertenece el script, como descubrimiento, explotación, enumeración, etc.

- **author** Este campo se utiliza para identificar al autor del script.

- **license** Este campo se utiliza para especificar los términos de la licencia bajo la cual se distribuye el script.

- **dependencias** Este campo se utiliza para especificar cualquier dependencia de biblioteca o software que requiera el script para funcionar correctamente.

- **actions** Este campo se utiliza para definir la funcionalidad especifica del script, como la realización de un escaneo de puertos, la detección de vulnerabilidades, etc.