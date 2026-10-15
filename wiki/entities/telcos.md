---
type: entity
created: 2026-09-23
updated: 2026-09-23
generation_complete: true
sources:
  - "[[sources/101-telcos-zabbix-optimizaciones_942fa6]]"
  - "[[sources/4-cedia_d7cef1]]"
tags:
  - "product"
aliases:
  - "Plataforma Telcos"
  - "telcos.telconet.ec"
  - "Telcos Telconet"
---

# Telcos

## Descripción

Telcos es la plataforma de gestión de soporte y tareas accesible en `telcos.telconet.ec`, sobre la cual se ejecutan todas las peticiones documentadas en la fuente. Constituye el sistema destino de la automatización que conecta el monitoreo de [[Zabbix]] con la operación de casos y tareas de [[Telconet]], de modo que su API es el núcleo alrededor del cual gira toda la optimización descrita.

La plataforma expone endpoints orientados a la operación de casos y tareas, entre ellos `/soporte/info_caso/actualizarHipotesis`, `/soporte/tareas/reasignarTarea`, `/soporte/info_caso/reiniciaEstadoRelacion`, `/soporte/tareas/obtenerHoraServer` y `/soporte/tareas/exportarConsulta`. Su API acepta parámetros codificados en formato URL-encoded y devuelve respuestas en JSON, lo que condiciona las estrategias de construcción de peticiones y de análisis de respuestas empleadas por la automatización.

Desde la perspectiva funcional, Telcos actúa como punto de convergencia entre el diagnóstico técnico proveniente del monitoreo y las acciones administrativas sobre los casos: la actualización de hipótesis mediante [[actualizarHipotesis]], la reasignación de responsables mediante [[reasignarTarea]] y el reinicio de estados de relación se apoyan en identificadores como [[id_detalle]] para localizar el registro correcto.

El acceso a la plataforma se realiza en `telcos.telconet.ec`, asociada a la dirección de red interna `172.24.15.70`. En el plano operativo, Telcos constituye una herramienta central para la gestión del ciclo de vida de los incidentes: en ella se abre el caso y se verifica el seguimiento de las tareas y los campos del informe. Adicionalmente, la gestión de contactos técnicos se realiza desde el menú comercial, donde el nuevo correo debe quedar registrado tanto como *contacto cliente* como *contacto punto*.
## Entidades relacionadas

- [[entities/telconet|telconet]]
- [[entities/zabbix|Zabbix]]

## Conceptos relacionados

- [[concepts/actualizarhipotesis|actualizarHipotesis]]
- [[concepts/reasignartarea|reasignarTarea]]
- [[concepts/id_detalle|id_detalle]]

## Menciones en la fuente

- "POST https://telcos.telconet.ec/soporte/info_caso/actualizarHipotesis" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "POST https://telcos.telconet.ec/soporte/tareas/reasignarTarea" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "Se debe abrir el caso en Telcos y verificar el seguimiento de las tareas y los campos del informe" — [[Work/4 Cedia|4 Cedia]]
- "El nuevo correo debe estar registrado como contacto tecnio en telcos, desde el menu comercial, tanto como *contacto cliente* y *contacto punto*" — [[Work/4 Cedia|4 Cedia]]
- "telcos.telconet.ec,   172.24.15.70" — [[Work/4 Cedia|4 Cedia]]