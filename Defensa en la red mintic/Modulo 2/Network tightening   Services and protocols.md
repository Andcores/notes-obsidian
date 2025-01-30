### Network and routing services

Los ciber atacantes usan servicios de red vulnerables para atacar un dispositivo o usarlo como parte del ataque. Estos servicios se verifican mediante un escaner de puertos 
garantizar la proteccion de los puertos y que esten abiertos los que sean necesarios para evitar estas vulnerabilidades 

- DHCP utiliza un servidor para asignar una direccion IP e informacion de configuracion a dispositivos en la red, medidas de seguridad como es snooping DHCP evitan que los servidores DHCP falsos proporcionen direcciones IP a los clientes mediante la validacion de los mensajes de fuentes que no son de confianza.
  * Proteja físicamente el servidor DHCP.
  * Aplique cualquier parche de software.
  * Ubique el servidor DHCP detrás de un firewall.
  * Supervise la actividad de DHCP revisando los registros de DHCP.
  * Mantenga una sólida solución antivirus.
  * Desinstale los servicios y las aplicaciones no utilizados.
  * Cierre los puertos no utilizados.
- DNS (Domain name system) Sistema de nombres de dominio Esto l oque ahce es traudcir al URL en una direccion IP numerica. Estos usualmente son utilizados para denegar los servicios o hacer re direcciones  a sitios web falsos .
  DNSSEC utiliza firma digital para fortalecer la autentiocacion y proteger  contra las amenazas al DNS 
  *  Mantenga actualizado el software del DNS.
  - Evite que la cadena de versión revele información.
  - Separe los servidores DNS internos y externos.
  - Restrinja las transacciones permitidas por dirección IP del cliente.
  - Utilice firmas de transacciones para autenticar las transacciones.
  - Deshabilite o restrinja las transferencias de zona y las actualizaciones dinámicas tanto como sea posible.
  - Habilite el registro y analice los registros.
  - Utilice las extensiones de seguridad del sistema de nombres de dominio (DNSSEC: Domain Name System Security Extensions).
  - Zonas de señalización.
- ICMP Este es usado apra enviar mensajes de erro cuando un servicio solicitado no esta disponible.
  El comando PING es una utilidad que emplea el ICMP para probar disponibilidad de conexion con el host.
  este puede ser usado como DoS , ataques de reconocimiento y de canar encubierto. Muchas redes filtran las solicitudes para evitar ataques ICMP 
*  RIP (Routing Information Protocol)Protocolo que limita el numero de saltos del origen al lugar donde va dirigido en una red.La cantidad maxima de saltos para estos es 15 usado RIP. Se utiliza para intercambiar informacion de routing sobre que redes alcanza cada router y el alcance de dichas redes.
  Los delincuentes peuden atacar a este protocolo afectando el rendimiento y disponibilidad: algunos ataques pueden re diirgir el trafico 
* NTP (Network Time Protocol) Este protocolo sincroniza los sistemas informaticos de la red. Esta es necesaria para la interpretacion correcta de los eventos de los archivos de data Syslog asi como para certificados digitales 

### Telnet, SSH y SCP
**Secure Shell (SSH)** es un protocolo que proporciona una conexión remota segura (cifrada) a un dispositivo. **Telnet** es un protocolo más antiguo que utiliza texto sin formato no seguro al autenticar un dispositivo (nombre de usuario y contraseña) y transmitir datos. Se debería usar SSH en lugar de Telnet para administrar las conexiones, ya que proporciona un cifrado sólido. El SSH utiliza el puerto TCP 22. Telnet utiliza el puerto TCP 23.

**Secure copy (SCP)** transfiere de forma segura archivos entre dos sistemas remotos. SCP utiliza SSH para la transferencia de datos y la autenticación, garantizando la autenticidad y la confidencialidad de los datos en tránsito.

### Safe Protocols 

* SNMP recopila estadísticas de dispositivos TCP/IP para monitorear la red y los equipos informáticos. SNMPv3 es el estándar actual: utiliza la criptografía para evitar las escuchas y asegurarse de que no se hayan manipulado los datos durante el tránsito.
* El protocolo de transferencia de hipertexto (HTTP: Hypertext Transfer Protocol) proporciona conectividad web básica y utiliza el puerto 80. HTTP contiene seguridad integrada limitada y está abierto a la supervisión del tráfico al transmitir contenido, lo que deja la computadora del usuario abierta a ataques. Veamos cómo otros protocolos proporcionan una conexión más segura:
  * Secure Sockets Layer (SSL) administra el cifrado mediante un protocolo de enlace SSL al comienzo de una sesión para proporcionar confidencialidad y evitar escuchas y manipulaciones.
  * Transport Layer Security (TLS) es un sustituto actualizado y más seguro de SSL.
  * SSL/TLS cifra la comunicación entre el cliente y el servidor. Cuando se utiliza, el usuario verá HTTPS en el campo URL de un navegador en lugar de HTTP.
* File Transfer Protocol (FTP) transfiere archivos informáticos entre un cliente y un servidor. En FTP, el cliente utiliza un nombre de usuario y una contraseña en texto plano para conectarse. File Transfer Protocol Secure (FTPS) es más seguro: añade soporte para TLS y SSL para evitar escuchas, manipulaciones y falsificaciones en los mensajes intercambiados.
* El correo electrónico utiliza Post Office Protocol (POP), Internet Message Access Protocol (IMAP) y Multipurpose Internet Mail Extensions (MIME) para adjuntar datos no textuales, como una imagen o un vídeo, a un mensaje de correo electrónico.

Para proteger POP (puerto 110) o IMAP (puerto 143), utilice SSL/TLS para cifrar el correo durante la transmisión. El protocolo Secure/Multipurpose Internet Mail Extensions (S/MIME) proporciona un método seguro de transmisión. Envía mensajes cifrados y firmados digitalmente que proporcionan autenticación, integridad de mensajes y no repudio.
### Protection of the apollo network

![[Pasted image 20250127000735.png]]