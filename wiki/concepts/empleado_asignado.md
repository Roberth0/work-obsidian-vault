---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/101-telcos-zabbix-optimizaciones_942fa6]]"
tags:
aliases:
  - "empleado_asignacionCaso"
  - "237805@@594591"
  - "assigned employee"
generation_complete: true
---

# empleado_asignado

## Definición

`empleado_asignado` es el parámetro que identifica al empleado responsable de una tarea o caso en [[Telcos]]. Su valor codifica de forma conjunta el número de empleado y su rol mediante un separador de doble arroba, por ejemplo `237805@@594591`; cuando se transmite dentro de una petición HTTP, el separador se envía URL-encoded como `237805%40%40594591`.

## Características clave

- **Formato compuesto:** une dos identificadores —número de empleado y rol— en una sola cadena separada por `@@`.
- **Codificación en transporte:** en las peticiones web el separador aparece como `%40%40`, lo que obliga a decodificar el valor antes de interpretarlo.
- **Uso consistente y acotado:** aparece de forma sistemática en todas las peticiones a [[reasignarTarea]], siempre acompañado de `departamento_asignado=132` y `tipo_asignado=empleado`.
- **Exclusividad de tipo de asignación:** en los ejemplos analizados, la asignación a empleado convive con [[cuadrilla_asignada]] y [[contratista_asignada]] vacíos, lo que lo distingue de otros modos de asignación.
- **Correspondencia en el flujo de hipótesis:** el mismo identificador se desdobla en dos campos, `empleado_asignacionCaso` (`237805`) y `personaEmpresaRol_asignacionCaso` (`594591`), asociados a Jaime Adrian Bonilla Fernandez.
- **Sensibilidad a la codificación:** una construcción incorrecta del valor (por ejemplo, no escapar las arrobas o alterar el orden empleado/rol) provoca que la reasignación no apunte al responsable esperado.

## Aplicaciones

- **Automatización de asignaciones desde Zabbix:** construir programáticamente el valor `empleado_asignado` es el paso crítico para que una alerta de Zabbix derive en la reasignación correcta del caso al técnico adecuado.
- **Integración con [[reasignarTarea]]:** el parámetro forma parte del conjunto mínimo de datos que debe enviarse en cada llamada de reasignación, junto con `departamento_asignado` y `tipo_asignado`.
- **Mapeo entre sistemas:** traducir entre la representación compacta (`237805@@594591`) y los campos desagregados del flujo de hipótesis (`empleado_asignacionCaso` + `personaEmpresaRol_asignacionCaso`) permite reconciliar datos entre el sistema origen y el destino.
- **Trazabilidad de responsabilidad:** sirve como referencia para saber a quién quedó encomendada una tarea una vez ejecutada la operación, en conjunto con [[fecha_ejecucion]].

## Conceptos relacionados

- [[concepts/reasignartarea|reasignarTarea]]
- [[concepts/autoasignacion-del-caso|Autoasignacion del Caso]]
- [[concepts/login-aux|login aux]]
- [[concepts/fecha_ejecucion|fecha_ejecucion]]

## Entidades relacionadas

- [[entities/telcos|Telcos]]

## Menciones en la fuente

- "empleado_asignado=237805%40%40594591&cuadrilla_asignada=&contratista_asignada=&tipo_asignado=empleado" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "&empleado_asignado=237805%40%40594591&cuadrilla_asignada=&contratista_asignada=&tipo_asignado=empleado&login=telepizza-shoppingportoviejo2" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]