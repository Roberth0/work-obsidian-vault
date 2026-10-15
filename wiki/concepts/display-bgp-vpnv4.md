---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/comandos_d202a8]]"
tags:
aliases:
  - "display bgp vpnv4 vpn-instance"
  - "show bgp vpnv4"
generation_complete: true
---

# display bgp vpnv4

## Definición

`display bgp vpnv4` es la familia de comandos de la CLI de Huawei que permite consultar información de la sesión BGP para la familia de direcciones VPNv4 (IPv4 dentro de VPN). A través de sus distintos modificadores se puede acotar la consulta a una instancia VPN concreta (`vpn-instance`) y a un vecino BGP específico (`peer`), añadiendo el modificador `verbose` para obtener el máximo nivel de detalle en la salida.

## Características clave

- **Consulta por familia de direcciones**: opera sobre VPNv4, la address family que transporta rutas IPv4 asociadas a una VPN mediante Route Distinguisher y Route Target.
- **Filtrado jerárquico**: admite filtrado por instancia VPN (`vpn-instance`) y por peer BGP individual, lo que permite aislar el diagnóstico a una sesión concreta.
- **Nivel de detalle configurable**: el modificador `verbose` amplía la salida con información extendida de la sesión y del vecino.
- **Información entregada**: estado de la sesión BGP, capacidades negociadas entre los peers y estadísticas del vecino BGP.
- **Naturaleza de solo lectura**: es un comando de visualización (`display`), no modifica la configuración ni el estado del protocolo.
- **Sintaxis de referencia**: `display bgp vpnv4 vpn-instance telconet peer 63.222.78.13 verbose`.

## Aplicaciones

- **Verificación de la salud de sesiones BGP**: comprobar si la sesión con un peer está establecida o caída dentro de una instancia VPN determinada.
- **Diagnóstico de una VPN específica**: en la nota se emplea sobre la instancia `telconet` para validar el estado de sus sesiones BGP.
- **Auditoría de capacidades negociadas**: confirmar qué capacidades (address families, extensiones) se han negociado efectivamente con el vecino.
- **Análisis de estadísticas del vecino**: revisar contadores y métricas del peer para detectar inestabilidad, reseteos o pérdida de rutas.
- **Soporte y troubleshooting**: herramienta principal del bloque BGP para el seguimiento operativo de la VPN telconet.

## Conceptos relacionados

- [[concepts/bgp|BGP]]
- [[concepts/vpn-instance|vpn-instance]]
- [[concepts/display-interface|display interface]]

## Entidades relacionadas

- [[entities/huawei|Huawei]]
- [[entities/telconet|telconet]]

## Menciones en la fuente

- "display bgp vpnv4 vpn-instance telconet peer 63.222.78.13 verbose" (display bgp vpnv4 vpn-instance telconet peer 63.222.78.13 verbose) — [[Work/Comandos|Comandos]]