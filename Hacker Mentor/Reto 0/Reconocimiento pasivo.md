Nombre: Andres Felipe Garcia Romero
correo: andcore.20@gmail.com

Subir en un documento PDF las 3 respuestas de las siguientes actividades:  
  
1.- Estás realizando un Ethical Hacking a la empresa Toyota sucursal Alemania, se presume que hubo una filtración de datos indexada en BreachParse, serás capaz de encontrar la contraseña de correo del usuario administrador Rainer Luecke? El dominio es "toyota.de"  
  
2.- Analizando los logs del sistema se ha detectado una intrusión pero están incompletos conocemos parte de su email hacker-root_ _ _ @live.cn, podrías encontrar la contraseña del hacker?  
  
  
3.- Elon Musk debido los cambios en las políticas de EEUU ha decidido instalar un servicio VPN para su empresa TESLA (tesla.com), en Japón, serás capaz de encontrar el nombre y dirección IP del servidor?


## Solución 1 
![[Pasted image 20241009011226.png]]

Para la solución de este punto lo primero que hice fue la función para para los procesos en medio del script con las teclas "Ctrl + c " mostrando un mensaje que esta saliendo y dando una salida = 1 que le dirá al sistema que el resultado fue error

### Asignación variable pass
luego para el comando asigne la variable "pass" con las siguientes especificaciones

**grep -RE "luecke@toyota.de"**
Aquí estaremos haciendo una búsqueda de patrones, la bandera -R nos dice que hará la búsqueda de manera recursiva "Buscando en sub-carpetas" , la bandera -E nos permite la búsqueda de expresiones regulares de la siguiente cadena de caracteres "luecke@toyota.de", lo que hará que todo lo que cualquier texto que involucre estas condiciones lo buscara

**2>/dev/null**
Esto lo que hara es que algun mensaje de error no sea mostrado

**awk -F':' '{print $NF}'**
En este comando se realiza un filtro para que la respuesta encontrada muestre lo que va a estar después de " : "  '{print $NF}' lo que me imprime es el ultimo campo luego de los dos puntos " : "

**head -n 1**

Este comando lo agregue para que solo me mostrara la primera linea del archivo ya que si lo colocaba sin este me mostraba mas información innecesaria 
### Asignación comando mail 
En la asignación de variable de  $mail se repite el mismo proceso anterior básicamente igual se diferencia en la parte del awk

**awk -F':' '{print $2}'**

este comando se encarga de imprimir el segundo campo encontrado luego de los dos puntos " : "

### if else 
Para finalizar usamos un condicional 

**if [ -n "$mail" ]; then
 echo "La contraseña es: $pass"
 echo "El correo es: $mail"
else
echo "No se encontro un archivo "
fi** 

**if *[ -n "$mail"]***
En esta parte la bandera de -n verifica que la cadena no este vacía osea  $mail>0 
Si la cadena no esta vacía esta lo que mandara sera un mensaje que diga **"El correo es: $mail"** en $mail es actualmente el resultado del comando que filtramos y **La contraseña es: $pass** que el $pass es el otro resultado filtrado
si la cadena esta vacía directamente se dirige al **else echo "no se encontró un archivo"**

Luego de ejecutar el script en donde estamos ubicados en el directorio BreachCompilation tenemos directamente el script, el resultado que nos da es la contraseña y el correo:
![[Pasted image 20241009012610.png]]


## Solución 2

![[Pasted image 20241009000228.png]]


Para la solución de este punto lo primero que hice fue la función para para los procesos en medio del script con las teclas "Ctrl + c " mostrando un mensaje que esta saliendo y dando una salida = 1 que le dirá al sistema que el resultado fue error

luego para el comando asigne la variable "pass" con las siguientes especificaciones

**grep -Re "hacker-root...@live.cn"**
Aquí estaremos haciendo una búsqueda de patrones, la bandera -R nos dice que hará la búsqueda de manera recursiva "Buscando en sub-carpetas" , la bandera -e nos permite la búsqueda de expresiones regulares de la siguiente cadena de caracteres "hacker-root...@live.cn", buscara las coincidencias con la cadena y en los tres puntos los buscara por caracteres que encuentre ejemplo: hacker-root123,hacker-rootrot,hacker-root456 etc.
**2>/dev/null**
Este comando se encarga de no mostrar algún mensaje de error.

**awk -F':' '{print $NF}'**
Con la adición de este comando con el pipe " | " lo que sucede es awk-F ':' se realiza un filtro para que la respuesta encontrada mostrara lo que va a estar después de " : "  '{print $NF}' lo que me imprime es el ultimo campo que es lo que busco, la contraseña.

**head -n 1**

Este comando lo agregue para que solo me mostrara la primera linea del archivo ya que si lo colocaba sin este me mostraba mas información innecesaria 

por ultimo use un condicional if else

**if *[ -n "$pass"  ]*; them
echo " la contraseña es: $pass"
else 
echo "no se encontró un archivo"
fi** 

**if *[ -n "pass"]***
En esta parte la bandera de -n verifica que la cadena no este vacía osea  $pass>0 
Si la cadena no esta vacía esta l oque mandara sera un mensaje que diga **" la contraseña es: $pass"** en $pass es actualmente el resultado del comando que filtramos
si la cadena esta vacía directamente se dirige al **else echo "no se encontró un archivo"**

Luego de ejecutar el script en donde estamos ubicados en el directorio BreachCompilation tenemos directamente el script, el resultado que nos da es la contraseña ![[Pasted image 20241009004037.png]]

## Solución 3
![[Pasted image 20241009124618.png]]
![[Pasted image 20241009124604.png]]
Para este punto use 2 herramientas vistas en las clases :
- https://dnsdumpster.com/ 
- https://www.iplocation.net/ip-lookup
Lo primero que hice fue en dnsdumpster busque a tesla.com para buscar esta información, luego encontré una IP que me daba su ubicación y decía "Japan", en esa misma linea se encuentra al principio el nombre del servidor que es "apacvpn1" , a continuación use iplocation para buscar el lugar donde se encontraba esta IP y verificar si era correcto esto, y me salieron los resultados de su ubicación 