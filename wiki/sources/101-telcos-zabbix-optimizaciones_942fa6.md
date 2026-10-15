---
type: source
created: 2026-09-23
updated: 2026-09-23
source_file: "[[Work/101. Telcos - Zabbix optimizaciones.md]]"
tags: [other]
aliases: ["Telcos - Zabbix optimizaciones", "Automatización Telcos y Zabbix"]
contentHash: 2c4e-12baf775
generation_complete: true
---

# 101. Telcos - Zabbix optimizaciones - Resumen

## Fuente

- Archivo original: [[Work/101. Telcos - Zabbix optimizaciones.md]]
- Ingerido: 2026-09-23

## Contenido principal

Esta nota técnica documenta las peticiones HTTP empleadas para automatizar la operación de soporte en la plataforma [[entities/telcos|Telcos]] de Telconet, integrada con el sistema de monitoreo [[entities/zabbix|Zabbix]]. Describe dos flujos principales: la asignación de casos mediante [[concepts/actualizarhipotesis|actualizarHipotesis]] y la asignación/reasignación de tareas de troubleshooting mediante [[concepts/reasignartarea|reasignarTarea]]. Se incluyen múltiples ejemplos reales de cuerpos de petición (URL-encoded y JSON), con campos como [[concepts/id_caso|id_caso]], [[concepts/id_detalle|id_detalle]], [[concepts/empleado_asignado|empleado_asignado]] y [[concepts/fecha_ejecucion|fecha_ejecucion]]. También se documentan endpoints auxiliares: [[concepts/reiniciaestadorelacion|reiniciaEstadoRelacion]], [[concepts/obtenerhoraserver|obtenerHoraServer]] y exportarConsulta. El autor identifica que el campo clave [[concepts/id_detalle|id_detalle]] debe rastrearse al crear tareas desde Zabbix, apoyándose en el código JavaScript de `Tareas.js` ([[concepts/ingresarseguimientoregistrocontactos|ingresarSeguimientoRegistroContactos]]). Quedan pendientes un convertidor hexadecimal a decimal para el ingreso de APs y el envío automático de correos para los APs.

## Entidades clave

- [[entities/telcos|Telcos]] — plataforma de gestión de soporte y tareas en telcos.telconet.ec, destino de toda la automatización.
- [[entities/zabbix|Zabbix]] — plataforma de monitoreo desde la cual se generan automáticamente las tareas y casos enviados a Telcos.

## Conceptos clave

- [[concepts/actualizarhipotesis|actualizarHipotesis]] — endpoint POST que asigna un caso e ingresa la hipótesis diagnóstica.
- [[concepts/reasignartarea|reasignarTarea]] — endpoint POST que crea o reasigna tareas de "Troubleshooting proactivo" (id_tarea=4023).
- [[concepts/id_detalle|id_detalle]] — campo identificador clave a rastrear al crear tareas desde Zabbix.
- [[concepts/obtenerhoraserver|obtenerHoraServer]] — endpoint POST que sincroniza fecha y hora del servidor.
- [[concepts/reiniciaestadorelacion|reiniciaEstadoRelacion]] — endpoint GET que cambia el estado de una tarea a "Activo".
- [[concepts/login-aux|login aux]] — identificador del enlace auxiliar del cliente asociado a cada tarea.
- [[concepts/motivo|motivo]] — texto libre que describe la razón de la tarea (enlace caído, IP, UM).
- [[concepts/ingresarseguimientoregistrocontactos|ingresarSeguimientoRegistroContactos]] — función JavaScript de `Tareas.js` que construye las peticiones de reasignación.
- [[concepts/id_caso|id_caso]] — identificador numérico del caso de soporte.
- [[concepts/autoasignacion-del-caso|Autoasignacion del Caso]] — mecanismo que asigna automáticamente el caso a un empleado y departamento.
- [[concepts/actualizarhipotesis|hipotesis]] — estructura JSON con síntoma e hipótesis de diagnóstico.
- [[concepts/empleado_asignado|empleado_asignado]] — empleado responsable, codificado como `237805@@594591`.
- [[concepts/fecha_ejecucion|fecha_ejecucion]] — parámetros de fecha y hora de ejecución de la tarea.
- [[concepts/numero_tarea|numero_tarea]] — identificador único de cada tarea individual.
- [[concepts/puerto-connected-no-aprende-mac|Puerto connected, no aprende MAC]] — síntoma técnico recurrente en el campo motivo.
- [[concepts/101-telcos-zabbix-optimizaciones|101. Telcos - Zabbix optimizaciones]] — concepto paraguas de esta optimización.

## Puntos principales

- La nota documenta la automatización de la operación de soporte en la plataforma [[entities/telcos|Telcos]] (telcos.telconet.ec), integrada con el monitoreo [[entities/zabbix|Zabbix]].
- El endpoint [[concepts/actualizarhipotesis|actualizarHipotesis]] asigna casos con [[concepts/id_caso|id_caso]] y un objeto JSON [[concepts/actualizarhipotesis|hipotesis]] que incluye el síntoma "Caída del servicio" y la hipótesis "Indisponibilidad del servicio".
- El endpoint [[concepts/reasignartarea|reasignarTarea]] crea y reasigna tareas de "Troubleshooting proactivo" (id_tarea=4023) con campos como [[concepts/id_detalle|id_detalle]], intIdDetalleHist y [[concepts/empleado_asignado|empleado_asignado]].
- Las tareas se autoasignan a Jaime Adrian Bonilla Fernandez (empleado 237805, personaEmpresaRol 594591) del departamento 132 mediante [[concepts/autoasignacion-del-caso|Autoasignacion del Caso]].
- El campo [[concepts/id_detalle|id_detalle]] es clave y debe rastrearse en las peticiones que [[entities/zabbix|Zabbix]] genera; en el frontend se asigna a `txtDetalleTareaSeg` mediante `objTarea.id_detalle` en `Tareas.js` ([[concepts/ingresarseguimientoregistrocontactos|ingresarSeguimientoRegistroContactos]]).
- Endpoints auxiliares documentados: [[concepts/reiniciaestadorelacion|reiniciaEstadoRelacion]], [[concepts/obtenerhoraserver|obtenerHoraServer]] y exportarConsulta (con campos `hid_*`).
- El ejemplo cifrado usa codificación URL (%7B, %22, %5Cu00edda) y su equivalente JSON descifrado, mostrando el formato exacto esperado por la API.
- El síntoma recurrente [[concepts/puerto-connected-no-aprende-mac|Puerto connected, no aprende MAC]] guía la clasificación y el envío de notificaciones.
- Quedan pendientes: un convertidor hexadecimal a decimal para el ingreso de APs y el envío automático de correos para los APs.

## Menciones en la fuente

- "POST https://telcos.telconet.ec/soporte/info_caso/actualizarHipotesis" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "POST https://telcos.telconet.ec/soporte/tareas/reasignarTarea" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "GET https://telcos.telconet.ec/soporte/info_caso/reiniciaEstadoRelacion?idDetalleTarea=49614306&estado=Activo" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "UM: sw1fortinesuio.telconet.net Fa0/33. Puerto connected, no aprende MAC y no ahi ping vrf." — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "Revisar peticiones al crera tareas desde el zabbix en busqueda del campo ***id_detalle***" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "id_detalle=49919695&id_tarea=4023&motivo=Mediante monitoreo se verifica enlace PRINCIPAL caído, asociado al login aux: aelgato-6demarzo_1 con IP: 10.202.75.10." — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- ""nombre_asignacionCaso":"Jaime Adrian Bonilla Fernandez","personaEmpresaRol_asignacionCaso":"594591"" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "empleado_asignado=237805%40%40594591" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "id_caso=1981368445&hipotesis={"total":1,"hipotesis":[{"id_sintomaHipotesis":381,"nombre_sintomaHipotesis":"Caída del servicio","id_hipotesis":"Indisponibilidad del servicio"" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "id_detalle=49413265&id_tarea=4023&motivo=Mediante monitoreo se verifica enlace caído, asociado al login aux: happy-comitepueblo2_2 con IP: 10.221.135.174." — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]