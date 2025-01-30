Un protocolo es un conjunto de reglas utilizadas por  o mas dispositivos de una red para describir el orden de entrega y la estructura de los datos. Los protocolos de red funcionan como instrucciones que acompañan a la información del paquete de datos.

En los protocolos tenemos 3 categorías principales, Aunque existen muchísimas mas, estas 3 es importantes conocerlas a diferencia de las otras :
## Protocolo de comunicación
Estos rigen el intercambio de información en la trasmisión por red. Dictan com ose trasmiten los datos enter dispositivos y el momento de la comunicación. También incluyen métodos para recuperar datos perdidos.

**TPC**   [[TCP-IP]]
Protocolo que permite que 2 dispositivos formen una conexion y transmitan datos. TPC utiliza un proceso de protocolo de enlace de 3 vias 
- Envia una solicitud de sincronizacion (SYN) A un servidor
- Luego este responde con un paquete SYN/ACK Para acusar recibo de la solicitud del dispositivo  
- Cuando el servidor recibe el ultimo paquete ACK del dispositivo, se establece una conexión TCP. En el modelo TPC/IP el TCP se produce en la capa de trasporte 
**Protocolo de datagramas de usuario (UDP)**
Un protocolo no orientado a la conexión que no establece una conexión entre dispositivos antes de una transmisión. Esto hace que sea menos segura que el TCP. Un uso de UDP es para enviar solicitudes DNS a servidores DNS locales.
Este se da en la capa de trasporte 

**protocolo de trasferencia de hipertexto(HTTP)**
Este protocolo se da en la capa de aplicación
Proporciona un metodo de comunicacion entre clientes y servidores web. HTTP utilizan el puerto. HTTP Se considera inseguro, esta siendo sustituido por algunos sitios we por HTTPS que utiliza la encriptacion SSL/TLS para la comunicacion.

**Sistema de nombres de dominio (DNS)**
Traduce los nombres de dominio de internet en direcciones IP. Cuando una persona quiere acceder al dominio de un sitio web, se envia una consulta a un servidor DNS dedicado. Este busca la dirección  IP que corresponde al sitio web. DNS utiliza normalmente UDP en el puerto 53. Pero si la solicitud es grande pasara a usar el protocolo TCP . El DNS se produce en la capa de aplicación 


## Protocolos de  gestion
Se utilizan para supervizar y gestionar la actividad en una red. incluyen protocolos para la notificación de errores y optimizacion del rendimiento en la red.

**Protocolo simple de administracion de red (SNMP)**
utilizado para gestionar y supervisar los dispositivos de una red. SNMP puede restablecer una contraseña en un dispositivo de red o cambiar su configuración base. Puede enviar solicitudes a los dispositivos de la red para  obtener un informe sobre la cantidad de ancho de banda de la red que se esta utilizando.
Se produce en la capa de aplicación

**Protocolo de mensajes de control de internet (ICMP)**
Protocolo de internet utilizado por los dispositivos para informarse mutuamente sobre errores de trasmisión de datos a través de la red. El ICMP es utilizado por un dispositivo receptor para enviar un informe  al dispositivo emisor sobre la trasmision de datos.Se utiliza normalmente como una forma rápida de solucionar problemas de conectividad y latencia de red mediante la emision del comando PING en un OS linux
este se produce en la capa de internet

## Protocolo de seguridad
Protocolos de red garantizan que los datos se envian y reciben de forma segura a través de la red, estos utilizan algoritmos de encriptacion para protefer los datos en transito.

**Protocolo seguro de trasferencia de hipertexto (HTTPS)**
Protocolo seguro que proporciona comunicacion entre clientes y servidores de sitios web. Este es la version segura de HTTP utiliza la encriptacion secure sockets layer/transport layer security (SSL/TLS) En todas las transmisiones para evitar amenazas. HTTPS utiliza el puerto 443 
Se produce en la capa de aplicación 

**Protocolo seguro de transferencia de archivos  (SFTP)**
Protocolo utilizado para enviar datos de un dispositivo a otro a través de una red. SFTP utiliza SSH (secure Shell) normalmente a través del puerto TCP 22 utiliza el Estandar de encriptacion AES y otros tipos de encriptacion para garantizar  que los destinatarios no deseados no puedan interceptar las transmisiones. Este se utiliza a menudo con el almacenamiento en la nube.
se produce en la capa de aplicacion 

| Direcciones IP privadas                                                                                                                                                                                                                                                                | Direcciones IP publicas                                                                                                                                                                                                                                                                                                                                                                                                       |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| - Asignadas por el router<br>    <br>- Únicas sólo dentro de la red privada<br>    <br>- Sin coste de uso<br>    <br>- Rangos de direcciones:<br>    <br>    - 10.0.0.0-10.255.255.255<br>        <br>    - 172.16.0.0-172.31.255.255<br>        <br>    - 192.168.0.0-192.168.255.255 | - Asignada por ISP e IANA<br>    <br>- Dirección Única en Internet global<br>    <br>- Costos de arrendamiento de una dirección IP pública<br>    <br>- Rangos de direcciones asignables:<br>    <br>    - 1.0.0.0-9.255.255.255<br>        <br>    - 11.0.0.0-126.255.255.255<br>        <br>    - 128.0.0.0-172.15.255.255<br>        <br>    - 172.32.0.0-192.167.255.255<br>        <br>    - 192.169.0.0-233.255.255.255 |

## protocolos adicionales 


 **DHCP (Protocolo de Configuración Dinámica de Host):** Este protocolo ayuda a los dispositivos en una red a obtener automáticamente una dirección IP y otra información importante como la dirección del servidor DNS y la puerta de enlace predeterminada. Funciona con el router para asignar direcciones IP únicas a cada dispositivo. Los servidores DHCP usan el puerto UDP 67, y los clientes DHCP el puerto UDP 68.
   
 **ARP (Protocolo de Resolución de Direcciones):** ARP traduce las direcciones IP a direcciones MAC dentro de la misma red. Cada dispositivo tiene una dirección MAC única que no cambia, mientras que la IP puede variar. ARP mantiene un registro de estas traducciones en un caché, pero no tiene un número de puerto específico ya que opera en la capa de acceso a la red.
   
 **Telnet:** Es un protocolo que permite conectarse a sistemas remotos usando texto claro. Utiliza la línea de comandos y el puerto TCP 23. Aunque es útil, no es seguro porque no cifra la información.
   
 **SSH (Secure Shell):** SSH ofrece una conexión segura a sistemas remotos mediante cifrado y autenticación. Usa el puerto TCP 22 y es más seguro que Telnet.
   
 **POP (Protocolo de Oficina de Correos):** Se usa para descargar correos electrónicos desde un servidor. POP3 es la versión más común y usa los puertos TCP/UDP 110 para correos no cifrados y TCP/UDP 995 con cifrado SSL/TLS. El correo se descarga al dispositivo local y puede no estar disponible en otros dispositivos.
   
 **IMAP (Protocolo de Acceso a Mensajes de Internet):** Permite acceder al correo electrónico sin tener que descargarlo completamente. Mantiene los correos en el servidor, lo que facilita la sincronización entre múltiples dispositivos. Usa los puertos TCP 143 para correos no cifrados y TCP 993 para correos cifrados.
   
 **SMTP (Protocolo Simple de Transmisión de Correo):** Este protocolo se encarga de enviar correos electrónicos desde el remitente hasta el destinatario. Usa el puerto TCP/UDP 25 para correos no cifrados y TCP/UDP 587 con TLS para correos cifrados. Ayuda a gestionar y filtrar el spam.
   
 **Protocolos y Puertos:** Los números de puerto ayudan a los dispositivos de red a manejar la información. Los firewalls pueden filtrar el tráfico en función de estos puertos. Es importante conocer estos protocolos y puertos si trabajas en seguridad informática, ya que son clave en la administración de redes y en entrevistas de trabajo.




