---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/101-telcos-zabbix-optimizaciones_942fa6]]"
tags:
aliases:
  - "ID de detalle"
  - "identificador de detalle"
  - "txtDetalleTareaSeg"
generation_complete: true
---

# id_detalle

## Definición

`id_detalle` es el campo identificador clave que vincula cada detalle de tarea dentro del sistema Telcos. Actúa como la referencia única que permite localizar, rastrear y reasignar un registro de detalle de tarea concreto, y es el campo señalado explícitamente como el que debe rastrearse cuando las tareas se crean desde Zabbix.

## Características clave

- Se comporta como identificador único de cada detalle de tarea dentro de Telcos.
- Aparece en prácticamente todos los ejemplos de uso de la operación [[reasignarTarea]], lo que lo convierte en el vínculo operativo entre la tarea y su detalle.
- En el código JavaScript se asigna al elemento `txtDetalleTareaSeg` mediante `objTarea.id_detalle`.
- Sus valores son numéricos de longitud fija; los valores de ejemplo documentados incluyen 49413265, 49572715, 49614306, 50850683, 50894791 y 51328607.
- Es indispensable para llevar el seguimiento de los registros de contactos y de tareas.
- Funciona como el punto de anclaje para la trazabilidad entre el sistema de monitorización y el sistema de gestión de tareas.

## Aplicaciones

- **Creación de tareas desde Zabbix**: es el campo que la nota marca explícitamente para rastrear al generar tareas originadas por eventos de monitorización, de modo que cada tarea creada pueda correlacionarse con su detalle correspondiente.
- **Reasignación de tareas**: sirve como entrada o referencia obligada en las llamadas a [[reasignarTarea]], ya que identifica sin ambigüedad el detalle sobre el que se va a operar.
- **Seguimiento de contactos y tareas**: permite auditar y reconstruir el historial de un detalle de tarea concreto, así como relacionarlo con los registros de contacto asociados.
- **Integración front-end**: su asignación a `txtDetalleTareaSeg` permite que la interfaz web muestre y manipule el detalle de tarea seleccionado.

## Conceptos relacionados

- [[concepts/reasignartarea|reasignarTarea]]

## Entidades relacionadas

- [[entities/telcos|Telcos]]
- [[entities/zabbix|Zabbix]]

## Menciones en la fuente

- "Revisar peticiones al crera tareas desde el zabbix en busqueda del campo ***id_detalle***" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "2095 document.getElementById('txtDetalleTareaSeg').value             = objTarea.id_detalle;" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]