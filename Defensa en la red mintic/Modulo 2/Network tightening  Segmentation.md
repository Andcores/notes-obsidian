### Virtual local area networks (VLAN)

![[Pasted image 20250127202415.png]] 
Las Lan Representan conexiones fisicas mientras que las VLAN son virtuales Los puertos de un Switch pueden asignarse como una VLAN especifica.
Se pueden usar otros puertos para interconectar fisicamente los switches y permitir trafico entre varias VLAN, Estos se denominan enlaces troncales.

![[Pasted image 20250127204330.png]]

L:as VLAN permiten segmentar una red basandose en factores como la funciona, el equipo del proyecto o la app.
Estas actúan como si estuvieran en su propia red independiente aunque compartac una infraestructura común con otras VLAN  de la misma LAN.
Básicamente segmenta la red en diferentes redes con la misma infraestructura para proteger la información y datos específicos 

### The Demilitarized Zone (DMZ)

Zona desmilitarizada, una pequeña red entre una red privada confiable e internet

![[Pasted image 20250127210455.png]]

* Acceso a redes no confiables
  Los servidores web y los servidores de correo generalmente se colocan dentro del DMZ, esto se hace para permiter que las personas puedan acceder desde una red no confiable sin comprometer la red interna 
* Zonas de riesgo La mayoria de las redes tienen de 2 a 4 zonas de riesgo: La LAN privada confiable, la DMZ, Internat y una extranet
  * Dentro de la zona LAN el riesgo es bajo y el nivel de confianza es alto
  * dentro de la zona de extranet el nivel de riesgo es medio-bajo y la confianza medio-alto
  * dentro del DMZ el nivel es medio-alto y el nivel de confianza es medio-bajo
  * dentro de la zona de internet el nivel de riesgo es alto y nivel de confianza bajo 
   
  
* Modelo zero Trust
  Los firewalls gestionan el tráfico este-oeste (el tráfico que va entre servidores dentro del centro de datos de la organización) y el tráfico norte-sur (los datos que entran y salen de la red de la organización).
  La red Zero Trust monitorea constantemente a todos los usuarios en la red, independientemente de su estado o función.



![[Pasted image 20250127231056.png]]

![[Pasted image 20250127231557.png]]
