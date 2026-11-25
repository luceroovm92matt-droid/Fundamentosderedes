### Red y Host

Toda dirección tiene dos partes: la parte de red, igual para todos los equipos del grupo, y la parte de host, que identifica a cada equipo.

La dirección sola no dice dónde termina una y empieza la otra

### Direcciones publicas 

Las direcciones públicas son únicas en todo Internet y las asigna el proveedor de servicio (ISP).

Un equipo con dirección pública es alcanzable desde Internet; las privadas, no

### Direcciones privadas 

Se usan solo dentro de una red y no se enrutan en Internet: 10.0.0.0/8, 172.16.0.0/12 y 192.168.0.0/16. Para salir a Internet usan NAT.

-Tarea que es nat 3 diapositivas 

### Direcciones Especiales

127.0.0.1 es el loopback (el propio equipo) y 169.254.0.0/16 es la asignación automática (APIPA) cuando falla el DHCP.

0.0.0.0/0 es la ruta predeterminada.

### Direcciones IPv4

Una dirección IPv4 tiene 32 bits escritos en 4 octetos decimales separados por puntos, como 192.168.1.10; una parte identifica la red y la otra el host.

### DHCP

El cliente obtiene su configuración en cuatro pasos, DORA: Discover, Offer, Request y Acknowledge. El primer mensaje es un broadcast.

El servidor entrega IP, máscara, puerta de enlace y DNS

### Para que sirve DHCP

-Dynamic
-Host
-Configuration
-Protocol

DHCP (Protocolo de configuración dinámica de host)

Es un servicio que asigna direcciones IP automáticamente a los equipos de la red.
Evita configurar cada equipo a mano y los conflictos por direcciones duplicadas.

______
1  | Discover        | Cliente (broadcast) |  Busca un servidor DHCP en la red
__________
2  | Offer             | Servidor                   |  Ofrece una direccion IP disponible
________
3  | Request        | Cliente (broadcast)   |  Pide la dirección ofrecida
_______
4 | Acnowledge  | servidor                     |  Confirma y entrega la configuración


### Tiempo de concesión

La dirección se entrega en préstamo por un tiempo de concesión (lease), no de forma permanente.

El cliente renueva a la mitad del tiempo; en Windows, ipconfig /release libera la dirección e ipconfig /renew pide otra.

### El pool de direcciones

El servidor reparte direcciones de un pool (rango) y entrega con ellas la máscara, la puerta de enlace y el DNS.

Las direcciones fijas de servidores, impresoras y routers se excluyen del pool, o se reservan por dirección MAC.

### Puertos y relevo de DHCP

DHCP usa UDP: el servidor escucha en el puerto 67 y el cliente en el 68.

El broadcast no cruza routers: un router con ip helper-address reenvía las solicitudes a un servidor en otra red (relay).


### Act. 3.2 (24/11/26)

### -  Capa 2

Que es?
creo que es la que se encarga de organizar algunos datos y se mandan entre dispositivos

Para que sirve?
sirve para que no se choquen entre si y asi no se confundan

### - Capa 3 

Que es?
este tambien es el encargado de mover los datos pero a distancia mas lejana entre dispositivos igual mediante paquetes

Para que sirve?
Sirve para que llege bien a su destino sin perder la ubicacion hasta el receptor quien lo recibe

### - Capa 4

Que es?
este lo que hace es una organizacion mas detallada como dividirlos 

Para que sirve?
Da ordenes como la capa tres al repartir la entrega completada