---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/1-backbone_5939cb]]"
tags:
aliases:
  - "CRC"
  - "errores CRC"
  - "Errores y CRCs de Cámaras"
generation_complete: true
---

# Errores y CRCs

## Definición

**Errores y CRCs** hace referencia a los errores de verificación por redundancia cíclica (CRC, *Cyclic Redundancy Check*) observados en los enlaces de cámaras monitoreados. Se trata de un indicador de calidad de enlace que cuantifica las tramas recibidas con fallos de integridad, expresado típicamente en errores por segundo (err/s).

El concepto opera como un **umbral operativo**: según la observación registrada, mientras los errores no superen las 50 err/s no afectan a la visualización del video, por lo que no requieren acción correctiva inmediata.

## Características clave

- **Métrica de integridad de enlace**: mide fallos de verificación CRC sobre el tráfico recibido de las cámaras.
- **Umbral cuantitativo definido**: el criterio de tolerancia establecido es de 50 err/s.
- **Relación directa con la calidad de servicio**: por debajo del umbral, la visualización no se ve afectada.
- **Carácter operativo más que absoluto**: un valor distinto de cero no implica necesariamente una falla visible; lo relevante es la magnitud y la persistencia.
- **Criterio de escalamiento**: permite al NOC diferenciar entre errores tolerables y aquellos que sí requieren escalamiento o intervención.
- **Dependiente del enlace**: los errores se asocian al enlace específico de cada cámara, no a un estado global de la red.

## Aplicaciones

- **Monitoreo proactivo de enlaces de cámaras**: evaluación continua de la salud del enlace mediante la tasa de errores CRC.
- **Triage en el NOC**: clasificación de alarmas en "tolerables" (por debajo de 50 err/s) y "escalables" (por encima del umbral).
- **Diagnóstico de causa raíz**: incrementos sostenidos de CRC pueden orientar hacia problemas físicos (cableado, conectores, interferencias) o de configuración del enlace.
- **Verificación posterior a cambios**: comprobar si una intervención de red redujo efectivamente la tasa de errores.
- **Definición de políticas de monitoreo**: uso del umbral como referencia para configurar alertas y SLA operativos.

## Conceptos relacionados

## Entidades relacionadas

- [[entities/telconet|Telconet]]

## Menciones en la fuente

- "# Errores y CRCs de Camaras" — [[Work/1. Backbone|1. Backbone]]
- "`Observación: Errores no supera umbral 50err/s, no afecta a visualización.`" — [[Work/1. Backbone|1. Backbone]]