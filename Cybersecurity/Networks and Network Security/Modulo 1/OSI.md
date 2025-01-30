El modelo OSI es un concepto estandarizado que describe las 7 capas que utilizan los ordenadores para comunicarse y enviar datos a travez de la red. los profesionales de las redes y la seguridad suelen utilizar este modelo para comunicarse entre si sobre las posibles fuentes de problemas o amenazas a la seguridad cuando se producen 
![[Pasted image 20240825002744.png]]

## Capa 7 capa de aplicación

Este tiene proceso que implican directamente al usuario cotidiano. Esta capa tiene los protocoles de redes que las app de software utilizan para conectar a un usuario a internet. La conexión del usuario a internet a través de aplicaciones y solicitudes 

## Capa 6: Capa de presentación 

Esta capa implica la traduccion y encriptacion de datos para la red. Esta capa añade y sustituye datos por formatos que puedan ser entendidos por las apps (capa 7)tanto en los emisiones como receptores. Estos procesos requieren el uso de un formato estandarizado.

## Capa 5: Capa de Sesión
Una sesion describe como se conectan 2 dispositivos. Los protocoles de la capa de sesion mantienen la sesion abierta mientras se trasfieren los datos y la termina una vez finalizada la trasmision.
Esta es tambien se encarga de la autentificacion, reconexion y establecimiento de puntos de control durante una trasferencia de datos, Esto permite reanudar la sesion si se pierde conexion. Estos  responden a las solicitudes de servicio de los procesos de la capa de presentación(capa 6) y envian solicitudes de servicios a la capa de trasporte

## Capa 4: Capa de trasporte 
Hace la entrega de datos entre dispositivos, velocidad de trasferencia, flujo de trasferencia y segmentar los datos mas pequeños para facilitar su trasferencia. Estos segmentos se deben re ensamblarse en su destino para que pueda ser procesados por la capa 5. La velocidad y el ritmod e la trasmision debe coincidir con la velocidad de conexion del sistema destino. TCP y UDP son protocoles de capa 4

## Capa 3: Capa de red

Superviza larecepcion de tramas desde la capa 2 y las entrega al destino. Este puede encontrarse basandose en la direccionque residen en la trama de los paquetes. Estos paquetes incluyen IP que indican a los routers donde enviarlos. 

## Capa 2: Capa de vinculo de datos

organiza el envio y recepcion de paquetes dentro de una misma red. En esta se encuentran Switches LAN y tarjetas de interfaz de red de dispositivos LAN 

En esta capa se utilizan protocolos de control de red (NCP)Network  Connection Protocol En control de enlace de datos de alto nivel (HDLC)y protocolo de control de enlace de datos sincrono (SDLC) 

## Capa 1: Capa fisica
Este es el hardware 


