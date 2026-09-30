# Marco teórico – Semana 08

# Compuertas lógicas y primer montaje en protoboard

## 1. Propósito de la semana

Convertir las variables digitales del proyecto en una primera función de decisión e implementarla mediante compuertas lógicas, simulación y montaje en protoboard.

## 2. Resultado de aprendizaje

Al finalizar la semana, el estudiante estará en capacidad de:

- Interpretar las compuertas AND, OR, NOT, NAND, NOR, XOR y XNOR.
- Construir tablas de verdad.
- Relacionar tabla, expresión y circuito.
- Identificar alimentación, niveles lógicos y terminales de un circuito integrado.
- Simular una función lógica.
- Construir y comprobar un primer circuito en protoboard.
- Documentar la relación entre la lógica y la situación problema.

## 3. Conexión con la Fase 2 ABPr

Esta semana inicia la evidencia práctica exigida institucionalmente:

```text
Variables del proyecto
        ↓
Tabla de verdad inicial
        ↓
Compuertas
        ↓
Simulación
        ↓
Primer montaje en protoboard
```

La Fase 2 no puede quedar como un ejercicio documental. Debe llegar a una implementación funcional.

## 4. Variable y nivel lógico

Una variable booleana toma valores 0 o 1. En el circuito real estos valores corresponden a rangos de voltaje, no a números abstractos.

Antes del montaje deben revisarse:

- Voltaje de alimentación.
- Umbrales de entrada.
- Capacidad de corriente de salida.
- Compatibilidad entre familias TTL y CMOS.
- Entradas y salidas activas en alto o en bajo.

## 5. Compuertas principales

| Compuerta | Expresión | Condición de salida 1 |
|---|---|---|
| AND | `A·B` | Todas las entradas son 1. |
| OR | `A+B` | Al menos una entrada es 1. |
| NOT | `A̅` | Invierte la entrada. |
| NAND | `(A·B)̅` | Negación de AND. |
| NOR | `(A+B)̅` | Negación de OR. |
| XOR | `A⊕B` | Las entradas son diferentes. |
| XNOR | `(A⊕B)̅` | Las entradas son iguales. |

## 6. Tabla de verdad

La tabla de verdad contiene todas las combinaciones posibles. Para `n` variables existen:

```text
2ⁿ combinaciones
```

Para dos variables A y B, esta tabla permite cerrar las seis funciones de dos entradas. NOT actúa sobre una sola variable: `¬0=1` y `¬1=0`.

| A | B | AND `A·B` | OR `A+B` | NAND `¬(A·B)` | NOR `¬(A+B)` | XOR `A⊕B` | XNOR `¬(A⊕B)` |
|---:|---:|---:|---:|---:|---:|---:|---:|
| 0 | 0 | 0 | 0 | 1 | 1 | 0 | 1 |
| 0 | 1 | 0 | 1 | 1 | 0 | 1 | 0 |
| 1 | 0 | 0 | 1 | 1 | 0 | 1 | 0 |
| 1 | 1 | 1 | 1 | 0 | 0 | 0 | 1 |

OR se activa si **al menos una** entrada vale 1, incluso cuando ambas valen 1. XOR se activa si las entradas **son distintas**. NAND y NOR invierten las salidas completas de AND y OR; la barra de negación abarca toda la operación.

### 6.1 De un circuito de varias etapas a su tabla

La presentación de José Caicedo suministrada para la clase muestra un circuito de tres entradas con señales intermedias. Reescrito con una notación uniforme:

```text
U = ¬A
V = U·B
W = B·C
X = V+W
```

Se calcula cada columna de izquierda a derecha. Por ejemplo, para `A=0, B=1, C=0`: `U=1`, `V=1`, `W=0` y `X=1`.

| A | B | C | U=¬A | V=U·B | W=B·C | X=V+W |
|---:|---:|---:|---:|---:|---:|---:|
| 0 | 0 | 0 | 1 | 0 | 0 | 0 |
| 0 | 0 | 1 | 1 | 0 | 0 | 0 |
| 0 | 1 | 0 | 1 | 1 | 0 | 1 |
| 0 | 1 | 1 | 1 | 1 | 1 | 1 |
| 1 | 0 | 0 | 0 | 0 | 0 | 0 |
| 1 | 0 | 1 | 0 | 0 | 0 | 0 |
| 1 | 1 | 0 | 0 | 0 | 0 | 0 |
| 1 | 1 | 1 | 0 | 0 | 1 | 1 |

Con tres entradas hay ocho filas. En un circuito de cuatro entradas habrá 16; no se deben omitir combinaciones cuando se solicita una tabla completa. Identifique primero cada salida intermedia y **después** calcule la salida final. Esta secuencia evita adivinar el resultado por la forma del dibujo.

## 7. Compuertas universales

NAND y NOR se consideran universales porque permiten construir cualquier función lógica.

Esta propiedad puede reducir la variedad de integrados necesarios, pero la implementación debe compararse en número de puertas, conexiones y niveles de negación.

## 8. Circuitos integrados y hoja de datos

Antes de montar se debe consultar:

- Referencia del integrado.
- Pin VCC y GND.
- Distribución de compuertas.
- Voltaje permitido.
- Corrientes de entrada y salida.
- Tabla de funcionamiento.
- Condiciones de entradas no utilizadas.

Ejemplos comunes: 7400, 7402, 7404, 7408, 7432 o equivalentes CMOS.

## 9. Entradas flotantes

Una entrada no conectada puede captar ruido y cambiar de estado. Todas las entradas deben quedar definidas mediante:

- Interruptor correctamente cableado.
- Resistencia pull-up.
- Resistencia pull-down.
- Conexión fija a un nivel permitido.

## 10. Salidas y cargas

Una compuerta puede encender un LED con resistencia, pero no debe alimentar directamente cargas de corriente elevada.

Cuando la salida deba controlar relé, motor o carga mayor, se utilizará la etapa BJT o MOSFET diseñada en el Corte 1.

## 11. Ejemplo aplicado

Una lámpara debe encender cuando el lugar está oscuro (`L=1`) y existe presencia (`P=1`):

```text
Y = L·P
```

La tabla de verdad es:

| L | P | Y |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

El circuito inicial utiliza una compuerta AND. Después de este ejemplo se desarrollan [tres problemas aplicados](problemas-aplicados.md) de iluminación, permiso de bombeo y diagnóstico de sensores. Cada uno requiere tabla completa, expresión, circuito y verificación por casos.

## 12. Procedimiento de simulación y montaje

1. Construir la tabla de verdad.
2. Dibujar el circuito.
3. Simular todas las combinaciones.
4. Consultar el pinout.
5. Montar VCC y GND.
6. Definir entradas con interruptores y resistencias.
7. Colocar LED de salida con resistencia.
8. Probar cada combinación.
9. Comparar tabla teórica, simulación y montaje.
10. Registrar fallas y correcciones.

## 13. Evidencia ABPr

- Tabla de verdad inicial.
- Expresión booleana.
- Simulación funcional.
- Fotografía del protoboard.
- Tabla de comprobación de entradas y salida.
- Hoja de datos utilizada.
- Explicación del aporte al proyecto.

## 14. Errores comunes

- Dejar entradas flotantes.
- Confundir OR con XOR.
- Conectar mal VCC o GND.
- Omitir resistencia del LED.
- Usar una salida lógica para una carga no permitida.
- No verificar si una señal es activa en bajo.
- Tomar una fotografía sin demostrar todas las combinaciones.

## 15. Preguntas orientadoras

1. ¿Qué condición física representa cada entrada?
2. ¿Cómo se comprueba que la salida coincide con la tabla?
3. ¿Qué ocurre si una entrada queda flotante?
4. ¿Por qué NAND y NOR son universales?
5. ¿Qué etapa se necesita para controlar una carga mayor?

## 16. Cierre y laboratorio 01

1. Termine la tabla maestra de NAND, NOR, XOR y XNOR y explique por qué OR y XOR difieren en `A=B=1`.
2. Analice el circuito por etapas y complete los [tres problemas aplicados](problemas-aplicados.md).
3. Realice la [guía del laboratorio 01 de compuertas lógicas](../../guias-laboratorio/digital/lab-01-compuertas-logicas/guia-lab-01-compuertas-logicas.md): identificación de CI, mediciones, tablas y simulación.
4. Compare las salidas lógicas esperadas con las medidas. No trate `0` y `1` como tensiones exactas de `0 V` y `5 V`.
5. Documente el montaje y deje preparada la expresión del proyecto para la simplificación posterior.

## 17. Conexión con la Semana 09

Una vez comprobadas las compuertas y el laboratorio 01, se simplificará la función mediante álgebra de Boole, De Morgan y mapas de Karnaugh. Después se actualizarán la simulación y el montaje en protoboard. Si el grupo aún está terminando NAND, NOR, XOR y XNOR, cierre primero estos contenidos antes de iniciar la simplificación.

## Referencias para este cierre

- José Caicedo Ortiz, *3. Compuertas lógicas*, PDF suministrado por el docente, pp. 3–12. Se contrastaron sus tablas y el ejemplo de circuito por señales intermedias.
- José Caicedo, [*Introducción a las compuertas lógicas*](https://www.youtube.com/watch?v=-XmCSXRkrBw&t=1200s), video de apoyo compartido por el docente.
