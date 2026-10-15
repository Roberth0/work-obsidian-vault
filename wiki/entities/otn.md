---
type: entity
created: 2026-09-23
updated: 2026-09-23
generation_complete: true
sources:
  - "[[sources/1-backbone_5939cb]]"
  - "[[sources/4-cedia_d7cef1]]"
tags:
aliases:
  - "Optical Transport Network"
  - "Área OTN"
---

# OTN

## Descripción

OTN es el área o departamento responsable de la red de transporte óptico al que se reportan las alarmas del equipo [[PacketLight]]. En el flujo operativo de backbone descrito en la fuente, OTN aparece como contraparte de escalamiento ante incidentes que superan el alcance del NOC. El documento indica que se debe dar prioridad a las alarmas de "Ethernet Link Failure" al momento de reportar a OTN. Asimismo, existe un procedimiento de "Ventanas Programadas de OTN" en el que el [[noc]] debe llamar para preguntar por novedades sobre las VMs planificadas y escalar una tarea de informe técnico al finalizar cada ventana. Por su rol de escalamiento, OTN se relaciona directamente con los demás involucrados del backbone, como [[Telconet]] y [[OPU]].

## Entidades relacionadas

- [[entities/packetlight|PacketLight]]
- [[entities/telconet|Telconet]]
- [[entities/opu|OPU]]

## Conceptos relacionados

- [[concepts/ventanas-de-mantenimiento|Ventanas de Mantenimiento]]
- [[concepts/gepon-tap|GEPON TAP]]

## Menciones en la fuente

- "Reportar alarmas a OTN // Dar prioridad a alarmas Ethernet Link Failure" — [[Work/1. Backbone|1. Backbone]]
- "# Ventanas Programadas de OTN" — [[Work/1. Backbone|1. Backbone]]
- "Se debe llamar a preguntar cualquier novedad sobre las VMs planificadas" — [[Work/1. Backbone|1. Backbone]]