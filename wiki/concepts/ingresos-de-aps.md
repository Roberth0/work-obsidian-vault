---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/4-1-telcograph_4a563a]]"
tags:
aliases:
  - "Ingreso de APs"
  - "Ingreso de APs (hasta 5)"
  - "AP Onboarding"
generation_complete: true
---

# Ingresos de APs

## Definición

El **Ingreso de APs** es el procedimiento operativo mediante el cual se registran puntos de acceso (hasta 5 por ejecución) en la infraestructura del cliente. El flujo parte de una IP de ingreso específica (**172.24.27.27**) y exige, por cada AP, un conjunto de datos mínimos: AP, Login Auxiliar, Nombre en la controladora, MAC e IP Controladora. El proceso se apoya en la modificación del hostname, la actualización de las [[MACROS]] y la revisión del grupo de asignación, por lo que constituye un flujo de trabajo estructurado con pasos verificables uno a uno.

## Características clave

- **Capacidad limitada por lote:** permite el ingreso de un máximo de 5 APs por procedimiento.
- **Punto de entrada fijo:** requiere acceder desde la IP de ingreso 172.24.27.27.
- **Conjunto de datos obligatorio por AP:** AP, Login Auxiliar, Nombre en la controladora, MAC e IP Controladora.
- **Normalización del hostname:** el hostname debe reescribirse al formato `login/mac`.
- **Actualización de [[MACROS]]:** se antepone el prefijo `6.` cuando la controladora es [[RUCKUS]].
- **Verificación de grupo:** se debe confirmar el grupo al cual queda asignado cada AP.
- **Ajuste de la sección inventory:** se registran *Host Router: Login Auxiliar* y *Name: Login*.
- **Naturaleza secuencial y auditable:** cada paso es comprobable antes de continuar con el siguiente.

## Aplicaciones

- **Alta de nuevos puntos de acceso:** incorporación de equipos AP a la red gestionada de un cliente.
- **Migración o reemplazo de hardware:** sustitución de APs existentes manteniendo la coherencia de nombres, MAC e IP de controladora.
- **Estandarización de inventario:** uso combinado con [[Union de Razones Sociales]] para mantener nombres y grupos consistentes en la documentación del cliente.
- **Operación sobre controladoras [[RUCKUS]]:** escenario en el que aplica la regla de prefijo `6.` en las [[MACROS]].
- **Trazabilidad mediante [[Telcograph]]:** registro de los datos de AP, MAC e IP Controladora para su seguimiento posterior.

## Conceptos relacionados

- [[concepts/union-de-razones-sociales|Union de Razones Sociales]]
- [[concepts/macros|MACROS]]

## Entidades relacionadas

- [[entities/access-point|AP]]
- [[entities/ruckus|RUCKUS]]
- [[entities/telcograph|Telcograph]]

## Menciones en la fuente

- "### Ingresos de APs (Hasta 5) 

Datos requeridos

IP de Ingreso : *172.24.27.27*" — [[Work/4.1 Telcograph|4.1 Telcograph]]
- "Cambiar hostname a: login/mac" — [[Work/4.1 Telcograph|4.1 Telcograph]]
- "Verificar el grupo al cual se asigna" — [[Work/4.1 Telcograph|4.1 Telcograph]]