Un hash es un algoritmo que produce un código que no se puede descifrar a diferencia de los algoritmos simétricos y asimétricos
Estas producen un identificador único conocido como valor hash o resumen, se puede utilizar para verificar que los datos no han sido alterados 
**INTEGRIDAD DE LOS DATOS**
Los valores hash se utilizan principalmente como una forma de determinar la integridad de archivos y aplicaciones, Un minimo cambio en la entrada da como resultado un valor hash totalmente diferente lo que ayuda a garantizar que la autenticidad de la informacion no pueda ser denegada (no repudio)

![[Pasted image 20241021214059.png]]
**Cinco funciones componen la familia de algoritmos SHA:**

- SHA-1
- SHA-224
- SHA-256
- SHA-384
- SHA-512

**El salting** es una salvaguarda adicional que se utiliza para reforzar las funciones hash. Una _sal_ es una cadena aleatoria de caracteres que se añade a los Datos antes de hacer el hash. Los caracteres adicionales producen un valor hash más único, lo que hace que los datos salados sean resistentes a los ataques de tabla rainbow.
![[Pasted image 20241021214934.png]]