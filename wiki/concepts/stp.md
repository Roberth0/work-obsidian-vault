---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/comandos_d202a8]]"
tags:
aliases:
  - "Spanning Tree Protocol"
  - "spanning-tree"
  - "Protocolo de Árbol de Expansión"
generation_complete: true
---

# STP

## Definición

STP (Spanning Tree Protocol) es el protocolo de capa 2 que evita la formación de bucles en redes conmutadas. Construye una topología lógica sin bucles (el árbol de expansión) sobre una topología física que puede contener enlaces redundantes, bloqueando selectivamente los puertos que generarían un bucle. En la nota de origen se emplea como herramienta de diagnóstico para comprobar la estabilidad de la topología de la red.

## Características clave

- **Ámbito de capa 2**: opera sobre dispositivos de conmutación (switches) y no requiere intervención de protocolos de enrutamiento de capa 3.
- **Prevención de bucles**: elimina la redundancia lógica mediante el bloqueo de puertos, evitando tormentas de broadcast y duplicación de tramas.
- **Reconvergencia ante fallos**: cuando un enlace cae, recalcula el árbol y activa rutas alternativas, lo que constituye un *cambio de topología* (topology change).
- **Observabilidad**: el estado y la actividad del árbol pueden consultarse directamente desde el equipo de red, lo que permite auditar su comportamiento.
- **Indicador de estabilidad**: la frecuencia de los cambios de topología es un síntoma directo de problemas de red.

## Aplicaciones

- **Diagnóstico de estabilidad de red**: con el comando `show spanning-tree detail` se consulta información detallada del árbol de expansión. La nota enfatiza revisar *hace cuánto tiempo se produjo un cambio de topología*, dato crucial porque los cambios de topología frecuentes indican inestabilidad (enlaces caídos, bucles o reconfiguraciones) que degrada el servicio.
- **Verificación de redundancia**: confirmar que los enlaces de respaldo están en estado bloqueado y disponibles para asumir tráfico ante un fallo.
- **Solución de problemas de rendimiento**: detectar bucles o reconvergencias constantes que provocan fluctuaciones y pérdida de servicio.
- **Auditoría de cambios**: correlacionar los cambios de topología con intervenciones de configuración o incidencias físicas en el cableado.
- **Bloque temático de la nota**: STP constituye el eje del segundo bloque temático, complementando el diagnóstico de [[BGP]] dentro de un procedimiento de verificación de red en equipos [[Huawei]].

## Conceptos relacionados

- [[concepts/display-spanning-tree-detail|display spanning-tree detail]]
- [[concepts/bgp|BGP]]

## Entidades relacionadas

- [[entities/huawei|Huawei]]

## Menciones en la fuente

- "Ver hace cuanto tiempo se produjo un cambio de topologia" (Ver hace cuánto tiempo se produjo un cambio de topología) — [[Work/Comandos|Comandos]]
- "show spanning-tree detail" (show spanning-tree detail) — [[Work/Comandos|Comandos]]