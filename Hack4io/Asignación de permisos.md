
## Permisos 

DRWX/RWX/RWX
user/ group/others

chmod u+(RX)--->Agrega permisos a user de lectura y ejecucion
chmod g+x, g-r ---> Agrega permisos de ejecucion retira permisos de lectura 
D= directorio

chmod +t = de nadie podra borrar nada sin los permisos del usuario 
### En octal permisos

RWX
421
Ejemplo: Asignación de permisos 
DR-X-----X
501

# Permisos especiales
SUID / SGID

SUID  ---> permite ejecutar el programa durante un tiempo como el propietario

witch python3.9 | xargs ls -l
Concatena otro comando en la ruta donde estoy buscando

chmod u+s /usr/bin/python3.9  Le agrega "s" en la x


2> /dev/null ----> dirige los errores al null que se podria decir que es un hoyo negro 
find / -type f -perm 4000 2>/dev/null
![[Pasted image 20240913212039.png]]
listando viendo que el python se puede ejecutar  como el usuario y el usuario en este caso es root, lo que permite hacer cosas como root

Aqui se uso los comandos de 
import os
os.setuid(0) = 0 es el root y dice que me establezca en el root 
manda la respuesta "0" Que significa que fue ejecutado el comando 


![[Pasted image 20240913214053.png]]

os.system("bash")
me da una terminal bash o puedo buscar otras terminales como zsh y ejecutar comandos como terminal 

![[Pasted image 20240913214323.png]]
SGID es lo mismo pero hacia el grupo en vez de el usuario 


## Esto se hace con sudo


chown --> cambia el dueño del archivo / directorio 
chown pepe:pepe pepe/  --->Asigna a pepe como grupo, dueño al directorio pepe

groupadd <Agregar nombre>

usermod -a -G Alumnos pepe  ---> Modifica a pepe agregandolo al grupo de alumnos

chgroup Alumnos prueba ---> A prueba le asigna el grupo de alumnos 

useradd pepe -s /bin/bash -d /home/pepe ---> Creamos el usuario pepe, le asignamos la Shell bash , y su directorio es pepe ubicado en /home/pepe

 esto se hace con sudo 

passwd ---> cambia la contraseña de los usuarios 


