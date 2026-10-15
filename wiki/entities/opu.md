---
type: entity
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/1-backbone_5939cb]]"
tags:
aliases:
  - "Operaciones OPU"
  - "Operations OPU"
generation_complete: true
---

# OPU

## Descripción

OPU es el área de operaciones a la que se escalan las tareas cuando se detectan fallas que el [[noc]] no puede resolver por sí mismo. En el flujo descrito en la fuente, cuando [[UIO]] o [[GYE]] no obtienen respuesta [[ICMP]], el caso debe escalarse a OPU; del mismo modo, para revisar intermitencias en la red metro se crea un caso asignado a OPU.

OPU también aparece en el contexto del seguimiento de switch stacks, donde asume los cambios de software y la revisión de stacks en conjunto con [[TS]]. Por este rol, OPU funciona como una de las contrapartes operativas clave dentro del proceso de escalamiento documentado, interactuando además con elementos de la red como [[OTN]] y [[NW]].

## Entidades relacionadas

- [[entities/uio|UIO]]
- [[entities/gye|GYE]]
- [[entities/otn|OTN]]
- [[entities/nw|NW]]

## Conceptos relacionados

- [[concepts/icmp|ICMP]]

## Menciones en la fuente

- "Para UIO o GYE al no tener respuesta ICMP se debe escalar a OPU" — [[Work/1. Backbone|1. Backbone]]
- "Se debe crear el caso asignado a OPU para la revision del enlace que este dando problemas" — [[Work/1. Backbone|1. Backbone]]
- "OPU - Cambios de sw, revision de stck" — [[Work/1. Backbone|1. Backbone]]