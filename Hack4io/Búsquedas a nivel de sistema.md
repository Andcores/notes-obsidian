![[Pasted image 20240917163432.png]]
Aqui usamos find para buscar a nivel de raíz, le colocamos lo que estamos buscando y como no estamos en usuarios root lo que hacemos es mandar los mensajes de error al dev-null, luego me mostrara los archivos
luego de esto aplicamos un pipe con el que concatenamos un comando mas que va a ser xargs para poder listar estos archivos 
![[Pasted image 20240917163819.png]]
Aqui buscamos a nivel de raiz los permisos 4000  y los mensajes de error se mandan al dev-null
