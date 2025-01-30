Un analizador de protocolo de red, Sniffer o analizador de paquetes, es una herramienta diseñada para capturar y analizar el trafico de datos dentro de una red, algunos de los sniffers mas comunes son:
- Analizador de trafico NetFlow de SolarWinds 
- ManageEngine PoManager
- Observador de redes Azure
- Wireshark
- tcpdump


## TCPdump
Es una analizador de protocolos de red en linea de comandos. Es popular, ligero y utiliza biblioteca de codigo abierto libcap. tcpdump esta basado en texto, osea que los comandos de tcpdump se ejecutan en el terminal, Puede instalarse en otros sistemas operativos basados en Unix.
tcpdump proporciona un breve analisis de paquetes y convierte la información clave sobre el trafico de red en formatos fácil de leer por humanos, Imprime información sobre cada paquete en la terminal. Muestra el Address IP de origen, las Addresses IP de destino y los números de puerto que se están utilizando en las comunicaciones 

**Interpretar la salida**
tcpdump imprime la salida del comando como los paquetes olfateados en la linea de comandos y opcionalmente en un archivo de registro " log ", La salida de una captura de paquete tiene muchas piezas de información importante sobre el tráfico de red.
![[Pasted image 20240903123247.png]]

información recibida
- Marca de tiempo: la salida comienza con la marca de tiempo, formateada como horas ,minutos, segundos y fracciones de segundo.
- IP de origen:el origen del paquete lo proporciona su dirección IP de origen
- Puerto de origen: Este numero de puerto es donde se origino el paquete
- IP destino: La dirección IP de destino es hacia donde se esta transmitiendo el paquete.
- Puerto de destino: Este numero de puerto es hacia donde se esta transmitiendo el paquete.
- **Nota:** Por defecto, tcpdump intentará resolver las direcciones de host a nombres de host. También sustituirá los números de puerto por servicios comúnmente asociados que utilicen estos puertos.

**Usos comunes** se utilizan habitualmente para capturar y visualizar las comunicaciones de red y para recopilar estadisticas sobre la red, como la solucion de problemas de rendimiento de la red. Tambien pueden utilizarse para:
- Establecer una linea de base para los patrones de trafico de red y las métricas de utilización de la red
- Detectar e identificar el trafico malicioso 
- Crear alertas personalizadas para enviar las notificaciones adecuadas cuando surjan problemas en la red o amenazas a la seguridad
- Localizar la mensajeria instantánea (MI), el trafico o los puntos de accesos inalambricos no autolizados.

"*Sin embargo, los atacantes también pueden utilizar los analizadores de protocolos de red de forma maliciosa para obtener información sobre una red específica. Por ejemplo, los atacantes pueden capturar paquetes de datos que contengan información confidencial, como nombres de usuario de cuentas y contraseñas. Como analista de ciberseguridad, es importante comprender la finalidad y los usos de los analizadores de protocolos de red.*"
