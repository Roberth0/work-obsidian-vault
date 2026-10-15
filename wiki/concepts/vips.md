---
type: concept
created: 2026-09-23
updated: 2026-09-23
generation_complete: true
type_confirmed: true
sources:
  - "[[sources/2-vips_147ea4]]"
tags:
  - "person"
  - "method"
aliases:
  - "Monitoreo VIPS"
  - "Monitoreo de VIPS"
  - "2. VIPS"
---

# VIPS

## Descripción

VIPS es el servicio de vigilancia y monitoreo continuo cuya supervisión constituye el objeto central del documento operativo que da origen a esta página. Su monitoreo se ejecuta de forma ininterrumpida 24/7 mediante plataformas [[Zabbix]] desplegadas en varios servidores, lo que permite mantener visibilidad permanente sobre la disponibilidad del servicio. La operación de VIPS implica protocolos de notificación, criterios de priorización de clientes y la gestión de casos y tareas asociados a cada incidencia. El servicio abarca también el monitoreo de cámaras corporativas, reflejado en el servidor dedicado a [[Camaras Corporacion GYE]], y se coordina con la operación de las sedes [[UIO]] y [[GYE]]. El documento de referencia establece las reglas de contacto, escalamiento y creación de casos que el equipo de soporte debe seguir para preservar la disponibilidad del servicio.

La operación del servicio incorpora reglas concretas de contacto, como llamar siempre al cliente con la etiqueta notificación 24/7 y, en caso de no obtener respuesta, especificar al pasar la tarea que no contestó David Morocho. Asimismo, se prioriza a clientes estratégicos como [[Produbanco]] y [[Banco Bolivariano]], para cuyos proactivos siempre se apertura casos por disposición de Edson (11-03-2024), mientras que no se gestionan los logins tlw, prueba, docker prueba, lan, saturacion, cm y safeentry.

El escalamiento también queda regulado: si una tarea o caso supera los dos días de creación sin avances en el seguimiento, se debe notificar en el chat de Telegram del grupo NOC IPCCL1 PROACTIVOS; en cortes de ruta se debe preguntar en el chat de L1 (Telegram/WhatsApp) si existe un caso asignado por dicha ruta y, de no tenerlo, crearlo (ejemplo de caso 20240831-0153B). Adicionalmente, en los casos de clientes con orden de reubicación no es necesario generar el proactivo para esos puntos, y el retiro de monitoreo se documenta como disposición con imágenes de apoyo.

El monitoreo de VIPS se ejecuta 24/7 sobre tres servidores Zabbix con sus respectivas URLs: UIO (https://172.24.27.13/zabbix/), GYE (https://monitoreovipsgye.telconet.ec/zabbix) y [[Camaras Corporacion GYE|Camaras Corporacion GYE]] (https://172.24.27.17/zabbix). Desde estos servidores se vigilan los puntos y servicios de los clientes, con el objetivo de garantizar la disponibilidad y la respuesta oportuna ante incidencias dentro de la operación de Telconet.
## Entidades relacionadas

- [[entities/zabbix|zabbix]]
- [[entities/uio|UIO]]
- [[entities/gye|GYE]]
- [[entities/camaras-corporacion-gye|Camaras Corporacion GYE]]

## Conceptos relacionados

- [[concepts/vips|Monitoreo VIPS]]
- [[concepts/proactivo|Proactivo]]
- [[concepts/corte-de-ruta|Corte de Ruta]]
- [[concepts/reubicacion|Reubicación]]

## Menciones en la fuente

- "El monitoreo de VIPS se lleva a cabo 24/7, se tienen los siguientes servidores." — [[Work/2. VIPS|2. VIPS]]
- "3. [Camaras Corporacion GYE](https://172.24.27.17/zabbix)" — [[Work/2. VIPS|2. VIPS]]
- "El monitoreo de VIPS se lleva a cabo 24/7, se tienen los siguientes servidores" — [[Work/2. VIPS|2. VIPS]]
- "1. [UIO](https://172.24.27.13/zabbix/)" — [[Work/2. VIPS|2. VIPS]]
- "2. [GYE](https://monitoreovipsgye.telconet.ec/zabbix)" — [[Work/2. VIPS|2. VIPS]]