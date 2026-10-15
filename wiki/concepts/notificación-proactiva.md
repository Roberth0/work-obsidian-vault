---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/4-cedia_d7cef1]]"
tags:
aliases:
  - "notificación proactiva de Zabbix"
  - "cambio de correo notificación proactivo"
  - "correo de notificación proactiva"
generation_complete: true
---

# notificación proactiva

## Definición

La **notificación proactiva** es el procedimiento operativo mediante el cual [[Zabbix]] envía las alertas al correo electrónico correcto en función del grupo de monitoreo al que pertenece cada host. El objetivo es asegurar que las alarmas generadas por la plataforma de monitoreo lleguen a los destinatarios adecuados y que cada grupo reciba únicamente las notificaciones que le corresponden.

## Características clave

- **Dependencia del grupo del host**: el correo de destino no se define por host individual, sino por el grupo de monitoreo al que el host está asociado.
- **Configuración centralizada en Zabbix**: la administración se realiza desde la sección *Administración* de la interfaz de Zabbix, no desde la configuración de cada host.
- **Identificación por alias**: el proceso requiere buscar el alias de notificaciones en orden alfabético (a–z) para localizar el registro correspondiente.
- **Edición en la subsección Media**: el cambio de correo se efectúa abriendo la subsección *Media* del alias y editando la dirección asociada al grupo.
- **Carácter correctivo**: se utiliza cuando un grupo de monitoreo cambia de responsable, de área o cuando la dirección de correo configurada deja de ser válida.
- **Trazabilidad del destinatario**: permite verificar el grupo del host como paso previo, garantizando que la modificación afecte al conjunto correcto de alarmas.

## Aplicaciones

- **Actualización de destinatarios tras cambios organizativos**: cuando un grupo de monitoreo cambia de responsable o de equipo, se actualiza el correo asociado al grupo para que las alarmas sigan llegando a las personas correctas.
- **Corrección de alarmas no entregadas**: si un grupo deja de recibir notificaciones porque la dirección configurada es inválida u obsoleta, se corrige el correo mediante este procedimiento.
- **Alta de nuevos grupos de monitoreo**: al incorporar un nuevo grupo de hosts a la plataforma, se define el alias y la dirección de correo que recibirá sus alarmas.
- **Operación de monitoreo en backbone**: aplicable al entorno de [[Zabbix]] de backbone, donde las alarmas de infraestructura deben llegar a los equipos de guardia correspondientes.
- **Soporte al [[Monitoreo OLT]]**: los hosts asociados al monitoreo de equipos OLT se benefician de la correcta asignación de destinatarios por grupo.

## Conceptos relacionados

- [[concepts/monitoreo-olt|Monitoreo OLT]]

## Entidades relacionadas

- [[entities/zabbix|Zabbix]]
- [[entities/telconet|Telconet]]

## Menciones en la fuente

- "### Cambio de correo notificacon proactivo" — [[Work/4 Cedia|4 Cedia]]
- "Se debe verificar a que grupo pertence el host en cuestion" — [[Work/4 Cedia|4 Cedia]]
- "Con el nombre del grupo se debe ingresar en la seccion Administracion del zabbix => Usuarios y buscar el alias de *notificaciones(a-z)*" — [[Work/4 Cedia|4 Cedia]]