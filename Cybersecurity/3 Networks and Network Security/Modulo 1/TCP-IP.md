# Modelo TCP/IP
Transmission Control Protocol/ Internet Protocol 
modelo estándar usado para la comunicación en red 
Este es un framework usado para visualizar como se organizan y trasmiten los datos a través de la red. esto ayuda a conceptualizar los proceso en la red y a comunicar donde se producen las interrupciones o amenazas. 

## TCP
Protocolo de de comunicación de internet que permite a dos dispositivos formar una conexión y trasmitir datos. El protocolo incluye un conjunto de instrucciones parta organizar los datos de forma que puedan enviarse a través de la red. establece conexión con 2 dispositivos y se asegura que los paquetes lleguen al destinatario apropiado.

Conjunto de estándares usados para enrutar y direccionar paquetes de datos a medida que viajan entre dispositivos en una red. en este esta la dirección IP que funciona como una dirección para cada red privada 

Dentro de cada OS de un dispositivo de red un puerto es una ubicación basada en software que organiza el envió y recepción de datos entre dispositivos de una red. los puertos dividen el trafico de red en segmentos basados en servicio que realizaran entre 2 dispositivos. las computadoras que envían y reciben estos segmentos de datos saben como priorizar y procesar estos segmentos basándose en su numero de puerto.
puertos comunes :
25- Correo electrónico
443- comunicación segura de internet
20 trasferencias de archivos de gran tamaño 

El modelo TCP/IP Es un framework que se utiliza para visualizar como se organizan y trasmiten los modelos a través de la red. este tiene 4 capas 
- Capa de acceso a la red
- Capa de internet
- Capa de trasporte
- Capa de application 
Esto ayuda a protegerse y vigilar contra los riesgos

**Capa de Acceso  a la red:**
Se ocupa de la creación de paquetes de datos y su trasmisión a través de una red

Capa de vinculo de datos. Esta capa corresponde al hardware implicado en la transmisión de la red. Switch, Modems, cableado ARP (Address resolution protocol) hace parte de esta capa. Como MAC se utiliza para identificar host de la misma red física, ARP es necesario para asignar direcciones IP a direcciones MAC para la comunicación de red local.

**Capa de internet:**
Aquí se adjuntas las direcciones IP a los paquetes de datos para indicar la ubicación del emisor y receptor, el como se conectan las redes entre si. Ejemplo Los pack tienen información que determina si se queda en LAN o se enviaran a una red remota como internet.

También denominada capa de red, se responsabilizar de la entrega al host de destino, potencialmente este reside en una red diferente, Esta también  determina que protocolo es responsable de entregar los paquetes de datos y garantiza la entrega al host del destino
protocolos comunes :
- IP: Envía paquetes al destino correcto y se basa en el protocolo de control de trasmision/ Protocolo de datagramas de usuario TCP/USP para entregarlos al servicio correspondiente. Los paquetes IP permiten la comunicación entre 2 redes. . El TCP , particular retransmite cualquier dato que se pierda o este corrupto
- ICMP(Internet Control Message Protocol) Este comparte información sobre errores de red. el ICMP Trasmite información sobre paquetes perdidos o desaparecidos en transito, problemas de conectividad en al red y paquetes redirigidos a otros routers.

**Capa de trasporte:**
Incluye protocolos para controlar el flujo del trafico a través de una red, estos protocolos permiten o deniegan la comunicación  con otros dispositivos e incluyen información sobre el estado de la conexión. Esta capa incluye control de errores, que garantiza que los datos fluyan sin problema por la red .
TCP Y UDP con los protocolos de trasporte que maneja esta capa 
- transmission control protocol(TCP) Permite que 2 dispositivos formen una conexión y trasmitan datos Garantiza que los datos se transmitan de manera fiable al servicio de destino. TCP contiene un numero de puerto de servicio de destino previsto, que reside en el encabezado TCP de un paquete TCP/IP
- User Data-grams protocol (UDP) es un protocolo sin conexion que no estable una conexión entre dispositivos antes de las trasmisiones. Lo utilizan apps que no les preocupa la fiabilidad de la trasmisión. Se utiliza sobre todo en apps sensibles al rendimiento que funciona en tiempo real como al trasmisión de un video

**Capa de aplicación:**
Los protocolos determinan como los paquetes de datos interactuan con los receptores. Las funciones incluyen la trasferencia de archivos y los servicios de correo electrónico
La capa de aplicación en el modelo TCP/IP es similar a las capas de aplicacion, presentación y sesión del modelo OSI, Es la responsable de realizar solicitudes a la red o de responder a las peticiones. Esta capa define a que servicios y aplicaciones de internet puede acceder cualquier usuario, Los protocolos de la capa de aplicacion determinan como interactuan los paquetes de datos con los dispositivos receptores 

- Protocolo de transferencia de hipertexto (HTTP)
- Protocolo simple de transmisión de correo (SMTP)
- Secure Shell (SSH)
- Protocolo de transferencia de archivos (FTP)
- Sistema de nombres de dominio (DNS)

![[Pasted image 20240824000213.png]]
![[Pasted image 20240824000416.png]]



[[Networks]]