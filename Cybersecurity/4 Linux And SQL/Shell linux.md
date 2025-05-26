echo Te da una salida del mensaje que le escribas a continuacion 
expr
clear
## Commandos Linux ##
**find -name,-iname,-mtime -x** 

" find /home/analyst/projects "se busca todo lo que comienza en el directorio projects.


find /home/analyst/projects -name " * log * ". También podrías ingresar find /home/analyst/projects -iname "*log*".
name, no se devolverán los archivos con nombres que incluyan Log o LOG,
Sin embargo, sí se devolverán si la opción es -iname.
al ingresar find /home/analyst/projects -mtime -3, se devuelven todos los archivos y directorios del directorio projects que han sido modificados en los últimos tres días.

**grep** 
si ingresas "grep OS updates.txt", obtendrás todas las líneas que contienen OS en el archivo updates.txt.

pipe(placa)= ( " | ")
Por ejemplo, "ls /home/analyst/reports | grep users "devuelve los nombres de archivos y directorios en el directorio reports que contienen la palabra users
![[Pasted image 20240917115704.png]]
Aqui se uso "ls " para listar los archivos usamos pipe para concatenar el otro comando de grep y listar los archivos que tuvieran Q1 es su nombre
![[Pasted image 20240917115827.png]]
Se realizo basicamente lo mismo solo que colocando la palabras " access" para hacer la busqueda
![[Pasted image 20240917120235.png]]
Aqui capturamos un texto en el cual aplicamos un filtrado diferente en el primero buscamos a quienes estaban en recusos humanos, en el segundo a quien se llamaba jhill
