---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/101-telcos-zabbix-optimizaciones_942fa6]]"
tags:
aliases:
  - "ingresarSeguimientoRegistroContacto"
  - "función ingresarSeguimientoRegistroContactos"
  - "registro de contactos de seguimiento"
generation_complete: true
---

# ingresarSeguimientoRegistroContactos

## Definición

`ingresarSeguimientoRegistroContactos` es una función JavaScript documentada en el archivo `Tareas.js` de la plataforma [[Telcos]]. Se encarga de gestionar el ingreso (registro) del seguimiento de contactos asociado a una tarea, recibiendo como parámetro un arreglo denominado `arraySeguimientoRegistroContacto` del cual extrae las variables necesarias para construir y enviar la petición correspondiente.

## Características clave

- Es una función de cliente (front-end) implementada en JavaScript dentro de `Tareas.js`.
- Recibe un único arreglo de entrada, `arraySeguimientoRegistroContacto`, del que deriva sus variables de trabajo.
- Extrae variables clave como `empresa_id`, `id_caso`, `id_detalle`, `login`, `departamento_id`, `str_empresa_tarea` y `tipo`.
- El comentario del código indica que su propósito cubre las opciones **"Reasignar"** y **"Cerrar"** de una tarea.
- Funciona como capa intermedia entre la acción del usuario en la interfaz y la petición de actualización enviada al servidor.

## Aplicaciones

- Registrar el seguimiento de contactos cuando un caso o tarea cambia de estado.
- Soporta el flujo de **"Reasignar"** tareas, construyendo la petición que se envía al backend con los identificadores de empresa, caso y detalle.
- Soporta el flujo de **"Cerrar"** tareas, registrando el contacto y la información de cierre.
- Permite trazar qué usuario (`login`) y qué departamento (`departamento_id`) realizó la acción de seguimiento.
- Sirve como punto de análisis para entender cómo el cliente de [[Telcos]] arma las peticiones de reasignación que se observan en la documentación del sistema.

## Conceptos relacionados

- [[concepts/id_detalle|id_detalle]]
- [[concepts/reasignartarea|reasignarTarea]]
- [[concepts/id_caso|id_caso]]
- [[concepts/login-aux|login aux]]

## Entidades relacionadas

- [[entities/telcos|Telcos]]

## Menciones en la fuente

- "function ingresarSeguimientoRegistroContactos(arraySeguimientoRegistroContacto)" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "//opcion: Reasignar, Cerrar" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "var idDetalle = arraySeguimientoRegistroContacto.id_detalle;" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]