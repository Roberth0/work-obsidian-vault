---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/comandos_d202a8]]"
tags:
aliases:
  - "spanning-tree detail"
  - "display stp detail"
  - "show spanning-tree detail"
generation_complete: true
---

# show spanning-tree detail

## Definición

`show spanning-tree detail` es un comando de diagnóstico de red que despliega información detallada del estado del árbol de expansión (Spanning Tree Protocol, STP) en un dispositivo de conmutación. A diferencia de las variantes resumidas, presenta los datos desglosados por instancia o por VLAN, incluyendo el rol y el estado de cada puerto, así como los temporizadores asociados a la convergencia.

Su valor principal en el diagnóstico operativo es que expone el tiempo transcurrido desde el último cambio de topología, lo que permite evaluar la estabilidad de la red de capa 2 y detectar fluctuaciones recurrentes que no son visibles en una vista resumida.

## Características clave

- Muestra información detallada y desglosada del estado de STP, organizada por instancia o por VLAN.
- Reporta el rol de cada puerto (raíz, designado, alternativo, bloqueado) y su estado operativo.
- Expone los temporizadores de STP y los valores relacionados con la convergencia de la topología.
- Indica hace cuánto tiempo se produjo un cambio de topología, dato clave para medir la estabilidad de la red.
- Es una herramienta de solo lectura, orientada a la verificación y la resolución de problemas, no a la configuración.
- En equipos Huawei, su función equivalente se obtiene mediante variantes como `display stp`, que se consultan en el mismo flujo de diagnóstico.

## Aplicaciones

- **Diagnóstico de inestabilidad de capa 2:** verificar si la topología cambió recientemente y con qué frecuencia, para distinguir un problema puntual de un comportamiento recurrente.
- **Verificación de convergencia:** comprobar que el árbol de expansión ha convergido tras un cambio de enlaces o de dispositivos.
- **Auditoría de roles y estados de puerto:** confirmar qué puerto actúa como raíz y cuáles permanecen bloqueados, evitando bucles de conmutación.
- **Soporte a la resolución de incidentes:** complementar la información de contadores y errores obtenida con [[display interface]] para correlacionar problemas físicos con cambios de topología.
- **Documentación de línea base:** registrar el estado del árbol de expansión en condiciones normales para comparar frente a futuras incidencias.

## Conceptos relacionados

- [[concepts/stp|STP]]
- [[concepts/display-interface|display interface]]

## Entidades relacionadas

- [[entities/huawei|Huawei]]

## Menciones en la fuente

- "show spanning-tree detail" (show spanning-tree detail) — [[Work/Comandos|Comandos]]
- "Ver hace cuanto tiempo se produjo un cambio de topologia" (Ver hace cuánto tiempo se produjo un cambio de topología) — [[Work/Comandos|Comandos]]