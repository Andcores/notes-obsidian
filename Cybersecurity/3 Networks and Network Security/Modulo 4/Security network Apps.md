![[Pasted image 20240905215837.png]]
## Firewall [[Networks]]
La mayoría de los firewalls son similares en sus funciones básicas. Los firewalls permiten o bloquean el trafico basándose en un conjunto de reglas. Cuando los paquetes de datos entran en una red , se inspecciona el encabezado de paquete y se permite o deniega en función de su numero de puerto. Los NGFW tambien puede inspeccionar la carga util de los paquetes . Cada sistema debe tener su propio firewall, Independientemente del cortafuegos de la red
![[Pasted image 20240905220727.png]]
## Intrusions detection system  (IDS)
Es una aplicación que monitorea la actividad del sistema y alerta sobre posibles intrusiones. Un IDS alerta a los administradores basándose en la firma del trafico malicioso 

El IDS esta configurado para detectar ataques conocidos. Los sistemas IDS suelen olfatear los paquetes de datos mientras se desplazan por la red y los analizan en busca de las características de ataques conocidos.
Algunos sistemas IDS no solo revisan en busca de firmas de ataques conocidos, si no también de anomalías que podrían ser el signo de una actividad maliciosa. Cuando el IDS descubre una anomalía , envía una alerta al administrador de la red, que puede investigar mas a fondo .
Las limitaciones de los sistemas IDS es que solo pueden buscar ataques conocidos o anomalías evidentes. Los ataques nuevos y sofisticados no pueden ser detectados. La otra limitación es que el IDS no detiene realmente el trafico entrante si detecta algo raro. depende del administrador de la red detectar la actividad maliciosa antes de que cause algún daño a la red .
![[Pasted image 20240905221558.png]]

Cuando se combina un IDS con un firewall es otra capa de defensa. El IDS se coloca detrás del firewall y antes de entrar en la red LAN , lo que permite al IDS analizar los flujos de datos después de que el trafico de red no permitido por el firewall haya sido filtrado 

## Intrusions Prevention system (IPS )
Un sistema de prevención de intrusiones es una app que monitorea la actividad de intrusiones y toma medidas para detenerlas. Ofrece incluido mas protección que un IDS porque detiene activamente las Anomalías cuando las detecta, a diferencia del IDS que simplemente informa de la anomalía un administrador de red.
![[Pasted image 20240905222406.png]]
El IPS (como un IDS) Se sitúa detrás del firewall en la arquitectura de red. Esto ofrece un alto nivel de seguridad porque los flujos de datos arriesgados se interrumpen incluso antes de lleguen a las partes sensibles de la red, Sin embargo , una limitation potencial es que esta en linea, Si se rompe, Se interrumpe la conexión entre la red privada e internet. Otra limitación de los IPS es la posibilidad de que se produzcan falsos positivos, lo que puede hacer que se interrumpa el trafico legitimo

## Dispositivos de captura de paquetes completos

Los dispositivos de captura de paquetes completos pueden ser increíblemente útiles para los administradores de redes y los profesionales de la Seguridad. Estos dispositivos le permiten registrar y analizar todos los Datos que se transmiten a través de su red. También ayudan a investigar las alertas creadas por un IDS.

## System Intrusion Event management [[LOGs and SIEM tools]]
Es una app que recopila y analiza los datos de registro para supervisar las actividades criticas de una organización. Las herramientas SIEM trabajan en tiempo real para supervisar las actividades criticas de una organizacion. Las herramientas SIEM analizan ademas de los datos de registro de red procedentes de IDS, IPS, Firewall, VPN, proxies y registros DNS. Las herramientas SIEM son una forma de agregar los datos de los eventos de seguridad para que aparezcan todos en un mismo lugar y puedan ser analizados por los analistas de seguridad. esto se conoce como un panel unico de cristal

![[Pasted image 20240905223429.png]]
Panel de control SIEM de  Chronicle herramienta nativa de la nube diseñada para retener, analizar y buscar datos 

**Splunk** es otra herramienta SIEM común. Splunk ofrece diferentes opciones de herramientas SIEM: Splunk Enterprise y Splunk Cloud. Ambas opciones incluyen cuadros de mando detallados que ayudan a los profesionales de la Seguridad a revisar y analizar los datos de una organización. También hay otras herramientas SIEM similares disponibles, y es importante que los profesionales de la Seguridad investiguen las diferentes herramientas para determinar cuál es la más beneficiosa para la organización.

Una herramienta SIEM no sustituye a los analistas de seguridad ni las actividades de refuerzos de redes y sistemas que se tratan en este curso, pero se utilizan en combinación con otros métodos de seguridad. Los analistas de seguridad suelen trabajar en un centro de operaciones de seguridad (SOC) donde pueden supervisar las actividades ene toda la red. 
 A continuation , se puede utilizar sus conocimientos y experiencias para determinar como responder a la información del cuadro de mandos y decidir cuando los eventos cumplen los criterios para ser escalados a supervision 
 ![[Pasted image 20240905224501.png]]