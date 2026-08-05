# Banco de ejercicios adaptados de Floyd – Cortes 2 y 3

## Propósito

Este banco utiliza la secuencia conceptual de **Fundamentos de sistemas digitales**, de Thomas L. Floyd, pero presenta valores, variables y aplicaciones diferentes. Los ejercicios se relacionan con energía, agua, iluminación, control de cargas y recursos.

No contiene reproducciones literales de los problemas ni las soluciones del libro.

## Forma de entrega sugerida

Para cada ejercicio, el estudiante debe incluir:

1. procedimiento;
2. resultado;
3. comprobación;
4. interpretación en lenguaje de ingeniería;
5. relación con el proyecto ABPr cuando aplique.

---

# Corte 2

## Semana 06 – Sistemas numéricos

### Ejercicio 6.1 – Representación de una medición

Un medidor registra el valor decimal `173`.

1. Convertirlo a binario de 8 bits.
2. Convertirlo a hexadecimal.
3. Representar el número decimal 173 en BCD.
4. Explicar por qué la representación BCD ocupa más bits que el binario puro.
5. Indicar cuál representación sería más práctica para almacenamiento y cuál para visualización decimal.

### Ejercicio 6.2 – Código de estados

Un sistema de nivel de agua tiene cinco estados:

- vacío;
- bajo;
- medio;
- alto;
- desbordamiento.

1. Determinar la cantidad mínima de bits necesaria.
2. Asignar un código binario a cada estado.
3. Identificar los códigos no utilizados.
4. Proponer qué debería hacer el sistema si recibe un código no válido.

### Ejercicio 6.3 – Variables del proyecto

Definir entre dos y cuatro variables digitales del proyecto. Para cada variable indicar:

- nombre;
- significado físico;
- condición de 0;
- condición de 1;
- activa en alto o activa en bajo;
- origen de la señal: interruptor, sensor, comparador u otro bloque.

---

## Semana 07 – Aritmética binaria

### Ejercicio 7.1 – Suma de eventos

Realizar las siguientes sumas de 8 bits:

```text
00110110 + 00011101
01011011 + 00100111
11100010 + 00110101
```

Para cada caso indicar:

- suma;
- acarreo de salida;
- interpretación sin signo;
- posible overflow si se interpreta con signo.

### Ejercicio 7.2 – Resta mediante complemento a 2

Resolver mediante complemento a 2:

```text
01001101 - 00011011
00110100 - 01000001
```

Mostrar:

1. complemento a 1 del sustraendo;
2. complemento a 2;
3. suma;
4. interpretación del resultado.

### Ejercicio 7.3 – Conteo de consumo

Un contador de energía registra 42 pulsos durante un intervalo y 27 durante el siguiente.

1. Representar ambos valores en binario de 8 bits.
2. Sumarlos.
3. Determinar si se necesita más de 8 bits.
4. Restar el menor del mayor usando complemento a 2.
5. Explicar qué representa la diferencia.

---

## Semana 08 – Compuertas lógicas

### Ejercicio 8.1 – Sistema fotosensible

Definir:

- `A=1`: oscuridad detectada.
- `B=1`: sistema habilitado.
- `Y=1`: LED encendido.

1. Construir la tabla de verdad.
2. Escribir la expresión de salida.
3. Dibujar el circuito con una AND.
4. Montar con SN74LS08.
5. Medir las tensiones de entrada y salida para cada combinación.
6. Explicar qué ocurre si el switch queda desconectado.

### Ejercicio 8.2 – Alarma con condición adicional

Una alarma debe activarse cuando el lugar está oscuro y ocupado, o cuando existe una falla crítica.

```text
L = oscuridad
P = presencia
F = falla crítica
A = alarma
```

1. Formular la expresión.
2. Construir la tabla de verdad.
3. Implementar con AND y OR.
4. Identificar qué condición tiene prioridad práctica.

### Ejercicio 8.3 – Diagnóstico del protoboard

Un LED de salida permanece apagado aunque la tabla indica que debería encender.

Aplicar el siguiente orden de diagnóstico:

1. VCC del integrado.
2. GND del integrado.
3. tensión en cada entrada.
4. tensión en la salida.
5. polaridad del LED.
6. valor de la resistencia.
7. continuidad de cables.
8. prueba de otra compuerta del mismo integrado.

Registrar la falla encontrada y la evidencia que permitió aislarla.

---

## Semana 09 – Boole, De Morgan y Karnaugh

### Ejercicio 9.1 – Tabla a expresiones estándar

Para la función:

```text
F(A,B,C)=Σm(1,2,3,5,7)
```

1. Construir la tabla.
2. Escribir la suma de productos estándar.
3. Escribir el producto de sumas estándar equivalente.
4. Verificar ambas expresiones con al menos tres combinaciones.

### Ejercicio 9.2 – Simplificación

Simplificar mediante álgebra y Karnaugh:

```text
F(A,B,C)=Σm(1,2,3,5,7)
```

Después:

1. dibujar circuito original;
2. dibujar circuito simplificado;
3. comparar cantidad de puertas;
4. simular ambos;
5. demostrar que las tablas coinciden.

### Ejercicio 9.3 – Implementación solo con NAND

Tomar la expresión simplificada del ejercicio anterior e implementarla utilizando únicamente puertas NAND.

Explicar:

- dónde se aplicó De Morgan;
- cuántas puertas se necesitan;
- qué implementación utilizaría menos integrados disponibles en el laboratorio.

---

## Semana 11 – Caso integrador del tanque

### Ejercicio 11.1 – Requisitos

Un depósito tiene sensores de nivel bajo `L` y nivel alto `H`, además de una habilitación `E`.

La bomba debe activarse cuando el sistema está habilitado y el nivel está bajo. Debe apagarse cuando se alcanza el nivel alto. Una alarma debe indicar una combinación incoherente de sensores.

1. Definir con precisión el significado de 0 y 1.
2. Determinar combinaciones físicamente válidas e inválidas.
3. Construir las tablas de la bomba y la alarma.
4. Obtener expresiones.
5. Simplificar.
6. Simular.
7. Montar en protoboard.

### Ejercicio 11.2 – Falla provocada

En el circuito anterior, desconectar intencionalmente una entrada o colocar un cable en una fila incorrecta.

El grupo que recibe el montaje debe:

1. observar el síntoma;
2. comparar con la tabla esperada;
3. comprobar alimentación;
4. medir señales;
5. identificar la falla;
6. corregirla;
7. documentar el procedimiento.

---

# Corte 3

## Semana 12 – XOR, sumadores y restadores

### Ejercicio 12.1 – Semi-sumador

1. Construir la tabla de suma de dos bits.
2. Identificar la columna de suma y la de acarreo.
3. Obtener:

```text
S=A⊕B
C=A·B
```

4. Simular.
5. Montar.
6. Explicar por qué una OR no puede sustituir a XOR en la salida de suma.

### Ejercicio 12.2 – Sumador completo

Construir la tabla para `A`, `B` y `Cin`.

1. Obtener `S` y `Cout`.
2. Implementar mediante dos semi-sumadores y una OR.
3. Probar ocho combinaciones.
4. Explicar el significado del acarreo.

### Ejercicio 12.3 – Detector de diferencia

Dos sensores redundantes deberían entregar el mismo estado. Diseñar una salida de falla que se active cuando sean diferentes.

1. Seleccionar XOR o XNOR.
2. Construir la tabla.
3. Justificar la elección.
4. Indicar qué pasa si ambos sensores fallan de la misma manera.

---

## Semana 13 – Comparadores y paridad

### Ejercicio 13.1 – Comparación de consumo

`A` representa el consumo actual y `B` el límite, ambos en 4 bits.

Evaluar:

```text
A=0110, B=1001
A=1010, B=1010
A=1101, B=0101
```

Para cada caso indicar `A>B`, `A=B` y `A<B` y explicar la decisión de control que podría tomarse.

### Ejercicio 13.2 – Comparador de 1 bit

1. Construir la tabla completa.
2. Obtener las expresiones de `A>B`, `A=B` y `A<B`.
3. Implementar.
4. Verificar las cuatro combinaciones.

### Ejercicio 13.3 – Paridad

Para cada palabra, generar el bit de paridad par:

```text
1011010
0110011
1111000
```

Luego modificar un bit y verificar la detección. Finalmente modificar dos bits y explicar la limitación observada.

---

## Semana 14 – Codificadores y decodificadores

### Ejercicio 14.1 – Decodificador de estados

Diseñar un decodificador para:

| Código | Estado |
|---|---|
| 00 | normal |
| 01 | advertencia |
| 10 | alarma |
| 11 | mantenimiento |

1. Construir tabla.
2. Obtener una expresión por salida.
3. Implementar o simular.
4. Indicar si las salidas son activas en alto o en bajo.

### Ejercicio 14.2 – BCD a 7 segmentos

Utilizando la hoja de datos del 74LS47:

1. identificar VCC y GND;
2. identificar entradas BCD;
3. identificar salidas `a–g`;
4. determinar el tipo de display compatible;
5. calcular resistencias de segmento;
6. probar los códigos de 0 a 9;
7. observar qué sucede con 10 a 15.

### Ejercicio 14.3 – Prioridad

Tres alarmas pueden activarse al mismo tiempo:

- temperatura alta;
- nivel crítico;
- falla eléctrica.

Diseñar una prioridad y producir un código de 2 bits que indique la condición más importante. Justificar el orden escogido.

---

## Semana 15 – Multiplexores y demultiplexores

### Ejercicio 15.1 – MUX 4 a 1

Cuatro señales `I0–I3` representan sensores. Completar la tabla de selección para `S1S0` y comprobar cada entrada.

Después responder:

- ¿qué ocurre si Enable está deshabilitado?;
- ¿cuántas líneas de selección necesitaría un MUX 8 a 1?;
- ¿qué ventaja aporta frente a conectar cuatro indicadores separados?

### Ejercicio 15.2 – Función mediante MUX

Implementar con un MUX 4 a 1:

```text
F(A,B,C)=Σm(1,2,6,7)
```

Usar `A` y `B` como selectores y determinar qué debe conectarse en cada entrada de datos: `0`, `1`, `C` o `C̅`.

### Ejercicio 15.3 – Distribución de alarma

Una entrada de alarma debe dirigirse a una de cuatro zonas mediante dos bits de selección.

1. Dibujar el DEMUX.
2. Construir la tabla.
3. Explicar qué ocurre en salidas no seleccionadas.
4. Identificar una condición insegura si las salidas son activas en bajo.

---

## Semana 16 – Flip-flops y contadores

### Ejercicio 16.1 – Flip-flop D

Para una señal de reloj de flanco positivo y la siguiente secuencia de `D`:

```text
D antes de cada flanco: 1, 0, 1, 1, 0, 0
```

1. determinar `Q` después de cada flanco;
2. dibujar el diagrama de tiempos;
3. explicar qué ocurre con cambios en D entre flancos;
4. analizar la acción de Clear.

### Ejercicio 16.2 – JK como divisor

Un flip-flop JK tiene `J=K=1` y recibe un reloj de 2 kHz.

1. determinar la frecuencia de `Q`;
2. conectar una segunda etapa igual;
3. determinar las frecuencias de ambas salidas;
4. explicar la relación con un contador binario.

### Ejercicio 16.3 – Contador módulo 6

Diseñar conceptualmente un contador para registrar seis ciclos de una bomba.

1. determinar la cantidad mínima de flip-flops;
2. escribir la secuencia de estados;
3. identificar estados no utilizados;
4. definir el reinicio;
5. decodificar el estado correspondiente al sexto evento;
6. explicar cómo evitar múltiples pulsos por rebote.

### Ejercicio 16.4 – Diagnóstico secuencial

Un contador salta estados cuando se acciona un pulsador.

Analizar como posibles causas:

- rebote mecánico;
- entrada de reloj flotante;
- alimentación deficiente;
- reset inestable;
- cableado incorrecto;
- retardo de propagación.

Diseñar una prueba para distinguir cada causa.

---

# Actividad de integración para la Semana 17

El grupo debe presentar su proyecto utilizando una secuencia de ingeniería inspirada en las aplicaciones integradoras de Floyd:

1. requisitos;
2. variables;
3. tabla o secuencia de estados;
4. expresiones y simplificación;
5. circuito combinacional;
6. memoria, temporización o conteo cuando aplique;
7. etapa de salida;
8. pruebas normales;
9. falla provocada;
10. diagnóstico y corrección.

## Regla de evaluación

Una respuesta numérica o una salida correcta no es suficiente. Debe existir coherencia entre:

```text
requisito = tabla = expresión = simulación = montaje = medición
```