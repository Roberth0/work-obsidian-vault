---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/comandos_d202a8]]"
tags:
aliases:
  - "Border Gateway Protocol"
  - "BGP VPNv4"
  - "Protocolo de Puerta de Enlace de Frontera"
generation_complete: true
---

# BGP

## Definición

BGP (Border Gateway Protocol) es el protocolo de enrutamiento entre sistemas autónomos (AS) utilizado para intercambiar información de alcanzabilidad de rutas entre dominios de enrutamiento independientes. Es el protocolo de enrutamiento exterior (EGP) estándar de Internet y opera sobre TCP en el puerto 179, manteniendo sesiones denominadas *peering* entre vecinos (peers) BGP.

En el contexto de esta nota, BGP se presenta en su variante **VPNv4**, una extensión multiprotocolo (MP-BGP) que transporta rutas asociadas a una instancia VPN concreta, identificadas mediante *Route Distinguisher* (RD) y *Route Target* (RT). Esto permite que un mismo equipo mantenga tablas de enrutamiento separadas por cliente o servicio dentro de una infraestructura MPLS/VPN.

## Características clave

- **Protocolo de enrutamiento exterior (EGP):** intercambia rutas entre sistemas autónomos, a diferencia de los protocolos internos como OSPF o STP en el ámbito de conmutación.
- **Sesión sobre TCP/179:** el establecimiento del vecino (*peering*) depende de la conectividad IP previa y pasa por estados como Idle, Connect, Active, OpenSent, OpenConfirm y Established.
- **Atributos de ruta:** la selección de mejor ruta se basa en atributos como AS_PATH, NEXT_HOP, LOCAL_PREF, MED y comunidades.
- **Extensible mediante multiprotocolo (MP-BGP):** admite familias de direcciones como VPNv4, IPv6 o L2VPN, lo que habilita su uso en escenarios MPLS/VPN.
- **Contexto por instancia VPN:** en VPNv4, las sesiones y tablas pueden asociarse a una `vpn-instance` específica, manteniendo la separación lógica de rutas.
- **Diagnóstico detallado por peer:** la variante *verbose* de los comandos de visualización expone estado de sesión, contadores de mensajes y capacidades negociadas.

## Aplicaciones

- **Enrutamiento entre sistemas autónomos en Internet:** intercambio de prefijos públicos entre operadores y proveedores de tránsito.
- **Redes MPLS/VPN de proveedor de servicios:** distribución de rutas VPNv4 entre los equipos de borde (PE) para dar conectividad a clientes con direccionamiento solapado.
- **Troubleshooting de conectividad VPN:** el comando `display bgp vpnv4 vpn-instance telconet peer 63.222.78.13 verbose` se emplea para inspeccionar el estado detallado de un peer BGP concreto dentro de la instancia `telconet`, verificando si la sesión está establecida, revisando contadores y capacidades negociadas. Resulta clave para diagnosticar problemas de establecimiento o inestabilidad del vecino BGP dentro de una rutina de verificación de la red VPN.
- **Verificación de políticas de enrutamiento:** comprobación de atributos y comunidades aplicadas a las rutas aprendidas o anunciadas.

## Conceptos relacionados

- [[concepts/vpn-instance|vpn-instance]]
- [[concepts/stp|STP]]
- [[concepts/display-bgp-vpnv4|display bgp vpnv4]]

## Entidades relacionadas

- [[entities/huawei|Huawei]]
- [[entities/telconet|telconet]]

## Menciones en la fuente

- "display bgp vpnv4 vpn-instance telconet peer 63.222.78.13 verbose" (display bgp vpnv4 vpn-instance telconet peer 63.222.78.13 verbose) — [[Work/Comandos|Comandos]]