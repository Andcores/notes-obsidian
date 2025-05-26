## Conceder autorización 
Si se ha autenticado al usuario correcto, la red debe garantizar que se ponen a su disposición los recursos adecuadios. Tenemos 3 frameworks comunes que las organizaciones utilizan para manejar esta paso IAM:
- Control de acceso obligatorio (MAC)
- Control de acceso discrecional (DAC)
- Control de acceso basado roles(RBAC)

### Control de acceso obligatorio 
![[Pasted image 20241021221423.png]]
Es el mas estricto de los tres framework. El acceso a la informacion debe ser concedido manualmente por una autoridad central o por el administrador de sistema 


### Control de acceso discrecional 
![[Pasted image 20241021222104.png]]
Se aplica normalmente cuando el propietario de los datos decide los niveles apropiados de accesibilidad. 

### Control de acceso basado en roles 
![[Pasted image 20241021222303.png]]

Se utiliza cuando la autorización viene determinada por la función de un usuario.
**Principios de autorización**

- La autorización está estrechamente relacionada con el principio de privilegio mínimo, lo que significa que a los usuarios solo se les debe otorgar el nivel mínimo de acceso necesario para realizar sus tareas.
- Otro principio crucial es la separación de funciones, que evita que una sola persona tenga demasiado poder o control sobre un sistema, lo que reduce el riesgo de uso indebido y errores.

**Métodos de autorización**

- HTTP Basic Auth, un método más antiguo que envía credenciales abiertamente a través de la red, lo que lo hace vulnerable a ataques.
- OAuth, un método más seguro que utiliza tokens de API para verificar el acceso entre aplicaciones sin compartir información confidencial como nombres de usuario y contraseñas.

