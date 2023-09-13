-------------
- Tags: #definicion #herramienta #cron #administrador #tareas #comandos #linux 
----------------------------
# Definición

> Es un administrador de tareas de Linux que permite ejecutar comandos en un momento determinado, por ejemplo cada día. Si queremos trabajar con cron, podemos hacerlo a través del comando **crontab**. 
> 
> El formato de configuración de cron es el siguiente: **Minuto** - **Hora** - **Día del Mes** - **Mes** - **Día de la semana** - **Comando a ejecutar**

El intervalo de tiempo se especifica mediante 5 campos que representan, de izquierda a derecha:

| Hora | 0-59 |
| :--- | :----:|
| Minuto | 0-23 |
| Día del Mes | 1-31 |
| Mes | 1-12 |
| Día de la semana | 1-6 (0-7) |
 
Si quisiéramos especificar todos los valores posibles de un parámetro podemos usar asterisco. Esto implica que si en lugar de un número utilizamos un asterisco, el comando indicado se ejecutara cada minuto, hora, día de mes, mes o día de la semana como en el siguiente ejemplo: **`*** /home/users/script.sh`**   

| * | Cualquier valor |
| :--- | :----:|
| ' | Separador de lista de valores |
| - | Valores de rango |
| / | Valores de paso |
| 0-23 | Valores permitidos |
| * /2 | Se lee cada dos minutos |
