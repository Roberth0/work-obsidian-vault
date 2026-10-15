---
type: entity
created: 2026-09-23
updated: 2026-09-23
generation_complete: true
sources:
  - "[[sources/101-telcos-zabbix-optimizaciones_942fa6]]"
  - "[[sources/2-vips_147ea4]]"
  - "[[sources/2-1-cscg_5bb2db]]"
  - "[[sources/3-corporativos_04d2e4]]"
  - "[[sources/4-cedia_d7cef1]]"
tags:
  - "product"
aliases:
  - "Zabbix monitoring"
  - "Zabbix Server"
---

# Zabbix

## Descripción

Zabbix es la plataforma de monitoreo que actúa como sistema origen de la información en el flujo de trabajo con [[Telcos]]. Desde Zabbix se generan automáticamente las tareas y los casos que luego se envían a Telcos, por lo que constituye el punto de partida de todo el proceso operativo descrito en la fuente.

Las tareas generadas son de tipo "Troubleshooting proactivo" y se disparan por la detección de enlaces caídos reportados por Zabbix. Esto convierte a la plataforma en el detonante de la actividad de soporte y seguimiento, en lugar de un sistema de reporte pasivo.

La nota vinculada menciona explícitamente la necesidad de revisar las peticiones creadas desde Zabbix para identificar el campo [[id_detalle]], considerado clave para la automatización. Dicho campo es el que permite enlazar la petición originada en el monitoreo con su registro correspondiente en el sistema destino.

En el contexto de [[telconet]], Zabbix es simultáneamente la fuente de los datos y el objeto de la optimización documentada, ya que las mejoras descritas buscan ordenar y estandarizar la información que la plataforma entrega hacia las herramientas de gestión de casos.

En el contexto de CSCG, el rol de Zabbix se amplía también a la creación de casos, no solo de tareas: se debe crear el caso desde Zabbix por la caída de la ONT, y si se verifica que no se tiene respuesta ICMP, se debe crear un caso por la caída de la cámara o cámaras desde Zabbix, para lo cual es necesario conocer su IP mediante la opción de inventario del propio Zabbix.

Asimismo, dentro del horario se debe crear una tarea hacia ***ANDY ENRIQUE BARBERAN CORTEZ*** desde el Zabbix de monitoreo; al crearse, la tarea se asigna al perfil propio en [[Telcos]], donde debe reasignarse hacia Andy Barberan. De este modo, la herramienta se consolida como el punto de partida y registro de las incidencias antes de su escalamiento a los niveles L1 y TS en el contexto operativo de CSCG.

La operación de Zabbix se realiza ingresando al Zabbix de Backbone y al dashboard disponible en https://monitoreorda.telconet.ec/zabbix/, lo que precisa la instancia y la ubicación concreta desde la que se gestiona la plataforma.

Zabbix también funciona como fuente de verdad para confirmar la fecha y hora de finalización de los incidentes en el Informe Ejecutivo, ya que la hora de subida del equipo se verifica mediante la resolución de la alarma en la herramienta.

Asimismo, la plataforma admite tareas de administración y configuración: con el nombre del grupo se ingresa en la sección Administración del Zabbix => Usuarios y se busca el alias de notificaciones (a-z) para cambiar el correo de notificación proactiva del cliente; además, el ingreso de monitoreo desde cero requiere 1) crear el nuevo grupo, 2) crear el MEDIA TYPE (clonar o new), 3) crear el ACTION (clonar o new) añadiendo el host group y el media type en Update operations, y 4) en Administración / Users añadir el correo del cliente al usuario de notificación (el segundo, notificaciones2).
## Entidades relacionadas

- [[entities/telcos|Telcos]]
- [[entities/telconet|telconet]]
- [[entities/oss|OSS]]
- [[entities/olt|OLT]]
- [[entities/ont|ONT]]
- [[entities/andy-enrique-barberan-cortez|Andy Enrique Barberan Cortez]]
- [[entities/cedia|CEDIA]]
- [[entities/fiberhome|fiberhome]]

## Conceptos relacionados

- [[concepts/id_detalle|id_detalle]]

## Menciones en la fuente

- "Revisar peticiones al crera tareas desde el zabbix en busqueda del campo ***id_detalle***" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "id_detalle=49919695&id_tarea=4023&motivo=Mediante monitoreo se verifica enlace PRINCIPAL caído, asociado al login aux: aelgato-6demarzo_1 con IP: 10.202.75.10." — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "Se debe crear el caso desde el zabbix por la caida de la ONT" — [[Work/2.1 CSCG|2.1 CSCG]]
- "Dentro del horario se debe crear una tarea hacia ***ANDY ENRIQUE BARBERAN CORTEZ*** desde el zabbix de monitoreo" — [[Work/2.1 CSCG|2.1 CSCG]]
- "Si se verifica que no se tiene respuesta ICMP se debe crear un caso por la caida de la camara/s desde el zabbix" — [[Work/2.1 CSCG|2.1 CSCG]]
- "**Fecha y hora de finalizacion:** Verificar hora de subida del equipo mediante resolucion de alarma en el zabbix" — [[Work/4 Cedia|4 Cedia]]
- "Se debe ingresar en el zabbix de Backbone y en el siguiente dashboard https://monitoreorda.telconet.ec/zabbix/" — [[Work/4 Cedia|4 Cedia]]
- "Con el nombre del grupo se debe ingresar en la seccion Administracion del zabbix => Usuarios y buscar el alias de *notificaciones(a-z)*" — [[Work/4 Cedia|4 Cedia]]