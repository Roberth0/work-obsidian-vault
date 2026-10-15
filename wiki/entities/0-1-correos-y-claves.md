---
type: entity
created: 2026-09-23
updated: 2026-09-23
generation_complete: true
sources:
  - "[[sources/0-1-correos-y-claves_b0e46c]]"
  - "[[sources/3-corporativos_04d2e4]]"
tags:
  - "term"
aliases:
  - "Correos y Claves"
  - "0.1 Correos y Claves Telconet"
  - "Nota de correos y claves NOC"
  - "Credenciales de acceso"
  - "Credenciales"
---

# 0.1 Correos y Claves

## Descripción

**0.1 Correos y Claves** es una nota operativa interna de [[Telconet]] que funciona como repositorio de correos electrónicos, credenciales de acceso y contactos de escalamiento empleados por el equipo de [[noc]] y áreas afines. El documento concentra usuarios y contraseñas de herramientas de monitoreo y gestión como [[eSyslog]], [[PacketLight]], [[Zabbix]], [[TeliGraph]], [[Kentik]], [[QlikSense]] y [[Fiberhome]], además de portales de terceros como [[Cirion]] y [[UFINET]].

También describe la estructura de [[Jefaturas]] organizada por área y ciudad —OTN UIO, OTN GYE, IPCCL1, IPCCL2, REDESLAN, AI GYE, BOC UIO/GYE, Infraestructura, CERT y Monitoreo Sistemas— junto con los nombres de los responsables de cada una. Complementariamente, reúne contactos corporativos de proveedores y clientes como [[Cloudflare]], [[Meta]]/Facebook, [[Amazon]], [[Telia]], [[Telxius]], [[CSD Movistar]], [[El Rosado]], [[Disney]], [[IBM]] y [[Kyndryl]], e incluye instrucciones para el escalamiento de incidencias (por ejemplo, contactar al NOC y al EPP de Cloudflare).

Por su contenido, la nota debe tratarse como información altamente sensible: es una fuente primaria de credenciales y contactos cuya circulación debería restringirse al personal autorizado. Su valor principal es operativo, ya que centraliza en un solo documento los accesos y las vías de escalamiento necesarios para la operación diaria del NOC.

Adicionalmente, la nota documenta una contraseña de extensión compartida para herramientas de comunicación como [[Linphone]]/[[Zoiper]] (`TNlAtam#2o2!`), credencial que amplía el inventario de accesos descrito en la página.

En cuanto a contactos de escalamiento, se registra el número de contacto NOC de [[CSD Movistar]] (`0999997036`) junto con los teléfonos asociados para escalamiento de incidencias, información que complementa la mención de dicho proveedor en el listado de contactos corporativos.

**Credenciales** es también el bloque dedicado que agrupa los pares usuario/contraseña necesarios para acceder a las controladoras y equipos gestionados por [[Telconet]]; lista usuarios como IPCC, Ipcc, noc y noc@telconet.ec junto con sus respectivas contraseñas organizadas por fabricante (Ruckus, Huawei, Omarsa, Cisco) y por controladora.

Entre los accesos se registran las direcciones IP y enlaces de administración de las controladoras: nodo WiFi `181.39.190.2`, controladoras de provincias `181.198.110.134`, `181.39.24.107` y `181.39.24.133`, y la del cliente Omarsa en Panamá `181.39.128.171:8081`; además, se indica que las contraseñas se rotan ocasionalmente, como en el caso de la controladora Meraki.

El uso de estas credenciales es un elemento operativo central para soporte, ya que sin ellas no es posible validar APs ni gestionar la red inalámbrica; los procedimientos asociados incluyen notificar por el chat NOC-RADIO, asignar tareas mediante números de tarea y validar los APs accediendo a la controladora en la sección Wireless / All APs.
## Entidades relacionadas

- [[entities/telconet|Telconet]]
- [[entities/cloudflare|Cloudflare]]
- [[entities/ruckus|Ruckus]]
- [[entities/huawei|Huawei]]
- [[entities/omarsa|Omarsa]]
- [[entities/cisco|Cisco]]
- [[entities/meraki|Meraki]]
- [[entities/ruijie|Ruijie]]

## Conceptos relacionados

- [[concepts/jefaturas|Jefaturas]]
- [[concepts/controladora|Controladora]]
- [[concepts/login|Login]]

## Menciones en la fuente

- "eSyslog User: `noc`Password: `VCzrk"kUr3xMH~E6`" (Usuario de eSyslog: `noc` Contraseña: `VCzrk"kUr3xMH~E6`) — [[Work/0.1 Correos y Claves|0.1 Correos y Claves]]
- "PacketLigh User: `PACKETLIGHT\nocgye`  Password: `nocgye2020`" (Usuario de PacketLigh: `PACKETLIGHT\nocgye` Contraseña: `nocgye2020`) — [[Work/0.1 Correos y Claves|0.1 Correos y Claves]]
- ">[!info]+ Credenciales" — [[Work/3. Corporativos|3. Corporativos]]
- "**Ruckus** User: `IPCC`Pass:  `T!pccN2016`" — [[Work/3. Corporativos|3. Corporativos]]
- "Tomar en cuenta que se realizó el cambio de contraseña de la controladora Meraki" — [[Work/3. Corporativos|3. Corporativos]]