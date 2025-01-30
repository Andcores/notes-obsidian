echo Te da una saldia delñ mensaje que le escribas acontinuacion 
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