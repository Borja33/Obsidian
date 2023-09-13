--------------------
- Tags: #herramienta #contenedores #creacion #distribuir #ejecucion #entornos #docker
-----------------------------
# Definición

> Es una plataforma de contenedores de software que permite crear, distribuir y ejecutar aplicaciones en entornos aislados. Esto significa que se pueden empaquetar las aplicaciones con todas sus dependencias y configuraciones en un contenedor que se puede mover fácilmente de una máquina a otra, independientemente de la configuración del sistema operativo o del hardware.
> 
> Algunas de las ventajas que se presentan a la hora de usar Docker son:
> 
> **- Aislamiento:** los contenedores de **`Docker`** están aislados entre sí, lo que significa que si una aplicación dentro de un contenedor es comprometida, el resto del sistema no se vera afectado.
> **- Portabilidad:** los contenedores de **`Docker`** se pueden mover fácilmente de un sistema a otro, lo que los hace ideales para desplegar entornos vulnerables para prácticas.
> **- Reproducibilidad:** los contenedores de **`Docker`** se pueden configurar de forma precisa y reproducible, lo que permite recrear escenarios.
> 
> Para instalar **`Docker`** en Linux, se puede utilizar el comando:

```bash
apt install docker.io
```

> En algunas distribuciones como Centos o RHEL se utiliza:

```bash
yum install docker
```

> Una vez que **`Docker`** ha sido instalado, es necesario iniciar el demonio de **`Docker`** para que los contenedores puedan ser creados y administrados. 
> Para iniciar el demonio de **`Docker`**, se puede utilizar el comando:

```bash
service start
```

### Definiendo la Estructura Básica de Dockerfile

> Un archivo **`Dockerfile`** se compone de varias secciones, cada una de las cuales comienza con una palabra clave en mayúsculas, seguida de uno o más argumentos.
> 
> Algunas de las secciones más comunes en un archivo **`Dockerfile`** son:
> 
> **- FROM:** se utiliza para especificar la imagen base desde la cual se construirá la nueva imagen.
> **- RUN:** se utiliza para ejecutar comandos en el interior del contenedor, como la instalación de paquetes o la configuración del entorno.
> **- COPY:** se utiliza para copiar archivos desde el sistema host al interior del contenedor.
> **- CMD:** se utiliza para especificar el comando que se ejecutará cuando arranque el contenedor.

### Creación y Construcción de Imágenes

> Para la creación de una imagen de **`Docker`**, es necesario tener un archivo **`Dockerfile`** que defina la configuración de la imagen. Una vez que se tiene el **`Dockerfile`** se puede utilizar el comando:

```bash
docker build
```

> para construir la imagen.
> 
> **- docker build:** es el comando que se utiliza para construir una imagen de **`Docker`** a partir de un **`Dockerfile`**. La sintaxis básica es la siguiente:

```bash
docker build [opciones] ruta-al-dockerfile
```

> El parámetro **-t** se utiliza para etiquetar la imagen con un nombre y una etiqueta.

```bash
docker buil -t mi-imagen:v1 ruta-al-dockerfile
```

> **- docker pull:** es el comando que se utiliza para descargar una imagen de **`Docker`** desde un registro de imágenes. La sintaxis básica es la siguiente:

```bash
docker pull nombre-de-la-imagen:etiqueta
```

> **- docker images:** es el comando que se utiliza para listar las imágenes de **`Docker`** que están disponibles en el sistema. La sintaxis básica es la siguiente:

```bash
docker images [opciones]
```

### Carga de Instrucciones en Docker y Despliegue

> El comando **docker run** se utiliza para crear y arrancar un contenedor a partir de una imagen. Algunas de las opciones más comunes para el comando son:
> 
> **-d o -detach** se utiliza para arrancar el contenedor en segundo plano, en lugar de en primer plano.
> **-i o -interactive** se utiliza para permitir la entrada interactiva al contenedor.
> **-t o -tty** se utiliza para asignar un seudoterminal al contenedor.
> **-name** se utiliza para asignar un nombre al contenedor.
> 
> Para arrancar el contenedor a partir de una imagen, se utiliza el siguiente comando:

```bash
docker run [opciones] nombre-de-la-imagen
```

> Una vez que el contenedor esta en ejecución, se puede utilizar el comando **docker ps** para listar los contenedores que están en ejecución en el sistema. Algunas de las opciones más comunes son:
> 
> **-a o -all** se utiliza para listar todos los contenedores, incluyendo los contenedores detenidos.
> **-q o -quiet** se utiliza para mostrar solo los identificadores numéricos de los contenedores.
> 
> Para ejecutar comandos en un contenedor que ya esta en ejecución, se utiliza el comando **docker exec** con diferentes opciones. Algunas opciones más comunes son:
> 
> **-i o -interactive** se utiliza para permitir la entrada interactiva al contenedor.
> **-t o -tty** se utiliza para asignar un seudoterminal al contenedor.

### Gestión de Contenedores

```bash
docker rm $(docker ps -a -q) --force
```

> Este comando se utiliza para eliminar todos los contenedores en el sistema, incluyendo los contenedores detenidos. La opción **-q** se utiliza para mostrar solo los identificadores numéricos de los contenedores, y la opción **--force** se utiliza para forzar la eliminación de los contenedores que están en ejecución. Es importante tener en cuenta que la eliminación de todos los contenedores en el sistema puede ser peligrosa, ya que puede borrar accidentalmente contenedores importantes o datos importantes.

```bash
docker rm id-contenedor
```

> Este comando se utiliza para eliminar un contenedor especifico a partir de su identificador. Es importante tener en cuenta que la eliminación de un contenedor eliminará también cualquier cambio que se haya realizado dentro del contenedor, como la instalación de paquetes o la modificación de archivos.

```bash
docker rmi $(docker images -q)
```

> Este comando se utiliza para eliminar todas las imágenes de **`Docker`** en el sistema. La opción **-q** se utiliza para mostrar solo los identificadores numéricos de las imágenes. Es importante tener en cuenta que la eliminación de todas las imágenes de **`Docker`** en el sistema es peligrosa.

```bash
docker rmi id-imagen
```

> Este comando se utiliza para eliminar una imagen especifica a partir de su identificador. Es importante tener en cuenta que las eliminación de una imagen eliminará también cualquier contenedor que se haya creado a partir de esa imagen. Se desea eliminar una imagen que tiene contenedores en ejecución, se deben detener primero los contenedores **docker stop id-contenedor** y luego eliminar la imagen.

### Port Forwarding y Monturas

> El **`Port Forwarding`** nos permitirá redirigir el trafico de red desde un puerto especifico en el host a un puerto especifico en el contenedor, lo que nos permitirá acceder a los servicios que se ejecutan dentro del contenedor desde el exterior.

> Las **`Monturas`**, por otro lado, nos permitirán compartir un directorio o archivo entre el sistema host y el contenedor, lo que nos permitirá persistir la información entre ejecuciones de contenedores y compartir datos entre diferentes contenedores.

> Para utilizar el **`Port Forwarding`**, se utiliza la opción **-p o --publish** en el comando **docker run**. Esta opción se utiliza para especificar la redirección de puertos y se puede utilizar de varias maneras. Por ejemplo, si se desea redirigir el puerto 80 el host al puerto 8080 del contenedor, se puede utilizar la siguiente sintaxis:

```bash
docker run -p 80:8080 mi-imagen
```

> Esto redirigirá cualquier tráfico entrante en el puerto 80 del host al puerto 8080 del contenedor. Si se desea especificar un [protocolo](Protocolos%20Comunes) diferente al protocolo [[TCP]] predeterminado, se puede utilizar la opción **-p** con un formato diferente.
> 
> Por ejemplo, si se desea redirigir el puerto 53 del host al 53 del contenedor utilizando el protocolo [[UDP]], se puede utilizar la siguiente sintaxis:

```bash
docker run -p 53:53/udp mi_imagen
```

> Para utilizar las **`monturas`**, se utiliza la opción **-v o --volumen** en el comando **docker run**. Este opción se utiliza para especificar la montura y se puede utilizar de varias maneras. Por ejemplo, si se desea montar el directorio **/home/usuario/datos** del host en el directorio **/datos** del contenedor, se puede utilizar la siguiente sintaxis:

```bash
docker run -v /home/usuarios/datos:/datos mi-imagen
```

> Esto montara en el directorio **/home/usuario/datos** del host en el directorio **/datos** del contenedor. Si se desea especificar una opción adicional, como la de montar el directorio en modo de solo lectura, se puede utilizar la opción **-v** con un formato diferente.
> 
> Por ejemplo, si se desea montar el directorio en modo de solo lectura, se puede utilizar la siguiente sintaxis:

```bash
docker run -v /home/usuario/datos:/datos:ro mi-imagen
```

### Docker-Compose

> Es una herramienta de orquestación de contenedores que  permite definir y ejecutar aplicaciones multicontenedor de manera fácil y eficiente. Con **`Docker-Compose`**, podemos describir los diferentes servicios que componen nuestra aplicación en un archivo **YAML** y, a continuación, utilizar un solo comando para ejecutar y gestionar todos estos servicios de manera coordinada. En otras palabras, **`Docker-Compose`** nos permite definir y configurar múltiples contenedores en un solo archivo **YAML**, lo que simplifica la gestión y coordinación de múltiples contenedores en una sola aplicación. Esto es especialmente útil para aplicaciones complejas que requieren la interacción de varios servicios diferentes, ya que **`Docker-Compose`** permite definir y configurar fácilmente la conexión y la comunicación entre estos servicios.

```bash
docker-compose up -d
```

> Con el comando anterior creamos los contenedores especificados en el archivo **.gm**
> 
> Para ver información detallada de bajo nivel sobre los objetos **`Docker`** podemos usar:

```bash
docker inspect
```
