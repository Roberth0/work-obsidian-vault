---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/comandos_d202a8]]"
tags:
aliases:
  - "display interface 100GE4/0/14"
  - "show interface"
generation_complete: true
---

# display interface

## Definición

**display interface** es un comando de diagnóstico de línea de comandos que muestra los parámetros de estado y operación de una interfaz concreta. Se invoca indicando la interfaz como argumento —por ejemplo `display interface 100GE4/0/14`— y devuelve información sobre el estado del puerto, su descripción configurada, contadores de tráfico y niveles de potencia óptica. Es una de las herramientas de diagnóstico físico más utilizadas para verificar enlaces de alta capacidad.

## Características clave

- **Alcance por interfaz**: se ejecuta sobre una interfaz específica identificada por su nombre (por ejemplo, `100GE4/0/14`), no sobre el dispositivo completo.
- **Salida filtrable**: admite filtros de texto encadenados mediante el carácter `|`, lo que permite aislar únicamente las líneas relevantes de la salida completa.
  - El filtro `i esc` (búsqueda de una cadena) extrae la línea de descripción del puerto, útil para identificar el enlace y su proveedor.
  - El filtro `inc Rx` (inclusión de líneas que contienen un patrón) filtra las líneas de potencia óptica de recepción.
- **Visibilidad de capa física**: expone los niveles de potencia óptica de recepción (Rx) y transmisión (Tx), lo que permite detectar valores fuera de rango que indiquen degradación del enlace de 100G.
- **Verificación de identidad del enlace**: la descripción del puerto actúa como metadato operativo, permitiendo confirmar a qué enlace y a qué proveedor corresponde la interfaz.
- **Bajo impacto**: es un comando de solo lectura, orientado a la consulta de estado, no a la modificación de configuración.

## Aplicaciones

- **Identificación de enlaces y proveedores**: ejecutar `display interface 100GE4/0/14 | i esc` para recuperar la descripción del puerto y determinar a qué enlace y operador corresponde la interfaz.
- **Diagnóstico de degradación óptica**: usar el modificador `| inc Rx` para revisar las potencias de recepción y detectar valores fuera de rango que sugieran atenuación excesiva, conector sucio o fallo de fibra.
- **Verificación de enlaces de 100G**: comprobar los niveles Rx/Tx en interfaces de alta capacidad donde una degradación mínima afecta al rendimiento agregado.
- **Validación post-intervención**: confirmar que, tras un cambio de configuración o un trabajo en el rack, la descripción y las potencias ópticas siguen siendo las esperadas.
- **Triaje antes de escalar**: descartar causas físicas antes de escalar un incidente a diagnóstico de capa 2/3.

## Conceptos relacionados

- [[concepts/potencia-óptica-rxtx|Potencia óptica Rx/Tx]]
- [[concepts/show-spanning-tree-detail|show spanning-tree detail]]

## Entidades relacionadas

- [[entities/huawei|Huawei]]

## Menciones en la fuente

- "display interface 100GE4/0/14 | i esc" (display interface 100GE4/0/14 | i esc) — [[Work/Comandos|Comandos]]
- "display interface 100GE4/0/14 | inc Rx" (display interface 100GE4/0/14 | inc Rx) — [[Work/Comandos|Comandos]]