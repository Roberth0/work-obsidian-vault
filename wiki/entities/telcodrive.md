---
type: entity
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/4-cedia_d7cef1]]"
tags:
aliases:
  - "telcodrive.telconet.net"
  - "Telconet Drive"
generation_complete: true
---

# telcodrive

## Descripción

telcodrive es el servicio de almacenamiento de archivos interno de [[Telconet]], accesible en la dirección `telcodrive.telconet.net` (172.24.5.141). Figura tanto en la lista de hosts internos como en un comando `Route ADD` de ejemplo, lo que indica que requiere una ruta específica para su acceso desde determinadas subredes. Es una herramienta de uso operativo destinada al personal del NOC, que la emplea para consultar y almacenar archivos de trabajo. Se relaciona directamente con las rutas estáticas añadidas para acceder a los servicios internos de la organización. Su dependencia de direccionamiento privado (172.24.5.141) lo convierte en un recurso no expuesto públicamente, cuyo acceso se resuelve mediante entradas de enrutamiento persistentes.

## Entidades relacionadas

- [[entities/telconet|Telconet]]

## Conceptos relacionados

- [[concepts/route-add-route-delete|Route ADD / Route DELETE]]

## Menciones en la fuente

- "telcodrive.telconet.net  172.24.5.141" (telcodrive.telconet.net  172.24.5.141) — [[Work/4 Cedia|4 Cedia]]
- "Route ADD -p 172.24.5.141 MASK 255.255.255.255  192.168.150.1" (Route ADD -p 172.24.5.141 MASK 255.255.255.255  192.168.150.1) — [[Work/4 Cedia|4 Cedia]]