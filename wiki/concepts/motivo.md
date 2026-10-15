---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/101-telcos-zabbix-optimizaciones_942fa6]]"
tags:
aliases:
  - "campo motivo"
  - "motivo de la tarea"
  - "motivo de reasignación"
generation_complete: true
---

# motivo

## Definición

El **motivo** es el campo de texto libre que describe la razón por la cual se genera o se reasigna una tarea de *Troubleshooting* proactivo en el entorno de [[Telcos]]. Funciona como el campo narrativo del registro: mientras los demás campos aportan identificadores y marcas temporales, el `motivo` documenta en lenguaje natural qué situación fue detectada y qué acciones de verificación se realizaron.

Su contenido típico indica que, mediante monitoreo, se verifica un enlace caído, y detalla el *login aux*, la IP, el contacto, la notificación por mail y el estado de la unidad de monitoreo.

## Características clave

- **Texto libre**: no sigue un esquema cerrado ni un vocabulario controlado; cada registro puede redactar el motivo con distinto nivel de detalle.
- **Función descriptiva**: explica la causa de la generación o reasignación de la tarea, no su identificación ni su programación.
- **Contenido recurrente**: las descripciones suelen incluir la verificación de enlace caído, el *login aux*, la IP, el contacto, la notificación por mail y el estado de la unidad de monitoreo.
- **Presencia dual**: aparece tanto en las peticiones a [[reasignarTarea]] como dentro de la estructura de la tarea.
- **Codificación URL**: en las peticiones reales los valores se transmiten codificados (por ejemplo, `%2C` para comas y `%C3%AD` para la letra «í»).
- **Persistencia junto a marcas temporales**: se conserva en los registros acompañado de [[fecha_ejecucion]] y [[hora_ejecucion]].
- **Reutilización**: es un elemento repetido en múltiples registros del documento fuente, con variaciones mínimas entre casos.

## Aplicaciones

- **Reasignación de tareas**: forma parte de la carga (*payload*) enviada al endpoint `https://telcos.telconet.ec/soporte/tareas/reasignarTarea`, junto con campos como [[id_detalle]].
- **Trazabilidad operativa**: permite reconstruir por qué se abrió o derivó una tarea de monitoreo, útil para auditoría y seguimiento de casos.
- **Diagnóstico de red**: los motivos que describen enlaces caídos se relacionan con síntomas técnicos como [[Puerto connected]] o [[no aprende MAC]].
- **Documentación de verificaciones**: registra las comprobaciones efectuadas (login aux, IP, contacto, notificación por mail, estado de la unidad de monitoreo).
- **Interoperabilidad de API**: al viajar dentro de una petición HTTP, su valor requiere codificación URL, lo que condiciona su construcción y su posterior decodificación.

## Conceptos relacionados

- [[concepts/reasignartarea|reasignarTarea]]
- [[concepts/id_detalle|id_detalle]]
- [[concepts/login-aux|login aux]]
- [[concepts/fecha_ejecucion|fecha_ejecucion]]
- [[concepts/puerto-connected-no-aprende-mac|Puerto connected, no aprende MAC]]

## Entidades relacionadas

- [[entities/telcos|Telcos]]

## Menciones en la fuente

- "motivo=Mediante monitoreo se verifica enlace PRINCIPAL caído, asociado al login aux: aelgato-6demarzo_1 con IP: 10.202.75.10. CONTACTO: . Se envia vía mail la notificación. UM: sw1allcomp1-ten.telconet.net Gi1/0/11. Puerto connected, no aprende MAC" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]