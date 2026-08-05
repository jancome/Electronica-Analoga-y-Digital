# Guía de uso de Thomas Floyd para los cortes 2 y 3

## Fuente principal

Thomas L. Floyd, **Fundamentos de sistemas digitales**, 9.ª edición, Pearson Prentice Hall.

Esta guía relaciona el libro con las semanas digitales de la asignatura. No reemplaza el marco teórico semanal: indica qué secciones respaldan cada tema, qué ejemplos pueden explicarse en clase y cómo conectarlos con el proyecto ABPr.

## Uso académico y derechos de autor

- No se publicarán capítulos completos, escaneos, figuras ni soluciones extensas del libro.
- Se citarán capítulo, sección y página de la edición utilizada.
- Los ejercicios del repositorio serán **adaptaciones propias**: se modifican valores, contexto, variables y aplicación.
- El estudiante debe resolver, explicar y comprobar; no basta con copiar una solución.

---

# Corte 2 – Fundamentos digitales y lógica combinacional

## Semana 06 – Sistemas numéricos y variables

### Base en Floyd

- Capítulo 1, Sección 1.2: bits, niveles lógicos, formas de onda y transferencia de datos, pp. 6–13.
- Capítulo 2, Secciones 2.2 y 2.3: números binarios y conversiones, pp. 56–62.
- Sección 2.8: hexadecimal, pp. 82–89.
- Sección 2.10: BCD, pp. 93–95.
- Sección 2.11: códigos digitales, pp. 96–103.

### Aporte al marco teórico

Floyd permite explicar que un sistema digital no trabaja con “números abstractos”, sino con niveles eléctricos que representan bits. También distingue número binario, código BCD, hexadecimal y transferencia serie/paralelo.

### Ejemplo docente adaptado

Una estación de control registra un nivel entre 0 y 255. Para el valor decimal 173:

1. convertir a binario de 8 bits;
2. expresar en hexadecimal;
3. representar cada dígito decimal en BCD;
4. explicar cuál representación usaría un microcontrolador y cuál facilitaría un display decimal.

### Conexión ABPr

Cada grupo define las variables de entrada y salida, indicando qué condición física corresponde a 0 y a 1, y qué estados requieren un código de más de un bit.

---

## Semana 07 – Aritmética binaria

### Base en Floyd

- Capítulo 2, Sección 2.4: aritmética binaria, pp. 63–66.
- Sección 2.5: complemento a 1 y complemento a 2, pp. 67–68.
- Secciones 2.6 y 2.7: números con signo y operaciones, pp. 69–81.
- Ejemplos 2.12 y 2.13: obtención del complemento a 2, p. 68.

### Aporte al marco teórico

El libro desarrolla suma, acarreo, resta mediante complemento a 2, números con signo y detección de overflow. Esto sirve para comprender contadores, comparadores y operaciones internas de sistemas digitales.

### Ejemplo docente adaptado

En 8 bits:

1. sumar `00110110` y `00011101`;
2. restar `01001101 - 00011011` mediante complemento a 2;
3. interpretar el resultado como número sin signo y como número con signo;
4. determinar si existe overflow.

### Conexión ABPr

Relacionar las operaciones con conteos de eventos, comparación de niveles codificados, acumulación de pulsos o representación de estados.

---

## Semana 08 – Compuertas lógicas y protoboard

### Base en Floyd

- Capítulo 3, Secciones 3.1–3.6: NOT, AND, OR, NAND, NOR, XOR y XNOR, pp. 124–154.
- Sección 3.8: lógica de función fija, pp. 164–173.
- Sección 3.9: localización de averías, pp. 174–197.
- Capítulo 14, Sección 14.1: niveles lógicos, disipación, retardos y fan-out, pp. 884–892.
- Secciones 14.2–14.5: CMOS, TTL y comparación práctica, pp. 893–914.

### Aporte al marco teórico

Floyd combina función lógica y comportamiento eléctrico. Esto es esencial para no tratar una compuerta como un símbolo ideal: deben revisarse VCC, GND, umbrales, corriente de salida, entradas no utilizadas y tiempos de propagación.

### Ejemplo docente adaptado

Sistema fotosensible con habilitación:

- `A=1`: oscuridad detectada por el módulo LDR.
- `B=1`: switch habilitado.
- `Y=1`: LED encendido.

Implementar `Y=A·B` con SN74LS08, comprobar las cuatro combinaciones y medir entrada y salida respecto a GND.

### Diagnóstico inspirado en Floyd

1. comprobar primero VCC y GND;
2. fijar todas las entradas en niveles conocidos;
3. aplicar combinaciones de prueba;
4. comparar salida medida con tabla de verdad;
5. aislar cableado, entrada o puerta defectuosa.

---

## Semana 09 – Álgebra de Boole, De Morgan y Karnaugh

### Base en Floyd

- Capítulo 4, Secciones 4.1–4.5: operaciones, leyes, De Morgan, análisis y simplificación, pp. 200–216.
- Secciones 4.6 y 4.7: formas estándar y tablas de verdad, pp. 217–227.
- Secciones 4.8–4.10: mapas de Karnaugh, pp. 228–246.
- Ejemplo 4.20: obtención de suma de productos y producto de sumas desde una tabla, p. 227.
- Ejemplos 4.30 y 4.33: transformación y minimización con Karnaugh, pp. 243–245.
- Capítulo 5, Ejemplos 5.5 y 5.6: reducción de circuitos combinacionales, pp. 282–283.

### Aporte al marco teórico

El libro presenta una secuencia completa:

```text
requerimientos → tabla → expresión → simplificación → circuito → verificación
```

Esta secuencia coincide directamente con la Fase 2 del ABPr.

### Ejemplo docente adaptado

Para una alarma de tres entradas:

```text
F(A,B,C)=Σm(1,2,3,5,7)
```

1. construir la tabla;
2. obtener la suma de productos estándar;
3. ubicar los minterminos en Karnaugh;
4. simplificar;
5. comparar número de compuertas antes y después;
6. comprobar todas las combinaciones en simulación y protoboard.

---

## Semana 11 – Cierre de la Fase 2

### Base en Floyd

- Capítulo 5: análisis e implementación de lógica combinacional, pp. 270–325.
- Aplicación a los sistemas digitales del Capítulo 5: control de un tanque de almacenamiento.
- Sección 5.7: localización de averías.

### Caso integrador adaptado

Sistema de administración de agua con tres entradas:

- `L`: nivel bajo.
- `H`: nivel alto.
- `E`: habilitación del sistema.

Salidas:

- `P`: activar bomba.
- `A`: activar alarma por condición incoherente o crítica.

El grupo debe:

1. establecer combinaciones físicamente posibles;
2. construir tablas de verdad;
3. obtener expresiones;
4. simplificar;
5. simular;
6. montar en protoboard;
7. provocar una falla de entrada o cableado y diagnosticarla.

Este caso conserva el enfoque de Floyd, pero se contextualiza al uso eficiente del agua en la región Caribe.

---

# Corte 3 – Aplicaciones combinacionales y secuenciales

## Semana 12 – XOR, sumadores y restadores

### Base en Floyd

- Capítulo 3, Sección 3.6: XOR y XNOR, pp. 151–154.
- Capítulo 6, Sección 6.1: semi-sumador y sumador completo, pp. 328–331.
- Sección 6.2: sumadores binarios en paralelo, pp. 332–339.
- Sección 6.3: acarreo serie y anticipado, pp. 340–343.

### Ejemplo docente adaptado

Diseñar un semi-sumador para dos pulsos binarios `A` y `B`:

- obtener la tabla;
- demostrar `S=A⊕B`;
- demostrar `C=A·B`;
- interpretar `S` como resultado y `C` como evento doble.

Después ampliar a sumador completo con `Cin` y verificar ocho combinaciones.

### Conexión ABPr

El bloque solo se integra cuando el proyecto necesita sumar eventos, detectar diferencia o producir acarreo. No se exige añadir un sumador sin una función real.

---

## Semana 13 – Comparadores y paridad

### Base en Floyd

- Capítulo 6, Sección 6.4: comparadores, pp. 344–347.
- Sección 6.10: generadores y comprobadores de paridad, pp. 379–382.
- Sección 2.12: detección y corrección de errores, pp. 104–121.

### Ejemplo docente adaptado – Comparación

Dos palabras de 4 bits representan consumo actual `A` y límite programado `B`.

Determinar para varios casos:

- `A>B`;
- `A=B`;
- `A<B`.

Explicar por qué el bit más significativo tiene prioridad en la comparación.

### Ejemplo docente adaptado – Paridad

Para la palabra `1011010`:

1. generar paridad par;
2. construir la palabra transmitida;
3. invertir un bit y comprobar el error;
4. invertir dos bits y analizar la limitación del método.

---

## Semana 14 – Codificadores, decodificadores y display

### Base en Floyd

- Capítulo 6, Sección 6.5: decodificadores, pp. 348–358.
- Sección 6.6: codificadores, pp. 359–363.
- Sección 6.7: convertidores de código, pp. 364–366.
- Figura 6.34 y desarrollo del 74LS47: decodificador/controlador BCD a 7 segmentos, pp. 356–358.

### Ejemplo docente adaptado

Un sistema tiene cuatro estados:

| Código | Estado |
|---|---|
| 00 | normal |
| 01 | advertencia |
| 10 | alarma |
| 11 | mantenimiento |

Diseñar un decodificador que active un indicador por estado. Después analizar cómo representar un dígito BCD mediante 74LS47 y display de ánodo común, prestando atención a salidas activas en bajo y resistencias de segmento.

---

## Semana 15 – Multiplexores y demultiplexores

### Base en Floyd

- Capítulo 6, Sección 6.8: multiplexores, pp. 367–376.
- Sección 6.9: demultiplexores, pp. 377–378.
- Ejercicios y respuestas del capítulo muestran implementación de funciones con 74LS151.

### Ejemplo docente adaptado

Un MUX 4 a 1 recibe cuatro señales de estado `I0–I3`. Dos selectores `S1S0` permiten observar una señal en una única salida.

El estudiante debe:

1. completar la tabla de selección;
2. identificar el estado de Enable;
3. comprobar cada canal;
4. proponer una aplicación real en el proyecto;
5. implementar una función booleana usando entradas conectadas a 0, 1 o una variable.

---

## Semana 16 – Flip-flops y contadores

### Base en Floyd

- Capítulo 7, Secciones 7.1–7.4: latches, flip-flops y aplicaciones, pp. 412–440.
- Sección 7.6: temporizador 555, pp. 448–453, como ampliación opcional.
- Capítulo 8, Secciones 8.1–8.3: contadores asíncronos, síncronos y ascendente/descendente, pp. 476–498.
- Secciones 8.5–8.7: cascada, decodificación y aplicaciones, pp. 509–522.
- Capítulo 14: retardo de propagación y límites eléctricos, como apoyo práctico.

### Ejemplo docente adaptado – Flip-flop

Para un flip-flop D, proporcionar una secuencia de reloj y una secuencia `D`. Determinar `Q` únicamente en el flanco activo y explicar por qué los cambios entre flancos no se almacenan.

### Ejemplo docente adaptado – Contador

Diseñar un contador módulo 6 para registrar ciclos de una bomba o activaciones de una carga:

1. determinar cantidad mínima de flip-flops;
2. escribir la secuencia de estados;
3. identificar estados no utilizados;
4. definir reset;
5. decodificar el sexto evento;
6. considerar rebote del pulsador y retardo de propagación.

---

## Semana 17 – Proyecto final

### Modelo de integración tomado de Floyd

Floyd desarrolla el sistema de control de semáforos durante los Capítulos 6, 7 y 8:

1. lógica combinacional;
2. temporización;
3. lógica secuencial;
4. integración de bloques;
5. localización de averías.

No se copiará el sistema como proyecto obligatorio. Se utilizará como **modelo de documentación progresiva** para que cada grupo demuestre:

```text
requisitos
→ diagrama de bloques
→ función lógica
→ temporización o memoria
→ interfaz de salida
→ pruebas
→ diagnóstico
→ correcciones
```

---

# Temas de Floyd que quedan como ampliación

- Registros de desplazamiento, Capítulo 9.
- Memorias, Capítulo 10.
- CPLD y FPGA, Capítulo 11.
- Introducción a computadoras y DSP, Capítulos 12 y 13.

Son valiosos, pero no deben desplazar los contenidos oficiales de las semanas 6 a 16.

# Recomendación metodológica

Cada marco teórico semanal deberá incluir cuatro elementos:

1. **Concepto:** definición y funcionamiento.
2. **Ejemplo guiado:** adaptación basada en Floyd.
3. **Ejercicio aplicado:** valores y contexto propios del curso.
4. **Comprobación:** tabla, simulación, protoboard o medición.

Así el libro se convierte en una base rigurosa sin transformar el repositorio en una reproducción de la obra.