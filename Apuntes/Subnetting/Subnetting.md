--------------------
- Tags: #tecnica #subnetting #red #ip #subredes 
-----------------------------
# Definición

> Es una técnica utilizada para dividir una red IP en subredes más pequeñas y manejables. Esto se logra mediante el uso de máscaras de red, que permiten definir que bits de la dirección IP corresponden a la red y cuales a los host.
> 
> Para interpretar una máscara de red, se deben identificar los bits que están en **1**. Estos bits representan la porción de la dirección IP que corresponde a la red. Por ejemplo, una mascara de red de **255.255.255.0** indica que los primeros tres octetos de la dirección IP corresponden a la red, mientras que el último octeto se utiliza para identificar los hosts.
>  
> Ahora bien, cuando hablamos de **`CIDR (Acronimo de Classless Inter Domain Routing)`**, a lo que nos referimos es a un método de asignación de direcciones IP más eficiente y flexible que el uso de clases de redes fijas. Con **`CIDR`**, una dirección IP se representa mediante una dirección IP base y una máscara de red, que se escriben juntas separadas por una barra **/**.
> 
> Por ejemplo, la dirección IP **192.168.1.1** con una máscara de red de **255.255.255.0** se escribirá como **192.168.1.1/24**. La máscara de red se representa en notación de prefijo, que indica el número de bits que están en **1** en la máscara. En este caso, la máscara de red **255.255.255.0** tiene 24 bits en **1** (los primeros tres octetos), por lo que su notación de prefijo es **/24**.
> 
> Para calcular la máscara de red a partir de una notación de prefijo se deben escribir los bits **1** en los primeros bits de una dirección IP de 32 bits y los bits **0** en los bits restantes. Por ejemplo, la máscara de red **/24** se calcularía como **11111111.11111111.11111111.00000000** en binario, lo que equivale **255.255.255.0**. En cuanto a clases de direcciones IP, existen tres tipos de máscara de red [[Clase A]], [[Clase B]] y [[Clase C]].
> 
> Es importante tener en cuenta que, además de estos tres tipos de máscaras de red, también existen máscaras de red personalizadas que se pueden utilizar para crear subredes de diferentes tamaños dentro de una red.
> 
> Para calcular la dirección IP **192.168.1.0/26**, su máscara de red, el número total de hosts a repartir, el identificador de red y la dirección Broadcast. Seguiremos los siguientes pasos:
> 
> [[1-Calculo de la Máscara de Red]]
> [[2-Calculo del Total de Hosts a Repartir]]
> [[3-Calculo del Network ID]]
> [[4-Calculo de la Broadcast Address]]