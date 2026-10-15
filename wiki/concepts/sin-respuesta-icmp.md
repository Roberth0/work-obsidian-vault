---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/2-1-cscg_5bb2db]]"
tags:
aliases:
  - "Motivo OSS: Sin respuesta ICMP"
  - "no respuesta ICMP"
  - "No ICMP response"
generation_complete: true
---

# Sin respuesta ICMP

## Definición

"Sin respuesta ICMP" es el motivo del [[OSS]] que corresponde a la caída de cámara ("Camara Down") dentro del listado de motivos documentado. Indica que la verificación mediante ping al dispositivo no obtiene respuesta alguna, lo que confirma la caída del equipo desde la perspectiva del sistema de gestión. El término articula así la acción de monitoreo (ping) con la clasificación del incidente en el OSS.

## Características clave

- Es un **motivo de OSS**, es decir, una categoría de clasificación de incidentes registrada por el sistema de gestión.
- Se corresponde de forma directa con la condición de caída de cámara ("Camara Down").
- Su evidencia técnica es la **ausencia de respuesta a una solicitud ICMP (ping)**: el dispositivo no contesta.
- Es una condición **verificable y automatizable**, ya que se determina a partir del resultado de una comprobación de red.
- No describe una causa raíz (energía, red, configuración), sino un **síntoma observable** desde la red.
- Se ubica en el mismo listado de motivos que [[Motivo NOC y Motivo OSS]], por lo que sirve de puente entre la clasificación del NOC y la del OSS.

## Aplicaciones

- **Diagnóstico de caída de cámaras:** el procedimiento de diagnóstico de caída de cámaras utiliza esta condición como criterio; si el dispositivo no responde al ping, se determina que está caído.
- **Apertura automática de casos:** cuando se verifica la ausencia de respuesta ICMP, se crea un caso desde [[Zabbix]], lo que permite pasar del monitoreo a la gestión del incidente sin intervención manual.
- **Clasificación en el OSS:** permite etiquetar el incidente con un motivo estandarizado, facilitando el reporte, la trazabilidad y el análisis de recurrencia de caídas.
- **Distinción frente a otros motivos:** al ser un síntoma de red, ayuda a diferenciar las caídas reales de [[Camaras]] de otras causas registradas en el listado de motivos.
- **Monitoreo y alertamiento:** sirve como disparador de alertas en plataformas de monitoreo que comprueban conectividad por ICMP.

## Conceptos relacionados

- [[concepts/caida-de-camaras|Caida de camara/s]]
- [[concepts/motivo-noc-y-motivo-oss|Motivo NOC y Motivo OSS]]

## Entidades relacionadas

- [[entities/camaras|Camaras]]
- [[entities/oss|OSS]]
- [[entities/zabbix|Zabbix]]

## Menciones en la fuente

- "Motivo OSS: Sin respuesta ICMP" — [[Work/2.1 CSCG|2.1 CSCG]]
- "Si se verifica que no se tiene respuesta ICMP se debe crear un caso por la caida de la camara/s desde el zabbix" — [[Work/2.1 CSCG|2.1 CSCG]]