# Marco teórico - Semana 15

# 3.5 Teclado matricial y display 7 segmentos

## 1. Del contacto al dígito

La aplicación se organiza en cuatro bloques: teclado matricial, identificación de fila y columna, conversión a un código de dígito y decodificación para el display. Detectar una tecla, codificarla y encender segmentos son funciones distintas.

## 2. Teclado matricial

Cada tecla une una fila con una columna. En una matriz 4 por 3 existen doce posiciones y siete líneas de fila/columna. El siguiente mapa es un ejemplo de trabajo, no el pinout de un teclado comercial:

| Fila / columna | C0 | C1 | C2 |
|---|---|---|---|
| R0 | 1 | 2 | 3 |
| R1 | 4 | 5 | 6 |
| R2 | 7 | 8 | 9 |
| R3 | * | 0 | # |

El barrido selecciona una fila a la vez y observa las columnas. El circuito real debe definir niveles de reposo, polaridad de activación y tratamiento de las filas no seleccionadas según su implementación. No se debe suponer la distribución de pines a partir de este mapa.

## 3. Ejemplo resuelto: tecla 5

1. El barrido llega a R1.
2. Detecta la tecla en C1.
3. La tabla identifica la posición R1/C1 como el dígito 5.
4. El bloque de codificación entrega BCD `0101`.
5. El decodificador enciende los segmentos `a, f, g, c, d`.

## 4. Display de 7 segmentos

Los segmentos se nombran `a` arriba, `b` arriba a la derecha, `c` abajo a la derecha, `d` abajo, `e` abajo a la izquierda, `f` arriba a la izquierda y `g` en el centro.

El tipo de display, ánodo común o cátodo común, determina la polaridad requerida. Se selecciona un controlador compatible y se limita la corriente de cada segmento. La tabla siguiente indica segmentos encendidos, independientemente del nivel eléctrico usado para encenderlos:

| Dígito | BCD | Segmentos encendidos |
|---|---|---|
| 0 | 0000 | a, b, c, d, e, f |
| 1 | 0001 | b, c |
| 2 | 0010 | a, b, d, e, g |
| 3 | 0011 | a, b, c, d, g |
| 4 | 0100 | b, c, f, g |
| 5 | 0101 | a, c, d, f, g |
| 6 | 0110 | a, c, d, e, f, g |
| 7 | 0111 | a, b, c |
| 8 | 1000 | a, b, c, d, e, f, g |
| 9 | 1001 | a, b, c, d, f, g |

## 5. Rebote, ausencia de tecla y pulsaciones simultáneas

El contacto mecánico puede producir transiciones repetidas. La práctica debe registrar una sola pulsación después de estabilizar la entrada. Debe definirse qué sucede cuando no hay tecla: apagar el display o conservar el último dígito, lo que requiere memoria. Para la primera práctica se admite una tecla a la vez; las pulsaciones simultáneas se registran como una limitación y no como códigos válidos garantizados.

## 6. Práctica de integración

1. Identificar filas y columnas del teclado real o simulado.
2. Construir la tabla de las doce posiciones.
3. Definir qué harán `*` y `#`, sin tratarlas como dígitos BCD.
4. Probar por separado identificación de tecla, código BCD y display.
5. Integrar los bloques y verificar los diez dígitos.
6. Repetir una pulsación y probar ausencia de tecla y pulsación prolongada.
7. Entregar esquema, tabla de pruebas y explicación individual.

**Ejercicio:** resolver el recorrido de las teclas 2, 7 y 0, indicando fila, columna, BCD y segmentos encendidos. Explicar qué bloque adicional hace falta para conservar el último dígito.

Esta práctica utiliza los Labs 07 y 08 como apoyo. No cambia su numeración ni crea una ponderación adicional.

## 7. Muestra formativa del proyecto

Presentar el problema, diagrama de bloques, prototipo funcional o parcialmente funcional, maqueta o base, simulación y mediciones. Registrar fallas abiertas y un plan de correcciones. La muestra no reemplaza la sustentación final.

## 8. Continuidad

Los temas 3.6 y 3.7 desarrollan la memoria mediante flip-flops y las aplicaciones con contadores.
