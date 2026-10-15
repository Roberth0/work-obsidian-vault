---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/comandos_d202a8]]"
tags:
aliases:
  - "Warning range"
  - "umbral óptico"
  - "Optical warning range"
generation_complete: true
---

# Rango de advertencia óptico

## Definición

El **rango de advertencia óptico** (en inglés, *warning range*) es el intervalo de valores de potencia óptica, expresado en dBm, dentro del cual un transceptor debe operar para que el enlace de fibra sea considerado saludable. Se define de forma independiente para recepción (Rx) y transmisión (Tx), y establece los umbrales inferior y superior que separan el funcionamiento normal de una condición de alarma.

En la documentación de referencia aparece para la interfaz `100GE4/0/14` como:

Rx Warning range: [-13.001,  3.999]dBm, Tx Warning range: [-4.000,  3.999]dBm

Cuando la potencia medida cae por debajo del límite inferior o supera el límite superior, el dispositivo emite una alarma que puede indicar degradación del enlace.

## Características clave

- Se expresa como un intervalo cerrado `[mínimo, máximo]` en dBm, diferenciado por dirección: un rango para Rx y otro para Tx.
- Los umbrales son específicos de cada interfaz y de cada tipo de transceptor (por ejemplo, ópticas de 100G); no son valores universales.
- El rango de advertencia es un nivel de aviso previo: antecede a condiciones más severas de alarma y permite detectar degradación antes de la pérdida total del enlace.
- Funciona como valor de referencia para comparar la medición real. En el ejemplo del documento, las lecturas `Rx0 Power:  -4.13dBm` y `Tx0 Power:   1.64dBm` se contrastan contra los umbrales declarados.
- El límite inferior del rango de advertencia para Tx suele ser más alto que el de Rx (`-4.000` dBm frente a `-13.001` dBm), reflejando la asimetría típica entre presupuesto de transmisión y sensibilidad de recepción.
- Su valor es diagnóstico: salir del rango no implica necesariamente fallo inmediato, pero sí una condición que requiere revisión.

## Aplicaciones

- **Monitoreo de enlaces de fibra a 100G**: verificación periódica de que la potencia Rx/Tx permanece dentro de los umbrales declarados por la interfaz.
- **Diagnóstico de degradación**: ante una alarma de potencia, comparar la lectura real con el rango de advertencia para estimar la magnitud y la dirección del problema (empalme deteriorado, conector sucio, fibra doblada, atenuación excesiva).
- **Validación posterior a intervenciones**: tras instalar o reemplazar un módulo óptico o empalmar fibra, confirmar que la potencia medida vuelve a situarse dentro del rango.
- **Automatización de alertas**: uso de los umbrales como disparadores en sistemas de gestión de red para notificar antes de que se cruce el umbral de alarma crítica.
- **Inventario y planificación**: conocer los rangos de advertencia por interfaz ayuda a calcular presupuestos ópticos y a seleccionar módulos compatibles.

## Conceptos relacionados

- [[concepts/display-interface|display interface]]
- [[concepts/potencia-óptica-rxtx|Potencia óptica Rx/Tx]]

## Entidades relacionadas

- [[entities/huawei|Huawei]]

## Menciones en la fuente

- "Rx Warning range: [-13.001,  3.999]dBm, Tx Warning range: [-4.000,  3.999]dBm" (Rango de advertencia de recepción: [-13.001, 3.999]dBm, Rango de advertencia de transmisión: [-4.000, 3.999]dBm) — [[Work/Comandos|Comandos]]
- "Rx0 Power:  -4.13dBm, Tx0 Power:   1.64dBm" (Potencia Rx0: -4.13dBm, Potencia Tx0: 1.64dBm) — [[Work/Comandos|Comandos]]