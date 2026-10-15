---
type: entity
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/2-1-cscg_5bb2db]]"
tags:
aliases:
  - "Optical Line Terminal"
  - "OLTs"
  - "Terminal de Línea Óptica"
generation_complete: true
---

# OLT

## Descripción

La OLT (Optical Line Terminal) es el equipo óptico terminal del lado de la red cuya caída o estado *down* es un punto clave para el diagnóstico de incidencias en el contexto de [[CSCG]]. Según la fuente, el primer paso consiste en revisar el estado de la OLT en el [[OSS]] y, si se encuentra caída, proceder con el diagnóstico correspondiente.

En la opción de estado de puertos se debe buscar el puerto y la [[Caja|Caja]] a la cual está conectada dicha OLT, ya que esto permite determinar el alcance del problema. La fuente distingue dos escenarios: si todas las OLTs de la caja están caídas se trata de un problema masivo o [[Caida de caja|caída de caja]], mientras que si alguna OLT permanece activa el problema es puntual.

En el ejemplo de diagnóstico de la fuente se menciona la OLT identificada como `olt-hw-1-mapasingue6-gye`. Cuando la caída es puntual, se crea un caso dirigido a [[Andy Enrique Barberan Cortez|Andy Barberan]] y asignado a [[Adrian Bonilla|L1 Adrian Bonilla]].

## Entidades relacionadas

- [[entities/oss|OSS]]
- [[entities/ont|ONT]]
- [[entities/zabbix|Zabbix]]
- [[entities/andy-enrique-barberan-cortez|Andy Enrique Barberan Cortez]]

## Conceptos relacionados

- [[concepts/caida-de-caja|Caida de caja]]
- [[concepts/caida-de-ont-y-camaras|Caida de ONT y camaras]]
- [[concepts/corte-de-fibra|Corte de Fibra]]

## Menciones en la fuente

- "Se debe revisar en el [OSS](https://oss.netlife.net.ec/dashboard) el estado de la OLT, si la OLT esta down se debe realizar el diagnostico" — [[Work/2.1 CSCG|2.1 CSCG]]
- "Se debe verificar el tipo de caida, si todos las OLTs de la caja se encuentran caidas se debe a un problema masivo / caida de caja. Si ahi alguna OLT activa significa que el problema es puntual." — [[Work/2.1 CSCG|2.1 CSCG]]
- "UM: olt-hw-1-mapasingue6-gye 1/8." — [[Work/2.1 CSCG|2.1 CSCG]]