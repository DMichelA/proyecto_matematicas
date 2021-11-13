# Mecanismos Autenticación Remota
La autenticación es una manera de controlar el acceso cuando los usuarios intentan acceder a un sistema remoto. La autenticación se puede configurar en el nivel del sistema y 
en el nivel de red. Después de que un usuario haya obtenido acceso a un sistema remoto, la autorización es una manera de limitar las operaciones que el usuario puede realizar.

* **IPsec:** IPsec proporciona autenticación basada en host y en certificado, y cifrado de tráfico de red.
* **Kerberos:** Kerberos utiliza el cifrado para autenticar y autorizar a un usuario que está iniciando sesión en el sistema.
* **LDAP:** El servicio de directorios LDAP puede proporcionar autenticación y autorización a nivel de red.
* **Comandos de inicio de sesión remoto:** Los comandos de inicio de sesión remoto permiten que los usuarios inicien sesión en un sistema remoto a través de la red y utilicen 
sus recursos. Algunos de los comandos de inicio de sesión remoto son rlogin, rcp y ftp. Si usted es un host de confianza, la autenticación es automática.
De lo contrario, se le pedirá que se autentique.
* **SASL:** La autenticación sencilla y capa de seguridad (SASL) es una estructura que proporciona autenticación y servicios de seguridad opcionales a los protocolos de red. 
Los complementos permiten seleccionar el protocolo de autenticación adecuado.
* **RPC segura:** Las RPC seguras mejoran la seguridad de los entornos de red al autenticar a los usuarios que realizan solicitudes en equipos remotos. 
Puede utilizar un mecanismo de autenticación UNIX, DES o Kerberos para las RPC seguras.
Las RPC seguras también se pueden utilizar para proporcionar seguridad adicional en un entorno NFS. Un entorno NFS con RPC seguras se denomina NFS seguro.
* **Secure Shell:** Secure Shell cifra el tráfico de red a través de una red no segura. Secure Shell proporciona autenticación mediante el uso de contraseñas, 
claves públicas, o ambos.

## Autenticación por token de sesión
En la autenticación por token de sesión, conocida normalmente como autenticación por sesión, se genera un token asociado internamente a un usuario. Este token suele tener además una caducidad establecida.

![image](https://user-images.githubusercontent.com/50505172/141599792-06b6cd99-6c5e-48ca-b43e-aed17b11ffa8.png)

## Autenticación por token de aplicación
La sesión es una forma de proveer de un estado al protocolo HTTP. Asociado al identificador de sesión, es posible guardar temporalmente información adicional del usuario al que está enlazado. Hay veces en las que no es necesario guardar un estado de la interacción con la aplicación y simplemente se desean realizar acciones. Además, para obtener un token de sesión es necesario autenticarse previamente, lo que en el caso de aplicaciones automatizadas supondría por un lado guardar credenciales y por otro tener que gestionar los procesos de autenticación que sean necesarios. Es por ello que muchas plataformas permiten la generación de un token de acceso que deberá guardarse de forma segura y que permitirá acceder a los recursos del usuario al que esté asociado, como si de una sesión se tratase del mismo. Algunas aplicaciones restringen los permisos del token de acceso generado en el momento de la creación del mismo. Aunque se pueden implementar caducidades, un token de acceso de aplicación generalmente no caduca y es siempre el mismo. (No confundir con el token de autorización de acceso a recursos generado por un proveedor de OAuth, que es distinto cada vez que se genera o renueva). Al igual que el token de sesión, si este token sufriera de una filtración el atacante que dispusiera de este podría realizar las acciones que le brinde el token. Aunque no tiene por qué, este token suele mandarse en la cabecera Authorization. Un caso de uso sería el de por ejemplo, Linode, que permite la generación de tokens de aplicación para hacer uso de su API y desplegar máquinas en la nube.

En este escenario, una medida de seguridad interesante a adoptar sería la de restringir el uso del token de aplicación generado, a una dirección IP siempre que se pueda.

Idealmente el reto inicial debe proveer de 3 elementos para probar la identidad del usuario.

* Algo que el usuario sabe
* Algo que el usuario posee
* Algo que el usuario es

Estos tres elementos pueden traducirse de la siguiente forma:

* Contraseña o información secreta que únicamente el usuario conoce
* Dispositivo de seguridad, certificado digital, código sms, etc.
* Elementos biométricos
