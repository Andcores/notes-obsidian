# Utilice herramientas SIEM para proteger a las organizaciones

Estado: Traducido automáticamente del Inglés

Traducido automáticamente del Inglés

Anteriormente, conoció las herramientas de administración de información y eventos de seguridad (SIEM) y algunos cuadros de mando SIEM. También aprendió sobre las diferentes amenazas, riesgos y vulnerabilidades que puede experimentar una organización. En esta lectura, aprenderá más sobre los datos del panel SIEM y cómo los profesionales de la ciberseguridad utilizan esos datos para identificar una posible amenaza, riesgo o vulnerabilidad.

## Splunk

Splunk ofrece diferentes opciones de herramientas SIEM: Splunk® Enterprise y Splunk® Cloud. Ambas permiten revisar los datos de una organización en cuadros de mando. Esto ayuda a los profesionales de la seguridad a gestionar la infraestructura interna de una organización mediante la recopilación, búsqueda, supervisión y análisis de los datos de registro de múltiples fuentes para obtener una visibilidad completa de las operaciones diarias de una organización.

Revise los siguientes paneles de Splunk y sus propósitos:

### **Panel de postura de seguridad**

El panel de Postura de seguridad está diseñado para los centros de operaciones de seguridad (SOC). Muestra las últimas 24 horas de los eventos y tendencias notables relacionados con la seguridad de una organización y permite a los profesionales de la Seguridad determinar si la infraestructura y las políticas de Seguridad están funcionando según lo diseñado. Los analistas de seguridad pueden utilizar este panel para supervisar e investigar las amenazas potenciales en tiempo real, como la actividad de red sospechosa que se origina desde una dirección IP específica.

### **Panel de resumen ejecutivo**

El panel de resumen ejecutivo analiza y supervisa la salud general de la organización a lo largo del tiempo. Esto ayuda a los Equipos de Seguridad a mejorar las medidas de Seguridad que reducen el Riesgo. Los analistas de Seguridad podrían utilizar este tablero para proporcionar estadísticas de alto nivel a las partes interesadas, como generar un resumen de los incidentes de seguridad y las tendencias durante un período de tiempo específico.

### **Panel de revisión de incidentes**

El cuadro de mandos de revisión de incidentes permite a los analistas identificar los patrones sospechosos que pueden producirse en caso de incidente. Ayuda resaltando los elementos de mayor riesgo que necesitan una revisión inmediata por parte de un analista. Este cuadro de mandos puede ser muy útil porque proporciona una cronología visual de los acontecimientos que conducen a un incidente.

### **Panel de análisis de riesgos**

El tablero de análisis de riesgos ayuda a los analistas a identificar el riesgo para cada objeto de riesgo (por ejemplo, un usuario específico, una computadora o una dirección IP). Muestra los cambios en la actividad o el comportamiento relacionados con el riesgo, como el inicio de sesión de un usuario fuera de las horas normales de trabajo o un tráfico de red inusualmente alto desde una computadora específica. Un analista de Seguridad podría utilizar este panel para analizar el impacto potencial de las vulnerabilidades en los recursos críticos, lo que ayuda a los analistas a priorizar sus esfuerzos de mitigación de riesgos.

## Chronicle

Chronicle es una herramienta SIEM de Google nativa de la nube que retiene, analiza y busca datos de registro para identificar posibles amenazas a la seguridad, riesgos y vulnerabilidades. Chronicle le permite recopilar y analizar datos de registro en función de:

- Un recurso específico

- Un nombre de dominio

- Un usuario

- Una dirección IP


Chronicle proporciona múltiples tableros que ayudan a los analistas a Monitorear los registros de una organización, crear filtros y alertas, y rastrear nombres de dominio sospechosos.

Revise los siguientes tableros de Chronicle y sus propósitos:

### **Panel de estadísticas empresariales**

El panel de información estadística de la empresa destaca las alertas recientes. Identifica nombres de dominio sospechosos en los registros, conocidos como Indicadores de compromiso (IOC). Cada resultado se etiqueta con una puntuación de confianza para indicar la probabilidad de una amenaza. También proporciona un nivel de gravedad que indica la importancia de cada amenaza para la organización. Un analista de seguridad podría utilizar este panel para monitorizar los intentos de inicio de sesión o de acceso a los datos relacionados con un recurso crítico -como una aplicación o un sistema- desde ubicaciones o dispositivos poco habituales.

### **Panel** de ingestión de**datos** y salud

El panel de ingestión de datos y salud muestra el número de registros de eventos, las fuentes de registro y las tasas de éxito de los datos que se están procesando en Chronicle. Un analista de Seguridad podría utilizar este panel para asegurarse de que las fuentes de registro están correctamente configuradas y que los registros se reciben sin errores. Esto ayuda a garantizar que se abordan los problemas relacionados con los registros para que el equipo de Seguridad tenga acceso a los datos de registro que necesita.

### **Cuadro** de mando de **coincidencias** de**COI**

El cuadro de mandos de coincidencias COI indica las principales amenazas, riesgos y vulnerabilidades para la organización. Los profesionales de la Seguridad utilizan este tablero para observar los nombres de dominio, las direcciones IP y los COI de los dispositivos a lo largo del tiempo con el fin de identificar tendencias. Esta información se utiliza después para dirigir el enfoque del equipo de seguridad hacia las amenazas de mayor prioridad. Por ejemplo, los analistas de Seguridad pueden utilizar este panel para buscar actividad adicional asociada a una alerta, como el inicio de sesión de un usuario sospechoso desde una ubicación geográfica inusual.

### **Panel****principal**

El cuadro de mandos principal muestra un resumen de alto nivel de la información relacionada con la actividad de ingestión de datos, alertas y eventos de la organización a lo largo del tiempo. Los profesionales de la Seguridad pueden utilizar este panel para acceder a una cronología de los eventos de seguridad -como un pico de intentos fallidos de inicio de sesión- para identificar las tendencias de las amenazas a través de las fuentes de registro, los dispositivos, las direcciones IP y las ubicaciones físicas.

### **Panel** de**detecciones** de reglas

El panel de detecciones de reglas proporciona estadísticas relacionadas con los incidentes de mayor incidencia, gravedad y detecciones a lo largo del tiempo. Los analistas de Seguridad pueden utilizar este tablero para acceder a una lista de todas las alertas activadas por una regla de detección específica, como una regla diseñada para alertar cada vez que un usuario abre un archivo adjunto malicioso conocido de un correo electrónico. A continuación, los analistas utilizan esas estadísticas para ayudar a gestionar los incidentes recurrentes y establecer tácticas de mitigación para reducir el nivel de riesgo de una organización.

### **Panel** general de inicio**de** sesión de usuario

El cuadro de mandos general del inicio de sesión de los usuarios proporciona información sobre el comportamiento de acceso de los usuarios en toda la organización. Los analistas de Seguridad pueden utilizar este panel para acceder a una Lista de todos los eventos de inicio de sesión de los usuarios para identificar actividades inusuales de los usuarios, como el inicio de sesión de un usuario desde varias ubicaciones al mismo tiempo. A continuación, esta información se utiliza para ayudar a mitigar las amenazas, los riesgos y las vulnerabilidades de las cuentas de usuario y las aplicaciones de la organización.

## Claves

Las herramientas SIEM proporcionan paneles que ayudan a los profesionales de la Seguridad a organizar y centrar sus esfuerzos en materia de Seguridad. Esto es importante porque permite a los analistas reducir el riesgo identificando, analizando y remediando los elementos de mayor prioridad de manera oportuna. Más adelante en el Programa, tendrá la oportunidad de practicar el uso de diversas características y comandos de las herramientas SIEM para realizar consultas de búsqueda.

Marcar como completo

Me gusta

No me gusta

Informar de un problema