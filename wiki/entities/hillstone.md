---
type: entity
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/1-backbone_5939cb]]"
tags:
aliases:
  - "Hillstone Networks"
  - "Firewall Hillstone"
  - "Hillstone Firewall"
generation_complete: true
---

# Hillstone

## Descripción

Hillstone es un firewall o equipo de seguridad de red fabricado por Hillstone Networks, gestionado por el NOC (Network Operations Center) de [[Telconet]] mediante conexiones SSH. En la documentación operativa se registran los comandos de acceso a dos nodos: `ssh -l noc-operator fwhdcgye1` para el nodo de Guayaquil (GYE) y `ssh -l noc-operator fwhdcuio1` para el nodo de Quito (UIO), ambos con el usuario `noc-operator` y su contraseña asociada. Para el diagnóstico de eventos de agotamiento de recursos se emplea el comando `show logging event | i exhausted`, que filtra los registros del sistema por dicho patrón. Hillstone se integra en las tareas de monitoreo del [[Backbone]] junto a otras plataformas como [[FiberHome]], PacketLight y [[Zabbix]]. Su nomenclatura de host sigue el patrón `fw` + código de sitio (`hdcgye1`, `hdcuio1`), coherente con la convención de nombrado de los nodos de red de la infraestructura.

## Entidades relacionadas

- [[entities/telconet|Telconet]]
- [[entities/fiberhome|FiberHome]]
- [[entities/backbone|Backbone]]

## Conceptos relacionados

## Menciones en la fuente

- "# Hillstone
`ssh -l noc-operator fwhdcgye1`
`ssh -l noc-operator fwhdcuio1`
`GyNterf$56&*%4s`" — [[Work/1. Backbone|1. Backbone]]
- "`show logging event | i exhausted`" — [[Work/1. Backbone|1. Backbone]]