## Ataques de fuerza bruta

Un **ataque de fuerza bruta** es un proceso de ensayo y error para descubrir información privada. Existen diferentes tipos de ataques de fuerza bruta que los actores maliciosos utilizan para adivinar contraseñas, entre ellos:

- _Ataques de fuerza bruta simples._ Cuando los atacantes intentan adivinar las credenciales de inicio de sesión de un usuario, se considera un ataque de fuerza bruta simple. Pueden hacerlo introduciendo cualquier combinación de nombres de usuario y contraseñas que se les ocurra hasta encontrar la que funcione.
    
- _Los ataques de diccionario_ utilizan una técnica similar. En los ataques de diccionario, los atacantes utilizan una lista de contraseñas de uso común y credenciales robadas en violaciones anteriores para acceder a un sistema. Se denominan ataques de diccionario porque los atacantes utilizaban originalmente una lista de palabras del diccionario para adivinar las contraseñas, antes de que las reglas de contraseñas complejas se convirtieran en una práctica habitual de Seguridad.
## Evaluar las vulnerabilidades

Antes de que se produzca un ataque de fuerza bruta u otro incidente de ciberseguridad, las empresas pueden realizar una serie de pruebas en su red o en sus aplicaciones web para evaluar las vulnerabilidades. Los analistas pueden utilizar máquinas virtuales y cajas de arena para probar archivos sospechosos, comprobar vulnerabilidades antes de que se produzca un evento o simular un incidente de ciberseguridad.

## VM(Virtual machines)

Las máquinas virtuales (VM) son versiones de software de computadoras físicas, y se utilizan para mejorar la seguridad de una organización al ejecutar código en un entorno aislado. Esto impide que el código malicioso afecte al resto del sistema. Las VM permiten probar software potencialmente dañino y luego eliminarlo sin riesgo para la máquina principal, ya que pueden restaurarse a un estado prístino. Además, son útiles para investigar dispositivos infectados o software malicioso en un entorno controlado.

Sin embargo, las VM presentan algunos riesgos, como la posibilidad de que un programa malicioso escape de la virtualización y acceda al sistema anfitrión. Aun así, permiten probar aplicaciones de manera segura y eficiente, facilitando muchas tareas de seguridad cibernética.

**Espacios aislados**: Estos entornos de pruebas permiten ejecutar software separado de la red, útiles para probar parches, detectar errores y vulnerabilidades. Los espacios aislados, o "cajones de arena", pueden ser máquinas físicas o virtuales, aunque las versiones basadas en la nube suelen ser más económicas. Sin embargo, algunos atacantes programan software malicioso para detectar si se ejecuta en una VM o entorno de caja de arena, comportándose como inofensivo en estos casos.

## Medidas de prevención

Algunas medidas comunes que las organizaciones utilizan para evitar que se produzcan ataques de fuerza bruta y ataques similares incluyen:

- **Salting y hash:** El hash convierte la información en un valor único que puede utilizarse para determinar su integridad. Es una función unidireccional, lo que significa que es imposible desencriptar y obtener el texto original. El salting añade caracteres aleatorios a las contraseñas hash. Esto aumenta la Longitud y la complejidad de los valores hash, haciéndolos más seguros.

- **Autenticación de múltiples factores (MFA) y autenticación de dos factores (2FA):** MFA es una medida de seguridad que requiere que un usuario verifique su identidad de dos o más formas para acceder a un sistema o red. Esta autenticación se realiza mediante una combinación de factores de autenticación: un nombre de usuario y una contraseña, huellas dactilares, reconocimiento facial o una contraseña de un solo uso (OTP) enviada a un número de teléfono o a un correo electrónico. la 2FA es similar a la MFA, salvo que sólo utiliza dos formas de verificación.

- **CAPTCHA y reCAPTCHA:** CAPTCHA son las siglas de Completely Automated Public Turing test to tell Computers and Humans Apart (Prueba de Turing pública completamente automatizada para distinguir entre ordenadores y humanos). Pide a los usuarios que completen una sencilla prueba que demuestra que son humanos. Esto ayuda a evitar que el software intente forzar una contraseña. reCAPTCHA es un servicio CAPTCHA gratuito de Google que ayuda a proteger los sitios web de bots y software malicioso.

- **Políticas de contraseñas:** Las organizaciones utilizan políticas de contraseñas para estandarizar las buenas prácticas de contraseñas en toda la empresa. Las políticas pueden incluir directrices sobre lo compleja que debe ser una contraseña, la frecuencia con la que los usuarios deben actualizar las contraseñas, si las contraseñas se pueden reutilizar o no, y si hay límites en el número de veces que un usuario puede intentar iniciar sesión antes de que se suspenda su cuenta.