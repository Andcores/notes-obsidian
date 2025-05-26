![[Pasted image 20240924212324.png]]

Este scrip puede ser usado para el futuro

en la primera parte tenemos una funcion de ctrl c para parar los procesos cuando este esta demasiado cargado con estos

En las siguiente parte definimos que " data.gz" el archivo que descomprimimos con "xxd" su nombre sera 
first_file_name
luego de esto mistraremos la infomacion del archivo a descomprimir 
decompressed_file_name = "$(7z l data.gz | tail -n 3 | head n 1 | awk 'NF(print $NF)')"
Aqui declaramos que el archivo con el nombre que estamos buscando desde la cola las ultimas tres filas luego la primera fila de esta y por ultimo, el ultimo argumento de este 

luego tenemos :7z x $first_file_name &>/dev/null
Este lo que hara es la salida que muestre no se mostrara 

entramos en un bucle while donde la condición empieza por " decompressed_file_name"
y este mostrare el mensaje del archivo descomprimido 
luego se volverá a descomprimir pero esta vez usando el condicional del bucle  y mos mensajes no serán vistos 
luego el nuevo reasignaremos cual es el decompressed_file_name de la misma manera y este se repetira

Básicamente funciona porque este detectara que decompressed_file_name sera un archivo que se pueda descomprimir, asi hasta descomprimir todo lo que se pueda descomprimir hasta llegar al punto donde el archivo no esta mas descomprimido y para el bucle 
![[Pasted image 20240926201224.png]]

Este que hicimos esta corregido
separamos los espacios de los corchetes del while ya que si los dejamos pegados los lee como un comando y se le agrego " -n " lo que hace es verificar que la cadena sea mayor a 0 o que la variable no esta vacía
el simbolo "$" tiene diferentes funciones
- como ejecutar un comando 
-Llamar a una variable
