pagina para practicar bash scripting con juegos y consola

https://overthewire.org/wargames/bandit/bandit2.html

## **Recordar Siempre leer las descripciones en la pagina de cada "maquina" a resolver**
# lvl 1-2
![[Pasted image 20240920133029.png]]
Aqui ya sabemos entrar al nivel 0 para leer un archivo 
Sacamos la contraseña para entrar al nivel 1
en el nivel 1 tenemos un archivo llamado "-" como no podemos hacerle un cat directo hacemos "cat ./-" que esto hara que yo puedo capturarlo con su nombre completo


# lvl 2-3
![[Pasted image 20240920133450.png]]
 Este nivel estaba facil era hacerle un cat a un archivo con espacios y solo dándole al tab escribiendo los 2 primeros caracteres el mismo shell lo auto completa

# lvl 3-4
![[Pasted image 20240920133852.png]]
 En este estaba sencillo igual, el archivo estaba en otro directorio pero estaba oculto, lo que hacemos es ir al directorio y luego con "ls -la" o simplemente con "ls -l " listamos los archivos ocultos, nos muestra el nombre y el nombre parece complicado pero haciendo el Cat escribiendo el nombre del archivo completo este nos mostrara su contenido
# lvl 4-5

![[Pasted image 20240920134332.png]]
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

Este estaba algo mas complicado, la instruccion decia que habian archivos y que la contraseña esta vez estaba en un archivo que se pudiera leer por el humano.
cambiamos al directorio donde estaban los archivos, usamos el comando " file " para ver que tenian, al momentos de usar "file ./-* " Esto lo que hizo fue listar todos los archivos que estaban ahi presentes con el inicio de "-" y en el archivo 7 nos dice ASCII text basicamente el que se puede leer

# lvl 5-6

![[Pasted image 20240920140135.png]]

HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
Aqui obtuvimos ayuda de youtube 
![[Pasted image 20240920140300.png]]
Aqui se busco lo que estabamos buscando en este caso el tamaño " size" y como lo podriamos colocar

![[Pasted image 20240920140400.png]]
Aqui tenemos el comando en el mismo manual del comando " find "  nos dice de buscar por permisos 

entonces 
se coloco el comando de "find ." para que busque desde la carpeta en la que nos encontramos 
Luego usamos el "-size 1033c" para buscar el tamaño que era 1033bytes la c es para especificar el tamaño 
por ultimo usamos el  "\! -executable" para buscar un archivo ejecutable con esa informacion se le dio a buscar, casualmente nos dio el archivo y lo miramos con un cat

# LVL 6-7
![[Pasted image 20240920181914.png]]
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
es igual al anterior 
*Recordar buscar siempre manual de los comandos*
lo buscamos con los bites que ocupaba y agregamos las condiciones respectivas de  grupo perteneciente y usuario 
le podriamos concatenar un xargs 


# lvl 7-8 
dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
![[Pasted image 20240920182559.png]]

Para probar le lanzamos un cat y nos arroja muchos archivos,  para buscar hicimos un cat seguido de un grep para filtrar la busqueda segun la palabra dada, este nos arroja donde esta la palabra y en la misma linea esta la contraseña 

# lvl 8-9
![[Pasted image 20240922002013.png]]
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
Aquí usamos sort para ordenar los datos alfabéticamente usamos luego el comando uniq -u para mostrar la unica linea que no se repite " disclamer: estaba viendo mal la pagina estaba viendo el lvl 9-10 y me confundi"

# lvl 9-10

![[Pasted image 20240922002448.png]]
FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey

usamos strings porque le archivo no es legible y pone solo lo legible por el humano, en la condicion nos dice que debemos buscar lo legible y a demas de ello la contraseña se encuentra luego de un =

# lvl 10-11
![[Pasted image 20240922002752.png]]
dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
Aqui nos dice que esta codificado en base 64 y este es un comando, usamos el "base64 --help" para ver que nos decia "se vale usar man base64 o base64 --help este ultimo es un poco mas resumido y con menos detalle"
decodificamos el archivo y nos da la contraseña

# lvl 11-12
![[Pasted image 20240922233518.png]]
7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
Aqui nos dieron una ayuda llamada rot13 que es una codificacion de correr los caracteres 13 posiciones.
En el codigo usamos tr basicamente para traducir que en le 1er argumento pasamos este de decirle de donde a donde se iban a traducir, luego de este colocamos las posiciones, n-z que son los primeros caracteres y luego a-m que son los segundos caracteres completando aso los 26 caracteres del alfabeto 

# lvl 12-13
![[Pasted image 20240924174928.png]]
FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
entramos a la maquina y le lanzamos un cat a data, este tiene archivos diferentes y hexadecimal
luego de esto usamos cat data le añadimos xxd -r que lo que va a hacer es decodificar el hexadecimal y de ahi le añadimos un sponge data que lo que va a hacer es la salida del xxd sea guardado en el mismo archivo y lo reescriba 
se uso el scrip de [[Scrip descompressor]]
que básicamente nos ahorra el tiempo de descomprimir tantos archivos 
comandos usados
7z x = descomprime el archivo
7z l = lista lo que tiene un archivo comprimido 

# lvl 13-14
![[Pasted image 20240926222604.png]]
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
entramos a la maquina listamos con  "ls" para que nos muestre los archivos es una key 
usamos el com,ando ssh -i  seguido de la sshkey para conectarnos a bandit14@localhost " aqui puede ir la IP"
me da error porque no conecte bien el puerto le agregamos el -p 2220 que es como nos conectamos al puerto normalmente
ya de ahi entramos y buscamos en el directorio la contraseña del bandit14

# 14-15
![[Pasted image 20240926231001.png]]
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
usamos el comando "nc" que es netcat el localhost lo cambiamos al puerto 30000, la contraseña de este era la misma contraseña con la cual se accedió al la misma maquina 14
![[Pasted image 20240926232940.png]]
aquí se usa un comando para pasar estas lines que están en hexadecimal a decimal muestra los puertos abiertos en el momento 

# lvl 15-16
![[Pasted image 20240927221200.png]]
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx
Aqui utilizamos ncat  con el argumento ssl 
**Ncat** puede encriptar el tráfico usando SSL. En el modo de conexión, basta con añadir la opción **–ssl**
![[Pasted image 20240927221633.png]]
podemos o usar la IP o en este caso el localhost
la IP la obtuve usando " ifconfig"

# lvl 16-17
EReVavePLFHtFlFsjn3hyzMlvSuSAcRD
![[Pasted image 20241002212429.png]]
"para usar este scrip usamos mktemp -d nos crea un directorio temporal para poder hacer esto y generar archivos en este lugar"
usamos el script [[HostScanScrip]]
En este empezamos analizar los puertos abiertos 
usamos el comando ncat --ssl 127.0.0.1 "XXXXX" 
las x las reemplazamos por los puertos abiertos le metemos la contraseña de este nivel y depende lo que nos de empezamos a colocar la contraseña a ver en donde encontramos algo
damos con una private key que se copio y se coloco en un archivo "id_rsa" y se le copio toda la pass. *Recordar colocarle los permisos 600 a la key o si no dara error*
usamos ssh -i id_rsa bandit17@localhost -p 2220 *se le puede colocar tambien la ip que es 127.0.0.1* 
![[Pasted image 20241002212959.png]]
colocamos todo para acceder y ya estamos dentro 
![[Pasted image 20241002213304.png]]
Ya aquí accedo a las keys del bandit para sacar la key de esta maquina 

# lvl 17-18
