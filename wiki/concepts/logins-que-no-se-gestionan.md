---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/2-vips_147ea4]]"
tags:
aliases:
  - "Logins no gestionados"
  - "Usuarios que no se gestionan"
  - "Non-managed logins"
generation_complete: true
---

# Logins que no se gestionan

## Definición

**Logins que no se gestionan** es la lista de identificadores de acceso (*logins*) que no deben ser atendidos ni gestionados por el equipo de monitoreo VIPS. Se trata de una lista de exclusión operativa: cualquier alerta, notificación o evento asociado a estos identificadores queda fuera del flujo de gestión, ya que corresponden a cuentas de prueba, internas o de uso técnico que no representan clientes reales.

Los valores incluidos en la lista son: `tlw`, `prueba`, `docker prueba`, `lan`, `saturacion`, `cm` y `safeentry`.

## Características clave

- **Lista cerrada y explícita**: los identificadores excluidos están enumerados de forma concreta (`tlw`, `prueba`, `docker prueba`, `lan`, `saturacion`, `cm`, `safeentry`).
- **Naturaleza no-cliente**: agrupa cuentas de prueba, internas o de uso técnico/infraestructura, no cuentas de clientes monitoreados.
- **Sin gestión operativa**: no generan tareas, casos ni seguimiento proactivo por parte del equipo de monitoreo.
- **Función de filtrado de ruido**: su propósito es evitar que el personal abra tareas o casos sobre estos identificadores.
- **Carácter de recordatorio rápido**: la nota se plantea como un apoyo de consulta ágil para el personal en turno.
- **Alcance acotado a los entornos monitoreados**: aplica a la operación de VIPS en UIO, GYE y Camaras Corporacion GYE.

## Aplicaciones

- **Triaje de alertas**: al recibir una notificación, el operador verifica primero si el login figura en esta lista antes de abrir un caso.
- **Onboarding de personal nuevo**: sirve como referencia rápida para que los nuevos analistas no generen gestión sobre cuentas técnicas.
- **Depuración de proactivos**: evita que los reportes o seguimientos proactivos incluyan eventos originados por estas cuentas.
- **Concentración del esfuerzo**: redirige la capacidad operativa hacia los clientes reales monitoreados en UIO, GYE y Camaras Corporacion GYE.
- **Documentación de excepciones**: respalda la decisión de no gestionar un identificador cuando se cuestiona la ausencia de seguimiento sobre una alerta.

## Conceptos relacionados

- [[concepts/vips|VIPS]]
- [[concepts/etiqueta-notificacion-247|Etiqueta notificacion 24/7]]
- [[concepts/caso-o-tarea-ya-aperturado-por-algun-tiempo|Caso o tarea ya aperturado por algun tiempo]]

## Entidades relacionadas

- [[entities/zabbix|zabbix]]

## Menciones en la fuente

- ">[!tip]+ Logins que no se gestionan
tlw
prueba
docker prueba
lan
saturacion
cm
safeentry" — [[Work/2. VIPS|2. VIPS]]