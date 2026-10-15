---
type: source
created: 2026-09-23
updated: 2026-09-23
source_file: "[[Work/1. Backbone.md]]"
tags: [backbone]
aliases: ["Backbone NOC", "Manual de Backbone Telconet"]
contentHash: 17ff-78024509
generation_complete: true
---

# 1. Backbone - Resumen

## Fuente

- Archivo original: [[Work/1. Backbone.md]]
- Ingerido: 2026-09-23

## Contenido principal

Documento operativo del NOC de [[entities/telconet|Telconet]] que recopila procedimientos, herramientas, credenciales y contactos de escalamiento para la gestión del [[entities/backbone|Backbone]]. Describe tareas de turno como la creación del chat de WhatsApp por parte del líder de grupo, el envío de la distribución del turno por Skype y el monitoreo de múltiples chats (Backbone Nacional, NOC-IPCCL1-Backbone, Eventos Netlife, Problemas masivos netlife, Netflow). Detalla herramientas clave como [[entities/digis|Digis]], [[entities/pruebas-l3|Pruebas L3]], el informe de Backbone Telcos y plataformas de monitoreo como [[entities/packetlight|PacketLight]], [[entities/fiberhome|FiberHome]], [[entities/arbor|Arbor]] y Zabbix. Incluye procedimientos de escalamiento para [[entities/alertas-dos|Alertas DoS]], [[entities/violaciones-de-mac|Violaciones de MAC]], fallas de LACP en RDA/OLT, enlaces STO Domingo, intermitencias en la metro y [[concepts/ventanas-de-mantenimiento|Ventanas de Mantenimiento]] de OTN. Finalmente enumera contactos y credenciales de organizaciones externas como [[entities/ufinet|UFINET]], TIGO, Fastly, NAP.EC Aeprovi y Metrovia.

## Entidades clave

- [[entities/telconet|Telconet]] — empresa operadora del Backbone
- [[entities/backbone|Backbone]] — red troncal objeto del manual
- [[entities/fiberhome|FiberHome]] — equipo de transmisión óptica
- [[entities/packetlight|PacketLight]] — equipo de transporte óptico (.246)
- [[entities/arbor|Arbor]] — plataforma de detección de ataques DoS
- [[entities/hillstone|Hillstone]] — firewall/equipo de seguridad
- [[entities/ufinet|UFINET]] — operador con portal de incidencias
- [[entities/digis|Digis]] — aplicativo de monitoreo ICMP/SSH
- [[entities/pruebas-l3|Pruebas L3]] — verificación de capa 3
- [[entities/snmp-v3|SNMP v3]] — protocolo de monitoreo (authPriv)
- [[entities/violaciones-de-mac|Violaciones de MAC]] — evento de red L2
- [[entities/alertas-dos|Alertas DoS]] — notificaciones de ataques
- [[entities/otn|OTN]], [[entities/opu|OPU]], [[entities/nw|NW]], [[entities/cert|CERT]] — contrapartes de escalamiento
- [[entities/teuno|Teuno]], [[entities/ibm|IBM]] — gestión de acceso a datacenter
- [[entities/uio|UIO]], [[entities/gye|GYE]] — jurisdicciones Quito y Guayaquil
- [[entities/backbone|1. Backbone]] — documento fuente

## Conceptos clave

- [[concepts/icmp|ICMP]] — verificación de conectividad
- [[concepts/ssh|SSH]] — acceso remoto y validación
- [[concepts/gepon-tap|GEPON TAP]] — responsable de escalamiento RDA/OLT
- [[concepts/ventanas-de-mantenimiento|Ventanas de Mantenimiento]] — intervenciones planificadas (VMs)
- [[concepts/veladas|Veladas]] — turnos nocturnos y asignación de roles
- [[concepts/errores-y-crcs|Errores y CRCs]] — umbral de 50 err/s en cámaras

## Puntos principales

- El líder de grupo crea el chat de WhatsApp y asigna roles; además envía la distribución del turno al grupo de Skype.
- El NOC debe estar pendiente de varios chats: Backbone Nacional, NOC-IPCCL1-Backbone, Eventos Netlife, Problemas masivos netlife y Netflow (Telegram).
- [[entities/digis|Digis]]: sin respuesta [[concepts/icmp|ICMP]] por 30-40 minutos se manda a revisar; para [[entities/uio|UIO]] o [[entities/gye|GYE]] sin ICMP se escala a [[entities/opu|OPU]], y sin respuesta [[concepts/ssh|SSH]] se escala la tarea a [[entities/nw|NW]].
- Las [[entities/pruebas-l3|Pruebas L3]] de UIO usan jurisdicción UIO, tipo "Todas" y reporte L3; si algún elemento sale en modo routed se valida en el equipo y se envía tarea a NW.
- [[entities/packetlight|PacketLight]]: reportar alarmas a [[entities/otn|OTN]] dando prioridad a alarmas Ethernet Link Failure.
- [[entities/arbor|Arbor]]: reportar [[entities/alertas-dos|Alertas DoS]] Ongoing o HIGH sin mitigar con tráfico mayor a 1 Gb y duración ≥ 10 min; considerar falsos positivos para 186.101.26.125 y 186.5.11.32 y notificar vía Telegram a [[entities/cert|CERT]].
- [[entities/snmp-v3|SNMP v3]]: comandos snmpwalk con authPriv (SHA/AES) usando credenciales estándar para equipos del Backbone y UPS; las respuestas SNMP de UPS se escalan a nivel nacional a Byron Reascos.
- Escalamientos: problemas de fibra en enlaces STO Domingo a Carlos Ureta; contacto de radio en Galápagos a Daniel Ushiña.
- Procedimientos de escalamiento RDA/OLT (alarmas LACP), intermitencias en la metro, ventanas programadas de OTN y revisiones de stacks de switch los lunes.
- Contactos externos y credenciales para [[entities/ufinet|UFINET]], TIGO, Fastly, NAP.EC Aeprovi, Metrovia y acceso a datacenter [[entities/ibm|IBM]] a través de clientes como [[entities/teuno|Teuno]].

## Páginas mencionadas

- [[entities/telconet|Telconet]]
- [[entities/fiberhome|FiberHome]]
- [[entities/packetlight|PacketLight]]
- [[entities/arbor|Arbor]]
- [[entities/hillstone|Hillstone]]
- [[entities/ufinet|UFINET]]
- [[entities/backbone|Backbone]]
- [[entities/digis|Digis]]
- [[entities/pruebas-l3|Pruebas L3]]
- [[entities/snmp-v3|SNMP v3]]
- [[entities/violaciones-de-mac|Violaciones de MAC]]
- [[entities/alertas-dos|Alertas DoS]]
- [[entities/otn|OTN]]
- [[entities/opu|OPU]]
- [[entities/nw|NW]]
- [[entities/cert|CERT]]
- [[entities/teuno|Teuno]]
- [[entities/ibm|IBM]]
- [[entities/uio|UIO]]
- [[entities/gye|GYE]]
- [[concepts/icmp|ICMP]]
- [[concepts/ssh|SSH]]
- [[concepts/gepon-tap|GEPON TAP]]
- [[concepts/ventanas-de-mantenimiento|Ventanas de Mantenimiento]]
- [[concepts/veladas|Veladas]]
- [[concepts/errores-y-crcs|Errores y CRCs]]

## Menciones en la fuente

- "Correo electrónico:  noc@telconet.ec     
Contraseña: Noctelconet123" — [[Work/1. Backbone|1. Backbone]]
- "- [I] vpn0.telconet.ec" — [[Work/1. Backbone|1. Backbone]]
- "### FiberHome
Conexion escritorio remoto 10.18.1.253
User: FIBERHOMEBK\nocuio
User: FIBERHOME" — [[Work/1. Backbone|1. Backbone]]
- "Acceso para el Fiberhome actulizado 29/03/2026" — [[Work/1. Backbone|1. Backbone]]
- "### PacketLight 
.246
Reportar alarmas a OTN // Dar prioridad a alarmas Ethernet Link Failure" — [[Work/1. Backbone|1. Backbone]]
- "### Arbor
Revisar Alertas DoS

 Se deben reportar las alarmas y tener en cuenta las siguientes consideraciones: " — [[Work/1. Backbone|1. Backbone]]
- "Tener en cuenta los falsos positivos para las IP's destino: 186.101.26.125, 186.5.11.32 
Se debe realizar la notificación via telegram a CERT" — [[Work/1. Backbone|1. Backbone]]
- "# Hillstone
`ssh -l noc-operator fwhdcgye1`
`ssh -l noc-operator fwhdcuio1`
`GyNterf$56&*%4s`" — [[Work/1. Backbone|1. Backbone]]
- "`show logging event | i exhausted`" — [[Work/1. Backbone|1. Backbone]]
- "### Revisar
[URL](http://172.30.147.31/zabbix/index.php)" — [[Work/1. Backbone|1. Backbone]]
- "# UFINET Portal incidencias

LINK: NUEVO PORTAL WEB - GENERACIÓN DE INCIDENCIAS
https://gestionticketing.ufinet.com/auth" — [[Work/1. Backbone|1. Backbone]]
- "# TIGO

"Gestion Plataformas" <GestionPlataformas@tigo.com.co>; 
"Lider De Turno Noc" <D-0461F@tigo.com.co>;" — [[Work/1. Backbone|1. Backbone]]
- "# Fastly

"Keith Wasserberger" <kwasserberger@fastly.com>; 
"Fastly Technical Operations" <techops@fastly.com>; 
jgreer@fastly.com; 
dci@fastly.com; 
"Didier Sorel" <dsorel@fastly.com>;" — [[Work/1. Backbone|1. Backbone]]
- "# NAP.EC Aeprovi
soporte@nap.ec" — [[Work/1. Backbone|1. Backbone]]
- "# Login Metrovia
User: ipccl2-gye1
Pass: `ct6yHH$rt230*t5`
`ssh -l ipccl2-gye1`" — [[Work/1. Backbone|1. Backbone]]
- "# Galapagos
Contacto Radio: Daniel Ushiña" — [[Work/1. Backbone|1. Backbone]]