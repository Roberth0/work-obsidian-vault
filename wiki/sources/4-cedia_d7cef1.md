---
type: source
created: 2026-09-23
updated: 2026-09-23
source_file: "[[Work/4 Cedia.md]]"
tags: [cedia]
aliases: ["Rol Operativo Cedia", "Cedia - Gestión de Incidentes Telconet"]
contentHash: 1418-63f630af
generation_complete: true
---

# 4 Cedia - Resumen

## Fuente

- Archivo original: [[Work/4 Cedia.md]]
- Ingerido: 2026-09-23

## Contenido principal

Este documento describe el rol operativo asociado al cliente [[entities/cedia|CEDIA]] dentro de [[entities/telconet|Telconet]], centrado en aceptar y resolver las tareas que llegan a los jefes de área de Quito (**Julia Marchan**) y Guayaquil (**Edson Hidalgo**). Detalla el procedimiento para elaborar y validar el [[concepts/informe-ejecutivo|Informe Ejecutivo]] que se genera ante una caída de equipo, especificando todos los campos obligatorios y el criterio especial para el [[concepts/caso-interurbano|caso interurbano]], donde la hora de finalización la determinan los clientes afectados (Nedetel, Xtrim, Claro, etc.). Explica el uso de herramientas como [[entities/telcograph|Telcograph]], [[entities/sam-client|SAM CLIENT]], [[entities/telcos|Telcos]] y [[entities/zabbix|Zabbix]], e incluye credenciales de acceso a varios sistemas. También documenta procedimientos de diagnóstico mediante comandos como [[concepts/show-lag-description|show lag description]] y [[concepts/show-port|show port]], el acceso a través de [[concepts/vpn|VPN]], el [[concepts/monitoreo-olt|Monitoreo OLT]], la [[concepts/notificación-proactiva|notificación proactiva]] y la gestión de rutas de red.

## Entidades clave

- [[entities/cedia|CEDIA]] — cliente de red académica cuyos enlaces se monitorean y atienden.
- [[entities/telconet|Telconet]] — empresa propietaria de la infraestructura y los procesos.
- [[entities/telcograph|Telcograph]] — plataforma de monitoreo y gestión de enlaces.
- [[entities/sam-client|SAM CLIENT]] — aplicación para revisar extremos de enlaces reportados.
- [[entities/telcos|Telcos]] — plataforma de gestión de casos, tareas y contactos.
- [[entities/zabbix|Zabbix]] — plataforma de monitoreo de alarmas y notificaciones.
- [[entities/nokia|Nokia]] — fabricante de equipos de red de los enlaces CEDIA.
- [[entities/concentrador-de-ambato|Concentrador de Ambato]] — punto inicial de verificación de enlaces.
- [[entities/telcodrive|telcodrive]] — servicio de almacenamiento interno de Telconet.

## Conceptos clave

- [[concepts/informe-ejecutivo|Informe Ejecutivo]] — documento formal ante caída de equipo.
- [[concepts/caso-interurbano|caso interurbano]] — incidencia entre ciudades con criterio especial de cierre.
- [[concepts/link-loss|link loss]] — alarma crítica de pérdida de enlace, prioritario.
- [[concepts/vpn|VPN]] y [[concepts/username-and-password|Username and Password]] — acceso remoto seguro.
- [[concepts/monitoreo-olt|Monitoreo OLT]] y [[concepts/notificación-proactiva|notificación proactiva]] — procedimientos sobre Zabbix.
- [[concepts/route-add-route-delete|Route ADD / Route DELETE]], [[concepts/show-lag-description|show lag description]] y [[concepts/show-port|show port]] — comandos y operaciones técnicas.

## Puntos principales

- El rol consiste en aceptar y resolver las tareas escaladas a los jefes de área de UIO (Julia Marchan) y GYE (Edson Hidalgo).
- El [[concepts/informe-ejecutivo|Informe Ejecutivo]] se elabora ante una caída de equipo y debe verificarse su redacción: cliente afectado, servicios, fechas, casos, departamento asignado, análisis, acciones correctivas, plan de mejoramiento y status.
- En un [[concepts/caso-interurbano|caso interurbano]], la hora de finalización corresponde al momento en que los clientes afectados (Nedetel, Xtrim, Claro, etc.) validan la operatividad.
- Se debe abrir el caso en [[entities/telcos|Telcos]], verificar el seguimiento de tareas y campos del informe, descargar el PDF y finalizar la tarea adjuntando el informe corregido.
- Se deben priorizar las alarmas de [[concepts/link-loss|link loss]]; el diagnóstico inicia en [[entities/sam-client|SAM CLIENT]] buscando los extremos y empezando por el [[entities/concentrador-de-ambato|Concentrador de Ambato]].
- Comandos de diagnóstico documentados: `show lag description | match UNIANDES` y `show port 2/3/2 | match tate`.
- El documento proporciona credenciales para SAM CLIENT, Nokia, CheckPoint VPN, Fiberhome y Telcograph Clientes, y define usuarios de [[concepts/vpn|VPN]] (userTelco / Telc0VPN).
- El caso CEDIA #2405210041 reporta errores en el enlace PE-AMB-SDH-1 (interfaz 1/1/4) sin afectación de equipos backbone ni servicios, con escalamiento a TS AMBATO.
- El [[concepts/monitoreo-olt|Monitoreo OLT]] se accede mediante el Zabbix de Backbone en `https://monitoreorda.telconet.ec/zabbix/`, con ingreso automático al entrar al dashboard de backbone.
- La [[concepts/notificación-proactiva|notificación proactiva]] requiere identificar el grupo del host y editar el correo en Administración ⇒ Usuarios ⇒ alias _notificaciones(a-z)_ ⇒ Media.
- El ingreso de monitoreo desde cero en [[entities/zabbix|Zabbix]] implica crear grupo, media type, action (con host group y media types) y usuario de notificación.
- Se listan rutas de red ADD/DELETE y direcciones de servidores internos de Telconet para el acceso a recursos.

## Menciones en la fuente

- "PROBLEMA: Cedia: ERRORES EN EL ENLACE : PE-AMB-SDH-1 - Interface 1/1/4(to_CPE-AMB-UTI_MS2-1)" — [[Work/4 Cedia|4 Cedia]]
- "9) Enviar a CEDIA que nos otorgue permisos para la revision del enlace de la red CEDIA / Nokia," — [[Work/4 Cedia|4 Cedia]]
- "Grupos donde se reporta: BB y OTN" — [[Work/4 Cedia|4 Cedia]]
- "Para acceder al SAM CLIENT se debe conectarse a la VPN de Cedia con las siguientes credenciales" — [[Work/4 Cedia|4 Cedia]]
- "En este rol se debe aceptar y resolver las tareas que llegan hacia los jefes de areas" — [[Work/4 Cedia|4 Cedia]]
- "- UIO  **Julia Marchan**" — [[Work/4 Cedia|4 Cedia]]
- "- GYE  **Edson Hidalgo**" — [[Work/4 Cedia|4 Cedia]]
- "### Cambio de usuario telcograph" — [[Work/4 Cedia|4 Cedia]]
- "El nuevo correo debe estar registrado como contacto tecnio en telcos, desde el menu comercial, tanto como *contacto cliente* y *contacto punto*" — [[Work/4 Cedia|4 Cedia]]
- "- Telcograph Clientes
	- noc // VCzrk"kUr3xMH~E10" — [[Work/4 Cedia|4 Cedia]]
- "1) Entrar al SAM, buscar los extremos que correspondan al enlace reportado" — [[Work/4 Cedia|4 Cedia]]
- "Usuario: `JuanGonzalez`" — [[Work/4 Cedia|4 Cedia]]
- "Nuevas Credenciales 
NOKIA. USER: SoporteTelconet // PASS: `C3d1@Tn$$N0k!@25`" — [[Work/4 Cedia|4 Cedia]]
- "Se debe abrir el caso en Telcos y verificar el seguimiento de las tareas y los campos del informe" — [[Work/4 Cedia|4 Cedia]]
- "telcos.telconet.ec,   172.24.15.70" — [[Work/4 Cedia|4 Cedia]]
- "**Fecha y hora de finalizacion:** Verificar hora de subida del equipo mediante resolucion de alarma en el zabbix" — [[Work/4 Cedia|4 Cedia]]
- "Se debe ingresar en el zabbix de Backbone y en el siguiente dashboard https://monitoreorda.telconet.ec/zabbix/" — [[Work/4 Cedia|4 Cedia]]
- "Con el nombre del grupo se debe ingresar en la seccion Administracion del zabbix => Usuarios y buscar el alias de *notificaciones(a-z)*" — [[Work/4 Cedia|4 Cedia]]
- "#Credenciales Fiberhome" — [[Work/4 Cedia|4 Cedia]]