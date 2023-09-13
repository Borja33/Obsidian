-------------
- Tags:  #datos #basedatos #recopilacion #info #almacenamiento #NoSQL #norelacional
----------------------------
# Definición

>**`Apache Cassandra`** es un **sistema de gestión de base de datos (DBMS)** de código abierto para bases de datos muy grandes, pero estructuradas. Gracias a la buena escalabilidad, estas bases de datos se pueden distribuir a diferentes clústeres, por lo que **`Cassandra`** no se encuentra unidad a un único servidor.
>
>**`Cassandra`** pertenece a las [[Bases de datos NoSQL]] columnares. Como base de datos NoSQL, **`Cassandra`** cuenta con un enfoque redundante, lo que reduce mucha la probabilidad de fallo. Sin embargo, las [[Bases de datos relacionales]] suelen tener problemas al replicar los datos.

### Funciones más importantes

> Al tratarse de un auténtico [[Sistema Distribuido]], **`Cassandra`** no usa un maestro. Todos los [[Clústeres]] tienen el mismo rango y pueden procesar cualquier consulta de base de datos, lo que aumenta notablemente la capacidad de rendimiento. Los datos están distribuidos en los nodos. El sistema es **fácilmente escalable** debido a que se pueden añadir más nodos de manera muy sencilla. Una vez realizada la instalación, ya solo tendrás que distribuir los archivos de configuración entre los nuevos nodos. **`Cassandra`** ofrece herramientas propias para ello.
> 
> Para garantizar una **baja probabilidad de fallo** y el restablecimiento de los datos en caso de emergencia, **`Apace Cassandra`** cuenta con un **sistema de replicación adecuadamente configurado**. La tolerancia de error se minimiza porque los datos se replican automáticamente entre los nodos. Los nodos averiados se pueden sustituir muy fácilmente. El sistema permanece disponible para consultas en todo momento.