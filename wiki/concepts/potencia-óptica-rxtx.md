---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/comandos_d202a8]]"
tags:
aliases:
  - "Rx/Tx Power"
  - "niveles de potencia óptica"
  - "Optical Rx/Tx Power"
generation_complete: true
---

# Potencia óptica Rx/Tx

## Definición

La **potencia óptica Rx/Tx** es el nivel de señal óptica recibida (Rx, *receive*) y transmitida (Tx, *transmit*) en una interfaz óptica, expresado normalmente en **dBm**. Es un indicador directo de la salud física del enlace: mide cuánta luz llega al receptor y cuánta emite el transmisor, permitiendo verificar que ambos extremos operan dentro de los márgenes soportados por los módulos ópticos.

En interfaces de alta capacidad, como un puerto de 100G, la potencia se reporta **por carril (lane)**: cada carril tiene su propio valor de Rx y Tx, además de un rango de advertencia (*warning range*) definido por el propio módulo.

## Características clave

- Se expresa en **dBm** y se evalúa contra un **rango de advertencia** (mínimo y máximo) definido por el módulo óptico.
- En óptica paralela (p. ej. 100G con múltiples carriles) se reporta un valor **RxN Power / TxN Power** por carril, no un único valor agregado.
- El valor de **Rx** refleja la pérdida acumulada del trayecto: atenuación de fibra, empalmes, conectores y margen de diseño del enlace.
- El valor de **Tx** refleja la potencia emitida por el transmisor y debe situarse típicamente en el extremo positivo del rango.
- Un valor medido **fuera del rango de warning** indica degradación del enlace, mientras que un valor **dentro del rango pero cercano al límite** es una señal temprana de deterioro.
- Es un dato de **capa física**: su análisis es independiente de la configuración lógica de la interfaz (VLANs, direccionamiento, agregación).

## Aplicaciones

- **Mantenimiento preventivo**: comparar periódicamente los valores medidos con los rangos de advertencia permite detectar degradación progresiva antes de que el enlace caiga.
- **Diagnóstico de fallos**: valores de Rx muy bajos sugieren empalmes defectuosos, conectores sucios, fibra doblada o excesiva atenuación del tramo.
- **Validación de instalación**: verificar que un módulo recién insertado opera dentro de especificación en todos sus carriles.
- **Supervisión de enlaces críticos**: en el enlace de 100G con PCCW, la lectura de potencia óptica Rx/Tx es esencial para el seguimiento continuo del servicio.
- **Análisis de asimetrías**: diferencias notables entre carriles del mismo puerto apuntan a un problema físico localizado (un hilo de fibra o un conector concreto).

Ejemplo de consulta en un equipo Huawei:

display interface 100GE4/0/14 | inc Rx
Rx Warning range: [-13.001,  3.999]dBm
Rx0 Power:  -4.13dBm, Tx0 Power:   1.64dBm

En este caso, el valor medido de Rx (−4.13 dBm) se encuentra dentro del rango de advertencia [−13.001, 3.999] dBm, por lo que el enlace opera dentro de los márgenes esperados.

## Conceptos relacionados

- [[concepts/display-interface|display interface]]

## Entidades relacionadas

- [[entities/huawei|Huawei]]

## Menciones en la fuente

- "Rx Warning range: [-13.001,  3.999]dBm, Tx Warning range: [-4.000,  3.999]dBm" (Rango de advertencia Rx: [-13.001,  3.999]dBm, Rango de advertencia Tx: [-4.000,  3.999]dBm) — [[Work/Comandos|Comandos]]
- "Rx0 Power:  -4.13dBm, Tx0 Power:   1.64dBm" (Potencia Rx0: -4.13dBm, Potencia Tx0: 1.64dBm) — [[Work/Comandos|Comandos]]
- "Rx2 Power:  -5.06dBm, Tx2 Power:   1.62dBm" (Potencia Rx2: -5.06dBm, Potencia Tx2: 1.62dBm) — [[Work/Comandos|Comandos]]