---
type: entity
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/1-backbone_5939cb]]"
tags:
aliases:
  - "Arbor Networks"
  - "Arbor Networks Peakflow"
  - "Peakflow"
generation_complete: true
---

# Arbor

## Descripción

Arbor es la plataforma de detección y mitigación de ataques de denegación de servicio (DoS) utilizada por el [[Telconet|NOC]] para revisar las [[Alertas DoS]] generadas sobre el [[Backbone]]. El documento de referencia describe las consideraciones para reportar alarmas: que éstas se encuentren en ejecución (Ongoing) o sean de severidad HIGH (rojas) sin mitigar, con tráfico superior a 1 Gb y una duración igual o superior a 10 minutos. Asimismo, advierte sobre falsos positivos para las IP de destino 186.101.26.125 y 186.5.11.32, y establece que la notificación de los eventos se realiza vía Telegram a CERT. Arbor ocupa un rol central en la gestión de ataques volumétricos dirigidos contra la infraestructura del Backbone.

## Entidades relacionadas

- [[entities/telconet|Telconet]]
- [[entities/alertas-dos|Alertas DoS]]
- [[entities/backbone|Backbone]]

## Conceptos relacionados

## Menciones en la fuente

- "### Arbor
Revisar Alertas DoS

 Se deben reportar las alarmas y tener en cuenta las siguientes consideraciones: " — [[Work/1. Backbone|1. Backbone]]
- "Tener en cuenta los falsos positivos para las IP's destino: 186.101.26.125, 186.5.11.32 
Se debe realizar la notificación via telegram a CERT" — [[Work/1. Backbone|1. Backbone]]