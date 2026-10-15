---
type: entity
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/2-1-cscg_5bb2db]]"
tags:
aliases:
  - "cámara/s"
  - "Camara"
  - "Cámaras de videovigilancia"
generation_complete: true
---

# Camaras

## Descripción

Las **Camaras** son los dispositivos de videovigilancia monitoreados dentro de la operación [[CSCG]], con presencia tanto en [[Machala]] y [[Salinas]] como en la zona de [[GYE]]. Su estado operativo se diagnostica siguiendo procedimientos concretos: primero se verifica la [[OLT]] en el [[OSS]] y, cuando se trata de una sola cámara caída, la OLT debería encontrarse activa. Posteriormente se realiza [[ping]] hacia la cámara utilizando la pestaña «lógico», conociendo su dirección IP a través del inventario de [[Zabbix]]. Si no hay respuesta [[ICMP]], se crea un caso por la [[Caida de camara/s|caída de la cámara]] desde el Zabbix, y durante ese flujo puede aparecer el [[Error 300]]. Las cámaras también están ligadas a la [[grabación analítica con IA]], por lo que su disponibilidad condiciona la continuidad de ese proceso.

## Entidades relacionadas

- [[entities/oss|OSS]]
- [[entities/olt|OLT]]
- [[entities/zabbix|Zabbix]]

## Conceptos relacionados

- [[concepts/caida-de-camaras|Caida de camara/s]]
- [[concepts/sin-respuesta-icmp|Sin respuesta ICMP]]
- [[concepts/error-300|Error 300]]

## Menciones en la fuente

- "OLT y Camaras de Machala y Salinas" — [[Work/2.1 CSCG|2.1 CSCG]]
- "Se debe verificar el estado de la OLT en el [OSS](https://oss.netlife.net.ec/dashboard) para realizar el diagnostico, al ser solo una camara/s la OLT se deberia encontrar activa" — [[Work/2.1 CSCG|2.1 CSCG]]
- "Si se verifica que no se tiene respuesta ICMP se debe crear un caso por la caida de la camara/s desde el zabbix" — [[Work/2.1 CSCG|2.1 CSCG]]