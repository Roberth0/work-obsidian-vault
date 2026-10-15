---
type: entity
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/2-1-cscg_5bb2db]]"
tags:
aliases:
  - "oss.netlife.net.ec"
  - "Open Source Systems"
  - "Sistema OSS"
generation_complete: true
---

# OSS

## Descripción

El OSS es el sistema de gestión de red (Operations Support System) disponible en `https://oss.netlife.net.ec/dashboard`, empleado por el equipo de soporte para diagnosticar el estado de las [[OLT|OLTs]] y de las cajas. La fuente indica que se debe revisar en el OSS el estado de la OLT para determinar si está down y realizar el diagnóstico correspondiente, además de consultar el estado de los puertos para ubicar el puerto y la caja asociada. Cuando se verifica en el OSS una [[Caida de caja|caída de caja]], corresponde contactar al equipo [[OPU GYE]]. El sistema también expone el motivo del incidente desde su interfaz, el cual se registra junto al [[Motivo NOC y Motivo OSS|Motivo NOC]] en el seguimiento de las tareas. Existe una tarea RDA específica por problemas en el OSS, identificada con el número 131799124. Por su función de verificación de disponibilidad y de puertos, el OSS complementa las alarmas provenientes de [[Zabbix]] y la información de inventario asociada a [[ONT|ONTs]] y OLTs.

## Entidades relacionadas

- [[entities/zabbix|Zabbix]]
- [[entities/olt|OLT]]
- [[entities/ont|ONT]]
- [[entities/opu-gye|OPU GYE]]

## Conceptos relacionados

- [[concepts/caida-de-caja|Caida de caja]]
- [[concepts/corte-de-fibra|Corte de Fibra]]
- [[concepts/corte-de-ultima-milla|Corte de ultima Milla]]
- [[concepts/motivo-noc-y-motivo-oss|Motivo NOC y Motivo OSS]]

## Menciones en la fuente

- "Se debe revisar en el [OSS](https://oss.netlife.net.ec/dashboard) el estado de la OLT, si la OLT esta down se debe realizar el diagnostico" — [[Work/2.1 CSCG|2.1 CSCG]]
- "Al verificar en el OSS que se tiene una caida de caja se debe llamar a OPU GYE para ello se tiene la siguiente distrubucion de acuerdo a la ubicacion de la caja" — [[Work/2.1 CSCG|2.1 CSCG]]