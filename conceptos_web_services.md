#  Web Services

## ¿Qué son los web services?
Un web service es una vía de intercomunicación e interoperabilidad entre máquinas conectadas en Red. 

* **SOAP:** es un protocolo que define cómo deben de realizarse las comunicaciones entre máquinas. SOAP usa XML como lenguaje de intercambio de datos con una estructura compleja que es capaz de albergar todo tipo de datos sobre la solicitud o respuesta generada.
* **REST:** usa el propio protocolo HTTP para la comunicación entre máquinas. HTTP es ampliamente soportado por todos los sistemas y de hecho para la transferencia de datos en la web se usa HTTP.
se caracteriza por no tener estado. Es decir, el servidor no es capaz de recordar el estado de la anterior solicitud REST que pudo, o no, hacer un cliente. Por ello, el cliente tiene que enviar en cada solicitud todo el estado de su sesión, lo que se suele hacer mediante un token que le *ayude a recordar* al servidor.

## XML vs JSON
Para los sistemas de comunicación entre máquinas se requiere una serie de características, básicamente marcadas porque las máquinas implicadas en la comunicación pueden tener sistemas muy diferentes. Pueden usar lenguajes de programación o bases de datos diferentes y hasta los sistemas operativos suelen ser distintos entre clientes y servidores. Por ello, para la comunicación de los datos se usa básicamente lenguajes escritos en archivos de texto plano.

* **XML:** está basado en etiquetas, como HTML. Es más tradicional pero también es un lenguaje más avanzado, que presenta diversas utilidades para su extensión, validación de la información y sintaxis de los datos, etc.
* **JSON:** es un lenguaje más nuevo, basado en sintaxis Javascript. Generalmente, es más ligero y requiere mucho mejor carga del servidor para su procesamiento.
