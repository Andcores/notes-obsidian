## Threats for key industry sectors

Los ciberataques como Stuxnet demostraron la vulnerabilidad de la infraestructura crítica controlada por sistemas SCADA en sectores como manufactura, energía y comunicaciones. Estos ataques pueden causar interrupciones operativas, riesgos de seguridad, daño a la reputación y pérdidas financieras. Para prevenirlos, se deben realizar evaluaciones de riesgos, implementar planes de ciberseguridad específicos para ICS, controlar el acceso, segmentar redes, monitorear actividades, tener planes de respuesta a incidentes, capacitar empleados y mantener los sistemas actualizados.

Los ciberataques como Stuxnet demostraron la vulnerabilidad de la infraestructura crítica controlada por sistemas SCADA en sectores como manufactura, energía y comunicaciones. Estos ataques pueden causar interrupciones operativas, riesgos de seguridad, daño a la reputación y pérdidas financieras. Para prevenirlos, se deben realizar evaluaciones de riesgos, implementar planes de ciberseguridad específicos para ICS, controlar el acceso, segmentar redes, monitorear actividades, tener planes de respuesta a incidentes, capacitar empleados y mantener los sistemas actualizados.

## The rise of the Internet of Things
El Internet de las Cosas (IoT) conecta miles de millones de dispositivos a internet, transformando el comercio y el consumo. Al permitir el acceso remoto, aumenta los puntos de entrada a las redes y la cantidad de datos a proteger, impulsando el crecimiento del 'Big Data'. La proliferación de dispositivos IoT amplía la superficie de ataque cibernético, como se evidenció en ataques DDoS. Es crucial asegurar estos dispositivos, permitiendo actualizaciones de firmware inalámbricas y cambiando las credenciales predeterminadas.

## Embedded Systems 
Los sistemas embebidos son sistemas electrónicos que se encuentran dentro de otros dispositivos y se encargan de tomar información (capturar), guardarla (almacenar) y utilizarla cuando es necesario (acceder). Debido a que se usan en muchísimos aparatos tanto para empresas como para personas, presentan problemas de seguridad especiales que hay que tener en cuenta.

**Ejemplos:**

- **Televisores inteligentes:** Capturan información sobre los canales que ves, almacenan tus preferencias y acceden a internet para mostrarte contenido.
- **Sistemas de control de HVAC (calefacción, ventilación y aire acondicionado):** Capturan la temperatura ambiente, almacenan la temperatura deseada y acceden a los mecanismos para regularla.
- **Dispositivos médicos (como monitores de ritmo cardíaco):** Capturan las señales del cuerpo, almacenan los datos del paciente y acceden a ellos para mostrarlos o enviar alertas.
- **Automóviles modernos:** Capturan información de los sensores (velocidad, presión de neumáticos), almacenan configuraciones del conductor y acceden a los sistemas para controlar el motor o los frenos.

Los ataques a sistemas embebidos se aprovechan de los fallos de seguridad que existen tanto en el software como en el hardware que los componen. Un tipo de ataque es el de "sincronización", donde los atacantes estudian cuánto tiempo tarda el sistema en responder a diferentes acciones para así encontrar sus puntos débiles. Este tipo de ataque se llama de "canal lateral" porque no ataca directamente el software, sino que se basa en la información que se puede obtener de cómo funciona el sistema, como el tiempo de respuesta, el consumo de energía, las ondas electromagnéticas que emite o incluso el sonido que produce.

**Ejemplos de cómo se podría usar un ataque de sincronización:**

- **Cerradura electrónica:** Un atacante podría intentar diferentes combinaciones de una clave y medir el tiempo que tarda la cerradura en indicar si la combinación es incorrecta. Si una parte de la clave correcta hace que la respuesta tarde un poco más, podría ser una pista para descifrar la clave completa.
Una forma de construir sistemas embebidos es utilizando la tecnología "System on Chip" (SoC). Un SoC es como una mini computadora muy pequeña, como las Raspberry Pi o Arduino. Estas pequeñas computadoras se pueden crear usando un tipo de chip llamado FPGA, que tiene la particularidad de poder ser reprogramado incluso después de que el dispositivo ya está funcionando.

Estos dispositivos SoC son potentes a pesar de su tamaño reducido, lo que significa que consumen menos energía, son más baratos y funcionan mejor que los componentes grandes tradicionales. Un SoC junta en un solo chip el cerebro del sistema (microcontrolador o microprocesador), la capacidad de ejecutar programas (como Windows, Linux o Android) y otros elementos necesarios como la tarjeta gráfica (GPU) o la conexión Wi-Fi.

Sin embargo, muchos de estos dispositivos SoC tienen problemas de seguridad, como una autenticación débil o la dificultad para actualizarlos y corregir fallos. Debido a cómo se utilizan estos dispositivos, a menudo se confía en ellos sin una revisión de seguridad formal.

**Ejemplos para entenderlo mejor:**

- **Raspberry Pi como un centro multimedia:** Una Raspberry Pi (un ejemplo de SoC) puede usarse como un pequeño computador para reproducir videos y música en un televisor inteligente. Tiene la potencia para ejecutar un sistema operativo y conectarse a internet a través de su módulo Wi-Fi integrado.

## Internet of Things 

El uso de dispositivos y sensores inteligentes está creciendo muy rápidamente en el mundo de la tecnología. Este sector es conocido principalmente como el Internet de las Cosas (IoT). Tanto empresas como personas utilizan dispositivos de IoT para hacer tareas automáticamente, vigilar las condiciones de su alrededor y recibir avisos sobre problemas. La mayoría de estos dispositivos se conectan a internet de forma inalámbrica e incluyen cosas como cámaras, cerraduras, sensores de movimiento, luces y otros sensores que recogen información sobre el ambiente o cómo está funcionando un aparato. Algunos fabricantes incluso usan sensores de IoT para avisar cuándo hay que cambiar piezas, si algo está fallando o si se están acabando los suministros.

**Ejemplos para entenderlo mejor:**

- **Automatización del hogar:** Un sistema de luces inteligentes (IoT) puede encenderse al detectar movimiento (sensor de proximidad) y apagarse a una hora determinada, todo automáticamente. Una cerradura de puerta inteligente (IoT) permite abrirla y cerrarla remotamente desde un teléfono.
- **Supervisión ambiental en una fábrica:** Sensores de IoT pueden medir la temperatura y la humedad en diferentes áreas de una fábrica y alertar si los niveles no son los adecuados para la producción.

Las empresas utilizan dispositivos de IoT para rastrear inventarios, vehículos y personal. Estos dispositivos suelen tener sensores de ubicación (geoespaciales), lo que permite a los usuarios localizar, monitorear y controlar a nivel global factores del entorno como la temperatura, la humedad y la luz. Las aplicaciones de IoT a menudo utilizan un "sistema operativo en tiempo real" (RTOS), que es un sistema operativo pequeño diseñado para realizar tareas rápidamente y con precisión en el tiempo, en lugar de enfocarse en el rendimiento general. Los RTOS se encuentran en muchos dispositivos, como los portátiles, los médicos, los sistemas de vehículos y los dispositivos de automatización del hogar.

El sector del IoT presenta un gran desafío para los expertos en seguridad informática, ya que muchos dispositivos de IoT recopilan y envían información privada. Los problemas de seguridad relacionados con los RTOS incluyen ataques como la inyección de código, los ataques de denegación de servicio (que hacen que el sistema deje de funcionar) y la inversión de prioridad (donde una tarea importante se retrasa por una menos importante).

**Ejemplos para entenderlo mejor:**

- **Seguimiento de flotas de vehículos:** Una empresa de logística podría usar dispositivos IoT con GPS en sus camiones para saber dónde están en todo momento, controlar la temperatura de la carga refrigerada y recibir alertas si un vehículo se desvía de su ruta.
## VoIP teams

**¿Qué equipo necesita?**

Necesita una conexión a Internet y un teléfono para VoIP. Varias opciones están disponibles para los equipos de teléfono:

- Un teléfono tradicional con un adaptador (el adaptador actúa como interfaz de hardware entre el teléfono analógico tradicional y la línea de VoIP digital).
- Un teléfono habilitado para VoIP.
- Software de VoIP instalado en una computadora.
- 
**¿Es segura la VoIP?**

La mayoría de los servicios de VoIP para consumidores utiliza Internet para las llamadas telefónicas. Muchas organizaciones, sin embargo, utilizan sus redes privadas debido a que proporcionan una seguridad más sólida y un servicio de calidad. La seguridad de VoIP es tan confiable como la seguridad de red subyacente. Los ciberdelincuentes atacan estos sistemas para obtener acceso a servicios telefónicos gratuitos, para espiar las llamadas telefónicas o para afectar al rendimiento y la disponibilidad.

**¿Cómo puede proteger su servicio de VoIP?**

Implemente las siguientes contramedidas para proteger la VoIP:

- Cifre los paquetes de mensajes de voz para protegerlos de las infiltraciones.
- Utilice el SSH para proteger los gateways y switches.
- Cambie las contraseñas predeterminadas.
- Utilice un sistema de detección de intrusiones para detectar ataques, como el envenenamiento del ARP.
- Utilice una autenticación fuerte para mitigar la suplantación de registro (los ciberdelincuentes enrutan todas las llamadas entrantes para la víctima hacia ellos mismos), la suplantación de proxy (engañando a la víctima para que se comunique a través de un proxy falso creado por los ciberdelincuentes) y el secuestro de llamadas (interceptando y redirigiendo las llamadas a una ruta diferente antes de llegar a su destino).
- Implemente firewalls que reconozcan la VoIP para monitorear las transmisiones y filtrar las señales anormales.
## Deception Technologies 
Las empresas utilizan "tecnologías de engaño" como una estrategia para confundir y desviar a los atacantes que intentan infiltrarse en sus redes principales (de producción). Estas tecnologías también sirven para estudiar las tácticas que utilizan los atacantes y para recibir alertas tempranas sobre posibles ataques dirigidos a la red real. En esencia, el engaño crea una capa falsa en la infraestructura de la organización.

### Honeypot 
Un "honeypot" es un sistema trampa que se configura para parecer un servidor real dentro de la red de una organización. Se deja vulnerable a propósito para atraer a los atacantes. Cuando un atacante intenta interactuar con el honeypot, todas sus acciones se registran y se vigilan para analizarlas después. El objetivo principal del honeypot es distraer al atacante de los recursos reales y valiosos de la red de la organización.

Además de los honeypots individuales, una organización puede crear una "honeynet", que es una colección de varios honeypots diseñados para imitar toda su red. Esto proporciona una imagen más realista para el atacante y permite observar sus movimientos en un entorno controlado.

Por otro lado, los "honeyfiles" son archivos falsos que se colocan estratégicamente para atraer a los atacantes, pero que no contienen ninguna información real de valor. Si un atacante intenta acceder a estos archivos, se genera una alerta.

**Honeynet simulando la red de una sucursal:** Una empresa con varias oficinas podría crear una red falsa que imite la estructura de una de sus sucursales. Si un atacante logra entrar en esta honeynet, la empresa puede observar cómo se mueve entre los diferentes "servidores" y "estaciones de trabajo" simulados, aprendiendo sobre sus tácticas sin poner en riesgo la red real de ninguna de sus sucursales.

### DNS sinkhole

Un "DNS sinkhole" es una herramienta de seguridad que impide que los nombres de los sitios web (nombres de host) se traduzcan a sus direcciones IP correspondientes para ciertas URLs específicas. Al hacer esto, evita que los usuarios accedan a recursos maliciosos en internet.

n **DNS sinkhole** interfiere con este proceso para ciertas direcciones web que se consideran peligrosas. En lugar de devolver la dirección IP real del sitio malicioso, el DNS sinkhole puede hacer una de estas cosas:

- **No devolver ninguna dirección IP:** Esto hace que el navegador no pueda encontrar el servidor y muestre un error.
- **Devolver una dirección IP falsa:** Esta dirección IP podría llevar al usuario a un servidor controlado por la organización, donde se le informa que el sitio al que intentaba acceder es peligroso, o simplemente a una página en blanco. 