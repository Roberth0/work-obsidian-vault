---
type: entity
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/1-backbone_5939cb]]"
tags:
aliases:
  - "MAC violations"
  - "Violación de MAC"
  - "MAC address violations"
generation_complete: true
---

# Violaciones de MAC

## Descripción

Las Violaciones de MAC son un evento de red que el [[noc]] debe gestionar cuando se detecta un exceso de direcciones MAC aprendidas en un puerto o en un equipo. Este evento aparece tratado en una sección propia de la documentación de [[Telconet]], donde se describe el procedimiento asociado al [[Backbone]] y se genera una tarea de ejemplo a nivel L2 con el número 116829309.

En la práctica, una violación de MAC suele ser un síntoma de bucles de red (loops) o de configuraciones incorrectas de las políticas de seguridad en los switches, ya que la tabla de direcciones MAC de un puerto supera el límite permitido y el equipo bloquea o restringe el tráfico. Por este motivo, el procedimiento está vinculado directamente a las tareas de capa 2 y al escalamiento hacia los equipos de [[NW]] o [[L2]] cuando la causa raíz no puede resolverse en el primer nivel de soporte.

Su gestión forma parte de las actividades de monitoreo y aseguramiento de la red, junto con otras verificaciones de conectividad como las [[Pruebas L3]], que cubren el diagnóstico complementario en capas superiores.

## Entidades relacionadas

- [[entities/telconet|Telconet]]
- [[entities/backbone|Backbone]]
- [[entities/pruebas-l3|Pruebas L3]]

## Conceptos relacionados

## Menciones en la fuente

- "# Violaciones de MAC
 Tarea de ejemplo a L2  116829309" — [[Work/1. Backbone|1. Backbone]]