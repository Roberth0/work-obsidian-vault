---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/comandos_d202a8]]"
tags:
aliases:
  - "instancia VPN"
  - "VPN instance"
  - "VRF"
generation_complete: true
---

# vpn-instance

## Definición

**vpn-instance** (instancia VPN) es el constructo de configuración que aísla tablas de enrutamiento y sesiones BGP independientes dentro de un mismo equipo de red, equivalente funcional a un VRF (*Virtual Routing and Forwarding*). Cada instancia mantiene su propio conjunto de rutas, interfaces asociadas y vecinos BGP, de modo que el tráfico de distintas redes lógicas puede coexistir en un mismo dispositivo sin mezclarse.

En el contexto del equipo documentado, `vpn-instance telconet` es el ámbito sobre el que se ejecutan tanto el diagnóstico de [[BGP]] como la consulta de la tabla de rutas. Los comandos `display bgp vpnv4 vpn-instance telconet ...` y `disp ip routing-table vpn-instance telconet 0.0.0.0 0` ilustran cómo se accede a datos específicos de esa instancia.

## Características clave

- Proporciona aislamiento lógico de tablas de enrutamiento dentro de un mismo equipo, sin necesidad de hardware separado.
- Mantiene sesiones y tablas BGP independientes por instancia, lo que permite políticas de enrutamiento diferenciadas.
- Es el equivalente en la implementación de [[Huawei]] al concepto estándar de VRF.
- Define el ámbito (*scope*) de los comandos de diagnóstico: una misma instrucción devuelve resultados distintos según la instancia indicada.
- Evita la ambigüedad al separar rutas pertenecientes a distintos clientes, servicios o redes superpuestas.
- Se identifica por un nombre (por ejemplo, `telconet`) que se especifica explícitamente en la línea de comandos.

## Aplicaciones

- **Diagnóstico de BGP VPNv4**: ejecutar `display bgp vpnv4 vpn-instance <nombre> ...` para inspeccionar vecinos, anuncios y estado de la sesión BGP de una instancia concreta, como se hace con [[display bgp vpnv4]].
- **Consulta de rutas por instancia**: usar `disp ip routing-table vpn-instance <nombre> 0.0.0.0 0` para revisar la tabla de enrutamiento completa de esa instancia y verificar la ruta por defecto o global.
- **Segmentación multicliente**: separar el tráfico y las rutas de distintos clientes o servicios desplegados sobre la misma infraestructura, por ejemplo la instancia asociada a [[telconet]].
- **Resolución de incidencias de alcanzabilidad**: confirmar que una ruta existe en la instancia correcta antes de atribuir un fallo a la red de transporte.

## Conceptos relacionados

- [[concepts/bgp|BGP]]
- [[concepts/display-bgp-vpnv4|display bgp vpnv4]]

## Entidades relacionadas

- [[entities/huawei|Huawei]]
- [[entities/telconet|telconet]]

## Menciones en la fuente

- "display bgp vpnv4 vpn-instance telconet peer 63.222.78.13 verbose" (display bgp vpnv4 vpn-instance telconet peer 63.222.78.13 verbose) — [[Work/Comandos|Comandos]]
- "disp ip routing-table vpn-instance telconet 0.0.0.0 0" (disp ip routing-table vpn-instance telconet 0.0.0.0 0) — [[Work/Comandos|Comandos]]