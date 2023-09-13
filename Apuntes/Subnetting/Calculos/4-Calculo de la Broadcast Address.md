--------------------
- Tags: #tecnica #subnetting #red #ip #subredes #calculo #broadcast #address
-----------------------------
# Definición

> La **`Broadcast Address`** es la dirección de red que se utiliza para enviar paquetes a todos los hosts de la subred.
> 
> Para calcularla, necesitamos saber el [Network ID](3-Calculo%20del%20Network%20ID) y la [cantidad de hosts](2-Calculo%20del%20Total%20de%20Hosts%20a%20Repartir) disponibles en la subred. 
> 
> En el ejemplo que estamos trabajando, ya hemos calculado el [Network ID](3-Calculo%20del%20Network%20ID) como **192.168.1.0**. La cantidad de hosts disponibles se calcula como 2<sup>n</sup>-2 donde **n** es la cantidad de bits utilizados para representar la parte de host en la máscara de red. En este caso, **n** es igual a **6**, ya que hay **6 bits** disponibles para la parte de host.
> 
> Para calcular la **`Broadcast Address`** debemos asignar todos los bits de la parte del host de la dirección IP a **1**. En este caso, la dirección IP es **192.168.1.0** y se convierte en binario como
> **11000000.10101000.00000001.00000000**
> Para encontrar la dirección **`Broadcast`** llenamos con unos la parte correspondiente a los bits de host, es decir, los últimos **6 bits**:
> **11000000.10101000.00000001.00111111**
> 
> Luego, convertimos este valor binario de regreso a decimal y obtenemos la dirección de **`Broadcast`**:
> **192.168.1.63**
> Esta es la dirección a la que enviaremos los paquetes para llegar a todos los hosts de la subred.

