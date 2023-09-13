--------------------
- Tags: #tecnica #subnetting #red #ip #subredes #calculo #network #id
-----------------------------
# Definición

> Para calcular el **`Network ID`**, lo que debemos hacer es aplicar la máscara de red a la dirección IP de la red. En este caso, la máscara de res es **255.255.255.192**, lo que significa que los primeros **26 bits** de la dirección IP pertenecer a la parte de red.
> 
> Para calcular el **`Network ID`**, convertimos tanto la dirección IP como la mascara de red en binario y luego hacemos una operación AND lógica entre  los dos. La operación AND compara los bits correspondientes en ambas direcciones y devuelve un resultado en el que todos los bits coincidentes son iguales a **1** y todos los bits no coincidentes son iguales a **0**. 
> 
> En este caso la dirección IP es **192.168.1..0** en decimal y se convierte en binario como **11000000.10101000.00000001.00000000**.
> La mascara de red es **255.255.255.192** en decimal y se convierte en binario como **11111111.11111111.11111111.11000000**.
> 
> Luego, aplicamos AND entre estos dos valores binarios bit a bit. Los bits correspondientes en ambos valores se comparan.
> El resultado final es el **`Networkd ID`**, que es **192.168.1.0** Este es el identificador único de la subred a la que pertenecen los hosts.