### desarrollo y testeo 
Los software son desarrolados y actualizados en entornos para estos donde son depurados testeados antes de salir a despliegue.
Durante el testeo los desarrolladores buscas el como interactua con un entorno normal, Los QA se encargan de buscar defectos en el software para ahcer mas facil arreglar estos defectos en esta fase

### Entorno preproduccion y produccion

Los entornos preproduccion deben ir de la mano con el entorno de produccion
Al probar en un ambiente preproduccion los desarroladores pueden verificar que el software funciona bajo la configuracion de seguridad requerida.
Luego de que los desarrolladores ejecutan y prueban la seguridad el programa esta listo para desplegar a produccion

### aprovisionamiento y desaprovisionamiento 
El aprovisionamiento es la creacion o actualizacion de software, el desaprovisionamiento es remover este
una organizacion puede usar un software para automatizar esto

# Safety coding techniques
Los desarrolladores tienen diferentes maneras de codificar para cumplir los requisitos de seguridad
1. Normalizacion: Esto es usado en las bases de datos para mantener la integridad de los mismos esta se usa para poder optimizar los datos y reducir la superficie de ataque de algun atacante 
2. Stored procedure: Grupo de instrucciones SQL almacenadas en una base de datos que ejecuta una tarea. Esto disminuye el trafico de red cuando los clientes usan bases ed datos de entrada diferentes.
3. ofuscación y camuflaje: Esto se hace con la intencion de evitar la ingeniería inversa. La ofuscacion oculta datos originales con caracteres o datos aleatorios . el camuflaje sustituye los datos sensibles por datos ficticios realistas 
4. Reutilizacion de codigo: esto se ahce para ahorrar tiempo y costos de desarrollo. Tener cuidado para evitar la introduccion de vulnerabilidades 
5. SDK: Las bibliotecas de 3ros y los kits de desarrollo de software proporcionan un repositorio de codigo util para que el desarrollo de aplicaciones sea mas rapido y barato . Desventaja es que si alguna de estas tiene alguna vulnerabilidad las aplicaciones que usan estos tambien lo son.

# Validation of entry
Controlar el proceso de introduccion de datos es fundamentar para mantener la integridad de estos.  Algunos de los ataques se ejecutan contra una base de datos e insertan datos con formato incorrecto . Haer un SLQI y hacer que una base de datos de mas informacion de la que debe

# Validation rules

Verifica que los datos se incluyan en parametros definidos por el diseñador de la DB. Estas reglas ayudan a garantizar la integridad, la precision y la coherencia de los datos. Los criterios utilizados en una regla de validación incluyen los siguientes:

- Tamaño: Controla la cantidad de caracteres en un elemento de datos
- Formato: Controla que los datos se ajusten a un formato específico
- Coherencia: Controla la coherencia de los códigos en los elementos de datos relacionados
- Rango: Controla que los datos se encuentran dentro de un valor mínimo y un valor máximo
- Dígito de control: Proporciona un cálculo adicional para generar un dígito de control para la detección de errores.

![[Pasted image 20250124213307.png]]
Multiplicar el primer digito del ISBN x10 el segundo x9 y así sucesivamente hasta el 2do digito

1x10 = 10  
5 x9 = 45  
8 x 8 = 64  
7 x 7 = 49  
1 x 6 = 6  
4 x 5 = 20  
3 x 4 = 12  
7 x 3 = 21  
3 x 2 = 6

Se suman todos estos resultados: 233
El digito de control es el numero necesario par que el total se sume a un multiplo de 11 
se suma 233 +9 = 242 y este es un multiplo de 11 

# Integrity controls 

![[Pasted image 20250124213738.png]]

Un control de integridad puede medir la consistencia de los datos en un archivo, imagen o registro, para garantizar que no se hayan da;ado. Este realiza un hash para verificar que los datos permanezcan sin cambio. Un checksum es un ejemplo de una funcion de hash

-  checksum: Los datos trasferidos son convertidos antes en una suma con un valor total, luego quien recibe los datos verifica la suma y debe dar el mismo resultado, de lo contrario en algun punto la informacion fue alterada.
- Funcion HASH: Las funciones de hash comunes incluyen MD5, SHA-1, SHA-256 y SHA-512.Utilizan complejos algoritmos matemáticos para comparar los datos con un valor hash.
- Control de versiones: Se podria dar como ejemplo GIT-HUB esto evita que usuarios autorizados realicen cambios accidentales. Esto tambien hace que 2 usuarios no puedan usuar y/o modificar el mismo archivo al tiempo
- Copias de respaldo: Esto mantiene la integridad de los datos, si los datos se dañan. 
- Autorización: Esto determina quien tiene acceso a los recursos de una empresa segun lo que necesiten. 
# Threat management to applications
Contramedidas 


| Acceso no autorizado a los centrosd e datos , las salas de computadoras y los armarios de cableado | Aplicar  politicas . normas y procedimientos para el personal y los visitantes a fin de garantizar la seguridad de las instalaciones                                                                       |
| -------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Tiempo de inactividad en el servidor                                                               | - Tener un plan te continuidad empresarial para que las aplicaciones criticas tengan disponibilidad de operaciones<br>- Tener un plan de recouperacion tras und esastre para aplicaciones y datos criticos |
| Vulnerabilidades de software del sistema operativo de la red                                       | Tener politicas para abordar actuailizaciones del OS y de las Apps<br>Instalar parches y actualizaciones                                                                                                   |
| acceso no autorizado a los sistemas                                                                | usar autentificacion de varios factores<br>supervicion de archivos de registro"logs"                                                                                                                       |
| Perdida de datos                                                                                   | Implementar estandares de clasificacion de datos <br>implementar procedimientos de copia de respaldo                                                                                                       |
| vulnerabilidad de desarrollo de software                                                           | realizar pruebas de software antes del lanzamiento                                                                                                                                                         |





