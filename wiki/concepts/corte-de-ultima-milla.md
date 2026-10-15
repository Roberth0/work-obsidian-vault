---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/2-1-cscg_5bb2db]]"
tags:
aliases:
  - "Corte de UM"
  - "corte de última milla"
  - "Last Mile Cut"
generation_complete: true
---

# Corte de ultima Milla

## Definición

El **Corte de ultima Milla** es la causa de incidencia que se registra como *Motivo OSS* en las plantillas de seguimiento de [[CSCG]]. Corresponde a la interrupción del servicio atribuible al segmento de última milla de la red —el tramo que conecta la infraestructura del operador con el cliente final— y se consigna como tal en los formularios de registro de incidencias, en paralelo al *Motivo NOC*, que recoge la causa observada desde el [[noc]].

## Características clave

- Se registra como valor del campo **Motivo OSS**, diferenciándose del campo **Motivo NOC**, que documenta la causa reportada desde la perspectiva de la red.
- Aparece en al menos dos plantillas de seguimiento de CSCG: la de caída de [[ONT]] y la de [[Caida masiva|caídas masivas]], donde se abrevia como **Corte de UM**.
- Se documenta junto con los datos técnicos de la incidencia: *login aux*, dirección IP y UM de la [[OLT]] afectada.
- Su clasificación permite distinguir la causa observada desde el [[OSS]] de aquella reportada por el NOC, evitando atribuciones erróneas del origen del corte.
- Es un fenómeno de naturaleza operativa y de registro: no describe el fallo físico en sí, sino la categoría con la que el OSS clasifica la incidencia.

## Aplicaciones

- **Registro de incidencias en plantillas de seguimiento:** al documentar una caída de ONT, se consigna `Motivo NOC: Corte de Fibra` y `Motivo OSS: Corte de ultima Milla`, de modo que la causa física queda separada de la clasificación del OSS.
- **Gestión de caídas masivas:** en la plantilla equivalente para caídas masivas se emplea la forma abreviada `Motivo OSS: Corte de UM`, junto con los datos de la OLT afectada.
- **Análisis y reportería de indisponibilidad:** la correcta asignación de este motivo permite construir métricas de afectación por segmento de red y distinguirla de otras causas registradas en el mismo campo.
- **Escalamiento y correlación entre áreas:** facilita contrastar lo observado por el NOC con lo clasificado por el OSS durante la investigación de una incidencia.

## Conceptos relacionados

- [[concepts/corte-de-fibra|Corte de Fibra]]
- [[concepts/motivo-noc-y-motivo-oss|Motivo NOC y Motivo OSS]]
- [[concepts/caida-de-ont-y-camaras|Caida de ONT y camaras]]
- [[concepts/caida-de-caja|Caida de caja]]

## Entidades relacionadas

- [[entities/oss|OSS]]
- [[entities/olt|OLT]]
- [[entities/ont|ONT]]

## Menciones en la fuente

- "Motivo OSS: Corte de ultima Milla" — [[Work/2.1 CSCG|2.1 CSCG]]
- "Motivo NOC: Corte de Fibra
Motivo OSS: Corte de UM" — [[Work/2.1 CSCG|2.1 CSCG]]
- "UM: olt-hw-1-mapasingue6-gye 1/8." — [[Work/2.1 CSCG|2.1 CSCG]]