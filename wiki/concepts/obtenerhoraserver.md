---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/101-telcos-zabbix-optimizaciones_942fa6]]"
tags:
aliases:
  - "Peticion de Hora"
  - "obtener hora del servidor"
  - "get server time"
generation_complete: true
---

# obtenerHoraServer

## Definición

`obtenerHoraServer` es el endpoint `POST /soporte/tareas/obtenerHoraServer` que devuelve la fecha y hora actual del servidor en formato JSON. Su respuesta de ejemplo es `{"success":true,"fechaActual":"2024-10-23","horaActual":"17:01"}`. Se trata de un servicio auxiliar dentro del flujo de automatización de tareas, cuyo propósito es proporcionar una referencia temporal confiable y única para las operaciones que dependen de marcas de tiempo.

## Características clave

- Es un servicio auxiliar expuesto como endpoint HTTP mediante el método `POST`, en la ruta `/soporte/tareas/obtenerHoraServer`.
- Devuelve la respuesta en formato JSON con los campos `success`, `fechaActual` (formato `YYYY-MM-DD`) y `horaActual` (formato `HH:MM`).
- La fecha y la hora se entregan separadas en dos campos, no como una única marca de tiempo combinada.
- La hora reportada es la del servidor, no la del cliente que realiza la petición, por lo que actúa como fuente de verdad temporal.
- No recibe parámetros de entrada relevantes: su función es exclusivamente de consulta.
- Es invocado como paso previo a operaciones que requieren que los valores de `fecha_ejecucion` y `hora_ejecucion` coincidan exactamente con el reloj del servidor de [[Telcos]].

## Aplicaciones

- **Sincronización de marcas de tiempo al reasignar tareas:** antes de ejecutar [[reasignarTarea]], se consulta `obtenerHoraServer` para asignar a `fecha_ejecucion` y `hora_ejecucion` los valores exactos del servidor, evitando desajustes entre el reloj del cliente y el del servidor.
- **Automatización de flujos de tareas:** funciona como servicio de apoyo dentro de pipelines donde la programación de tareas depende de la hora oficial del backend.
- **Validación y diagnóstico:** permite verificar de forma rápida la fecha y hora efectivas del servidor, útil para depurar discrepancias horarias en las ejecuciones.

## Conceptos relacionados

- [[concepts/reasignartarea|reasignarTarea]]

## Entidades relacionadas

- [[entities/telcos|Telcos]]

## Menciones en la fuente

- "POST https://telcos.telconet.ec/soporte/tareas/obtenerHoraServer" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "{"success":true,"fechaActual":"2024-10-23","horaActual":"17:01"}" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]