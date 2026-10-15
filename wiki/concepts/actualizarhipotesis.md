---
type: concept
created: 2026-09-23
updated: 2026-09-23
generation_complete: true
sources:
  - "[[sources/101-telcos-zabbix-optimizaciones_942fa6]]"
tags:
  - "term"
aliases:
  - "Actualizar hipótesis"
  - "Asignar Caso Telcos"
  - "Actualizar hipotesis"
  - "hipotesis"
---

# actualizarHipotesis

## Definición

`actualizarHipotesis` es el endpoint POST de la plataforma [[Telcos]], accesible en la ruta `/soporte/info_caso/actualizarHipotesis`, que permite **asignar un caso a un empleado** y **ingresar la hipótesis diagnóstica** asociada a ese caso. Constituye el mecanismo central para crear y clasificar casos de indisponibilidad de servicio dentro del flujo de soporte técnico.

La operación recibe el parámetro `id_caso` y un objeto JSON llamado `hipotesis`, que transporta tanto la información del síntoma y del diagnóstico como los datos de asignación del caso.

## Características clave

- **Método HTTP POST**: se invoca enviando datos al servidor, no como consulta de solo lectura.
- **Ruta fija**: `/soporte/info_caso/actualizarHipotesis`.
- **Parámetros de entrada**:
  - `id_caso`: identificador del caso que se desea actualizar.
  - `hipotesis`: objeto JSON con los campos del síntoma, la hipótesis y la asignación.
- **Campos del objeto `hipotesis`**:
  - `id_sintomaHipotesis` — identificador del síntoma.
  - `nombre_sintomaHipotesis` — nombre legible del síntoma.
  - `id_hipotesis` — identificador de la hipótesis diagnóstica.
  - `nombre_hipotesis` — nombre legible de la hipótesis.
  - `asunto_asignacionCaso` — asunto con el que se registra la asignación.
  - `departamento_asignacionCaso` — departamento al que se deriva el caso.
  - `empleado_asignacionCaso` — empleado responsable del caso.
- **Doble función**: combina en una sola llamada la clasificación diagnóstica (síntoma + hipótesis) y la asignación organizativa (departamento + empleado).
- **Uso documentado con autoasignación**: los ejemplos de la nota muestran peticiones idénticas en estructura para `id_caso=1981368445` e `id_caso=1981368444`, ambas con autoasignación del caso.
- **Campos adicionales del objeto `hipotesis`**: `criterios_hipotesis`, `afectados_hipotesis`, `observacion_asignacionCaso`, `nombre_asignacionCaso` ("Jaime Adrian Bonilla Fernandez"), `personaEmpresaRol_asignacionCaso` ("594591"), `fecha_asignacionCaso` ("18-10-2024 1:02") y `origen` ("Nuevo").
- **Codificación del parámetro**: `hipotesis` viaja URL-encoded en la petición (por ejemplo `%7B` para `{` y `%22` para `"`), aunque en la nota también se muestra en formato JSON legible para depuración.
- **Estructura del JSON**: contiene un arreglo con `"total":1` y una lista `hipotesis` con los objetos de síntoma/hipótesis.
- **Respuesta esperada**: el envío de la petición devuelve `{"success":true}`, lo que confirma que la actualización del caso fue exitosa.
## Aplicaciones

- **Registro y clasificación de casos de indisponibilidad de servicio**: el operador crea o actualiza el caso indicando el síntoma observado y la hipótesis de causa raíz.
- **Asignación de casos a empleados y departamentos**: la misma petición deriva el caso al área y al responsable que deben atenderlo.
- **Autoasignación**: un técnico puede tomar el caso directamente asignándoselo a sí mismo, tal como reflejan los ejemplos de la nota.
- **Automatización desde herramientas de monitoreo**: al integrarse con sistemas como [[Zabbix]], una alerta puede originar la llamada a `actualizarHipotesis` para abrir y clasificar el caso sin intervención manual.
- **Reasignación posterior**: cuando la hipótesis o el responsable cambian, el caso puede reasignarse mediante [[reasignarTarea]], complementario a este endpoint.
- **Valores concretos de asignación en los ejemplos**: los datos enviados incluyen `departamento_asignacionCaso`:132, `empleado_asignacionCaso`:"237805", `asunto_asignacionCaso`:"Autoasignacion del Caso" y `origen`:"Nuevo", reforzando con valores concretos el escenario de autoasignación ya descrito.
## Conceptos relacionados

- [[concepts/reasignartarea|reasignarTarea]]

## Entidades relacionadas

- [[entities/telcos|Telcos]]

## Menciones en la fuente

- "POST https://telcos.telconet.ec/soporte/info_caso/actualizarHipotesis" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "id_caso=1981368445&hipotesis={"total":1,"hipotesis":[{"id_sintomaHipotesis":381,"nombre_sintomaHipotesis":"Caída del servicio","id_hipotesis":"Indisponibilidad del servicio"" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "id_caso=1981368445&hipotesis={"total":1,"hipotesis":[{"id_sintomaHipotesis":381,"nombre_sintomaHipotesis":"Ca\u00edda del servicio","id_hipotesis":"Indisponibilidad del servicio"" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "id_caso=1981368445&hipotesis=%7B%22total%22%3A1%2C%22hipotesis%22%3A%5B%7B%22id_sintomaHipotesis%22%3A381" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]