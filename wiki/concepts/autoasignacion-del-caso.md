---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/101-telcos-zabbix-optimizaciones_942fa6]]"
tags:
aliases:
  - "asunto_asignacionCaso"
  - "Autoasignación del Caso"
  - "Auto Assignment of Case"
generation_complete: true
---

# Autoasignacion del Caso

## Definición

"Autoasignacion del Caso" es el valor del campo `asunto_asignacionCaso` dentro de la estructura JSON de hipótesis que se envía al endpoint [[actualizarHipotesis]]. Este campo, junto con `empleado_asignacionCaso` (237805), `departamento_asignacionCaso` (132) y `personaEmpresaRol_asignacionCaso` (594591), define que el [[id_caso|caso]] se asigne automáticamente a un empleado y a un departamento específicos, sin intervención manual en la distribución.

Se trata, por tanto, del identificador textual que activa y describe el mecanismo de autoasignación dentro del flujo de actualización de [[hipotesis]] en [[Telcos]].

## Características clave

- **Campo de asunto**: se transporta en la propiedad `asunto_asignacionCaso` de la estructura JSON de hipótesis, no como un parámetro independiente.
- **Asignación determinista**: el caso queda vinculado a un empleado concreto (`empleado_asignacionCaso` = 237805) y a un departamento concreto (`departamento_asignacionCaso` = 132).
- **Rol asociado**: el campo `personaEmpresaRol_asignacionCaso` (594591) identifica el rol de la persona dentro de la empresa que recibe la asignación.
- **Metadatos fijos**: la `observacion_asignacionCaso` se registra como `"."` y el `origen` como `"Nuevo"`.
- **Responsable identificado**: el `nombre_asignacionCaso` corresponde a Jaime Adrian Bonilla Fernandez.
- **Uso recurrente**: el asunto aparece en los dos ejemplos de actualización de hipótesis documentados, correspondientes a los casos 1981368445 y 1981368444.
- **Automatización**: sustituye la distribución manual de casos por una regla embebida en la propia petición de actualización.

## Aplicaciones

- **Actualización masiva de hipótesis**: al enviar hipótesis al endpoint [[actualizarHipotesis]], incluir este asunto garantiza que cada caso se derive al empleado y departamento definidos.
- **Enrutamiento automático de casos**: permite que los casos nuevos (`origen` = `"Nuevo"`) entren directamente en la cola del equipo responsable, reduciendo tiempos de triaje.
- **Integración con Zabbix y monitoreo de Telcos**: dentro de las optimizaciones descritas para Telcos, la autoasignación asegura que las incidencias detectadas se atribuyan a un [[empleado_asignado|empleado asignado]] sin pasos intermedios.
- **Trazabilidad**: el uso de valores constantes (observación `"."`, persona-rol y departamento fijos) facilita auditar qué casos fueron autoasignados y bajo qué configuración.

## Conceptos relacionados

- [[concepts/actualizarhipotesis|actualizarHipotesis]]
- [[concepts/id_caso|id_caso]]
- [[concepts/actualizarhipotesis|hipotesis]]
- [[concepts/empleado_asignado|empleado_asignado]]

## Entidades relacionadas

- [[entities/telcos|Telcos]]

## Menciones en la fuente

- ""asunto_asignacionCaso":"Autoasignacion del Caso","departamento_asignacionCaso":132,"empleado_asignacionCaso":"237805"" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- ""observacion_asignacionCaso":".","nombre_asignacionCaso":"Jaime Adrian Bonilla Fernandez","personaEmpresaRol_asignacionCaso":"594591"" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]