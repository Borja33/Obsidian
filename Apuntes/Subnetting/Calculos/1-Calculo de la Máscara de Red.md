--------------------
- Tags: #tecnica #subnetting #red #ip #subredes #calculo #mascara #red 
-----------------------------
# Definición

> La dirección IP que se nos dio es **192.168.1.0/26**, lo que significa que los primeros **26 bits** de la dirección IP corresponden a la red y los últimos **6 bits** corresponden a los hosts.
> 
> Para calcular la máscara de red, necesitamos colocar los primeros **26 bits** en **1** y los últimos **6 bits** en **0**. En binario, esto se ve así:
> **11111111.11111111.11111111.11000000**
> Cada octeto de la máscara de red se compone de **8 bits**. El valor de cada octeto se determina convirtiendo los **8 bits** a decimal. En este caso, los primeros **24 bits** son todos **1**, lo que significa que el valor decimal de cada uno de estos octetos es **255**. El último octeto tiene los últimos **6 bits** en **0**, lo que significa que su valor decimal es **192**. 
> 
> Por lo tanto, la máscara de red para esta dirección IP es **255.255.255.192**.

