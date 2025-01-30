useradd agrega un nuevo usuario " sudo useradd fgarcia"
useradd -g :Establece el grupo predeterminado del usuario, también conocido como su grupo principal.
al ingresar  "sudo useradd -g security fgarcia"se agrega a fgarcia como un nuevo usuario y se le asigna security como grupo principal.

useradd-G :agrega al usuario a grupos adicionales, también llamados grupos complementarios o secundarios.
al ingresar "sudo useradd -G finance,admin fgarcia"se agrega a fgarcia como usuario nuevo y se lo añade a los grupos existentes finance y admin.

usermod: modifica los usuarios ya existentes y usa los mismos modificadores de useradd
Por ejemplo, al ingresar" sudo usermod -g executive fgarcia", se cambiaría el grupo principal de fgarcia a executive.

Por ejemplo, al ingresar "sudo usermod -a -G marketing fgarcia", se agregaría el usuario existente fgarcia al grupo complementario marketing.

**userdel** sudo userdel -r fgarcia, se eliminaría a fgarcia
usermod -L.
**chown**
El comando chown cambia la propiedad de un archivo o un directorio
Para cambiar el usuario propietario del archivo access.txt a fgarcia, ingresa sudo chown fgarcia access.txt.
Para cambiar el grupo propietario del archivo _access.txt_ a _security_, ingresa sudo chown :security access.txt.