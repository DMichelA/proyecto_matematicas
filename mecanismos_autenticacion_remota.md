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
