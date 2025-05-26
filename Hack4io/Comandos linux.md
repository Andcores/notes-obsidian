
which ----> me muestra si existe // command -v 
whoami-->me dice quien soy  
cat---> me captura lo que necesito 
| ----> pipe este es un comando para conectar comandos 
grep ---> filtro para buscar algo en especifico 
![[Pasted image 20240909132928.png]]
manda los errores a un tip ode agujero negro  o lo que queramos mandar
![[Pasted image 20240909133016.png]]
En este caso es la manera cómoda de mandar a  el agujero negro los commandos erróneos 
![[Pasted image 20240909133242.png]]
&> esto redirige  a la carpeta . en este caso el comando ejecuta el programa no manda mensaje de ejecutado y se ejecuta en segundo plano por la & al final
![[Pasted image 20240909133510.png]]
disown hace que se quede el programa sin depender de cerrar la consola, el numero de abajo es el proceso en el que se encuentra listado 

Listado de mas comandos mas espesificos ![[Pasted image 20240909133813.png]]


# comandos a buscar y  organizar 
awk - aun no lo entiendo bien: da un filtrado de archivos por cantidad de argumentos cada argumento puede estar separado por un espacio o por una coma"aunque supongo que puede separarse por mas cosas " la cual lo vuelve un vector o matrix en el cual este filtra los archivos según le especificaremos la columna o " argumento " el argumento se podría definir como la posición que ocupa en espacio como un vector pero no iniciando en el espacio 0 si no en el 1
## **Comandos que se deben averiguar mejor su funcionamiento y manera de mejorarlos o combinarlos**
sort organiza de orden alfabético un archivo txt
find busca archivos y se le pueden poner especificaciones
cat captura archivos y se puede usar coin un xargs
du mira el peso de los archivos 
file da detalles de los archivos
xargs comando que recibe una salida para realizar algo de otro comando 
strings = imprime las cadenas legibles de un archivo 
- ssh
- telnet
- nc
- ncat
- socat
- openssl
- s_client
- nmap
- netstatss
- sed
- cut
- tr
- grep
- mktemp -d 