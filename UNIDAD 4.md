
### Capa de red y capa de transporte

### ==🔵 IPv4==
IPv4 es el protocolo de la capa de red que direcciona y enruta los paquetes entre redes, usando direcciones de 32 bits (unos 4,300 millones en total).

### Historia IPv4
IPv4 se definio en 1981 (RFC 791) dentro de la familia TCP/IP, diseñada por Vint Cerf y Bob Kahn

EN 1983 ARPANET adopto TCP/IP, el origen de lo que hoy es internet

### Como se agotaron las direcciones

Las 4,300 millones de direcciones parecían suficientes, pero se repartieron en bloques por clases: una Clase A daba más de 16 millones a una sola organización. Además, los dispositivos conectados crecieron sin parar.

En 2011 la IANA entregó sus últimos bloques a los registros regionales. Se alargó la vida de IPv4 con CIDR, las direcciones privadas y NAT; la solución definitiva es IPv6.

### Diferencias entre IP Publica y IP Privada

- **IP Pública:** Dirección única asignada por tu proveedor de internet que identifica a tu red de forma global en todo internet.

- **IP Privada:** Dirección que asigna tu router para identificar a cada dispositivo de forma interna dentro de tu red local (casa u oficina).

**Diferencia principal:** La IP pública es para comunicarse hacia el exterior (internet) y es única en el mundo, mientras que la IP privada solo sirve para conectar tus aparatos entre sí dentro de la misma red y puede repetirse en millones de hogares.

### caracteristicas IPv4

Es sin conexión(cada paquete viaja por separado), de mejor esfuerzo(no garantiza la entrega) e independientemente del medio (funciona sobre cobre; fibra o WI-fi)

### Encabezado IPv4

El encabezado mide 20 bytes como minimo y lleva la IP de origen, la IP de destino, el TTL (limite de saltos) y el campo protocolo (TCP)

### IPv6

Ipv6 usa direcciones de 128 bits y se creo pq las direcciones IPv4 se agotaron; permite un número práctimente ilimitado de dispositivos

### Cuantas direcciones tiene IPv6

A inicios de los años 90 el IETF empezó a diseñar el reemplazo de IPv4 al prever que sus direcciones se agotarian.

Su especificación se publicó en 1995, se actualizó en 1998 (RFC 2460) y hoy está vigente en el RFC 8200 (2017).

La Evolución de las Direcciones IP:PIv4 IPv6

Con 128 bits hay 2^128 direcciones: unos 340 sextillones (3.4 × 10^38), es decir, 2^96 veces más que IPv4.

Cada subred estándar (/64) por si sola tiene 2^64 direcciones, más de 18 trillones

### Ventajas de IPv6

Ofrece un espacio de direcciones enorme, un encabezado simplificado de 40 bytes, autoconfiguración de direcciones y no usa broadcast: lo reemplaza el multicast.

### Division de la red en grupos 

Una red grande se divide en subredes: grupos de dispositivos organizados por ubicación, función o departamento, cada uno con su propio rango de direcciones.

### Por qué dividir una red

Al dividir se reduce el tráfico de broadcast, mejora el rendimiento, se aplican políticas de seguridad por grupo y se facilita la administración.