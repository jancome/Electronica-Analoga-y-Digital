# Tres problemas de circuitos digitales

Estas actividades cierran el tema de compuertas y tablas de verdad. Cada equipo debe traducir una condición física a variables binarias, completar todas las combinaciones, obtener una expresión booleana, dibujar el circuito y comprobarlo en simulación. Las salidas propuestas son **señales de control de baja tensión**; una compuerta TTL no alimenta directamente lámparas, motores ni alarmas de potencia.

## Método común

1. Defina con precisión qué significan `0` y `1` en cada entrada y salida.
2. Enumere las `2ⁿ` combinaciones, con `n` entradas. Para tres entradas son ocho filas.
3. Decida la salida de cada fila usando únicamente la regla del problema.
4. Escriba una expresión y dibuje las compuertas, identificando señales intermedias.
5. Simule las ocho filas. Compare cada salida simulada con la tabla.
6. Indique qué etapa de interfaz se necesitaría para controlar la carga real.

### Problema 1 · Iluminación de un pasillo

La luz debe encenderse **solo cuando está oscuro** y, además, hay presencia o una solicitud manual de encendido. El sistema usa tres entradas digitales:

| Variable | Valor 1 | Valor 0 |
|---|---|---|
| `D` | El sensor detecta oscuridad. | Hay luz suficiente. |
| `P` | Hay presencia. | No hay presencia. |
| `M` | Se solicita encendido manual. | No hay solicitud manual. |

La salida `L=1` significa **orden de encendido**. Complete la tabla sin confundir «o» con XOR: presencia y solicitud manual pueden ocurrir a la vez.

| D | P | M | L esperada | L simulada | ¿Coinciden? |
|---:|---:|---:|:---:|:---:|:---:|
| 0 | 0 | 0 |  |  |  |
| 0 | 0 | 1 |  |  |  |
| 0 | 1 | 0 |  |  |  |
| 0 | 1 | 1 |  |  |  |
| 1 | 0 | 0 |  |  |  |
| 1 | 0 | 1 |  |  |  |
| 1 | 1 | 0 |  |  |  |
| 1 | 1 | 1 |  |  |  |

**Diseño:** escriba la expresión de `L`, dibuje su circuito y compruebe especialmente los casos `D=0, P=1, M=1` y `D=1, P=1, M=1`. Proponga después una implementación equivalente que utilice solo compuertas NAND.

### Problema 2 · Permiso de bombeo de un tanque

Un controlador debe dar la orden de bombeo cuando hay agua en el depósito de origen, el tanque de destino **no** está lleno y el paro de emergencia **no** está activado. El circuito entrega una señal lógica de permiso; el motor requiere una etapa de potencia y protecciones propias.

| Variable | Valor 1 | Valor 0 |
|---|---|---|
| `S` | Hay agua disponible en el origen. | No hay agua disponible. |
| `F` | El tanque de destino está lleno. | El tanque necesita agua. |
| `E` | El paro de emergencia está activado. | El paro no está activado. |

La salida `B=1` significa **permiso lógico para bombear**.

| S | F | E | B esperada | B simulada | ¿Coinciden? |
|---:|---:|---:|:---:|:---:|:---:|
| 0 | 0 | 0 |  |  |  |
| 0 | 0 | 1 |  |  |  |
| 0 | 1 | 0 |  |  |  |
| 0 | 1 | 1 |  |  |  |
| 1 | 0 | 0 |  |  |  |
| 1 | 0 | 1 |  |  |  |
| 1 | 1 | 0 |  |  |  |
| 1 | 1 | 1 |  |  |  |

**Diseño:** escriba la expresión de `B` y proponga un circuito que use una compuerta NOR para reunir las dos condiciones que bloquean la bomba. Explique qué fila demuestra que el paro tiene prioridad. Este ejercicio es didáctico; un paro de emergencia real requiere una arquitectura de seguridad independiente y certificada.

### Problema 3 · Diagnóstico de dos sensores redundantes

Dos sensores `A` y `B` informan el mismo estado físico. Si sus lecturas son distintas, el controlador genera una señal de discrepancia. Una entrada `I` permite inhibir **solo la alarma visible** durante una prueba, sin ocultar el estado de los sensores.

| Variable | Valor 1 | Valor 0 |
|---|---|---|
| `A`, `B` | El sensor correspondiente detecta la condición. | No la detecta. |
| `I` | La alarma visible está inhibida para prueba. | La alarma visible está habilitada. |

Se piden dos salidas: `C=1` cuando **ambos sensores coinciden** y `R=1` cuando hay **discrepancia y la alarma no está inhibida**. Compare qué hacen XOR y XNOR en este caso.

| A | B | I | C esperada | R esperada | C simulada | R simulada |
|---:|---:|---:|:---:|:---:|:---:|:---:|
| 0 | 0 | 0 |  |  |  |  |
| 0 | 0 | 1 |  |  |  |  |
| 0 | 1 | 0 |  |  |  |  |
| 0 | 1 | 1 |  |  |  |  |
| 1 | 0 | 0 |  |  |  |  |
| 1 | 0 | 1 |  |  |  |  |
| 1 | 1 | 0 |  |  |  |  |
| 1 | 1 | 1 |  |  |  |  |

**Diseño:** escriba las expresiones de `C` y `R`. Compruebe las dos filas donde `A≠B` e `I` cambia de `0` a `1`: la coincidencia entre sensores no cambia, pero la alarma visible sí. Si el sistema fuera crítico, una inhibición de prueba no debería desactivar la protección física.

## Entrega de los tres problemas

Por cada problema presente la tabla completa, una expresión, el diagrama de compuertas, una captura de simulación y dos frases que expliquen las filas de prueba indicadas. En el informe distinga siempre entre **salida lógica** y **energía necesaria para la carga**.

## Referencias de clase

- José Caicedo Ortiz, *3. Compuertas lógicas*, PDF suministrado por el docente, pp. 3–12. Las tablas de NAND, NOR, XOR y XNOR y el análisis por señales intermedias sustentan el repaso; los tres casos aplicados de esta hoja fueron diseñados para esta clase.
- José Caicedo, [*Introducción a las compuertas lógicas*](https://www.youtube.com/watch?v=-XmCSXRkrBw&t=1200s), video de apoyo compartido por el docente.
