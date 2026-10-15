---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/4-1-telcograph_4a563a]]"
tags:
aliases:
  - "MACROS de configuración"
generation_complete: true
---

# MACROS

## Definición

MACROS son plantillas o variables de configuración que deben actualizarse durante el ingreso de un AP. Constituyen un mecanismo de parametrización dentro del sistema de gestión de puntos de acceso: su valor determina cómo queda configurado el AP una vez completado el proceso de alta, y deben ajustarse según la marca de la controladora que gobierna la red.

## Características clave

- Son plantillas o variables configurables, no valores fijos ni parámetros de hardware.
- Se actualizan como parte obligatoria del flujo de ingreso de un AP.
- Su contenido depende del tipo de controladora: la regla condicional documentada indica que, si la controladora es RUCKUS, se debe anteponer `6.` al actualizar las MACROS.
- Su correcta aplicación condiciona que el AP quede configurado adecuadamente.
- Funcionan como punto de parametrización dependiente de la marca del controlador, por lo que una actualización omitida o incorrecta produce una configuración inválida.

## Aplicaciones

- **Alta de puntos de acceso**: durante el ingreso de un AP, se actualizan las MACROS antes de finalizar la configuración.
- **Entornos con controladora RUCKUS**: se aplica la regla específica de anteponer `6.` en la actualización de las MACROS.
- **Estandarización de despliegues**: permiten parametrizar de forma homogénea múltiples AP dentro de una misma red gestionada.
- **Diagnóstico de errores de configuración**: verificar que las MACROS se hayan actualizado según la marca de la controladora sirve para descartar fallos en el alta de un AP.

## Conceptos relacionados

- [[concepts/ingresos-de-aps|Ingresos de APs]]

## Entidades relacionadas

- [[entities/ruckus|RUCKUS]]
- [[entities/access-point|AP]]

## Menciones en la fuente

- "Actualizar MACROS, si la controladora es **RUCKUS** agregar *6.* adelante" — [[Work/4.1 Telcograph|4.1 Telcograph]]