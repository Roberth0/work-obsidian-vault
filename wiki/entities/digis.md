---
type: entity
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/1-backbone_5939cb]]"
tags:
aliases:
  - "Aplicativo Digis"
  - "Digis NOC"
generation_complete: true
---

# Digis

## Descripción

Digis es una herramienta o aplicativo de monitoreo utilizado por el NOC (Network Operations Center) para verificar la respuesta de los equipos de red. Su función principal es determinar la existencia de respuesta ICMP: cuando el aplicativo muestra el icono del rayo en verde o indica "conectado", se confirma que sí existe respuesta ICMP hacia el equipo monitoreado. La ausencia de dicha respuesta durante aproximadamente 30 o 40 minutos constituye un criterio operativo para enviar el equipo a revisión. En el contexto de [[Telconet]], las sedes [[UIO]] y [[GYE]] presentan flujos de escalamiento diferenciados ante fallas de conectividad detectadas mediante Digis. Digis es, por tanto, un punto clave en el diagnóstico y escalamiento de la conectividad del [[Backbone]].

Los criterios de escalamiento asociados a Digis son los siguientes: si no existe respuesta ICMP en UIO o GYE, el caso debe escalarse a [[OPU]]; si además no hay respuesta SSH, la tarea debe escalarse a [[NW]]. Estas reglas se aplican durante las [[Pruebas L3]], donde la verificación de conectividad y el diagnóstico de fallas requieren evidencia objetiva del estado de los equipos.

## Entidades relacionadas

- [[entities/telconet|Telconet]]
- [[entities/backbone|Backbone]]
- [[entities/pruebas-l3|Pruebas L3]]

## Conceptos relacionados

## Menciones en la fuente

- "### Digis
Si no se tiene respuesta ICMP por unos 30 o 40 minutos, se debe mandar a revisar
Si en el aplicativo se encuentra el icono del rayo en verde / o dice conectado es que **si se tiene respuesta ICMP**" — [[Work/1. Backbone|1. Backbone]]
- "Para UIO o GYE al no tener respuesta ICMP se debe escalar a OPU
Si no se tiene respuesta SSH se debe escalar la tarea a NW" — [[Work/1. Backbone|1. Backbone]]