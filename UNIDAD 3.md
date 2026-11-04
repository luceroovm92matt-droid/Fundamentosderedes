¿Como se mide su desempeño?

-Ancho de Banda 
-Rendimineto
-Latencia

Ancho de banda (Capacidad máxima)

- **Qué es:** Es el límite teórico máximo de datos que pueden transmitirse por un enlace de red en un periodo determinado. 

- **Cómo se mide:** Se expresa en bits por segundo (bps, Kbps, Mbps, Gbps). 

- **Qué es:** Es la cantidad real de datos útiles que se transmiten o reciben con éxito a través de la red en un tiempo dado (considerando pérdidas, congestión y sobrecarga de protocolos). 
- **Cómo se mide:** Se expresa en unidades de velocidad por segundo (Mbps, Kbps). 

Latencia (_Ping_ o RTT - _Round Trip Time_)

- **Qué es:** Es el tiempo exacto que tarda un paquete de datos en viajar desde el origen hasta su destino y regresar. 
- **Cómo se mide:** Se expresa en **milisegundos (ms)**.

### Como se mide su desempeño?

1. Pruebas de estrés y saturación (_Sustained Load Testing_)

Consiste en forzar la red al máximo para ver en qué punto se degrada el servicio.

- **Metodología:** Se generan flujos masivos de datos para ocupar todo el ancho de banda disponible (usando herramientas como **iPerf3**). Al mismo tiempo, se ejecutan pruebas de latencia (`ping`).
- **Qué se busca:** Identificar el fenómeno llamado **Bufferbloat** (cuando los routers acumulan paquetes en cola debido a la saturación, provocando que la latencia se dispare a cientos de milisegundos).

2. Monitoreo pasivo y activo (SaaS y SRE)

Las empresas no solo miden la red en un momento exacto, sino de forma constante.

- **Monitoreo Activo (Sintético):** Herramientas como **ThousandEyes** o **Datadog** envían paquetes artificiales de forma regular (cada minuto, por ejemplo) a servidores en la nube para medir latencia y rendimiento constante, simulando el comportamiento de un usuario.
- **Monitoreo Pasivo:** Analizadores de tráfico (como **Wireshark** o flujos de **NetFlow**) examinan el tráfico real de los usuarios en tiempo real para detectar caídas en el rendimiento o pérdida de paquetes sin interferir en la red.
- Simulación de escenarios reales

Se utilizan herramientas para recrear el comportamiento de aplicaciones críticas (como llamadas de Zoom, bases de datos o transferencias de archivos masivos). El desempeño se mide bajo el estándar del **Factor R** o **MOS (Mean Opinion Score)**, que califica numéricamente del 1 al 5 si la combinación de ancho de banda, rendimiento y latencia es óptima para la experiencia humana.

### Tipos de cable
cobre -> UTP -> señales -> RJ-45 -> 100 metris electricos


### Activiadad 3.1

Figura explicando porque van en pares

![[Pasted image 20261015165342.png]]



### Capa fisica de datos

-capa fisica
Es la primera capa del modelo OSI , transporta los bits como señales electricas , de luz o de redio a travez del medio  

-Principios componentes
La capa fisica se compone de tres elementos, los medios fisicos   

-Principios parámetros 
Su desempeño se mide con tres parámetros , el ancho de banda (capacidad máxima ) el mantenimiento (lo que realmente se transfiere ) y la latencia (el retardo en llegar)

-Tipos de cables : Cobre
El cable de par trenzado (UTP) transmite señales electricas con conector RJ-45 , alcanza hasta 100 M y es el mas usado en LAN ; el trenzado reduce la interferencia

-UTP: porque los cables van en pares

Los 8 hilos del UTP forman 4 pares trenzados. Cada par envía la señal con polaridad opuesta en sus dos hilos; la interferencia afecta a ambos por igual y el receptor la cancela al comparar los dos.

Cada par tiene un trenzado distinto para reducir la diafonía entre pares vecinos

-Tipos de cable: fibra óptica

La fibra óptica transmite pulsos de luz: llega a mayores distancias y es inmune a la interferencia electromagnética, pero es más costosa y delicada de instalar

-Medios inalámbricos 

Transmiten por ondas de radio (Wi-Fi, Bluetooth, celular); dan movilidad, pero el medio es compartido, sufre interferencia y requiere medidas de seguridad.

-La capa física: señal de comunicación 

Una señal es una variación de una propiedad física que representa bits: cambios de voltaje en cobre, pulsos de luz en fibra u ondas de radio en el aire

-Señalización y codificacion fisica 

La codificación convierte los bits en un patrón predefinido que facilita la sincronía y la detección de errores; la señalización define cómo se representa ese patrón en el medio

-Medios fisicos: conexion de la comunicacion 

Un dispositivo se conecta mediante su tarjeta de red (NIC), un puerto, un conector y el medio; la NIC convierte los bits en la señal que el medio puede transportar

-Ethernet capa 1 y 2

Ethernet (IEEE 802.3) es el estándar dominante en LAN y trabaja en dos capas: en la capa 1 define medios y señalización, y en la capa 2 define las tramas y las direcciones MAC

-ARP: de dirección IP a dirección MAC

El protocolo ARP permite descubrir la dirección MAC de un dispositivo a partir de su dirección IP. Envía una petición por broadcast; solo el dueño de esa IP responde por unicast, y el resultado se guarda en la tabla ARP

-Envenenamiento ARP (ARP poisoning)

ARP no verifica quién responde: un atacante envía respuestas ARP falsas para que otros equipos asocien su MAC con la IP de otro dispositivo, por ejemplo la del router, y asíintercepta el tráfico (ataque de intermediario).

Se mitiga con inspección dinámica de ARP (DAI) en el switch y con entradas ARP estáticas en los equipos críticos

### Act 3.2


==🔵Porque los puntos de intercambio reducen la latencia?

Porque al saltar de cada punto así cerca se va reduciendo la intensidad de cada conexión , en cambio si se salta todo es mejor ya que no hay tantos saltos

### Act 3.3

Nombre: Gabriel Garcia

Campo 1
Dato de ejemplo: 10101010 10101010 10101010 10101010 10101010 10101010 10101010 10101011 (8 bytes)

Nombre del campo: Padding 

Para qué sirve: Sirve para completar el tamaño requerido de un bloque de datos o una estructura cifrada cuando la información original no alcanza los bytes necesarios. 

Campo 2
Dato de ejemplo: FFFF.FFFF.FFFF (6 bytes)

Nombre del campo: Dirección MAC de destino (Destination MAC Address)

Para qué sirve: Sirve para enviar un mensaje a todos los dispositivos que se encuentran dentro de la misma red local para que todos la reciban y procesen

Campo 3
Dato de ejemplo: 0001.4321.ABCD (6 bytes)

Nombre del campo: Dirección MAC de origen (Source MAC Address)

Para qué sirve: Identifica de manera única al dispositivo que está enviando la trama. Permite que el receptor sepa qn le mandó los datos y sepa a dónde responder

Campo 4
Dato de ejemplo: 0x0806 (2 bytes)

Nombre del campo: Tipo / EtherType

Para qué sirve: Indica q protocolo de capa superior viene encapsulado dentro de la carga útil de la trama Ethernet.

Campo 5
Dato de ejemplo: ¿Quién tiene la IP 192.168.1.2? Responde a 192.168.1.1 (entre 46 y 1500 bytes)

Nombre del campo: Datos / Carga útil (Payload / ARP Request)

Para qué sirve: Contiene la información que transporta la trama. En este caso una trama ARP, lleva la petición en texto preguntando qué dispositivo físico (MAC) corresponde a una determinada dirección IP dentro de la red local

Campo 6
Dato de ejemplo: 0x3A7F91C2 (4 bytes)

Nombre del campo: FCS (Frame Check Sequence) / Código de redundancia cíclica (CRC)

Para qué sirve: Es un valor de verificación de errores de 4 bytes que se coloca al final de la trama Ethernet. Sirve para comprobar que los datos no se hayan corrompido o alterado durante la transmisión por el medio físico

### Act 3.4


Switch de capa 3

Además de conmutar por MAC, puede enrutar usando la dirección IP del paquete y su tabla de rutas, y conecta varias redes o VLAN entre sí.


 Capa 2 frente a сара 3

Capa 2: lee la MAC, trabaja en una sola red, necesita un router para comunicar redes distintas y cuesta menos.

Capa 3: lee MAC e IP, conecta varias redes o VLAN, enruta por sí mismo y a alta velocidad, y cuesta más.

Ejemplo: de una red a otra

Un equipo de la red 192.168.1.0/24 quiere hablar con la 192.168.2.0/24. Con un switch de capa 2 hace falta un router; un switch de capa 3 mira la IP de destino y crea una trama nueva hacia la otra red


Reemplaza a un router?

No del todo: el router sigue siendo mejor para conectar con el exterior (WAN, Internet) y para funciones como NAT. El switch de capa 3 se usa en campus y centros de datos para enrutar entre VLAN a alta velocidad



Switch 2

Que son?
Es un dispositivo de interconexión que opera en la **Capa de Enlace de Datos (Capa 2)** del Modelo OSI. Conecta dispositivos dentro de una misma red local (LAN) y transmite tramas de datos (Frames) basándose en direcciones físicas MAC

Diferencias:

- **Tablas de Direcciones MAC:** Construye una tabla CAM (dirección MAC $\leftrightarrow$ puerto físico) mediante aprendizaje de direcciones de origen

- **Dominio de Broadcast:** Pertenece a un único dominio de difusión por defecto. Puede segmentar la red en múltiples VLANs

Switch 3

Que son?
Es un switch avanzado que opera tanto en la **Capa de Enlace de Datos (Capa 2)** como en la **Capa de Red (Capa 3)** del Modelo OSI. Combina la alta velocidad de conmutación de un switch local con las funciones de enrutamiento de un router

Diferencias:
- **Tablas IP y MAC:** Inspecciona tanto el encabezado Ethernet como el paquete IP (direcciones IP de origen y destino)

- **Enrutamiento Inter-VLAN por Hardware:** Realiza enrutamiento de alta velocidad mediante hardware especializado (ASICs) a través de **SVIs** (_Switched Virtual Interfaces_) o puertos enrutados