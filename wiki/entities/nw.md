---
type: entity
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/1-backbone_5939cb]]"
tags:
aliases:
  - "Network"
  - "Departamento NW"
generation_complete: true
---

# NW

## Descripción

NW es el área de red a la que el NOC escala las tareas que requieren cambios o validaciones sobre los equipos de red. Según el documento, cuando una tarea no obtiene respuesta por [[SSH]] debe escalarse a NW antes de continuar con cualquier intervención. Asimismo, antes de reiniciar un stack de switches —por ejemplo durante la revisión de switch stacks propia de la [[tecnica-sucursal|técnica de sucursal]]— es obligatorio confirmar la decisión con NW. Las alertas por tráfico superior al 90% también deben notificarse a NW a través del chat. Adicionalmente, NW mantiene un turno de standby de lunes a viernes de 6:00 p.m. a 10:00 p.m., fuera del horario laboral regular, lo que la convierte en el punto de contacto para intervenciones fuera de horario.

## Entidades relacionadas

- [[entities/opu|OPU]]
- [[entities/otn|OTN]]

## Conceptos relacionados

- [[concepts/tecnica-sucursal|tecnica-sucursal]]
- [[concepts/ssh|SSH]]

## Menciones en la fuente

- "Si no se tiene respuesta SSH se debe escalar la tarea a NW" — [[Work/1. Backbone|1. Backbone]]
- "Se debe notifcar a NW via chat" — [[Work/1. Backbone|1. Backbone]]
- "Confirmar con NW si se debe reiniciar el equipo" — [[Work/1. Backbone|1. Backbone]]
- "# Standby de NW" — [[Work/1. Backbone|1. Backbone]]