# Marco teórico – Semana 08

# Compuertas lógicas

## 1. Tema de la semana

Compuertas lógicas básicas y su relación con tablas de verdad y expresiones booleanas.

## 2. Objetivo de aprendizaje

Interpretar el funcionamiento de las compuertas AND, OR, NOT, NAND, NOR, XOR y XNOR, relacionando sus entradas y salidas con tablas de verdad y circuitos digitales.

## 3. Contexto

Las compuertas lógicas son los bloques básicos de los sistemas digitales. A partir de ellas se construyen circuitos de control, calculadoras, procesadores, sistemas de seguridad, automatismos y equipos de comunicación.

## 4. Conceptos fundamentales

- Variable lógica: puede tomar valores 0 o 1.
- Nivel bajo: generalmente asociado a 0 lógico.
- Nivel alto: generalmente asociado a 1 lógico.
- Tabla de verdad: muestra todas las combinaciones posibles de entrada y su salida.
- Compuerta lógica: circuito que realiza una operación booleana.

## 5. Compuertas principales

| Compuerta | Operación | Descripción |
|---|---|---|
| AND | A·B | La salida es 1 solo si todas las entradas son 1. |
| OR | A+B | La salida es 1 si al menos una entrada es 1. |
| NOT | A̅ | Invierte el valor lógico de la entrada. |
| NAND | (A·B)̅ | Es la negación de AND. |
| NOR | (A+B)̅ | Es la negación de OR. |
| XOR | A⊕B | La salida es 1 cuando las entradas son diferentes. |
| XNOR | (A⊕B)̅ | La salida es 1 cuando las entradas son iguales. |

## 6. Ejemplo guiado

Para una compuerta AND de dos entradas:

| A | B | Salida A·B |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

## 7. Errores comunes

- Dejar entradas de circuitos integrados sin conectar.
- Confundir la operación OR con XOR.
- No alimentar correctamente el circuito integrado.
- No consultar el pinout del integrado antes de montar.
- Medir la salida sin referencia común de tierra.

## 8. Preguntas orientadoras

1. ¿Por qué las compuertas lógicas trabajan con niveles 0 y 1?
2. ¿Qué diferencia existe entre OR y XOR?
3. ¿Por qué NAND y NOR se consideran compuertas universales?
4. ¿Cómo se comprueba una compuerta mediante una tabla de verdad?
5. ¿Qué pasa si una entrada queda flotante?

## 9. Trabajo independiente

Revisar el resumen del Lab 01, construir tablas de verdad y simular al menos tres compuertas lógicas básicas.
