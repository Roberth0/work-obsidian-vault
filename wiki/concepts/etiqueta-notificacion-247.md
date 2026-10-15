---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/2-vips_147ea4]]"
tags:
aliases:
  - "Notificacion 24/7"
  - "Etiqueta de notificacion"
  - "Etiqueta de notificación 24/7"
generation_complete: true
---

# Etiqueta notificacion 24/7

## Definición

La **Etiqueta notificacion 24/7** es la marca que debe registrarse al momento de contactar a un cliente dentro del monitoreo VIPS, el cual opera de forma continua, todos los días. El procedimiento establece que siempre se debe llamar al cliente utilizando esta etiqueta y, en caso de que este no conteste, al pasar la tarea se debe especificar expresamente que no hubo respuesta. La etiqueta funciona como un control operativo destinado a asegurar la trazabilidad de los intentos de contacto y el cumplimiento de los acuerdos de servicio (SLA).

## Características clave

- **Registro obligatorio:** toda llamada de contacto al cliente dentro del monitoreo VIPS debe quedar marcada con esta etiqueta.
- **Cobertura continua:** responde a un esquema de monitoreo 24/7, sin interrupción de días ni horarios.
- **Trazabilidad del intento:** cuando el cliente no contesta, la tarea debe pasarse indicando de forma explícita que no hubo respuesta.
- **Vinculación con escalamiento:** el flujo contempla una referencia de escalamiento — [[David Morocho]] — para los casos en que el cliente no responde.
- **Priorización de clientes:** dentro de la misma disposición se establece dar prioridad a determinados clientes, entre ellos [[Produbanco]] y [[Banco Bolivariano]].
- **Carácter de control operativo:** permite auditar intentos de contacto y verificar el cumplimiento de los acuerdos de servicio.

## Aplicaciones

- **Monitoreo VIPS:** registro de intentos de contacto con clientes bajo seguimiento continuo.
- **Gestión de tareas y traspasos:** documentación del resultado de la llamada (contactado / sin respuesta) al momento de derivar o cerrar la tarea.
- **Escalamiento:** activación del flujo de escalamiento con [[David Morocho]] cuando el cliente no atiende.
- **Atención preferente:** soporte a la priorización operativa de clientes como [[Produbanco]] y [[Banco Bolivariano]].
- **Auditoría y cumplimiento de SLA:** evidencia de los intentos realizados y de los tiempos de respuesta frente a los acuerdos de servicio.

## Conceptos relacionados

- [[concepts/vips|VIPS]]
- [[concepts/logins-que-no-se-gestionan|Logins que no se gestionan]]
- [[concepts/caso-o-tarea-ya-aperturado-por-algun-tiempo|Caso o tarea ya aperturado por algun tiempo]]

## Entidades relacionadas

- [[entities/produbanco|Produbanco]]
- [[entities/banco-bolivariano|Banco Bolivariano]]

## Menciones en la fuente

- ">[!error] Llamar siempre al cliente con la etiqueta notificacion 24/7 y si no contesta al pasar la tarea especificar que no contesto David Morocho" — [[Work/2. VIPS|2. VIPS]]
- "Ademas se debe dar prioridad a clientes como" — [[Work/2. VIPS|2. VIPS]]