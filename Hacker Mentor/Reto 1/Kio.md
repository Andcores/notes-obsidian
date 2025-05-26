Nombre: Andres Felipe Garcia Romero 
correo: andcore.20@gmail.com
# Identificación de la maquina
Para empezar montamos la maquina a vulnerar KIO
Al momento de montar la maquina lanzamos el comando "ifconfig"
![[Pasted image 20241016144415.png]]
Aqui puedo conocer mi IP gracias a que mi PC esta conectado a internet por WiFi la interface usada es wlp4s0.(Se recomienda familiarizarse con el comando "ip" y sus banderillas que se podria decir que es el reemplazo de "ifconfig")
Proseguimos haciendo el siguiente comando:
"arp-scan -l " nos arroja las IP y MAC de las maquinas
![[Pasted image 20241016150158.png]]
Aquí veo que,el comando se esta se esta ejecutando en la interfaz principal de mi PC la que esta siendo usada, no encuentro el MAC de la maquina, que tengo montada y es porque en mi PC la interfaz de red usada por Vmware es diferente a la local
como ya se cual es la dirección MAC de mi maquina KIO pero no la veo ahí use el comando "ip -brief addr" que me va a listar todas las interfaces de red con su IP 
![[Pasted image 20241016150019.png]]
Luego de averiguar un poco de como se distribuyen las interfaces de red en Vmware logro comprender que vmnet8 es la interfaz de red a la que debo mandarle el arp

Con el comando "sudo arp-scan --interface=vmnet8 --localnet" hago el escaneo 
![[Pasted image 20241016150855.png]]
Y encuentro 2 MAC les hago un ping para ver cual IP me responde y encuentro cual es la maquina KIO.
como uso el entorno que usa el creador de contenido "s4vitar" mi polybar esta configurada de esta manera: 
![[Pasted image 20241016151356.png]]
donde puedo visualizar mi IP y colocar la IP objetivo en ella con un comando
el siguiente paso es usar nmap para poder escanear los puertos abiertos 
usaremos el siguiente comando (se ejecutan con permisos de root, recomendable quedarse en SU)
# Búsqueda de puertos abiertos
"nmap -p- -sS 172.16.12.128 -oA allports -v"
- -p- : esta banderilla lo que hará es escanear todos los puertos
- -sS: esta banderilla (steal scan) se podría decir que es un saludo de 2 pasos hacia la IP que le coloquemos nos dará la información 
- -oA: nos mandara la información en todos los formatos con un nombre que especificaremos 
- -v: Verbose lo que hace es que nos permite es ver información de lo que esta pasando mientras el comando se esta ejecutando 

![[Pasted image 20241016152904.png]]
Con los puertos abiertos identificados lanzaremos el siguiente comando 
"nmap -p22,80,111,139,443,1024 -sV -v 172.16.12.128 -oA services"
- p22,80,111,139,443,1024: esta banderilla apunta directamente a estos puertos que ya verificamos que estan abiertos 
- sV: esta banderilla buscara servicios y versiones
- -oA: nos mandara la información en todos los formatos con un nombre que especificaremos 
- -v: Verbose lo que hace es que nos permite es ver información de lo que esta pasando mientras el comando se esta ejecutando 

![[Pasted image 20241016154038.png]]

Encontramos de manera mas especifica puertos abiertos y sus versiones de los servicios en los que se encuentran 

Nos faltaria encontrar que version tiene Samba, y usamos metasploit, lo abrimos en una termina y luego colocamos el siguiente comando 
![[Pasted image 20241017113211.png]]
"search smb version"
esto nos arrojara un resultado con las herramientas que podemos usar
![[Pasted image 20241017113402.png]]
la opcion 9 es la que necesitamos usar para encontrar la version del smb
colocamos "use 9" para acceder a esta 
![[Pasted image 20241017113519.png]]
colocamos "options" para mirar que opciones tenemos 
necesitamos colocar la IP objetivo entonces usamos 
set rhost "172.16.12.128" para dejar la IP objetivo y verificamos que esta bien usando de nuevo "options"
![[Pasted image 20241017113934.png]]
verificamos que la IP esta bien y ejecutamos con el comando "run"
![[Pasted image 20241017114032.png]]
Identificamos el sistema y la version de samba ya con esto tenemos mas informacion para buscar vulnerabilidades 
# Búsqueda de vulnerabilidades

## Búsqueda de directorios a los cuales se es posible acceder
![[Pasted image 20241017105843.png]]
"gobuster dir -u http://172.16.12.128 -w /usr/share/dirbuster/wordlists/directory-list-2.3-medium.txt -t 200 "
El comando usado nos ayuda a buscar directorios a los cuales podríamos acceder desde la URL 
- dir : este activa el escaneo de directorios de gobuster, ya que este tiene mas opciones de escaneo
- -u: En esta banderilla colocamos la URL objetivo, que en este caso se coloco la dirección IP
- -w: aqui colocaremos la ruta de donde esta nuestro directorio y usamos uno de tamaño medio
- -t: esto nos dejara especificar el numero de hilos concurrentes(threats)
  "Tener en cuenta y cuidado, un numero de hilos alto hará el procedimiento mas rápido pero puede sobrecargar el servidor o nuestra propia conexión". 

Con estos directorios podemos mirar la pagina y diferentes carpetas si encontramos informacion importante o si el código fuente tiene algo que nos pueda ayudar 
# Búsqueda de Exploits 

## searchsploit
En mi caso use "searchsploit" para buscar que podríamos hacer y cuales usar

1. searchsploit apache 1.3.20 ![[Pasted image 20241017112338.png]]
Lo buscamos apache 1.3.20 pero no encontramos resultados relacionados pero encontramos exploits de "mod_ssl 2.8.7" que es de version mas alta de la que tenemos que en este caso es "mod_ssl 2.8.4"
2. searchsploit samba 2.2 | grep unix
![[Pasted image 20241017112837.png]]
Aquí uso este comando y lo filtro con grep para ver específicamente los resultados de unix ya que anteriormente habíamos visto que se usaba unix 

## Ejecución exploit 
### Samba
Ejecutamos el metasploit
![[Pasted image 20241017142225.png]]
vamos a buscar el exploit en metasploit del samba, en este caso se llama trans2open
"search trans2open"
![[Pasted image 20241017140401.png]]
Vemos los resultados y el que necesitamos es la opción 1 ya que específicamente es para Linux.
"use 1"
Entramos al exploit y observamos sus opciones
![[Pasted image 20241017141339.png]]
En rhost podemos ver la IP que deseamos atacar, colocamos la IP  a la cual se desea atacar con el siguiente comando 
"set rhost 172.16.12.128" (En este caso esta es la IP que deseo atacar), Cuando este este configurado podremos iniciar el ataque.
Este es un ataque tipo reverse shell.
Reverse shell es hacer que nuestro objetivo se conecte a nuestra maquina por consola.

Iniciamos el ataque
![[Pasted image 20241017141708.png]]
Después de un tiempo estamos dentro como usuarios root
usamos el comando "id" para ver que usuario somos (también se puede usar el comando "whoami" )

"find / -iname bandera*"
Con este comando quería buscar los archivos en este caso las banderas
![[Pasted image 20241017141727.png]]
- find /: Esto me permitirá hacer una búsqueda desde la raíz
- -iname: Este me buscara específicamente los archivos con el nombre especifico .
- bandera* : Aquí especifique el nombre del archivo y el " asterisco " lo que hace es buscarme todos los archivos que empiecen con el nombre "bandera" y lo que le pueda seguir
encontramos la ubicación de las banderas, ya luego capturaremos lo que tienen estas

"cat /home/john/bandera1.txt && cat /root/bandera2.txt && cat /home/harold/bandera3.txt"
Aquí capturaremos el contenido de todas las banderas al tiempo 
![[Pasted image 20241017141904.png]]
- cat /home/john/bandera1.txt : esto me mostrara el contenido del archivo que le especifique, en este caso le di la ruta completa y el nombre del archivo del que necesito el contenido
- &&: Este comando me permite concatenar otro comando con la condición de Si solo Si el comando anterior fue exitoso 

Bandera1: 684d0624c19cac22a44a8413795368b9
Bandera2: c9b2db2dbe3d8e65485c6c348785a760
Bandera3: 9699a2a93f0d7eeb172dca2de51d3db2




