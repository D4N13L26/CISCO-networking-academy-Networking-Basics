CISCO networking academy
Networking Basics 9.4.1

La transmisión unidifusión se refiere a un dispositivo que envía un mensaje a otro dispositivo en comunicaciones uno a uno. 
Un paquete de unidifusión tiene una dirección IP de destino que es una dirección de unidifusión que va a un único destinatario. 
Una dirección IP de origen sólo puede ser una dirección de unidifusión, ya que el paquete sólo puede originarse de un único origen. 
Esto es independientemente de si la dirección IP de destino es una unidifusión, difusión o multidifusión. 
Las direcciones de host de unidifusión IPv4 están en el rango de direcciones de 1.1.1.1 a 223.255.255.255.

Transmisión de transmisión hace referencia a un dispositivo que envía un mensaje a todos los dispositivos de una red en comunicaciones unipersonales. 
Los paquetes de difusión tienen una dirección IPv4 de destino que contiene solo números uno (1) en la porción de host. 
Todos los dispositivos del mismo dominio de difusión deben procesar un paquete de difusión. Una transmisión puede ser dirigida o limitada. 
Una difusión dirigida se envía a todos los hosts de una red específica. Se envía una difusión limitada a 255.255.255.255. De manera predeterminada, los enrutadores no reenvían difusiones.

La transmisión de multidifusión reduce el tráfico al permitir que un host envíe un único paquete a un grupo seleccionado de hosts que estén suscritos a un grupo de multidifusión. 
Un paquete de multidifusión es un paquete con una dirección IP de destino que es una dirección de multidifusión. 
IPv4 reservó las direcciones de 224.0.0.0 a 239.255.255.255 como rango de multidifusión. 
Cada grupo de multidifusión está representado por una sola dirección IPv4 de destino de multidifusión. 
Cuando un host IPv4 se suscribe a un grupo de multidifusión, el host procesa los paquetes dirigidos a esta dirección de multidifusión y los paquetes dirigidos a la dirección de unidifusión asignada exclusivamente.

Las direcciones IPv4 públicas son direcciones en las que se realiza routing globalmente entre los routers ISP. Sin embargo, no todas las direcciones IPv4 disponibles pueden usarse en Internet. 
Existen bloques de direcciones denominadas direcciones privadas que la mayoría de las organizaciones usan para asignar direcciones IPv4 a los hosts internos. 
La mayoría de las redes internas, desde grandes empresas hasta redes domésticas, utilizan direcciones IPv4 privadas para dirigirse a todos los dispositivos internos (intranet), incluidos los hosts y enrutadores. 
Sin embargo, las direcciones privadas no son enrutables globalmente. Antes de que el ISP pueda reenviar este paquete, debe traducir la dirección IPv4 de origen, que es una dirección privada, a una dirección IPv4 pública mediante NAT.

Direcciones de Loopback (127.0.0.0 /8 or 127.0.0.1 to 127.255.255.254) generalmente identificadas solo como 127.0.0.1, son direcciones especiales que usa un host para dirigir el tráfico hacia sí mismo. 
Direcciones link-local o direcciones IP privadas automáticas (APIPA) 169.254.0.0/16o 169.254.0.1 a 169.254.255.254 Los utiliza un cliente DHCP de Windows para autoconfigurarse en caso de que no haya servidores DHCP disponibles.

En 1981, las direcciones IPv4 se asignaron utilizando direccionamiento con clase:
Clase A (0.0.0.0/8 a 127.0.0.0/8) - Diseñada para admitir redes extremadamente grandes, con más de 16 millones de direcciones de host.
  Clase B (128.0.0.0/16 a 191.255.0.0/16) - Diseñada para satisfacer las necesidades de redes de tamaño moderado a grande, con hasta 65,000 direcciones de host.
    Clase C (192.0.0.0/24 a 223.255.255.0/24) - Diseñada para admitir redes pequeñas con un máximo de 254 hosts.
      También existe un bloque de multidifusión de clase D que va de 224.0.0.0 a 239.0.0.0, y un bloque de direcciones experimentales de clase E que va de 240.0.0.0 a 255.0.0.0.

Las direcciones IPv4 públicas son direcciones en las que se realiza routing globalmente entre los routers ISP. 
Las direcciones IPv4 públicas deben ser únicas. Tanto las direcciones IPv4 como las IPv6 son administradas por la IANA. 
La IANA administra y asigna bloques de direcciones IP a los RIR. Los RIR se encargan de asignar direcciones IP a los ISP, quienes a su vez proporcionan bloques de direcciones IPv4 a las organizaciones y a los ISP más pequeños. 
Las organizaciones también pueden obtener sus direcciones directamente de un RIR.

En una LAN Ethernet, los dispositivos usan transmisiones y ARP para ubicar otros dispositivos. 
ARP envía transmisiones de capa 2 a una dirección IPv4 conocida en la red local para descubrir la dirección MAC asociada. 
Los dispositivos de LAN Ethernet también localizan otros dispositivos que utilizan servicios. Un host generalmente adquiere su configuración de dirección IPv4 mediante DHCP, que envía transmisiones en la red local para ubicar un servidor DHCP. 
Los switches propagan las broadcasts por todas las interfaces, salvo por aquella en la cual se recibieron.

Un dominio de difusión grande es una red que conecta muchos hosts. Un problema con un dominio de broadcast grande es que estos hosts pueden generar broadcasts excesivas y afectar la red de manera negativa. 
La solución es reducir el tamaño de la red para crear dominios de difusión más pequeños mediante un proceso que se denomina división en subredes. 
Estos espacios de red más pequeños se denominan subredes. La base de la división en subredes es usar bits de host para crear subredes adicionales.
La división en subredes disminuye el tráfico de red general y mejora su rendimiento. Ayuda a los administradores a implementar políticas de seguridad, como qué subredes pueden o no pueden comunicarse entre sí. 
Reduce la cantidad de dispositivos afectados por tráfico de transmisión anormal debido a malas configuraciones, problemas de hardware/software o intenciones maliciosas.


