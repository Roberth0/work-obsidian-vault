---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/4-cedia_d7cef1]]"
tags:
aliases:
  - "pérdida de enlace"
  - "alarma link loss"
  - "link loss alarm"
generation_complete: true
---

# link loss

## Definición

**link loss** (pérdida de enlace) es la alarma de pérdida de conectividad de un enlace de red y constituye la alarma de atención prioritaria dentro de la gestión de monitoreo de CEDIA. Se manifiesta cuando un enlace monitoreado deja de responder, por lo que su revisión determina la afectación real de los servicios entregados a los clientes.

## Características clave

- **Prioridad alta**: es la primera alarma que debe atenderse al recibir un reporte, por encima de otras alertas del monitoreo.
- **Diagnóstico por extremos**: ante su detección se deben localizar los extremos correspondientes al enlace, comenzando por el Concentrador de Ambato.
- **Verificación de redundancia**: se debe comprobar cuántos enlaces posee el dispositivo afectado, ya que la existencia de enlaces alternos condiciona el impacto.
- **Medición del tiempo de caída**: la duración de la interrupción se determina mediante comandos de consulta sobre la configuración del equipo, como `show lag description | match UNIANDES` y `show port 2/3/2 | match tate`.
- **Indicador de impacto al cliente**: su atención permite establecer la afectación real de los servicios prestados a los clientes.
- **Vinculada al escalamiento**: su gestión se articula con los procedimientos de escalamiento hacia CEDIA.

## Aplicaciones

- **Gestión de monitoreo de red**: identificación y priorización de alarmas de pérdida de enlace en la operación del NOC.
- **Diagnóstico de incidentes**: localización de los extremos del enlace y verificación del número de enlaces disponibles para acotar el alcance del problema.
- **Cálculo de indisponibilidad**: determinación del tiempo de caída del enlace como insumo para la evaluación de afectación a clientes.
- **Escalamiento operativo**: activación de los procedimientos de escalamiento a CEDIA cuando la alarma compromete servicios críticos.
- **Correlación con diagnósticos de servicio**: uso conjunto con las verificaciones realizadas en SAM CLIENT.

## Conceptos relacionados

- [[concepts/informe-ejecutivo|Informe Ejecutivo]]
- [[concepts/vpn|VPN]]

## Entidades relacionadas

- [[entities/cedia|CEDIA]]
- [[entities/sam-client|SAM CLIENT]]
- [[entities/nokia|Nokia]]

## Menciones en la fuente

- "dar prioridad a alarmas link loss." — [[Work/4 Cedia|4 Cedia]]
- "show lag description | match UNIANDES" — [[Work/4 Cedia|4 Cedia]]
- "Verificar tiempo en el que se cayo" — [[Work/4 Cedia|4 Cedia]]