---
type: entity
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/1-backbone_5939cb]]"
tags:
aliases:
  - "SNMPv3"
  - "Simple Network Management Protocol v3"
  - "SNMP versión 3"
generation_complete: true
---

# SNMP v3

## Descripción

SNMP v3 (Simple Network Management Protocol versión 3) es el protocolo de monitoreo de red empleado para consultar los equipos del [[Backbone]] y los sistemas UPS de [[Telconet]]. Su uso se documenta mediante comandos `snmpwalk` configurados con los niveles de autenticación y privacidad propios de esta versión (authPriv), utilizando los algoritmos SHA para autenticación y AES para cifrado. El documento de referencia define credenciales estándar por dispositivo: `Estandar3PDU-TN` para el host `10.211.11.171` y `EstandarSNMPupsTN` para el UPS `172.19.10.11`. La validación de la respuesta SNMP en equipos UPS cuenta con un procedimiento de escalamiento de alcance nacional, asignado a [[Byron Reascos]], cuya notificación se realiza en el chat "Configuraciones Monitoreo". Por su capacidad de autenticación y cifrado, SNMP v3 resulta esencial para el monitoreo automatizado de la infraestructura del Backbone.

## Entidades relacionadas

- [[entities/telconet|Telconet]]
- [[entities/backbone|Backbone]]

## Conceptos relacionados

## Menciones en la fuente

- "# SNMP v3
snmpwalk -v3 -a SHA -u 1E9mpv24 -l authPriv -A 'Estandar3PDU-TN' -x AES -X 'Estandar3PDU-TN' 10.211.11.171" — [[Work/1. Backbone|1. Backbone]]
- "# SNMP v3 UPS
`snmpwalk -v3 -a SHA -u 1E9mpv24 -l authPriv -A 'EstandarSNMPupsTN' -x AES -X 'EstandarSNMPupsTN' 172.19.10.11`" — [[Work/1. Backbone|1. Backbone]]