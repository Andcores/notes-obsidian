# PKI(Public key infrastructure) framework

Proporciona un framework para proteger el intercambio de informacion en linea utilizando una combinación de cifrado y certificados 
- Utiliza cifrado asimétrico, que implica claves publicas y privadas, para permitir un intercambio seguro de la informacion en linea, mientras que la clave publica puede ser compartida la clave privada permanece secreta, para asegurar que el destinatario es el único que puede descifrar el mensaje 
- El Cifrado simétrico usa una clave única para cifrar y descifrar datos, lo que lo hace mas rápido que le cifrado asimétrico pero mas vulnerabre a las brechas de seguridad 

## Establecimiento de confianza con los certificados 
Los certificados digitales verifican la identidad de los titulares de claves publicas, abordando la vulnerabilidad de compartir claves en el cifrado simétrico y asimétrico.
Actúan como verificadores digitales asegurando la autenticidad y permitiendo a los ordenadores establecer confianza para una comunicación segura 
las CA(autoridades de certificación) tienen el papel de la emisión y verificación de certificados digitales, estableciendo una cadena de confianza que ayuda  a garantizar la legitimidad de las entidades implicadas en el intercambio de informacion 


### **Algoritmos simétricos**

- _Triple DES (3DES)_ se conoce como un algoritmo de cifrado por bloques por la forma en que convierte el texto plano en texto cifrado en "bloques" Sus orígenes se remontan al Data Encryption Standard (DES), desarrollado a principios de la década de 1970. DES fue uno de los primeros algoritmos de encriptación simétrica que generaba claves de 64 bits. Un **bit** es la unidad más pequeña de medida de datos en una computadora. Como podrá imaginar, Triple DES genera claves de 192 bits, es decir, tres veces más largas. A pesar de que las claves son más largas, muchas organizaciones están dejando de utilizar Triple DES debido a las limitaciones en la cantidad de datos que pueden encriptarse. Sin embargo, es probable que Triple DES siga utilizándose por motivos de retrocompatibilidad.

- _Estándar de encriptación avanzada (AES_) es uno de los algoritmos simétricos más seguros de la actualidad. AES genera claves de 128, 192 o 256 bits. Se considera que las claves criptográficas de este tamaño están a salvo de ataques de fuerza bruta. Se calcula que forzar por la fuerza bruta una clave AES de 128 bits podría llevarle a una computadora moderna ¡miles de millones de años!


### **Algoritmos asimétricos**

- _Rivest Shamir Adleman (RSA_) recibe el nombre de sus tres creadores, que lo desarrollaron mientras estaban en el Instituto Tecnológico de Massachusetts (MIT). RSA es uno de los primeros algoritmos de criptografía asimétrica que produce un par de claves pública y privada. Los algoritmos asimétricos como el RSA producen longitudes de la clave aún más largas. En parte, esto se debe al hecho de que estas funciones crean dos claves. Los tamaños de la clave RSA son de 1.024, 2.048 o 4.096 bits. El RSA se utiliza principalmente para proteger datos altamente sensibles.

- _Algoritmo de firma digital (DSA_) es un algoritmo asimétrico estándar que fue introducido por el NIST a principios de la década de 1990. DSA también genera longitudes de la clave de 2.048 bits. Este algoritmo se utiliza mucho hoy en día como complemento de RSA en infraestructuras de clave pública.