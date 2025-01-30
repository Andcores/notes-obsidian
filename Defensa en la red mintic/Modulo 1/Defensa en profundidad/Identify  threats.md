Las empresas deben emplear una defensa profunda para identificar amenazas y asegurad activos vulnerables.

![[Pasted image 20250103005637.png]]
La ilustración de esta diapositiva muestra una topología simple de un enfoque de defensa en profundidad.

- **Router de borde -** La primera línea de defensa se conoce como router de borde (R1 en la figura). El router perimetral tiene un conjunto de reglas que especifica el tráfico autorizado y denegado, y pasa por el firewall todas las conexiones destinadas a la red LAN interna.
- **Firewall -** La segunda línea de defensa es el firewall. El firewall es un dispositivo de control que efectúa un filtrado adicional y rastrea el estado de las conexiones. Deniega el inicio de conexiones desde las redes externas (no confiables) a la red interna (confiable) mientras permite que los usuarios internos establezcan conexiones bidireccionales con las redes no confiables. También puede realizar la autenticación de usuario (proxy de autenticación) para otorgarles a los usuarios remotos externos acceso a recursos de la red interna.
- **Router interno -** Otra línea de defensa es el router interno (R2 en la imagen). Puede aplicar las reglas de filtrado finales en el tráfico antes de que se reenvíe a su destino.