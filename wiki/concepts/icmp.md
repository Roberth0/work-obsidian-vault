---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/1-backbone_5939cb]]"
tags:
aliases:
  - "Internet Control Message Protocol"
  - "Protocolo de Mensajes de Control de Internet"
  - "respuesta ICMP"
generation_complete: true
---

# ICMP

## Definición

ICMP (Internet Control Message Protocol) es el protocolo de la capa de red utilizado para verificar la conectividad de los enlaces de los equipos [[Digis]]. En el contexto operativo descrito por la fuente, la presencia o ausencia de respuesta ICMP constituye el principal indicador de disponibilidad de dichos equipos, por encima de otras señales de estado.

## Características clave

- Es el mecanismo de verificación de conectividad empleado sobre los enlaces de los equipos [[Digis]].
- La ausencia de respuesta ICMP durante aproximadamente 30 o 40 minutos constituye el criterio para enviar el equipo a revisión.
- La presencia de respuesta ICMP se refleja en indicadores visuales y de aplicación: el ícono del rayo en verde o el estado «conectado» en el aplicativo.
- Su ausencia sostenida activa un procedimiento de escalamiento diferenciado por sitio: para [[UIO]] o [[GYE]] obliga a escalar a [[OPU]].
- Funciona como indicador binario (hay o no hay respuesta), lo que lo hace simple de monitorear pero sensible a cortes de enlace o caídas del equipo.

## Aplicaciones

- **Monitoreo de disponibilidad**: verificación continua de que los equipos [[Digis]] mantienen conectividad de red activa.
- **Gestión de incidencias**: la falta de respuesta ICMP por 30 o 40 minutos dispara el envío del equipo a revisión técnica.
- **Escalamiento operativo**: en los sitios [[UIO]] y [[GYE]], la ausencia de respuesta ICMP es el criterio que obliga a escalar el caso a [[OPU]].
- **Validación de estado en el aplicativo**: la confirmación visual del ícono del rayo en verde o del estado «conectado» permite corroborar que existe respuesta ICMP.
- **Diagnóstico complementario**: suele combinarse con el acceso remoto vía [[SSH]] para distinguir entre un problema de red y un problema a nivel de equipo.

## Conceptos relacionados

- [[concepts/ssh|SSH]]

## Entidades relacionadas

- [[entities/digis|Digis]]
- [[entities/opu|OPU]]
- [[entities/uio|UIO]]
- [[entities/gye|GYE]]

## Menciones en la fuente

- "Si no se tiene respuesta ICMP por unos 30 o 40 minutos, se debe mandar a revisar" — [[Work/1. Backbone|1. Backbone]]
- "Si en el aplicativo se encuentra el icono del rayo en verde / o dice conectado es que **si se tiene respuesta ICMP**" — [[Work/1. Backbone|1. Backbone]]
- "Para UIO o GYE al no tener respuesta ICMP se debe escalar a OPU" — [[Work/1. Backbone|1. Backbone]]