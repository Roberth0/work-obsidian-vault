---
type: entity
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/1-backbone_5939cb]]"
tags:
aliases:
  - "Packet Light"
generation_complete: true
---

# PacketLight

## Descripción

PacketLight es un equipo de transporte óptico monitoreado por el NOC, asociado al identificador `.246`. Según el documento de referencia, sus alarmas deben reportarse a [[OTN|OTN]] (Optical Transport Network), dando prioridad a las alarmas de tipo *Ethernet Link Failure*. Este procedimiento vincula a PacketLight directamente con la tecnología OTN y con las [[Ventanas Programadas de OTN]] descritas más adelante en el documento. Se trata de una de las plataformas de transmisión clave para la operación del [[Backbone]], junto a [[FiberHome]] y [[Hillstone]].

## Entidades relacionadas

- [[entities/telconet|Telconet]]
- [[entities/fiberhome|FiberHome]]
- [[entities/backbone|Backbone]]

## Conceptos relacionados

- [[concepts/ventanas-de-mantenimiento|Ventanas Programadas de OTN]]

## Menciones en la fuente

- "### PacketLight 
.246
Reportar alarmas a OTN // Dar prioridad a alarmas Ethernet Link Failure" — [[Work/1. Backbone|1. Backbone]]