---
type: entity
created: 2026-09-23
updated: 2026-09-23
generation_complete: true
sources:
  - "[[sources/0-directorio-telefonico_b3619c]]"
  - "[[sources/1-backbone_5939cb]]"
  - "[[sources/2-vips_147ea4]]"
  - "[[sources/2-1-cscg_5bb2db]]"
  - "[[sources/3-corporativos_04d2e4]]"
  - "[[sources/4-cedia_d7cef1]]"
tags:
  - "place"
aliases:
  - "Guayaquil"
  - "Aeropuerto de Guayaquil"
  - "GYE (Guayaquil)"
---

# GYE

## Descripción

GYE es el código IATA del aeropuerto de Guayaquil y, en el directorio telefónico, la etiqueta con la que se identifican las operaciones de esa ciudad. En la sección eléctrica del documento se indica que para GYE se debe "Revisar personal de turno en correo", lo que vincula a esta sede con un procedimiento de contacto específico. La ciudad alberga además un [[Datacenter BOC]], con contactos propios de monitoreo (0987231363) y de [[Manos Remotas|manos remotas]] (099 812 2715). Cuenta también con una unidad de operaciones, [[OPU GYE]], que define su propia [[Distribucion Zonas|distribución de zonas]] y horario laboral, cubriendo las zonas Aurora/Duran, Sur 1, Sur 2, Inmaconsa, Miraflores, Kennedy y Centro Sur. De este modo, GYE reúne varios contactos y estructuras operativas dentro del mismo documento, en paralelo a otras sedes como [[UIO]].

GYE es además la jurisdicción correspondiente a Guayaquil dentro de la operación del [[noc]] de Telconet y, junto con [[UIO]], conforma las dos jurisdicciones geográficas principales gestionadas por el NOC; para UIO o GYE, al no tener respuesta ICMP se debe escalar a [[OPU GYE|OPU]]. La sede cuenta con apartados operativos propios como "Permisos DC GYE (Datacenter GYE)" y la "IP VPN GYE", así como con un responsable GEPON TAP, Andres Xavier Rogel Valarezo, y credenciales de acceso a equipos como fwhdcgye1 (`ssh -l noc-operator fwhdcgye1`).

GYE es también el servidor de monitoreo de VIPS correspondiente a la instancia accesible en https://monitoreovipsgye.telconet.ec/zabbix, siendo el segundo de los tres servidores Zabbix enumerados (junto con UIO y Camaras Corporacion GYE); su URL con el dominio telconet.ec confirma la pertenencia de la infraestructura a Telconet. El monitoreo de VIPS se lleva a cabo 24/7 sobre los servidores UIO, GYE y Camaras Corporacion GYE.

En el área CSCG, al verificar en el OSS una caída de caja se debe escalar la tarea de acuerdo a la [[Distribucion Zonas|distribución de zonas]] de GYE y llamar a [[OPU GYE]]; la distribución de responsables depende de la ubicación de la caja y del horario, lo que amplía el rol operativo de GYE como referencia geográfica que organiza los escalamientos técnicos.

GYE funciona además como referencia geográfica en identificadores de dispositivos y logins auxiliares, por ejemplo el login auxiliar cscgvidanalit-mapa95mz17_1 con UM olt-hw-1-mapasingue6-gye 1/8, un uso concreto del sufijo "gye" como identificador de dispositivos dentro de la operación CSCG.

En el documento de corporativos se indica "Gestiona NOC MIMG logins con tn_wifi2_.... que sean de guayaquil y de quito los que esten en el siguiente listado del [Telcograf]", lo que sitúa a Guayaquil (GYE) como uno de los ámbitos geográficos de los logins gestionados por NOC MIMG. Asimismo, "Estimados Radios GYE por favor su ayuda con la tarea 102757614" muestra a GYE como destinatario de tareas de soporte dirigidas a los equipos de radio de la ciudad, y se verifica un enlace caído asociado al login auxiliar coopjipijapa-tterrestregye_1 con IP 181.39.39.230 y contacto 052600367, con UM sw2cc4ttgye.telconet.net Fa0/11, otro uso del sufijo "gye" en identificadores de dispositivos y logins auxiliares dentro de la operación de radio. Finalmente, se escala el caso 20240430-0187B por caída del servicio de clientes que dependen de la ruta "GYE-Miraflores 1-Puerto Hondo 1/Puerto Azul 1-F01", donde GYE forma parte de la ruta de enlaces y del escalamiento de incidencias.
## Entidades relacionadas

- [[entities/uio|UIO]]
- [[entities/opu-gye|OPU GYE]]
- [[entities/datacenter-boc|Datacenter BOC]]
- [[entities/fiberhome|FiberHome]]
- [[entities/hillstone|Hillstone]]

## Conceptos relacionados

- [[concepts/distribucion-zonas|Distribucion Zonas]]
- [[concepts/manos-remotas|Manos Remotas]]

## Menciones en la fuente

- "GYE  - Revisar personal de turno en correo" — [[Work/0. Directorio Telefonico|0. Directorio Telefonico]]
- "Monitoreo BOC GYE `0987231363`
Manos remotsas Datacenter GYE `099 812 2715`" — [[Work/0. Directorio Telefonico|0. Directorio Telefonico]]
- "# OPU GYE - Horario Laboral" — [[Work/0. Directorio Telefonico|0. Directorio Telefonico]]