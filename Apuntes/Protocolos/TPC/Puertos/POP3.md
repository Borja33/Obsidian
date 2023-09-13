--------------------
- Tags: #protocolo #pop3 #red #tcp 
-----------------------------
# Definición

> **`110:POP3 (Post Office Protocol v3)`** Se conecta la servidor de correo, recupera todos los mensajes del buzón. Luego los almacena en tu ordenador local y los elimina del servidor remoto. 
> 
> Es uno de los protocolos fundamentales para la gestión de correo electrónico o email. Este protocolo se utiliza por los clientes locales de email para obtener los mensajes de email de un servidor remoto de coreo electrónico. 

### Funcionamiento e intercambio de mensajes

> Lo primero que debe hacer el cliente de correo es establecer una conexión con el servidor **`POP3`**, ya sea usando el puerto 110 [[TCP]] (sin cifrado) o el puerto 995 [[TCP]] (con cifrado de datos [[SSL]]/[[TLS]]). Una vez que se ha establecido la conexión, el servidor POP pedirá la autenticación con usuario y contraseña, el cliente enviará el nombre de usuario y clave de forma segura para autenticarse en el servidor. Si la autenticación es incorrecta volverá a pedir la autenticación. Si la autenticación es correcta, el cliente POP pasará al estado de transición, y podremos listar los correos, descargarlos y borrarlos del servidor.
> 
> El borrado del servidor no se realiza hasta que se envía la orden QUIT para terminar la sesión **`POP3`**, en ese momento el servidor comenzará a actualizar su base de datos de emails. Debemos recordar que el cliente **`POP3`** puede **dejar los mensajes en el servidor** para que no se borren, si no tiene habilitada esta opción los mensajes del servidor de correo se borrarán en cuanto se descarguen por primera vez.
> 
> El punto fuerte de **`POP3`** es que nos permitirá descargar los correos cuando nuestra conexión es intermitente, también debemos tener en cuenta que es un [protocolo](Protocolos%20Comunes) muy sencillo que no tiene demasiadas órdenes para comunicarse. No obstante, hoy en día lo que se suele utilizar es IMAP, un protocolo más avanzado que nos permite la sincronización de los emails y marcarlos como leídos, no leídos, descargarlos e incluso borrarlos, no es tan básico como POP3.