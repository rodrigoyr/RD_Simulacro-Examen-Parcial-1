# Simulacro Examen Parcial 1

Rodrigo Yepes Rubio

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
   -
