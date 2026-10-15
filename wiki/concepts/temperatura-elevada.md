---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/2-1-cscg_5bb2db]]"
tags:
aliases:
  - "Alerta de temperatura elevada"
  - "High temperature"
  - "Temperatura elevada ONT"
generation_complete: true
---

# Temperatura elevada

## Definición

La **temperatura elevada** es una alerta de monitoreo asociada a las [[ONT]] que se genera desde la plataforma de monitoreo [[Zabbix]]. Se trata de un evento operativo sujeto a una ventana horaria de gestión: únicamente se gestiona después de las 18H00, por lo que la alerta permanece sin atención durante la jornada de 07H00 a 18H00.

## Características clave

- Es una alerta de monitoreo sobre [[ONT]], no una falla de servicio: indica que el equipo reporta un valor de temperatura por encima del umbral esperado.
- Está sujeta a una **restricción horaria de gestión**: solo se atiende después de las 18H00.
- Fuera de la ventana permitida (07H00 a 18H00) no corresponde gestión; en su lugar se registra el texto `---No se da gestion de 07H00 a 18H00`.
- La gestión dentro del horario permitido implica la creación de una **tarea desde Zabbix** hacia [[Andy Enrique Barberan Cortez]].
- El flujo de asignación es secuencial: la tarea se asigna primero al propio perfil en Telcos y luego se reasigna hacia Andy Barberan.
- Requiere comunicación formal en el chat de WhatsApp *Monitoreo CSCG*, con un formato específico que incluye el número de tarea y el valor de temperatura registrado.

## Aplicaciones

- **Gestión de alarmas de red**: permite distinguir entre alertas que demandan acción inmediata y alertas que se difieren por política operativa, evitando intervenciones innecesarias durante el horario diurno.
- **Seguimiento térmico de ONTs**: el valor registrado (por ejemplo `VALUE: 51 C` sobre la ONT `tncto-pasillocoworking-gye`) sirve como indicador de condiciones ambientales o de degradación del equipo.
- **Trazabilidad y escalamiento**: la creación de la tarea en Zabbix y su reasignación hacia Andy Barberan, junto con el comentario en el chat Monitoreo CSCG, deja registro auditable del caso y de su responsable.
- **Estandarización de la comunicación**: el formato de mensaje con número de tarea y valor de temperatura unifica el reporte entre turnos.

## Conceptos relacionados

- [[concepts/caida-de-ont-y-camaras|Caida de ONT y camaras]]
- [[concepts/error-300|Error 300]]

## Entidades relacionadas

- [[entities/zabbix|Zabbix]]
- [[entities/ont|ONT]]
- [[entities/andy-enrique-barberan-cortez|Andy Enrique Barberan Cortez]]

## Menciones en la fuente

- "Unicamente se da gestion despues de las **18H00**, caso contrario se comenta con:" — [[Work/2.1 CSCG|2.1 CSCG]]
- "---No se da gestion de 07H00 a 18H00" — [[Work/2.1 CSCG|2.1 CSCG]]
- "Estimado @+593 99 871 8125 (Andy Barberan) se asigna la tarea 107853621 || Temperatura elevada ONT: tncto-pasillocoworking-gye VALUE: 51 C" — [[Work/2.1 CSCG|2.1 CSCG]]