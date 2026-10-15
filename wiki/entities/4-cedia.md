---
type: entity
created: 2026-09-23
updated: 2026-09-23
generation_complete: true
sources:
  - "[[sources/4-cedia_d7cef1]]"
  - "[[sources/4-1-telcograph_4a563a]]"
tags:
aliases:
  - "4 Cedia"
  - "Cliente CEDIA"
  - "CEDIA"
---

# 4 Cedia

## Descripción

**4 Cedia** es un rol operativo asociado al cliente [[CEDIA]] dentro de [[Telconet]], responsable de la atención y el monitoreo de los servicios de red contratados por dicha institución. El rol contempla la gestión de tareas escaladas a los jefes de área de Quito ([[Julia Marchan]]) y de Guayaquil ([[Edson Hidalgo]]), así como la elaboración y validación del **Informe Ejecutivo** que se genera ante una caída de equipo. Dicho informe exige campos obligatorios: cliente afectado, servicios, fechas, casos, departamento asignado, análisis, acciones correctivas, plan de mejoramiento y status.

Para el desempeño de sus funciones, el rol utiliza herramientas como [[Telcograph]], [[SAM CLIENT]], Telcos y [[Zabbix]], e incluye credenciales de acceso para SAM CLIENT, Nokia, CheckPoint VPN, Fiberhome y Telcograph Clientes. La documentación incluye además un caso real de CEDIA con errores en el enlace PE-AMB-SDH-1 y la interfaz 1/1/4, con la indicación de los equipos y servicios afectados.

En el plano técnico, el rol abarca comandos de diagnóstico como `show lag description` y `show port`, procedimientos para el ingreso de monitoreo OLT, el cambio de usuario en Telcograph, el cambio de correo de notificación proactiva y la configuración de monitoreo desde cero en Zabbix. Finalmente, se listan rutas de red ADD/DELETE y direcciones de servidores internos.

## Entidades relacionadas

- [[entities/4-cedia|CEDIA]]
- [[entities/telcograph|Telcograph]]
- [[entities/sam-client|SAM CLIENT]]

## Conceptos relacionados