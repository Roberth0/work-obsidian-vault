---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/101-telcos-zabbix-optimizaciones_942fa6]]"
tags:
aliases:
  - "idCaso"
  - "identificador de caso"
  - "ID del caso"
generation_complete: true
---

# id_caso

## Definición

`id_caso` es el identificador numérico del caso de soporte dentro de la plataforma [[Telcos]]. Se utiliza como parámetro principal en la petición [[actualizarHipotesis]] y aparece también en el código JavaScript de seguimiento, lo que permite vincular cada tarea con el caso al que pertenece.

## Características clave

- Es un identificador **numérico** de formato largo; en los ejemplos del documento adopta valores como `1981368445` y `1981368444`.
- Funciona como **parámetro de entrada** de la petición [[actualizarHipotesis]], por lo que determina sobre qué caso se registra la información.
- Aparece referenciado en el código de seguimiento del lado cliente mediante `var idCaso = arraySeguimientoRegistroContacto.id_caso`, lo que evidencia su rol como clave de correlación entre tareas, hipótesis y contactos.
- Es distinto de `numeroCaso`, que emplea un formato tipo fecha (por ejemplo `20241124-1012`), y de [[id_detalle]], que identifica la tarea concreta y no el caso.
- Es un valor estable y reutilizado a lo largo del flujo de soporte: un mismo caso puede acumular múltiples tareas e hipótesis.

## Aplicaciones

- **Autoasignación de casos**: se emplea en escenarios de [[Autoasignacion del Caso]] para casos de indisponibilidad del servicio, tal como muestran los ejemplos `1981368445` y `1981368444`.
- **Actualización de hipótesis**: sirve como referencia obligatoria al invocar [[actualizarHipotesis]], asociando la [[hipotesis]] al caso correcto.
- **Seguimiento de contactos**: en [[ingresarSeguimientoRegistroContactos]] el identificador viaja en la estructura `arraySeguimientoRegistroContacto` bajo la propiedad `id_caso`, permitiendo registrar el contacto sobre el caso adecuado.
- **Correlación y trazabilidad**: permite cruzar hipótesis, tareas ([[id_detalle]]) y registros de contacto dentro del flujo de soporte de [[Telcos]].

## Conceptos relacionados

- [[concepts/actualizarhipotesis|actualizarHipotesis]]
- [[concepts/id_detalle|id_detalle]]
- [[concepts/actualizarhipotesis|hipotesis]]
- [[concepts/autoasignacion-del-caso|Autoasignacion del Caso]]
- [[concepts/ingresarseguimientoregistrocontactos|ingresarSeguimientoRegistroContactos]]

## Entidades relacionadas

- [[entities/telcos|Telcos]]

## Menciones en la fuente

- "POST https://telcos.telconet.ec/soporte/info_caso/actualizarHipotesis" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "id_caso=1981368445&hipotesis={"total":1,"hipotesis":[{"id_sintomaHipotesis":381" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "var idCaso = arraySeguimientoRegistroContacto.id_caso;" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]