---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/101-telcos-zabbix-optimizaciones_942fa6]]"
tags:
aliases:
  - "reiniciar estado Activo"
  - "reiniciarEstadoRelacion"
  - "reinicia estado relacion"
generation_complete: true
---

# reiniciaEstadoRelacion

## Definición

`reiniciaEstadoRelacion` es un endpoint de tipo `GET`, expuesto en la ruta `/soporte/info_caso/reiniciaEstadoRelacion`, que permite cambiar el estado de una tarea a `'Activo'`. La operación se parametriza mediante `idDetalleTarea` y `estado`, y su finalidad es reactivar la relación asociada a un detalle de tarea.

## Características clave

- **Método HTTP:** `GET`.
- **Ruta:** `/soporte/info_caso/reiniciaEstadoRelacion`.
- **Parámetros de entrada:** `idDetalleTarea` (identificador del detalle de tarea) y `estado` (estado destino, típicamente `Activo`).
- **Invocación documentada:** `idDetalleTarea=49614306&estado=Activo`.
- **Respuesta de ejemplo:** `{"encontrados":[{"response":""}]}` — una estructura con una lista `encontrados` que contiene un objeto con el campo `response`.
- **Efecto:** devuelve una tarea o su relación de detalle a estado activo, sin crear ni eliminar registros.

## Aplicaciones

- **Reactivación tras reasignación:** cuando una tarea ha sido reasignada y su detalle queda en un estado no activo, este endpoint permite volver a ponerlo en `'Activo'` para que continúe su flujo normal.
- **Corrección de estados:** útil para revertir un estado inconsistente de un detalle de tarea sin recurrir a operaciones de escritura más complejas.
- **Automatización en soporte:** puede invocarse desde scripts o integraciones de soporte para normalizar el estado de casos identificados por su `idDetalleTarea`.
- **Encadenamiento con reasignación:** se utiliza como paso complementario dentro de un procedimiento de [[reasignarTarea|reasignación de tareas]].

## Conceptos relacionados

- [[concepts/reasignartarea|reasignarTarea]]

## Entidades relacionadas

- [[entities/telcos|Telcos]]

## Menciones en la fuente

- "GET https://telcos.telconet.ec/soporte/info_caso/reiniciaEstadoRelacion?idDetalleTarea=49614306&estado=Activo" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "{"encontrados":[{"response":""}]}" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]