---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/4-cedia_d7cef1]]"
tags:
aliases:
  - "Monitoreo de OLT"
  - "Ingreso monitoreo OLT"
  - "OLT Monitoring"
generation_complete: true
---

# Monitoreo OLT

## Definición

El **Monitoreo OLT** es el procedimiento mediante el cual se ingresa al monitoreo de equipos de fibra óptica (OLT) a través del Zabbix de Backbone y del dashboard `https://monitoreorda.telconet.ec/zabbix/`. Actualmente el ingreso es automático una vez que se accede al dashboard de backbone, por lo que no requiere una habilitación manual adicional por equipo. El procedimiento se complementa con el ingreso de monitoreo desde cero en Zabbix, orientado a los casos en que el equipo aún no está incorporado a la plataforma.

## Características clave

- Se ejecuta sobre el **Zabbix de Backbone**, apoyándose en el dashboard `https://monitoreorda.telconet.ec/zabbix/`.
- El ingreso al monitoreo de las OLT es **automático**: basta con ingresar al dashboard de backbone para que el equipo quede monitoreado.
- Es complementario al procedimiento de **ingreso de monitoreo desde cero en Zabbix**, que implica crear cuatro elementos: grupo, media type, action y usuario de notificación.
- Se aplica sobre **equipos de fibra óptica (OLT)** de la infraestructura de Fiberhome.
- Habilita la generación de notificaciones y alertas sobre eventos de la red óptica, como el link loss.

## Aplicaciones

- Incorporación de equipos OLT al monitoreo centralizado de la red sin intervención manual adicional.
- Configuración inicial de monitoreo en Zabbix (grupo, media type, action y usuario de notificación) para equipos que aún no cuentan con monitoreo previo.
- Detección y notificación proactiva de incidentes en la red de fibra óptica, incluyendo pérdidas de enlace entre nodos.
- Verificación del estado operativo de las OLT de la infraestructura de Fiberhome desde un dashboard unificado.

## Conceptos relacionados

- [[concepts/notificación-proactiva|notificación proactiva]]
- [[concepts/link-loss|link loss]]

## Entidades relacionadas

- [[entities/zabbix|Zabbix]]
- [[entities/fiberhome|fiberhome]]
- [[entities/telconet|Telconet]]

## Menciones en la fuente

- "Se debe ingresar en el zabbix de Backbone y en el siguiente dashboard https://monitoreorda.telconet.ec/zabbix/" — [[Work/4 Cedia|4 Cedia]]
- "*Actualmente el ingreso es automatico una vez se ingrese en el dashboard de backbone*" — [[Work/4 Cedia|4 Cedia]]
- "### Ingreso de monitoreo desde cero en zabbix" — [[Work/4 Cedia|4 Cedia]]