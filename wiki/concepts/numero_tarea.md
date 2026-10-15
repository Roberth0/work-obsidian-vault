---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/101-telcos-zabbix-optimizaciones_942fa6]]"
tags:
aliases:
  - "numeroTarea"
  - "número de tarea"
  - "hid_numeroTarea"
generation_complete: true
---

# numero_tarea

## Definición

`numero_tarea` es el identificador único de una tarea individual dentro de la plataforma [[Telcos]]. Se distingue de [[id_detalle|id_tarea]], que en este flujo no identifica la tarea concreta sino que agrupa su tipo (por ejemplo, `4023` para "Troubleshooting proactivo"). Mientras `id_tarea` clasifica, `numero_tarea` singulariza: cada petición de reasignación se refiere a una tarea concreta y trazable mediante este valor.

## Características clave

- **Identificador único de instancia**: cada valor de `numero_tarea` corresponde a una tarea específica, no a una categoría de tarea.
- **Valores de ejemplo**: aparece con valores como `114977930`, `115349090`, `115441273`, `116102560` o `119214634` en las peticiones analizadas.
- **Acompañamiento constante**: siempre se presenta junto a `nombre_tarea` y `nombreFinTarea`, ambos con el valor "Troubleshooting proactivo".
- **Contexto de fin de tarea**: en cada petición de reasignación viaja junto a `idFinTarea=4023` y `motivoFinTarea="Sin Motivo"`.
- **Consultable**: el endpoint `exportarConsulta` permite buscar por `hid_numeroTarea`, lo que confirma su estatus de criterio de consulta válido y no solo de campo informativo.
- **Naturaleza numérica**: se expresa como entero largo, sin prefijos ni formato semántico, lo que lo hace apto para búsquedas exactas.

## Aplicaciones

- **Rastreo de tareas individuales**: permite seguir el ciclo de vida de una tarea concreta a lo largo del flujo automatizado, desde su detección hasta su cierre o reasignación.
- **Reasignación automatizada**: se incluye en cada petición de [[reasignarTarea]] para que el sistema receptor sepa exactamente qué tarea se está moviendo.
- **Consultas y exportaciones**: sirve como clave de búsqueda en `exportarConsulta` mediante el parámetro `hid_numeroTarea`.
- **Auditoría y trazabilidad**: al ser único, facilita la reconciliación entre registros de origen y destino y la detección de duplicados o tareas huérfanas.
- **Depuración de integraciones**: al contrastarlo con [[id_detalle|id_tarea]], permite verificar que el mapeo entre tipo de tarea e instancia concreta es correcto.

## Conceptos relacionados

- [[concepts/reasignartarea|reasignarTarea]]
- [[concepts/id_detalle|id_detalle]]
- [[concepts/login-aux|login aux]]
- [[concepts/motivo|motivo]]
- [[concepts/id_caso|id_caso]]

## Entidades relacionadas

- [[entities/telcos|Telcos]]

## Menciones en la fuente

- "numero_tarea=114977930&nombreFinTarea=Troubleshooting proactivo&idFinTarea=4023" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "hid_numeroTarea=&hid_numeroCaso=&hid_departamento=&hid_opcion_busqueda=N" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]