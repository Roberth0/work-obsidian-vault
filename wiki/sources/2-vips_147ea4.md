---
type: source
created: 2026-09-23
updated: 2026-09-23
source_file: "[[Work/2. VIPS.md]]"
tags:
  - other
aliases:
  - Monitoreo VIPS
  - Guía de Monitoreo VIPS
sources:
  - "[[sources/vips]]"
  - "[[entities/produbanco]]"
  - "[[entities/banco-bolivariano]]"
  - "[[entities/telegram]]"
  - "[[entities/noc-ipccl1-proactivos]]"
  - "[[entities/uio]]"
  - "[[entities/gye]]"
  - "[[entities/camaras-corporacion-gye]]"
  - "[[concepts/vips]]"
  - "[[concepts/proactivo]]"
  - "[[concepts/corte-de-ruta]]"
  - "[[concepts/reubicacion]]"
  - "[[concepts/etiqueta-notificacion-247]]"
  - "[[concepts/logins-que-no-se-gestionan]]"
  - "[[concepts/caso-o-tarea-ya-aperturado-por-algun-tiempo]]"
contentHash: 66e-b9f6666e
generation_complete: true
---

# 2. VIPS - Resumen

## Fuente

- Archivo original: [[Work/2. VIPS.md]]
- Ingerido: 2026-09-23

## Contenido principal

Este documento operativo establece las directrices para el [[concepts/vips|Monitoreo VIPS]], una vigilancia continua 24/7 ejecutada sobre tres servidores Zabbix: [[entities/uio|UIO]] (172.24.27.13), [[entities/gye|GYE]] (monitoreovipsgye.telconet.ec) y [[entities/camaras-corporacion-gye|Camaras Corporacion GYE]] (172.24.27.17). Define protocolos de contacto con el cliente mediante la [[concepts/etiqueta-notificacion-247|Etiqueta notificacion 24/7]] y la priorización de clientes estratégicos como [[entities/produbanco|Produbanco]] y [[entities/banco-bolivariano|Banco Bolivariano]]. Enumera los [[concepts/logins-que-no-se-gestionan|Logins que no se gestionan]] (tlw, prueba, docker prueba, lan, saturacion, cm, safeentry) y el procedimiento para [[concepts/caso-o-tarea-ya-aperturado-por-algun-tiempo|casos o tareas ya aperturados por algun tiempo]], que se escalan en el chat de [[entities/telegram|Telegram]] del grupo [[entities/noc-ipccl1-proactivos|NOC IPCCL1 PROACTIVOS]]. Describe además el [[concepts/corte-de-ruta|Corte de Ruta]], la apertura de casos en el [[concepts/proactivo|Proactivo]] y excepciones como la [[concepts/reubicacion|Reubicacion]] y el retiro de monitoreo.

## Entidades clave

- [[vips|VIPS]] — Servicio central monitoreado 24/7.
- [[entities/produbanco|Produbanco]] — Cliente bancario prioritario.
- [[entities/banco-bolivariano|Banco Bolivariano]] — Cliente bancario prioritario.
- [[entities/telegram|Telegram]] — Canal de comunicación y escalamiento.
- [[entities/noc-ipccl1-proactivos|NOC IPCCL1 PROACTIVOS]] — Equipo/chat de escalamiento.
- [[entities/uio|UIO]] — Servidor de monitoreo (Quito).
- [[entities/gye|GYE]] — Servidor de monitoreo (Guayaquil).
- [[entities/camaras-corporacion-gye|Camaras Corporacion GYE]] — Servidor de monitoreo de cámaras.
- [[concepts/vips|2. VIPS]] — Documento operativo de referencia.

## Conceptos clave

- [[concepts/vips|Monitoreo VIPS]] — Proceso operativo central.
- [[concepts/etiqueta-notificacion-247|Etiqueta notificacion 24/7]] — Marca obligatoria al contactar al cliente.
- [[concepts/logins-que-no-se-gestionan|Logins que no se gestionan]] — Lista de cuentas excluidas de gestión.
- [[concepts/caso-o-tarea-ya-aperturado-por-algun-tiempo|Caso o tarea ya aperturado por algun tiempo]] — Regla de escalamiento tras dos días sin avances.
- [[concepts/corte-de-ruta|Corte de Ruta]] — Procedimiento ante caída de rutas.
- [[concepts/proactivo|Proactivo]] — Apertura anticipada de casos.
- [[concepts/reubicacion|Reubicacion]] — Excepción al proceso proactivo.

## Puntos principales

- El [[concepts/vips|Monitoreo VIPS]] se realiza 24/7 sobre tres servidores Zabbix: [[entities/uio|UIO]] (172.24.27.13), [[entities/gye|GYE]] (monitoreovipsgye.telconet.ec) y [[entities/camaras-corporacion-gye|Camaras Corporacion GYE]] (172.24.27.17).
- Siempre se debe llamar al cliente con la [[concepts/etiqueta-notificacion-247|Etiqueta notificacion 24/7]]; si no contesta, al pasar la tarea se debe especificar que no contestó David Morocho.
- Se debe dar prioridad a clientes estratégicos como [[entities/produbanco|Produbanco]] y [[entities/banco-bolivariano|Banco Bolivariano]].
- Existen [[concepts/logins-que-no-se-gestionan|Logins que no se gestionan]]: tlw, prueba, docker prueba, lan, saturacion, cm y safeentry.
- Los [[concepts/caso-o-tarea-ya-aperturado-por-algun-tiempo|casos o tareas con más de dos días sin avances]] deben notificarse en el chat de [[entities/telegram|Telegram]] de [[entities/noc-ipccl1-proactivos|NOC IPCCL1 PROACTIVOS]] con un texto estandarizado que incluye número de tarea, punto y último seguimiento.
- Ante un [[concepts/corte-de-ruta|Corte de Ruta]] se debe preguntar en el chat de L1 ([[entities/telegram|Telegram]]/WhatsApp) si existe un caso asignado; si no existe, crearlo (ejemplo de caso 20240831-0153B).
- Para [[entities/banco-bolivariano|Banco Bolivariano]] y [[entities/produbanco|Produbanco]], en el [[concepts/proactivo|Proactivo]] siempre se apertura casos (disposición de Edson, 11-03-2024).
- En casos con orden de [[concepts/reubicacion|Reubicacion]] no es necesario generar el proactivo para esos puntos.
- El documento incluye además un apartado sobre el proceso de Retiro de Monitoreo respaldado por imágenes.

## Menciones en la fuente

- "El monitoreo de VIPS se lleva a cabo 24/7, se tienen los siguientes servidores." — [[Work/2. VIPS|2. VIPS]]
- "3. [Camaras Corporacion GYE](https://172.24.27.17/zabbix)" — [[Work/2. VIPS|2. VIPS]]
- "1. [UIO](https://172.24.27.13/zabbix/)" — [[Work/2. VIPS|2. VIPS]]
- "2. [GYE](https://monitoreovipsgye.telconet.ec/zabbix)" — [[Work/2. VIPS|2. VIPS]]
- "Ademas se debe dar prioridad a clientes como" — [[Work/2. VIPS|2. VIPS]]
- "- [ ] Produbanco" — [[Work/2. VIPS|2. VIPS]]
- "chicos para los clientes Banco Bolivariano y Produbanco para el proactivo siempre se apertura casos, no se olviden de esa disposición" — [[Work/2. VIPS|2. VIPS]]
- "- [ ] Bolivariano" — [[Work/2. VIPS|2. VIPS]]
- "Si la tarea/caso en cuestion ya tiene mas de dos dias de creacion y no se tiene avances en el seguimiento se debe notificar en el chat de ***Telegram*** de NOC IPCCL1 PROACTIVOS con el siguiente texto:" — [[Work/2. VIPS|2. VIPS]]
- "Preguntar en el chat de L1, Telegram/WhatsApp si se dispone de un caso asignado por dicha ruta." — [[Work/2. VIPS|2. VIPS]]
- "Llamar siempre al cliente con la etiqueta notificacion 24/7 y si no contesta al pasar la tarea especificar que no contesto David Morocho" — [[Work/2. VIPS|2. VIPS]]
- "Edson: Whatsapp: 11-03-2024: chicos para los clientes Banco Bolivariano y Produbanco para el proactivo siempre se apertura casos, no se olviden de esa disposición" — [[Work/2. VIPS|2. VIPS]]
- "Estimados IPCCL1, su gentil ayuda con el seguimiento de la tarea 101322100 /// ijsud-carapungo1 Se valida punto caído, ultimo seguimiento: 2024-04-11 12:49" — [[Work/2. VIPS|2. VIPS]]
- "El monitoreo de VIPS se lleva a cabo 24/7, se tienen los siguientes servidores" — [[Work/2. VIPS|2. VIPS]]
- "Chicos, respecto al proceso de proactivo. En los casos de clientes en los que se tenga una orden de reubicación, no es necesario generar el proactivo para esos puntos. ej:" — [[Work/2. VIPS|2. VIPS]]
- "Si no se tiene caso se lo debe crear" — [[Work/2. VIPS|2. VIPS]]