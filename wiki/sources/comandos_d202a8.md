---
type: source
created: 2026-09-23
updated: 2026-09-23
source_file: "[[Work/Comandos.md]]"
tags: [other]
aliases: ["Comandos de red Huawei", "Chuleta de comandos Huawei"]
contentHash: 2f1-21e21047
generation_complete: true
---

# Comandos - Resumen

## Fuente

- Archivo original: [[Work/Comandos.md]]
- Ingerido: 2026-09-23

## Contenido principal

La nota **Comandos** es una chuleta operativa de *troubleshooting* de red sobre equipamiento [[entities/huawei|huawei]] con VRP. Se estructura en dos bloques temáticos: **BGP** y **STP**. En el bloque BGP se documenta `display bgp vpnv4 vpn-instance telconet peer 63.222.78.13 verbose`, empleado para inspeccionar el estado detallado de un peer dentro de la instancia VPN [[entities/telconet|telconet]] (véase [[concepts/bgp|bgp]], [[concepts/display-bgp-vpnv4|display-bgp-vpnv4]] y [[concepts/vpn-instance|vpn-instance]]). En el bloque STP se usa `show spanning-tree detail` para averiguar **cuánto tiempo ha transcurrido desde el último cambio de topología** (véase [[concepts/stp|stp]] y [[concepts/show-spanning-tree-detail|show-spanning-tree-detail]]).

Además, la nota recoge capturas de sesión interactiva en el host `rointernetgye1h`, donde se ejecutan `display interface 100GE4/0/14` para revisar la descripción del enlace (proveedor PCCW/CIRION) y los niveles de potencia óptica ([[concepts/display-interface|display-interface]], [[concepts/potencia-óptica-rxtx|potencia-óptica-rxtx]], [[concepts/rango-de-advertencia-óptico|rango-de-advertencia-óptico]]), así como `disp ip routing-table vpn-instance telconet 0.0.0.0 0` para consultar la tabla de enrutamiento. En conjunto, funciona como referencia rápida para verificar sesiones BGP/VPN, convergencia de spanning-tree y salud óptica de interfaces de 100G. Véase también [[concepts/comandos|comandos]].

## Entidades clave

- [[entities/huawei|huawei]] — fabricante del equipamiento; determina la sintaxis de todos los comandos registrados (`display`, prompt `<rointernetgye1h>`, interfaz `100GE4/0/14`).
- [[entities/telconet|telconet]] — nombre de la instancia VPN sobre la que se parametrizan las consultas BGP y de tabla de enrutamiento.

## Conceptos clave

- [[concepts/bgp|bgp]] — protocolo de enrutamiento entre sistemas autónomos, aquí en su variante VPNv4.
- [[concepts/display-bgp-vpnv4|display-bgp-vpnv4]] — familia de comandos para consultar la sesión BGP VPNv4 de un peer concreto.
- [[concepts/vpn-instance|vpn-instance]] — constructo que aísla tablas de enrutamiento y sesiones BGP (equivalente a VRF).
- [[concepts/stp|stp]] — protocolo de capa 2 que evita bucles en redes conmutadas.
- [[concepts/show-spanning-tree-detail|show-spanning-tree-detail]] — comando para ver el detalle del árbol de expansión y el tiempo desde el último cambio de topología.
- [[concepts/display-interface|display-interface]] — comando de estado y operación de una interfaz concreta.
- [[concepts/potencia-óptica-rxtx|potencia-óptica-rxtx]] — niveles de señal recibida y transmitida en dBm.
- [[concepts/rango-de-advertencia-óptico|rango-de-advertencia-óptico]] — umbrales que definen el funcionamiento saludable del transceptor.
- [[concepts/comandos|comandos]] — la propia nota como referencia operativa.

## Puntos principales

- La nota es una **chuleta operativa de troubleshooting** de red sobre equipamiento Huawei.
- El bloque BGP usa `display bgp vpnv4 vpn-instance telconet peer 63.222.78.13 verbose` para inspeccionar en detalle un peer BGP de la instancia VPN telconet.
- El bloque STP usa `show spanning-tree detail` para comprobar **hace cuánto tiempo se produjo un cambio de topología** y evaluar la estabilidad de capa 2.
- Se consulta la tabla de enrutamiento por instancia VPN con `disp ip routing-table vpn-instance telconet 0.0.0.0 0`.
- `display interface 100GE4/0/14 | i esc` permite identificar la descripción del enlace (proveedor **PCCW/CIRION**) y `| inc Rx` filtra las líneas de potencia óptica.
- Los valores medidos se comparan con los rangos de advertencia **Rx [-13.001, 3.999] dBm** y **Tx [-4.000, 3.999] dBm**; las lecturas (p. ej. Rx0 −4.13 dBm, Rx2 −5.06 dBm) quedan dentro de rango.
- El host de ejecución es `rointernetgye1h`, coherente con un router/switch Huawei de la familia CE con enlaces de 100G.

## Páginas mencionadas

- [[entities/huawei|huawei]]
- [[entities/telconet|telconet]]
- [[concepts/bgp|bgp]]
- [[concepts/stp|stp]]
- [[concepts/vpn-instance|vpn-instance]]
- [[concepts/show-spanning-tree-detail|show-spanning-tree-detail]]
- [[concepts/display-bgp-vpnv4|display-bgp-vpnv4]]
- [[concepts/display-interface|display-interface]]
- [[concepts/potencia-óptica-rxtx|potencia-óptica-rxtx]]
- [[concepts/rango-de-advertencia-óptico|rango-de-advertencia-óptico]]
- [[concepts/comandos|comandos]]

## Menciones en la fuente

- "display bgp vpnv4 vpn-instance telconet peer 63.222.78.13 verbose" — [[Work/Comandos|Comandos]]
- "display interface 100GE4/0/14 | inc Rx" — [[Work/Comandos|Comandos]]
- "disp ip routing-table vpn-instance telconet 0.0.0.0 0" — [[Work/Comandos|Comandos]]
- "Description: PCCW/100GIGA/CIRION_SID_81-5569V0E-CRM500361398/PCCW-SR233574/PIT" — [[Work/Comandos|Comandos]]
- "Ver hace cuanto tiempo se produjo un cambio de topologia" — [[Work/Comandos|Comandos]]
- "show spanning-tree detail" — [[Work/Comandos|Comandos]]
- "display interface 100GE4/0/14 | i esc" — [[Work/Comandos|Comandos]]
- "Rx Warning range: [-13.001,  3.999]dBm, Tx Warning range: [-4.000,  3.999]dBm" — [[Work/Comandos|Comandos]]
- "Rx0 Power:  -4.13dBm, Tx0 Power:   1.64dBm" — [[Work/Comandos|Comandos]]
- "Rx2 Power:  -5.06dBm, Tx2 Power:   1.62dBm" — [[Work/Comandos|Comandos]]