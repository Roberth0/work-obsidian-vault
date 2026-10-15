---
type: entity
created: 2026-09-23
updated: 2026-09-23
generation_complete: true
type_confirmed: true
sources:
  - "[[sources/1-backbone_5939cb]]"
  - "[[sources/1-2-backbone-proveedores-internacionales_861235]]"
tags:
  - "person"
  - "term"
aliases:
  - "Backbone Nacional"
  - "NOC-IPCCL1-Backbone"
  - "Red Troncal"
  - "1. Backbone"
---

# Backbone

## Descripción

El Backbone es la red troncal de [[Telconet]] y su operación constituye el objeto central del documento de origen, identificado con la etiqueta 'backbone' en su frontmatter. Su monitoreo se realiza a través de varios chats de operación, entre ellos 'Backbone Nacional' y 'NOC-IPCCL1-Backbone'. A lo largo del texto se detallan procedimientos asociados a la red troncal, como la revisión de alertas de tráfico superior al 90%, la ejecución de [[Pruebas L3]], el escalamiento de fallas de fibra y la coordinación de [[Ventanas Programadas de OTN]]. Sobre esta red convergen equipos de transmisión como los de [[FiberHome]] y [[PacketLight]], además de la gestión de [[Alertas DoS]] y los contactos con operadores externos como [[Digis]]. El Backbone articula, por tanto, las plataformas técnicas, los procedimientos operativos y los canales de escalamiento descritos en la fuente.

Las tareas de turno del Backbone incluyen la creación del chat de WhatsApp por parte del líder de grupo y la asignación de roles a los demás integrantes del turno; en caso de ser líder, este debe enviar la distribución del turno al grupo de Skype. A los chats de monitoreo ya mencionados se suman 'Eventos Netlife', 'Problemas masivos netlife' y el chat de Telegram 'Netflow'. Entre las plataformas de monitoreo figuran Arbor, empleada para la revisión de [[Alertas DoS]] con criterios como Ongoing, HIGH no mitigadas, tráfico superior a 1 Gb y duración mayor o igual a 10 minutos, con reporte a CERT vía Telegram, y Zabbix (http://172.30.147.31/zabbix/index.php).

Los procedimientos de escalamiento adicionales abarcan violaciones de MAC (tarea de ejemplo a L2 116829309), fallas de LACP en RDA/OLT (GEPON TAP GYE: Andres Xavier Rogel Valarezo; UIO: Juan Carlos Chavez Alarcon), intermitencia en la metro (creación de caso a OPU y tarea de eventos para parar tiempos de afectación), enlaces STO Domingo y revisión de power supply en Huawei (disp power / disp device). Los responsables internos de escalamiento son Daniel Ushiña (contacto radio en Galápagos), Carlos Ureta (problemas de fibra en enlaces STO Domingo) y Byron Reascos (respuesta SNMP en UPS, notificada en el chat 'Configuraciones Monitoreo').

Los casos de backbone requieren la creación de una tarea asignada al perfil del operador para dar seguimiento del tiempo hasta que se solvente el incidente; una vez resuelto, se genera una tarea de RFO, procedimiento operativo que complementa los ya descritos.

La dimensión internacional del Backbone de [[Telconet]] se organiza mediante niveles de escalamiento y contactos de proveedores como [[Akamai]], Cables & Wireless (C&W), [[PCCW]], [[Sparkle]], [[Claro]] y [[CNT]], con listas de correos específicas, logins de circuitos CNT (cnt-burts, cnt-inaquito-bogota, tn-cnt-salinas, tn-cnt-manta), el circuito UFINET ECCOTEL10267004C asociado a Edge uno, las credenciales del Portal Arelion y la referencia al nodo PE05CAR.

El enlace a la herramienta de salidas internacionales (NetFlow) constituye el punto de partida para revisar el estado de la red troncal.
## Entidades relacionadas

- [[entities/telconet|Telconet]]
- [[entities/fiberhome|FiberHome]]
- [[entities/packetlight|PacketLight]]
- [[entities/digis|Digis]]
- [[entities/pruebas-l3|Pruebas L3]]
- [[entities/alertas-dos|Alertas DoS]]
- [[entities/ufinet|UFINET]]
- [[entities/tigo|TIGO]]
- [[entities/fastly|Fastly]]
- [[entities/napec-aeprovi|NAP.EC Aeprovi]]
- [[entities/metrovia|Metrovia]]

## Conceptos relacionados

- [[concepts/ventanas-de-mantenimiento|Ventanas Programadas de OTN]]

## Menciones en la fuente

- "Estar pendiente de los siguientes chats
- [ ] Backbone Nacional
- [ ] NOC-IPCCL1-Backbone" — [[Work/1. Backbone|1. Backbone]]
- "### Informe de Backbone Telcos" — [[Work/1. Backbone|1. Backbone]]