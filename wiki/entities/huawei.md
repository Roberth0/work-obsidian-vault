---
type: entity
created: 2026-09-23
updated: 2026-09-23
generation_complete: true
sources:
  - "[[sources/3-corporativos_04d2e4]]"
  - "[[sources/comandos_d202a8]]"
tags:
  - "organization"
aliases:
  - "HW"
  - "Huawei Technologies Co."
  - "Ltd."
  - "华为"
---

# Huawei

## Descripción

Huawei es uno de los fabricantes de controladoras WiFi administradas que aparecen documentados en el inventario de equipos de red, y se le asocia credenciales compartidas para sus controladoras (User IPCC / Pass T!pccN2016). En el documento se le vincula a la "Nueva Controladora https://181.39.24.107/ Claves Huawei" y a la "Nueva controladora Provincias https://181.39.24.133", ambas con la misma clave. También se le menciona mediante la abreviatura **HW**, empleada en una notificación de enlace caído que reporta el AP tn_wifi2_parquesanrafael1 como DOWN "en la controladora HW https://157.100.14.130/". Sus equipos operan como [[Controladora|controladoras]] que gestionan [[Access Point|Access Points]] desplegados en distintas provincias, y su monitorización se integra en los flujos de [[Monitorización proactiva]] de la operación de red. Dentro del ecosistema documentado, Huawei convive con otros fabricantes como [[Cisco]] y con proveedores de servicio como [[Telconet S.A.]] y [[Omarsa]].

Además, Huawei es el fabricante del equipamiento de red (switches/routers de la serie CE con VRP — Versatile Routing Platform) sobre el que se ejecutan los comandos de diagnóstico documentados en la nota "Comandos". El uso del comando `display` (en lugar de `show`), el prompt `<rointernetgye1h>` y las interfaces `100GE4/0/14` corresponden a dicha plataforma, lo que confirma su rol como base técnica subyacente de las operaciones de red documentadas.
## Entidades relacionadas

- [[entities/telconet|Telconet S.A.]]
- [[entities/cisco|Cisco]]
- [[entities/omarsa|Omarsa]]

## Conceptos relacionados

- [[concepts/controladora|Controladora]]
- [[access-point|Access Point]]
- [[concepts/monitorización-proactiva|Monitorización proactiva]]

## Menciones en la fuente

- "**Huawei** User: `IPCC`Pass:  `T!pccN2016`" — [[Work/3. Corporativos|3. Corporativos]]
- "Nueva Controladora `https://181.39.24.107/`Claves Huawei" — [[Work/3. Corporativos|3. Corporativos]]
- "Mediante monitoreo proactivo se observa la caida del enlace AP Login: 	tn_wifi2_parquesanrafael1 con MAC 2C AC 5C 9C B0 is DOWN en la controladora HW  https://157.100.14.130/" — [[Work/3. Corporativos|3. Corporativos]]
- "display bgp vpnv4 vpn-instance telconet peer 63.222.78.13 verbose" (display bgp vpnv4 vpn-instance telconet peer 63.222.78.13 verbose) — [[Work/Comandos|Comandos]]
- "display interface 100GE4/0/14 | inc Rx" (display interface 100GE4/0/14 | inc Rx) — [[Work/Comandos|Comandos]]