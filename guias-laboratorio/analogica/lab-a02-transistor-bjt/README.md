# Lab A02 – Transistor BJT como interruptor

## Guía

- [Experiencia A02 – Transistor BJT: corte, saturación y control de carga](guia-lab-a02-transistor-bjt.md)

## Imagen de apoyo

Esta imagen ayuda a comparar el BJT como dispositivo controlado por corriente frente al MOSFET como dispositivo controlado por voltaje.

![Comparación BJT vs MOSFET como interruptor](../../../recursos/imagenes/analogica/bjt-vs-mosfet-interruptor.svg)

## Propósito

Comprobar experimentalmente el BJT NPN como interruptor electrónico, reconociendo corte y saturación mediante cálculos y mediciones sencillas.

La práctica fue reducida para que pueda completarse dentro de una sesión de laboratorio sin convertirla en una práctica extensa de amplificación.

## Estructura de la práctica

### Experiencia 1 – Física

**BJT como interruptor para LED**

- identificación de terminales;
- estado de corte;
- estado de saturación;
- medición de `VBE`, `VCE` y voltaje sobre la resistencia de carga;
- cálculo de `IB`, `IC` e `IE`.

### Experiencia 2 – Física

**Efecto de la resistencia de base**

Se comparan únicamente tres valores:

- `100 kΩ`;
- `10 kΩ`;
- `2,2 kΩ`.

El objetivo es observar cómo cambia la excitación de base y reconocer la transición hacia saturación.

### Experiencia 3 – Simulada

**Control de carga inductiva con diodo de protección**

- motor DC pequeño o relé;
- BJT NPN como interruptor de lado bajo;
- diodo de rueda libre;
- comparación con y sin diodo únicamente mediante simulación.

Puede utilizarse Multisim, Proteus, Tinkercad Circuits, Falstad u otro simulador equivalente.

## Temas asociados

- BJT NPN.
- Base, colector y emisor.
- Corrientes `IB`, `IC` e `IE`.
- Corte, región activa y saturación.
- BJT como interruptor.
- Resistencia de base.
- Diodo de protección en cargas inductivas.
- Comparación posterior con MOSFET.

## Entrega

Informe corto con:

1. cálculos y tabla de la Experiencia 1;
2. tabla comparativa de la Experiencia 2;
3. dos capturas de la simulación de la Experiencia 3;
4. respuestas de análisis;
5. máximo tres conclusiones técnicas.

## Referencia principal

Boylestad, R. L. y Nashelsky, L., *Electrónica: teoría de circuitos y dispositivos electrónicos*, 10.ª edición, capítulos 3 y 4; especialmente las redes de conmutación con transistores y técnicas de solución de fallas.
