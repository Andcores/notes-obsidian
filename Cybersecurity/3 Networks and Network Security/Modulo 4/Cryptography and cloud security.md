## Endurecimiento de seguridad en la nube

Las tecnicas mas comunes son la incorporación de IAM, Hipervisores, lineas de base, Criptografia y borrado criptografico

## Gestion acceso a la identidad (IAM)

Conjunto de procesos y tecnologías que ayudan a las organizaciones a gestionar las identidades digitales de su entorno

## Hipervisores 
Abstrae el hardware del host del entorno del software operativo
Tenemos los hipervisores que se ejecutan en el hardware de la computadora anfitriona. un ejemplo es ESXi de VMware. Hipervisores de tipo 2 Funcionan en el software de la computadora host, un ejemplo es VB. Los CSP suelen utilizar hipervisores del tipo 1. Los CSP son responsables de gestionar el hipervisor y otros componentes de la virtualizacion. El CSP se ocupa de sus actualizaciones y parches  de seguridad. Las vulnerabilidades de estos pueden provocar VM Escapes es un exploit en el que un actor malicioso obtiene acceso al hipervisor principal, potencialmente a la computadora host y otras VM 

## Linea de base 

La linea de base para las redes y operaciones en la nube cubre como se configura y establece el entorno de la nube. Una linea de base es un punto de referencia fijo. Este puede utilizarse para comprar los cambios realizados en un entorno de nube. Una configuración y puesta a punto adecuadas pueden mejorar en gran medida la seguridad y el rendimiento ode un entorno en la nube. Algunos ejemplos de establecimiento de una linea de base es un entorno de nube son :Restringir acceso al portal de administración del entorno de nube, habilitar la gestión de contraseñas, Habilitar la encriptación de archivos y habilitar los servicios de detección de amenazas para las bases de datos en SQL 

## Criptografia en la nube
Esta se utiliza en sis temas de encriptacion y gestion segura de claves para proporcionar integridad y confidencialidad a los datos. Partes claves para garantizar la seguridad de los datos.
La encriptación es el proceso de convertir la información en texto cifrado , que no es legible para nadie sin la clave de encriptación. 

## Borrado criptografico 

El borrado criptografico es borrar la clave de encriptacion de los datos. Cuando se destruyen los datos en la nube, los métodos mas tradicionales de destrucción d datos no son tan eficaces . El borrado criptográfico es una técnica más reciente en la que se destruyen las claves criptográficas utilizadas para la desencriptación de los Datos. Esto hace que los Datos sean indescifrables e impide que nadie pueda desencriptarlos. Al cripto-triturar, todas las copias de la clave deben ser destruidas para que nadie tenga la oportunidad de acceder a los Datos en el futuro.

## Gestión de claves

La encriptación moderna se basa en mantener seguras las claves de encriptación. A continuación se indican las medidas que puede tomar para proteger aún más sus Datos cuando utilice aplicaciones en la nube:

- Módulo de plataforma de confianza (TPM). El TPM es un chip de computadora que puede almacenar de forma segura contraseñas, certificados y claves de encriptación.
    
- Módulo de seguridad de hardware de la nube (CloudHSM). El CloudHSM es un dispositivo informático que proporciona almacenamiento seguro para claves criptográficas y procesa operaciones criptográficas, como la encriptación y la desencriptación.
    

Las organizaciones y los clientes no tienen acceso al proveedor de servicios en la nube (CSP) directamente, pero pueden solicitar auditorías e informes de seguridad poniéndose en contacto con el CSP. Los clientes no suelen tener acceso a las claves de encriptación específicas que los CSP utilizan para encriptar los Datos de los clientes. Sin embargo, casi todos los CSP permiten a los clientes proporcionar sus propias claves de encriptación, dependiendo del servicio al que acceda el cliente. A su vez, el cliente es responsable de sus claves de encriptación y de garantizar la confidencialidad de las mismas. El CSP está limitado en cuanto a cómo puede ayudar al cliente si las claves de éste se ven comprometidas o destruidas. Una ventaja clave del Modelo de responsabilidad compartida es que el cliente no es totalmente responsable del mantenimiento de la infraestructura criptográfica. Las organizaciones pueden evaluar y supervisar el riesgo que implica permitir que el CSP gestione la infraestructura revisando la auditoría y los Controles de seguridad de un CSP. Para los contratistas federales, FEDRAMP proporciona una Lista de CSP verificados.