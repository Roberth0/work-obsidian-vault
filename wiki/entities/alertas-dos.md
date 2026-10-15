---
type: entity
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/1-backbone_5939cb]]"
tags:
aliases:
  - "Alertas de Denial of Service"
  - "Ataques DoS"
  - "Denegación de servicio"
generation_complete: true
---

# Alertas DoS

## Descripción

Las **Alertas DoS** son notificaciones de posibles ataques de denegación de servicio (Denial of Service) detectadas por la plataforma [[Arbor]] y gestionadas por el [[noc]] sobre la infraestructura del [[Backbone]] de [[Telconet]]. El procedimiento asociado establece los criterios que debe cumplir una alerta para ser reportada: que esté en ejecución (*Ongoing*) o que sea clasificada como HIGH (roja) sin mitigar, con un tráfico superior a 1 Gb y una duración igual o superior a 10 minutos. El documento advierte además sobre la necesidad de considerar falsos positivos cuando el tráfico se dirige a determinadas IP de destino específicas. La notificación de las alertas que cumplen los criterios se realiza vía Telegram al equipo [[CERT]]. De este modo, el procedimiento conecta la plataforma de detección [[Arbor]] con el equipo [[CERT]] y con la operación diaria del [[Backbone]].

## Entidades relacionadas

- [[entities/telconet|Telconet]]
- [[entities/arbor|Arbor]]
- [[entities/backbone|Backbone]]

## Conceptos relacionados

## Menciones en la fuente

- "### Arbor
Revisar Alertas DoS" — [[Work/1. Backbone|1. Backbone]]
- " Se deben reportar las alarmas y tener en cuenta las siguientes consideraciones: 
- [ ]  Que se encuentren en ejecución (Ongoing) 
- [ ] o HIGH (Rojas) que no hayan sido mitigadas. 
- [ ]  Trafico mayor a 1gb. 
- [ ] Tiempo de duración >= a 10 min." — [[Work/1. Backbone|1. Backbone]]