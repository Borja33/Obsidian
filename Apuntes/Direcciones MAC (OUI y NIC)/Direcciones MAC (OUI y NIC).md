--------------------
- Tags: #mac #oui #nic
-----------------------------
# Definición

> La **`dirección MAC`** es un número hexadecimal de **12 dígitos (número binario de 6 Bytes)**, que esta representando principalmente por notación hexadecimal de los puntos.
> 
> Los primeros **6 dígitos** (digamos 00:40:96) del **`MAC Adress`** identifican al fabricante, llamado **OUI (Identificador Único Organización)**. El Comité de la Autoridad de Registro de IEEE asigna estos prefijos MAC a sus proveedores registrados.
> 
> Los **6 dígitos** más a la derecha representan el controlador de interfaz de red, que es asignado por el fabricante. Es decir, los primeros **3 Bytes (24 bits)** representan el fabricante de la tarjeta, y los últimos **3 Bytes (24 bits)** identificar la tarjeta particular de ese fabricante. Cada grupo de **3 Bytes** se puede representar con **6 dígitos** hexadecimales, formando un número hexadecimal de **12 dígitos** que representan la MAC completa.
> 
> Para la búsqueda del fabricante utilizando **`direcciones MAC`**, se requieren al menos los primeros **3 Bytes (6 caracteres)** de la dirección MAC. Una de las herramientas para lograr este fin [[macchanger]].