# Simulacro Examen Parcial 1
Rodrigo Yepes Rubio
<br>https://github.com/rodrigoyr/RD_Simulacro-Examen-Parcial-1.git<br>
## Parte I: Conceptos y Teoría

### Pregunta 1: Modelos OSI y TCP/IP

#### a) Describe las principales diferencias entre el modelo OSI y el modelo TCP/IP, considerando aspectos como el número de capas, la orientación (teórica vs. práctica) y el manejo de la capa de aplicación.

1. **Número de capas**:
   - **Modelo OSI**: 7 capas (física, enlace de datos, red, transporte, sesión, presentación, aplicación).
   - **Modelo TCP/IP**: 4 capas (enlace/acceso a la red, internet, transporte, aplicación).

2. **Orientación**:
   - **Modelo OSI**: Teórico, desarrollado por la ISO como una guía general.
   - **Modelo TCP/IP**: Práctico, basado en protocolos reales usados en Internet.

3. **Capa de aplicación**:
   - **Modelo OSI**: Incluye protocolos de uso frecuente (transferencia de archivos, correo electrónico) y distingue entre servicio, interfaz y protocolo.
   - **Modelo TCP/IP**: Incluye protocolos como TELNET, FTP, SMTP, DNS, pero no distingue entre servicio, interfaz y protocolo.

4. **Redes de difusión**:
   - **Modelo OSI**: No soporta redes de difusión (solo conexiones punto a punto).
   - **Modelo TCP/IP**: Soporta redes de difusión.

5. **Orientación a conexión**:
   - **Modelo OSI**: Solo soporta comunicación orientada a conexión en la capa de transporte.
   - **Modelo TCP/IP**: Soporta comunicación orientada a conexión (TCP) y no orientada a conexión (UDP).

6. **Eficiencia**:
   - **Modelo OSI**: Repite funciones como direccionamiento y control de flujo en varias capas, lo que puede ser ineficiente.
   - **Modelo TCP/IP**: Tiende a ser más eficiente al evitar la repetición de funciones.

**Conclusión**: Ambos modelos son esenciales para el diseño y operación de redes de ordenadores. El modelo OSI proporciona una estructura teórica clara, mientras que el modelo TCP/IP se centra en la implementación práctica y el uso en redes reales.

#### b) Explica brevemente las ventajas y limitaciones de cada uno de estos modelos.

**Ventajas y limitaciones del modelo OSI**

**Ventajas**:
- **Estructura clara**: Proporciona una guía teórica bien definida con siete capas, facilitando la comprensión y enseñanza de redes.
- **Estándares internacionales**: Define protocolos estandarizados, promoviendo la interoperabilidad entre diferentes sistemas y fabricantes.
- **Modularidad**: Cada capa tiene funciones específicas, permitiendo la actualización y mejora de una capa sin afectar las demás.

**Limitaciones**:
- **Teórico**: No está vinculado a protocolos específicos, lo que puede dificultar su aplicación práctica.
- **Ineficiencia**: Repite funciones como direccionamiento y control de flujo en varias capas, lo que puede aumentar la ineficiencia.
- **Redes de difusión**: No soporta redes de difusión, limitando su aplicabilidad en ciertos entornos.

**Ventajas y limitaciones del modelo TCP/IP**

**Ventajas**:
- **Práctico**: Basado en protocolos reales utilizados en Internet, facilitando su implementación en redes reales.
- **Eficiencia**: Evita la repetición de funciones, siendo más eficiente en la transmisión de datos.
- **Flexibilidad**: Soporta tanto comunicación orientada a conexión (TCP) como no orientada a conexión (UDP), adaptándose a diferentes necesidades.

**Limitaciones**:
- **Menos estructurado**: No distingue claramente entre servicio, interfaz y protocolo, lo que puede ser problemático desde el punto de vista de la ingeniería del software.
- **Estándares menos definidos**: Menos enfocado en la estandarización internacional, lo que puede afectar la interoperabilidad.
- **Menos capas**: La simplificación a cuatro capas puede limitar la granularidad y especificidad en la definición de funciones.

### Pregunta 2: Función de la Capa de Transporte

Explica el papel de la capa de transporte en ambos modelos (OSI y TCP/IP). En tu respuesta, menciona cómo se garantiza la entrega de datos y da ejemplos de protocolos asociados a esta capa.

#### Modelo OSI

- **Función principal**: Abstraer a las capas superiores de los cambios tecnológicos en las capas inferiores (física, enlace y red), y dividir los datos de las capas superiores para adaptarlos a la red.
- **Entrega de datos**: Garantiza una comunicación punto a punto libre de errores, asegurando que los mensajes lleguen en el orden en que fueron enviados y que todas las partes del mensaje sean recibidas. También puede manejar mensajes aislados, donde no se garantiza el orden de entrega.
- **Protocolos asociados**: Aunque el modelo OSI es teórico y no especifica protocolos concretos, en la práctica, se pueden considerar protocolos como TCP y UDP que cumplen funciones similares en el modelo TCP/IP.

#### Modelo TCP/IP

- **Función principal**: Permitir la comunicación entre dos entidades mediante protocolos de transporte extremo a extremo.
- **Entrega de datos**: Utiliza dos protocolos principales:
  - **TCP (Transmission Control Protocol)**: Protocolo confiable y orientado a conexión que entrega un flujo de bytes sin errores a otro nodo. Gestiona el control de flujo para evitar saturar a un receptor lento.
  - **UDP (User Datagram Protocol)**: Protocolo no confiable y no orientado a conexión que realiza entregas puntuales donde no importan los errores.

#### Ejemplos de protocolos

- **TCP (Transmission Control Protocol)**:
  - **Características**: Confiable, orientado a conexión, garantiza la entrega ordenada y sin errores de los datos.
  - **Uso**: Aplicaciones que requieren una transmisión de datos segura y ordenada, como la navegación web (HTTP/HTTPS), transferencia de archivos (FTP) y correo electrónico (SMTP).

- **UDP (User Datagram Protocol)**:
  - **Características**: No confiable, no orientado a conexión, entrega rápida sin garantía de orden ni de integridad.
  - **Uso**: Aplicaciones que requieren velocidad y pueden tolerar pérdida de datos, como transmisión de video en tiempo real (streaming), juegos en línea y consultas DNS.

### Pregunta 3: TCP vs. UDP

Compara y contrasta TCP y UDP en términos de:

- **Orientación a conexión**:
  - **TCP (Transmission Control Protocol)**: Orientado a conexión: Establece una conexión antes de transmitir datos, asegurando que ambos extremos están listos para la comunicación.
  - **UDP (User Datagram Protocol)**: No orientado a conexión: No establece una conexión previa, simplemente envía los datos sin verificar si el receptor está listo.

- **Fiabilidad y control de errores**:
  - **TCP**: Fiable: Garantiza la entrega de datos sin errores, en el orden correcto y sin pérdidas. Utiliza mecanismos de control de flujo y retransmisión de paquetes perdidos.
  - **UDP**: No fiable: No garantiza la entrega de datos ni el orden. No tiene mecanismos de control de flujo ni retransmisión de paquetes perdidos.

- **Velocidad y orden de entrega**:
  - **TCP**: Velocidad: Más lento debido a los mecanismos de control de errores y la necesidad de establecer una conexión. Orden de entrega: Garantiza que los datos se entreguen en el orden correcto.
  - **UDP**: Velocidad: Más rápido porque no establece conexión ni realiza control de errores. Orden de entrega: No garantiza el orden de entrega de los datos.

- **Ejemplos de aplicaciones**:
  - **TCP**: Aplicaciones: Navegación web (HTTP/HTTPS), transferencia de archivos (FTP), correo electrónico (SMTP), aplicaciones que requieren transmisión de datos segura y ordenada.
  - **UDP**: Aplicaciones: Transmisión de video en tiempo real (streaming), juegos en línea, consultas DNS, aplicaciones que requieren velocidad y pueden tolerar pérdida de datos.

**En resumen**, TCP es adecuado para aplicaciones que requieren fiabilidad y orden en la entrega de datos, mientras que UDP es preferido para aplicaciones que necesitan velocidad y pueden tolerar cierta pérdida de datos.

### Pregunta 4: Protocolo para Transferencia de Archivos

#### a) ¿Qué protocolo de la capa de aplicación se utiliza tradicionalmente para la transferencia de archivos en redes TCP/IP?

El protocolo de la capa de aplicación que se utiliza tradicionalmente para la transferencia de archivos en redes TCP/IP es el **FTP (File Transfer Protocol)**. Este protocolo permite la transferencia de archivos entre un cliente y un servidor en una red TCP/IP, proporcionando funciones como la autenticación de usuarios, la gestión de archivos y la transferencia de datos de manera eficiente.

#### b) Menciona al menos dos alternativas a este protocolo, resaltando sus diferencias principales en cuanto a seguridad o funcionalidad.

1. **SFTP (SSH File Transfer Protocol)**:
   - **Seguridad**: SFTP es una alternativa segura a FTP que utiliza el protocolo SSH (Secure Shell) para cifrar tanto los datos como las credenciales de acceso durante la transferencia. Esto garantiza que la información no pueda ser interceptada ni manipulada por terceros.
   - **Funcionalidad**: Además de la transferencia de archivos, SFTP permite realizar operaciones de gestión de archivos como renombrar, eliminar y cambiar permisos de archivos en el servidor remoto.
   - **Diferencias principales**: A diferencia de FTP, SFTP proporciona una capa de seguridad adicional mediante el cifrado y no requiere múltiples conexiones, ya que todas las operaciones se realizan a través de una única conexión segura.

2. **FTPS (FTP Secure)**:
   - **Seguridad**: FTPS es una extensión de FTP que añade soporte para SSL/TLS (Secure Sockets Layer/Transport Layer Security) para cifrar la conexión. Esto protege los datos y las credenciales de acceso durante la transferencia.
   - **Funcionalidad**: FTPS mantiene la misma funcionalidad básica de FTP, permitiendo la transferencia de archivos y la gestión de directorios, pero con la ventaja de la seguridad añadida por el cifrado.
   - **Diferencias principales**: A diferencia de FTP, FTPS utiliza certificados SSL/TLS para autenticar la conexión y cifrar los datos, lo que mejora significativamente la seguridad. Sin embargo, al igual que FTP, FTPS puede requerir múltiples conexiones para el control y la transferencia de datos.

Estas alternativas ofrecen mejoras significativas en términos de seguridad y, en algunos casos, funcionalidad adicional, lo que las hace más adecuadas para entornos donde la protección de datos es crucial.

### Pregunta 5: Resolución de Nombres en DNS

Describe detalladamente el proceso de resolución de nombres en DNS, desde que un usuario ingresa una URL en el navegador hasta que se establece la conexión con el servidor web. Incluye en tu respuesta el rol de la caché y de los servidores raíz.

#### Paso 1: Ingreso de la URL
Cuando un usuario ingresa una URL en el navegador, el navegador necesita convertir ese nombre de dominio en una dirección IP para establecer la conexión con el servidor web.

#### Paso 2: Consulta al resolvedor DNS
El navegador utiliza un programa llamado resolvedor que envía una consulta DNS a un servidor DNS local. Esta consulta se realiza generalmente mediante el protocolo UDP.

#### Paso 3: Verificación de la caché
El servidor DNS local primero verifica su caché para ver si ya tiene la dirección IP correspondiente al nombre de dominio solicitado. La caché almacena temporalmente las respuestas a consultas DNS anteriores para acelerar el proceso de resolución.

#### Paso 4: Consulta a los servidores raíz
Si la dirección IP no se encuentra en la caché, el servidor DNS local envía una consulta a uno de los servidores raíz. Los servidores raíz son los puntos de inicio en la jerarquía del DNS y tienen información sobre los servidores de nombres de los dominios de nivel superior (como .com, .org, .net).

#### Paso 5: Consulta a los servidores de nivel superior
El servidor raíz responde con la dirección de un servidor DNS correspondiente al dominio de nivel superior del nombre de dominio solicitado. El servidor DNS local entonces envía una consulta a este servidor de nivel superior.

#### Paso 6: Consulta a los servidores autoritativos
El servidor de nivel superior responde con la dirección de un servidor autoritativo que tiene la información específica sobre el nombre de dominio solicitado. El servidor DNS local envía una consulta a este servidor autoritativo.

#### Paso 7: Respuesta del servidor autoritativo
El servidor autoritativo responde con la dirección IP correspondiente al nombre de dominio solicitado. Esta respuesta se almacena en la caché del servidor DNS local para futuras consultas.

#### Paso 8: Establecimiento de la conexión
El servidor DNS local devuelve la dirección IP al resolvedor, que a su vez la proporciona al navegador. El navegador utiliza esta dirección IP para establecer una conexión TCP con el servidor web y enviar la solicitud HTTP para obtener la página web.

### Rol de la caché
La caché en el servidor DNS local juega un papel crucial en la aceleración del proceso de resolución de nombres. Al almacenar temporalmente las respuestas a consultas DNS anteriores, la caché permite que las consultas futuras para los mismos nombres de dominio se resuelvan rápidamente sin necesidad de contactar a los servidores raíz y autoritativos nuevamente.

### Rol de los servidores raíz
Los servidores raíz son fundamentales en la jerarquía del DNS. Actúan como el punto de inicio para la resolución de nombres, proporcionando información sobre los servidores de nombres de los dominios de nivel superior. Sin los servidores raíz, el proceso de resolución de nombres no podría comenzar, ya que no habría un punto de referencia inicial para encontrar la dirección IP correspondiente a un nombre de dominio.

### Pregunta 6: Comunicación en el Modelo TCP/IP

Explica el proceso de comunicación entre dos dispositivos en una red utilizando el modelo TCP/IP. Describe el rol y la función de cada capa (Aplicación, Transporte, Internet y Acceso a Red) durante el envío y recepción de datos.

#### 1. Capa de Aplicación
**Rol y función**:
- La capa de aplicación es la más cercana al usuario y proporciona servicios de red directamente a las aplicaciones.
- Ejemplos de protocolos en esta capa incluyen HTTP (para navegación web), FTP (para transferencia de archivos), SMTP (para correo electrónico), y DNS (para resolución de nombres).

**Envío de datos**:
- Una aplicación (por ejemplo, un navegador web) genera datos y utiliza un protocolo de la capa de aplicación (como HTTP) para preparar los datos para su transmisión.
- Los datos se encapsulan en un formato adecuado para el protocolo de la capa de aplicación.

**Recepción de datos**:
- Los datos recibidos se pasan a la aplicación correspondiente (por ejemplo, un navegador web) que los procesa y presenta al usuario.

#### 2. Capa de Transporte
**Rol y función**:
- La capa de transporte proporciona comunicación de extremo a extremo entre dispositivos.
- Los principales protocolos en esta capa son TCP (Transmission Control Protocol) y UDP (User Datagram Protocol).

**Envío de datos**:
- Si se utiliza TCP, la capa de transporte establece una conexión, divide los datos en segmentos, añade números de secuencia y realiza el control de flujo y de errores.
- Si se utiliza UDP, los datos se dividen en datagramas sin establecer una conexión previa ni garantizar la entrega ordenada.

**Recepción de datos**:
- TCP reensambla los segmentos en el orden correcto, verifica la integridad de los datos y los pasa a la capa de aplicación.
- UDP simplemente pasa los datagramas a la capa de aplicación sin reensamblar ni verificar la integridad.

#### 3. Capa de Internet
**Rol y función**:
- La capa de Internet es responsable del direccionamiento y enrutamiento de los paquetes de datos a través de la red.
- El principal protocolo en esta capa es IP (Internet Protocol).

**Envío de datos**:
- Los segmentos o datagramas de la capa de transporte se encapsulan en paquetes IP.
- La capa de Internet añade direcciones IP de origen y destino y determina la ruta que los paquetes deben seguir para llegar al destino.

**Recepción de datos**:
- La capa de Internet verifica las direcciones IP de destino y pasa los paquetes a la capa de transporte correspondiente.

#### 4. Capa de Acceso a Red
**Rol y función**:
- La capa de acceso a red maneja la transmisión física de los datos a través de la red.
- Incluye tanto la capa física (hardware) como la capa de enlace de datos (protocolos de enlace).

**Envío de datos**:
- Los paquetes IP se encapsulan en tramas de enlace de datos, que incluyen direcciones MAC (Media Access Control) y otros datos necesarios para la transmisión física.
- Las tramas se transmiten a través del medio físico (cable, fibra óptica, inalámbrico).

**Recepción de datos**:
- La capa de acceso a red recibe las tramas, verifica las direcciones MAC y extrae los paquetes IP.
- Los paquetes IP se pasan a la capa de Internet para su procesamiento posterior.

### Resumen del proceso
1. **Capa de Aplicación**: La aplicación genera datos y utiliza un protocolo de aplicación para prepararlos.
2. **Capa de Transporte**: Los datos se dividen en segmentos (TCP) o datagramas (UDP) y se añaden números de secuencia y control de errores (TCP).
3. **Capa de Internet**: Los segmentos/datagramas se encapsulan en paquetes IP con direcciones IP de origen y destino.
4. **Capa de Acceso a Red**: Los paquetes IP se encapsulan en tramas de enlace de datos y se transmiten físicamente a través de la red.

