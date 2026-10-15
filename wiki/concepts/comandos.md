---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/comandos_d202a8]]"
tags:
aliases:
  - "Comandos de diagnóstico"
  - "Comandos de troubleshooting de red"
generation_complete: true
---

# Comandos

## Definición

**Comandos** es una nota técnica de operación de red que compila un conjunto de comandos de diagnóstico ejecutados sobre equipamiento [[Huawei]], empleada como chuleta operativa para tareas de troubleshooting. Su contenido se organiza en dos bloques temáticos principales: [[BGP]] y [[STP]].

## Características clave

- Es una nota operativa de referencia rápida (chuleta), no una guía normativa ni una especificación de configuración.
- Se estructura en bloques temáticos: uno dedicado a BGP y otro a STP.
- Combina comandos de diagnóstico con capturas de sesión interactiva en el host `rointernetgye1h`.
- Aborda tres áreas de verificación: sesiones BGP/VPN, convergencia de spanning-tree y salud óptica de interfaces de 100G.
- Incluye ejemplos de comandos orientados a proveedores y enlaces concretos, como la revisión de la descripción del enlace del proveedor PCCW/CIRION.

## Aplicaciones

- **Verificación de BGP/VPN:** inspeccionar el estado detallado de un peer BGP dentro de una instancia VPN, por ejemplo con `display bgp vpnv4 vpn-instance telconet peer 63.222.78.13 verbose`.
- **Convergencia de spanning-tree:** averiguar cuánto tiempo ha transcurrido desde el último cambio de topología mediante `show spanning-tree detail`.
- **Salud óptica de interfaces de 100G:** revisar la descripción del enlace y los niveles de potencia óptica Rx/Tx, por ejemplo con `display interface 100GE4/0/14`.
- **Consulta de enrutamiento:** revisar la tabla de enrutamiento de una instancia VPN, por ejemplo con `disp ip routing-table vpn-instance telconet 0.0.0.0 0`.

## Conceptos relacionados

- [[concepts/bgp|BGP]]

## Entidades relacionadas

- [[entities/huawei|Huawei]]
- [[entities/telconet|telconet]]