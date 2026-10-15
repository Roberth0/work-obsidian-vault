---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/101-telcos-zabbix-optimizaciones_942fa6]]"
tags:
aliases:
  - "hora_ejecucion"
  - "fecha y hora de ejecución"
  - "fecha de ejecución"
generation_complete: true
---

# fecha_ejecucion

## Definición

`fecha_ejecucion` es el parámetro que define la fecha en la que debe ejecutarse una tarea reasignada dentro del sistema de Telcos. Se utiliza en conjunto con [[hora_ejecucion]], su campo complementario, y ambos se expresan en formato ISO 8601 truncado a minutos (por ejemplo, `2024-10-18T00:00` para la fecha y `2024-10-18T01:00` para la hora). Ambos valores se incluyen junto a [[login aux|login]], [[empleado_asignado]] e [[id_detalle|intIdDetalleHist]] en cada petición enviada al endpoint [[reasignarTarea]].

## Características clave

- **Formato ISO**: el valor sigue el patrón `YYYY-MM-DDThh:mm`, sin segundos ni zona horaria explícita.
- **Par fecha–hora**: `fecha_ejecucion` y [[hora_ejecucion]] se envían siempre juntos; la fecha aporta el día y la hora completa el instante de ejecución.
- **Valores variables**: el documento de origen incluye una sección de «Campos distintos» con múltiples pares de ejemplo (`2024-10-18`, `2024-10-22`, `2024-10-23`, `2024-11-24`), lo que demuestra la variabilidad que la automatización debe soportar.
- **Dependencia de sincronización**: se recomienda contrastar el valor con el endpoint [[obtenerHoraServer]], que devuelve `fechaActual` y `horaActual` del servidor.
- **Obligatoriedad contextual**: resulta crítico cuando la tarea se reasigna a una fecha distinta de la prevista originalmente.

## Aplicaciones

- **Reasignación de tareas con reprogramación**: al invocar [[reasignarTarea]], se envía `fecha_ejecucion` para fijar el nuevo día de ejecución de la tarea asignada a un empleado.
- **Automatización de pruebas de integración**: los distintos pares de fechas del documento se emplean como casos de prueba para verificar que el sistema acepta fechas futuras variadas (octubre y noviembre de 2024).
- **Sincronización horaria con el servidor**: antes de construir la petición, la automatización consulta [[obtenerHoraServer]] para alinear `fecha_ejecucion` y [[hora_ejecucion]] con la referencia temporal del backend.
- **Trazabilidad de reprogramaciones**: combinada con [[id_detalle]] y [[motivo]], permite registrar por qué y cuándo se movió una tarea.

## Conceptos relacionados

- [[concepts/reasignartarea|reasignarTarea]]
- [[concepts/obtenerhoraserver|obtenerHoraServer]]
- [[concepts/id_detalle|id_detalle]]
- [[concepts/motivo|motivo]]
- [[concepts/login-aux|login aux]]

## Entidades relacionadas

- [[entities/telcos|Telcos]]

## Menciones en la fuente

- "fecha_ejecucion=2024-10-18T00:00&hora_ejecucion=2024-10-18T01:00" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "fecha_ejecucion=2024-10-22T00:00&hora_ejecucion=2024-10-22T18:21" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "Reasingar tarea fecha distinta" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]