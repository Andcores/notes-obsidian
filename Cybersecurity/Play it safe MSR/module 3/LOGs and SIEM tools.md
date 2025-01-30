un log  es un registro  de los eventos que ocurren en el sistema y red de una organizacion. En estos tenemos 3 tripos de log comunes, Firewall logs, network logs, server logs 

**Firewall logs**:
Es un registro de conexiones intentadas o establecidas para el trafico entrante de internet. también las solicitudes salientes a internet dentro de la red

**Network logs**:
Es un registro que todos los ordenadores y dispositivos que entran y salen de una red, conexiones entre dispositivos y servicios de la red

**Server logs**:
son Registros relacionados con los servicios de sitios web, correos electrónicos o archivos compartidos incluyen acciones como solicitudes de inicio de sesión, contraseña y nombre de usuario .

# SIEM tools
Son herramientas que recopila y analiza los datos de registro para monitorear las actividades criticas de una organización. Da visibilidad en tiempo real, monitoreo y análisis de eventos y alertas automatizadas. Almacena igual datos de registro en una ubicación centralizada .\

Estas herramientas deben configurarse y personalizarse para satisfacer necesidades de seguridad únicas de cada organización. Con la evolución de las ciber amenazas deben estar configurarse continuamente estas herramientas para garantizar que las amenazas se detecten y aborden posibles incidentes de seguridad

**Autoalojadas**: es donde la empresa tiene un control fisico sobre los datos de este operando desde su propia infraestructura ideales para mantener el control fisico de datos confidenciales.

**Alojadas en la nube**: Son herramientas que las mantiene y gestiona un proveedor externo a través de internet. Ideales para organizaciones que no quieren invertir en crear y mantener su propia infraestructura.

**Hibrida**:ES una combinacion de estas 2 permite tener las ventajas de estas 2 mantener control fisico de los datos confidenciales y aprovechar las ventajas de la nube.

### Splunk Enterprise, Splunk Cloud y Chronicle

- Splunk es una plataforma de análisis de datos, Splunk Enterprise es una herramienta auto-alojada que se utiliza para retener, analizar y buscar en los datos de registro de una organization
- Splunk Cloud es una herramienta alojada en la nube que se utiliza para recopilar, buscar y supervisar datos de registro, es util para organizaciones con entornos hibridos o solo nube.
- Chronicle de google es una herramienta nativa de la nube para retener, analizar y buscar datos. Ofrece supervision de registros, analisis de datos y recopilacion de datos 