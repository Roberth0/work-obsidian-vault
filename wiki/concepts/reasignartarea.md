---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/101-telcos-zabbix-optimizaciones_942fa6]]"
tags:
aliases:
  - "Asignar Tarea"
  - "reasignarTarea endpoint"
  - "reasignar tarea"
generation_complete: true
---

# reasignarTarea

## Definición

**reasignarTarea** es el endpoint `POST (/soporte/tareas/reasignarTarea)` que permite crear o reasignar tareas de *troubleshooting* en el contexto de [[Telcos]]. Constituye el flujo principal de la automatización de asignación de tareas, ya que expone de forma programática la operación que normalmente se realiza de manera manual sobre el sistema de gestión.

## Características clave

- **Método y ruta:** se invoca mediante `POST` sobre la ruta `/soporte/tareas/reasignarTarea`.
- **Doble propósito:** el mismo endpoint sirve tanto para *crear* una tarea como para *reasignar* una existente.
- **Formato de entrada:** admite cuerpos con codificación URL (*URL-encoded*) y sus equivalentes en JSON.
- **Parámetros de identificación de la tarea:** `id_tarea`, `nombre_tarea` y `numero_tarea`.
- **Parámetros de detalle:** `id_detalle` e `intIdDetalleHist`, que vinculan la tarea con su registro de detalle e historial.
- **Parámetros de asignación:** `departamento_asignado`, `empleado_asignado` y `tipo_asignado` determinan a quién se dirige la tarea.
- **Parámetros de contexto y auditoría:** `motivo`, `login`, `fecha_ejecucion` y `hora_ejecucion` documentan la razón del cambio, el usuario ejecutor y el momento de la ejecución.
- **Campos de cierre:** incorpora campos relacionados con el cierre de tarea, lo que permite finalizar el ciclo de vida de la misma.
- **Uso documentado:** la nota fuente incluye múltiples ejemplos reales de cuerpos URL-encoded y sus equivalentes JSON, todos ellos empleando `id_tarea=4023` y `nombre_tarea='Troubleshooting proactivo'`.

## Aplicaciones

- **Automatización de la asignación de tareas:** sustituye la asignación manual por llamadas programáticas desde scripts o integraciones.
- **Reasignación operativa:** permite mover una tarea de troubleshooting entre departamentos o empleados cuando cambian las prioridades o la carga de trabajo.
- **Integración con monitoreo:** combinado con plataformas como [[Zabbix]], puede disparar la creación o reasignación de tareas ante la detección de incidentes.
- **Trazabilidad:** el uso de `motivo`, `login` y las marcas temporales facilita la auditoría de cada cambio de asignación.
- **Cierre controlado:** los campos de cierre de tarea permiten completar el flujo de extremo a extremo sin intervención manual.

## Conceptos relacionados

- [[concepts/id_detalle|id_detalle]]

## Entidades relacionadas

- [[entities/telcos|Telcos]]
- [[entities/telconet|telconet]]

## Menciones en la fuente

- "POST https://telcos.telconet.ec/soporte/tareas/reasignarTarea" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "id_detalle=49413265&id_tarea=4023&motivo=Mediante monitoreo se verifica enlace caído, asociado al login aux: happy-comitepueblo2_2 con IP: 10.221.135.174." — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]