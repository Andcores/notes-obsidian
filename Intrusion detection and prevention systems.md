Estos son medidas de seguridad implementados en una red para detectar y prevenir actividades maliciosas 

# IDS
![[Pasted image 20250129161019.png]]

Puede ser un dispositivo de red dedicado o una de varias herramientas de un servidor, firewall o incluso un sistema operativo de computadora host, que escanea datos contra una base de datos, reglas o firmas de ataques en busca de un trafico malicioso 
Si se detecta una coincidencia , el IDS registrara la deteccion y creara una alerta para un administrador de red. No tomara medidas y por lo tanto no evitara que ocurran ataques, el IDS solo avisa registra y genera informes, Esto hace que ralentice el sistema cuando el IDS analiza, para evitar esto , se colocan fuera de la red, separado del trafico normal
estos datos son copiados y enviados a al IDS para que estos luego hagan la deteccion sin conexion 
# IPS
![[Pasted image 20250129161028.png]]
Un IPS bloquea o detecta el trafico segun una regla positiva o una coincidencia de firma. Uno de los IPS/IDS mas conocido es *Snort* . La version comercial de snort es Sourcefire de Cisco. Sourcefire Tiene la capacidad de hacer y realizar un analisis de trafico y puertos en tiempo real, registrar buscar y comprar contenido: detecta Sondas de ataques y escaneos de puertos, También se integra con otras herramientas de terceros para informes, Rendimiento y analisis de registros .
