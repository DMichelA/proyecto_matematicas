# Principios Codificación Segura

## La codificación segura es diseñar y desarrollar software evitando las debilidades que conducen a vulnerabilidades relacionadas 
con la seguridad al adherirse a los estándares de seguridad especificados y las mejores prácticas de la industria.

* Privilegio mínimo
A un proceso o usuario se le deben otorgar solo los privilegios que son necesarios para completar una tarea. 
Los privilegios de usuario deben asignarse de acuerdo con su rol, pero no de otra manera. Para crearlo se asigna derechos cuando un proceso o subproceso 
los requiera y se eliminan posteriormente. Este principio limita el daño potencial que puede resultar de ataques y errores del usuario.

* Economía del mecanismo
Se debe tratar de mantener un diseño simple. Hay menos que posibilidad a equivocarse, menos inconsistencias son posibles y el código es más fácil de entender y depurar.

* Mediación completa
Se debe comprobar cada intento de acceder a un recurso, no solo el primero.  Por ejemplo, Linux comprueba los permisos de acceso cuando un proceso abre un archivo, 
pero no a partir de entonces. Si los permisos de un archivo cambian mientras un proceso tiene el archivo abierto, puede resultar un acceso no autorizado.

* Diseño abierto
La seguridad no debe depender del secreto del diseño o la implementación del código, a veces denominado seguridad a *través de la oscuridad*. 
Por ejemplo, una puerta trasera abierta a un sistema es tan segura como el conocimiento de su existencia. Por supuesto, este principio 
no se aplica a información como contraseñas o claves criptográficas, cuyo conocimiento también debe compartirse entre la menor cantidad de personas posible.

* Separación de privilegios
Se debe dividir el código en módulos, donde cada módulo requiere un conjunto específico y limitado de privilegios para realizar una tarea específica. 
Normalmente, se deben requerir varios privilegios para conceder acceso a una operación confidencial. 
Este principio asegura la separación del deber y proporciona una defensa en profundidad.

* Mecanismo menos común
Un sistema debe aislar a los usuarios y sus actividades entre sí. Los usuarios no deben compartir procesos o subprocesos y 
los canales de información no deben compartirse entre usuarios.

* Valores predeterminados a prueba de fallos 
La acción predeterminada debe ser denegar el acceso a una operación. Si se deniega un intento de realizar una operación, 
el sistema es tan seguro como lo era antes de que comenzara la operación.

* Responsabilidad
Registrar al usuario y sus privilegios para cada acción que intente realizar. Cualquier registro debe poder rotarse y archivarse para evitar llenar un sistema de archivos.

* Aceptabilidad psicológica
Los mecanismos de seguridad deben ser fáciles de instalar, configurar y usar para que un usuario esté menos tentado a tratar de omitirlos.




