---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/1-2-backbone-proveedores-internacionales_861235]]"
tags:
generation_complete: true
---

# Salidas Internacionales

## Definición

**Salidas Internacionales** es la denominación operativa del conjunto de enlaces del [[Backbone]] que conectan la red de [[Telconet]] con el exterior. Agrupa los circuitos contratados a proveedores internacionales y los puntos de interconexión por los cuales el tráfico de la red sale hacia otras redes autónomas y hacia Internet global.

## Características clave

- **Naturaleza de backbone:** no son enlaces de acceso de cliente, sino tramos troncales de interconexión internacional.
- **Multi-proveedor:** la conectividad se reparte entre varios operadores —[[Cables & Wireless]], PCCW, Sparkle y CNT— lo que aporta redundancia y diversidad de rutas.
- **Monitoreo centralizado:** su estado se consulta mediante la herramienta de monitoreo NetFlow, publicada en `aplicaciones.telconet.ec/netflow/salidasInternacionales`.
- **Punto de partida del diagnóstico:** figura como el primer elemento del inventario de referencia del backbone, por lo que es el primer recurso a revisar ante incidentes de conectividad internacional.
- **Carácter operativo:** es un concepto de uso diario para equipos de red y NOC, más que un concepto arquitectónico teórico.

## Aplicaciones

- **Diagnóstico de incidentes:** verificar el estado y el consumo de las salidas internacionales es el primer paso al investigar degradación de latencia, pérdida de paquetes o cortes hacia destinos fuera de la red.
- **Monitoreo de tráfico:** el análisis NetFlow permite observar el volumen y la distribución del tráfico por enlace y por proveedor.
- **Gestión de capacidad:** el consumo por circuito sirve de insumo para decisiones de ampliación o rebalanceo de ancho de banda entre proveedores.
- **Verificación de redundancia:** permite confirmar que ante la caída de un operador el tráfico conmuta hacia las salidas restantes.

## Conceptos relacionados

## Entidades relacionadas

- [[entities/telconet|Telconet]]
- [[entities/cables-&-wireless|Cables & Wireless]]
- [[entities/backbone|Backbone]]

## Menciones en la fuente

- "Revisar [Link](https://aplicaciones.telconet.ec/netflow/salidasInternacionales)" — [[Work/1.2 Backbone Proveedores Internacionales|1.2 Backbone Proveedores Internacionales]]