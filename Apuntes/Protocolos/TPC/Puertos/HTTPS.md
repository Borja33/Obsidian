--------------------
- Tags: #protocolo #https #red #tcp 
-----------------------------
# Definición

> **`443:HTTPS (Hypertext Transfer Protocol Secure)`** la versión segura de [[HTTP]], que utiliza encriptación [[SSL]]/[[TLS]] para proteger las comunicaciones web.
> 
> Es lo mismo que [[HTTP]] con la salvedad de que se le añade el término **seguro**.

### Funcionamiento

- Abrimos una página de Internet y el navegador intentará conectarse a un sitio que ha sido protegido con SSL
- El navegador requerirá que el servidor web se identifique
- Será así como el servidor mandará una copia de su certificado SSL a nuestro navegador
- El navegador, una vez ha recibido la copia, comprobará si el sitio web es de confianza. Si es así, manda una mensaje que lo acredita
- El servidor mandará acuse de recibo con firma digital que permitirá que se inicie la conexión cifrada
- Así es como empezarán a transferirse datos cifrados entre el servidor y el navegador