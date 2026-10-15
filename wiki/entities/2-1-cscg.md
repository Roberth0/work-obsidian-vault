---
type: entity
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/2-1-cscg_5bb2db]]"
tags:
aliases:
  - "CSCG"
  - "Monitoreo CSCG"
generation_complete: true
---

# 2.1 CSCG

## Descripción

CSCG es el área responsable del monitoreo y la gestión de incidencias vinculada a la red de [[VIPS]]. Sus procedimientos operativos cubren las alertas provenientes del sistema de monitoreo [[Zabbix]] y del [[OSS]]: caída de [[OLT]] y cámaras en Machala y Salinas, caída de caja, temperatura elevada en [[ONT]] y caída de ONT o cámaras individuales. Para cada escenario se especifican pasos concretos, como crear el caso en Zabbix, escalar la tarea o el caso a los niveles L1 y TS, verificar el estado de puertos y OLTs, y notificar a personas determinadas. El documento también define la distribución de responsables por horario y zona para caídas masivas de cajas —Miguel Angel Montoya, Erick Uscocovich y Marlon Brito—, los formatos de comentarios en el chat de WhatsApp de Monitoreo CSCG, las plantillas de motivos NOC/OSS y el tratamiento del error 300 de Inteligencia Artificial. Finalmente, se menciona la tarea RDA 131799124 por problemas en el OSS.

## Entidades relacionadas

- [[entities/zabbix|Zabbix]]
- [[entities/oss|OSS]]
- [[entities/olt|OLT]]

## Conceptos relacionados