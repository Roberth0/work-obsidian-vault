---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/101-telcos-zabbix-optimizaciones_942fa6]]"
tags:
aliases:
  - "Telcos - Zabbix optimizaciones"
  - "Optimizaciones Zabbix en Telcos"
  - "Automatización de soporte Telcos con Zabbix"
generation_complete: true
---

# 101. Telcos - Zabbix optimizaciones

## Definición

**101. Telcos - Zabbix optimizaciones** es una nota técnica que documenta el conjunto de peticiones HTTP utilizadas para automatizar la operación de soporte dentro de la plataforma [[Telcos]] de Telconet, en su integración con el sistema de monitoreo [[Zabbix]]. La nota describe los flujos de asignación de casos y de asignación/reasignación de tareas de *troubleshooting*, junto con los endpoints auxiliares necesarios para completar dichos flujos.

Se trata de un documento de referencia operativa: registra los contratos de comunicación (URLs, parámetros y formatos de cuerpo) que permiten que la monitorización de Zabbix derive en tareas de soporte ejecutables dentro de la plataforma Telcos.

## Características clave

- **Dos flujos principales documentados**: la asignación de casos mediante el endpoint `actualizarHipotesis` y la asignación/reasignación de tareas de *troubleshooting* mediante `reasignarTarea`.
- **Múltiples formatos de cuerpo de petición**: se incluyen ejemplos reales tanto en *URL-encoded* como en JSON.
- **Campos recurrentes en las peticiones**: `id_caso`, `id_detalle`, `id_tarea`, `intIdDetalleHist`, `empleado_asignado`, `fecha_ejecucion` y `hora_ejecucion`.
- **Endpoints auxiliares complementarios**:
  - `reiniciaEstadoRelacion`: cambia el estado de una tarea a *Activo*.
  - `obtenerHoraServer`: permite sincronizar la hora.
  - `exportarConsulta`: exportación de consultas.
- **Campo clave identificado**: `id_detalle` debe poder rastrearse al crear tareas desde Zabbix. La nota referencia el código JavaScript del archivo `Tareas.js`, que asigna dicho valor al campo `txtDetalleTareaSeg`.
- **Tareas pendientes declaradas por el autor**: un convertidor de hexadecimal a decimal para el ingreso de APs y el envío automático de correos para los APs.
- **Naturaleza evolutiva**: el documento combina procedimientos ya operativos con trabajo pendiente, por lo que funciona como bitácora técnica además de referencia de API.

## Aplicaciones

- **Automatización de la asignación de casos** en la plataforma Telcos a partir de eventos detectados por Zabbix, usando `actualizarHipotesis`.
- **Asignación y reasignación de tareas de troubleshooting**, tanto a nivel individual como por historial de detalle (`intIdDetalleHist`), mediante `reasignarTarea`.
- **Reactivación de tareas** cerradas o inactivas por medio de `reiniciaEstadoRelacion`.
- **Sincronización horaria** de los procesos automatizados con `obtenerHoraServer`, relevante para el correcto llenado de `fecha_ejecucion` y `hora_ejecucion`.
- **Integración monitor–soporte**: vincular alarmas de Zabbix con acciones concretas de soporte, garantizando la trazabilidad mediante `id_detalle`.
- **Extracción y análisis de datos** operativos a través de `exportarConsulta`.
- **Desarrollo de extensiones pendientes**: normalización de identificadores de APs (hexadecimal a decimal) y notificación automática por correo para APs.

## Conceptos relacionados

- [[concepts/actualizarhipotesis|actualizarHipotesis]]

## Entidades relacionadas

- [[entities/telcos|Telcos]]
- [[entities/zabbix|Zabbix]]