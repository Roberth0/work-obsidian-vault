---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/4-cedia_d7cef1]]"
tags:
aliases:
  - "route add"
  - "route delete"
  - "comandos de ruteo"
  - "agregar y eliminar rutas"
generation_complete: true
---

# Route ADD / Route DELETE

## Definición

**Route ADD** y **Route DELETE** son subcomandos de la utilidad de línea de comandos `route` de Windows que permiten manipular la tabla de enrutamiento local del sistema operativo. `route ADD` inserta una ruta estática nueva hacia una red o host destino, mientras que `route DELETE` elimina una entrada existente de dicha tabla. En el contexto operativo de Telconet, se emplean para habilitar o retirar el acceso de la estación de trabajo del operador hacia hosts y servicios internos de la red corporativa.

## Características clave

- **Rutas estáticas manuales**: la entrada se define explícitamente y persiste hasta que se elimina o hasta que el sistema se reinicia (salvo que se use la opción persistente).
- **Alcance por host o por red**: permiten enrutar hacia una dirección IP específica (host interno) o hacia un rango de red completo.
- **Requieren privilegios elevados**: la modificación de la tabla de enrutamiento exige ejecutar la consola con permisos de administrador.
- **Efecto inmediato**: los cambios se aplican a la tabla de enrutamiento en el momento de la ejecución del comando, sin reinicio.
- **Operación bidireccional**: `ADD` incorpora rutas necesarias para alcanzar recursos internos; `DELETE` depura rutas obsoletas o incorrectas que pueden desviar el tráfico.
- **Dependencia del gateway correcto**: la ruta debe apuntar a la puerta de enlace adecuada; de lo contrario, el tráfico hacia el destino no se resolverá.

## Aplicaciones

- **Acceso a sistemas internos**: agregar rutas hacia hosts como [[telcodrive]], [[sisred]] o las direcciones de gestión de equipos de red, de modo que el operador del NOC pueda alcanzarlos desde su estación de trabajo.
- **Depuración de rutas obsoletas**: eliminar rutas antiguas —por ejemplo, una ruta hacia `telcos` que ya no es válida— para evitar que el tráfico se dirija a un destino incorrecto o inexistente.
- **Diagnóstico de conectividad**: cuando se detecta una [[link loss|pérdida de enlace (link loss)]] o inalcanzabilidad hacia un recurso, verificar y corregir la tabla de enrutamiento es uno de los primeros pasos de troubleshooting.
- **Preparación del puesto de trabajo del NOC**: estandarizar el conjunto de rutas estáticas requeridas para operar las herramientas de monitoreo y administración.

## Conceptos relacionados

- [[concepts/link-loss|link loss]]

## Entidades relacionadas

- [[entities/telcodrive|telcodrive]]

## Menciones en la fuente

- "Route DELETE -p 172.24.15.70 MASK 255.255.255.255  192.168.150.1" (Route DELETE -p 172.24.15.70 MASK 255.255.255.255  192.168.150.1) — [[Work/4 Cedia|4 Cedia]]
- "Route ADD -p 172.24.5.141 MASK 255.255.255.255  192.168.150.1" (Route ADD -p 172.24.5.141 MASK 255.255.255.255  192.168.150.1) — [[Work/4 Cedia|4 Cedia]]