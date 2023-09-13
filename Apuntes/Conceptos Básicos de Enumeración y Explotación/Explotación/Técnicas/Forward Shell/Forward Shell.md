--------------
- Tags: #remoto #explotacion #tecnica 
---------------------
# Definición

> Esta técnica se utiliza cuando no se pueden establecer conexiones [[Reverse Shell]] o [[Bind Shell]] debido a reglas de Firewall implementadas en la red. Se logra mediante el uso de [[mkfifo]], que crea un archivo [FIFO](FIFO) (named pipe) que se utiliza como una especie de **`consola simulada`** interactiva a través de la cual el atacante puede operar en la máquina remota. En lugar de establecer una conexión directa, el atacante redirige el tráfico a través del archivo [FIFO](fifo), lo que permite la comunicación bidireccional con la máquina remota.



