---
type: entity
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/2-1-cscg_5bb2db]]"
tags:
aliases:
  - "Optical Network Terminal"
  - "ONT caída"
  - "Terminal de Red Óptica"
generation_complete: true
---

# ONT

## Descripción

La **ONT** (Optical Network Terminal) es el equipo óptico de cliente que actúa como punto terminal de la red de acceso y cuya caída constituye uno de los eventos disparadores de alertas y casos dentro del flujo operativo de CSCG. Según la fuente, ante la caída de una ONT se debe crear el caso desde [[Zabbix]] y luego escalar la tarea conforme a la distribución de zonas de GYE, derivando el caso a L1. La ONT se ubica aguas abajo de la [[OLT]] y su estado se refleja en las plataformas de monitoreo y de gestión, como [[OSS]].

Además de la caída, la temperatura del equipo es una métrica monitoreada: en el ejemplo de diagnóstico se registra una ONT caída asociada al login aux `cscgvidanalit-mapa95mz17_1` con IP `10.211.16.15`, y también se reporta temperatura elevada sobre una ONT identificada como `tncto-pasillocoworking-gye` con `VALUE: 51 C`. La ONT aparece tanto en casos de [[Caida de caja|caída de caja]] como en caídas puntuales de cámaras, lo que la convierte en un elemento transversal en el diagnóstico de incidentes de acceso. El seguimiento operativo de estos eventos recae en personal como [[Andy Enrique Barberan Cortez]].

## Entidades relacionadas

- [[entities/zabbix|Zabbix]]
- [[entities/olt|OLT]]
- [[entities/oss|OSS]]
- [[entities/andy-enrique-barberan-cortez|Andy Enrique Barberan Cortez]]

## Conceptos relacionados

- [[concepts/caida-de-caja|Caida de caja]]
- [[concepts/temperatura-elevada|Temperatura elevada]]
- [[concepts/corte-de-fibra|Corte de Fibra]]
- [[concepts/corte-de-ultima-milla|Corte de ultima Milla]]

## Menciones en la fuente

- "Se debe crear el caso desde el zabbix por la caida de la ONT" — [[Work/2.1 CSCG|2.1 CSCG]]
- "Mediante monitoreo se verifica ONT caído, asociado al login aux: cscgvidanalit-mapa95mz17_1. IP: 10.211.16.15. Se envia vía mail la notificación. UM: olt-hw-1-mapasingue6-gye 1/8." — [[Work/2.1 CSCG|2.1 CSCG]]
- "Estimado @+593 99 871 8125 (Andy Barberan) se asigna la tarea 107853621 || Temperatura elevada ONT: tncto-pasillocoworking-gye VALUE: 51 C" — [[Work/2.1 CSCG|2.1 CSCG]]