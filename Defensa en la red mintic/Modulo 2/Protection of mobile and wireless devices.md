# Protection of wireless devices
El primer protocolo de seguridad fue WEP (Wired Equivalent Privacity), este fue reemplazado por WPA (Wi-Fi Protected Access)

* Wi-Fi Protected Access (WPA) fue la respuesta del sector informático a las debilidades del estándar WEP. WPA-PSK (Pre-Shared Key) es la configuración más común de WPA. Las claves utilizadas por el WPA son de 256 bits, un aumento significativo respecto de las claves de 64 y 128 bits empleadas por el sistema de WEP.
* WPA Mejoro los Protocolos, proporcionó controles de integridad de mensajes (MIC) que podían detectar si un atacante había capturado y alterado los datos que pasaban entre el punto de acceso inalámbrico y un cliente inalámbrico. Protocolo de integridad de la clave temporal (TKIP). El estándar TKIP mejoró la capacidad para manejar, proteger y modificar las claves de cifrado. Advanced Encryption Standard (AES) reemplazó a TKIP para una mejor protección de la administración y cifrado de claves.
* El estándar Wi-Fi Protected Access II (WPA2) fue publicado en 2006. Esto introdujo el uso obligatorio de los algoritmos AES y sustituyó el TKIP por el modo de contracifrado con el protocolo de código de autenticación de mensajes en cadena de bloques (CCMP).
* WPA3 agregó más funciones a WPA2, como mantener algoritmos criptográficos sólidos y mejorar el intercambio de claves.
* Wi-Fi Protected Setup (WPS) se puede utilizar para configurar una red doméstica inalámbrica segura. Se utiliza un código PIN para conectar los dispositivos a la red inalámbrica. Sin embargo, WPS plantea una vulnerabilidad de seguridad importante, ya que el PIN del usuario puede detectarse mediante un ataque de fuerza bruta. Debido a esto, WPS no debería utilizarse y debería deshabilitarse por completo.

# Authentication 

La mejor manera de proteger una red inalámbrica es utilizar la autenticación y el cifrado. El estándar inalámbrico original (801.11) introdujo dos tipos de autenticación.

* Autenticación Abierta: Cualquier dispositivo inalambrico puede conectarse a l;a red inalambríca. Use este método en situaciones donde la seguridad no sea un problema 
* Autenticación con clave compartida: Proporciona mecanismos para autenticar y cifrar datos entre un cliente inalambrico y un punto de acceso o router inalambrico 

# Authentication Protocols

El protocolo de autenticación extensible (EAP: Extensible Authentication Protocol) es un marco de autenticación utilizado en redes inalámbricas.

1. El usuario solicita conectarse a la red inalámbrica a través de un punto de acceso.
2. El punto de acceso le solicita al usuario los datos de identificación (nombre de usuario) que luego se envían a un servidor de autenticación.
3. El servidor de autenticación solicita pruebas de que la ID es válida.
4. El punto de acceso le solicita al usuario pruebas de que la ID es válida , en forma de contraseña.
5. El usuario le proporciona al punto de acceso su contraseña. El punto de acceso envía esto de vuelta al servidor de autenticación.
6. El servidor confirma que el nombre de usuario y la contraseña son correctos y pasa esta información al punto de acceso y al usuario.
7. El usuario se conecta a la red inalámbrica.

## Protocolos EAP 
### EAP-TLS
Requiere certificado de cliente: Sí  
Requiere certificado de servidor: Sí  
Fácil de implementar: Difícil  
Seguridad: Alta

### PEAP 
Requiere certificado de cliente: No  
Requiere certificado de servidor: Sí  
Fácil de implementar: Moderado  
Seguridad: Media

### EAP-TTLS
Requiere certificado de cliente: No  
Requiere certificado de servidor: Sí  
Fácil de implementar: Moderado  
Seguridad: Media

### EAP-FAST
Requiere certificado de cliente: No  
Requiere certificado de servidor: No  
Fácil de implementar: Fácil  
Seguridad: Media

# Mutual authentication
![[Pasted image 20250207221021.png]]
Su red inalámbrica y sus datos confidenciales son susceptibles de acceso no autorizado por parte de hackers, ¿qué puede hacer para evitar un ataque?

## Punto de acceso no autorizado
El punto de acceso no autorizado suele imitar a un punto de acceso autorizado, permitiendo a los usuarios conectarse a la red inalámbrica, pero pudiendo robar sus datos o realizar otras actividades nefastas en el proceso.
## Prevencion de ataques
La autenticación mutua es una autenticación bidireccional que puede evitar puntos de acceso no autorizados. Es un proceso en el que ambas entidades en un enlace de comunicaciones se autentican entre sí antes de conectarse. Esto permite a los clientes detectar puntos de acceso no autorizados y evitar estos ataques MitM.

# Methods of communication
Wio
