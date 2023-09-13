--------------------
- Tags: #enumeracion #http #https #servicios 
-----------------------------
# Definición

> [[HTTP]] es un [protocolo](Protocolos%20Comunes) es un protocolo de comunicación utilizado para la transferencia de datos en la World Wide Web. Se utiliza para la transferencia de contenido de texto, imágenes, video, hipervínculos, etc. El puerto predeterminado para [[HTTP]] es el puerto 80.
> 
> [[HTTPS]] es una versión segura de [[HTTP]] que utiliza [[SSL]]/[[TLS]] para cifrar la comunicación entre el cliente y el servidor. Utiliza el puerto 443 por defecto. 
> 
> Una de las herramientas para inspeccionar el certificado [[SSL]] es **Openssl**. **Openssl** es una biblioteca de software libre y de código abierto que se utiliza para implementar protocolos de seguridad en línea, como [[TLS]],[[SSL]]. La biblioteca **Openssl** proporciona una implementación de estos protocolos para permitir que las aplicaciones se comuniquen de manera segura y encriptada a través de la red.

```bash
openssl s_client -connet ejemplo.com:443
```

> Con este comando, podemos inspeccionar el certificado [[SSL]] de un servidor web. El comando se conecta al servidor en el puerto 443 y muestra información detallada sobre el certificado [[SSL]], como la validez del certificado, la fecha de caducidad, el tipo de certificado, etc.
> 
> Asimismo, otras de las herramientas que vemos son [[sslyze]] y [[sslscan]]. La principal diferencia entre [[sslyze]] y [[sslscan]] es que [[sslyze]] se enfoca en la evaluación de la seguridad [[SSL]]/[[TLS]] de un servidor web mediante una exploración exhaustiva de los protocolos y configuraciones [[SSL]]/[[TLS]], mientras que [[sslscan]] se enfoca en la identificación de los protocolos [[SSL]]/[[TLS]] admitidos por el servidor y los cifrados utilizados.
> 
> La identificación de las informaciones arrojadas por las herramientas de análisis [[SSL]]/[[TLS]] es una de suma importancia, ya que nos puede permitir detectar vulnerabilidades en la configuración de un servidor y tomar medidas para proteger nuestra información confidencial.
> 
> Por ejemplo, [[Heartbleed]] es una vulnerabilidad de seguridad que afecta a la biblioteca **Openssl** y permite a los atacantes acceder a la memoria de un servidor vulnerable. Si un servidor web es vulnerable a [[Heartbleed]] y lo detectamos a través de estas herramientas, esto significa que un atacante podría potencialmente acceder a información confidencia, como claves privadas, nombres de usuario y contraseñas, etc.