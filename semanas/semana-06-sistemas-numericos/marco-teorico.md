# Marco teórico – Semana 06

# Sistemas numéricos y definición de variables del proyecto

## Metas de aprendizaje verificables

- Convertir valores entre decimal, binario y hexadecimal y distinguir el código BCD.
- Dimensionar bits y documentar orden, rango, resolución y estados inválidos.
- Vincular cada condición física del ABPr con un nivel eléctrico y una representación lógica.

## 1. Propósito de la semana

Iniciar la Fase 2 del ABPr mostrando cómo un sistema digital representa cantidades, estados y condiciones mediante bits.

El objetivo no es realizar conversiones de forma aislada, sino utilizarlas para definir las variables de entrada y salida del proyecto.

## 2. Resultado de aprendizaje

Al finalizar la semana, el estudiante estará en capacidad de:

- Diferenciar decimal, binario, hexadecimal y BCD.
- Realizar conversiones básicas entre sistemas.
- Diferenciar número binario y código.
- Definir variables digitales relacionadas con la situación problema.
- Establecer qué condición física representa 0 y qué condición representa 1.
- Actualizar el diagrama de bloques para iniciar la etapa lógica.

## 3. Conexión con la Fase 2 ABPr

La Fase 2 debe producir una solución digital funcional:

```text
Condiciones del problema
        ↓
Variables digitales
        ↓
Tabla de verdad
        ↓
Expresión y simplificación
        ↓
Simulación
        ↓
Montaje en protoboard
```

## 4. Conceptos fundamentales

- **Bit:** unidad mínima de información, con valores 0 o 1.
- **Nibble:** conjunto de 4 bits.
- **Byte:** conjunto de 8 bits.
- **Palabra:** grupo de bits tratado como una unidad.
- **Base:** cantidad de símbolos utilizados por un sistema numérico.

## 5. Sistema decimal

Utiliza diez símbolos, del 0 al 9. Cada posición representa una potencia de 10.

## 6. Sistema binario

Utiliza 0 y 1. Cada posición representa una potencia de 2.

```text
1011₂ = 1×2³ + 0×2² + 1×2¹ + 1×2⁰ = 11₁₀
```

## 7. Sistema hexadecimal

Utiliza los símbolos 0–9 y A–F. Cada dígito hexadecimal equivale a 4 bits.

```text
1010₂ = A₁₆
1111₂ = F₁₆
```

Es útil para representar patrones binarios de manera compacta.

## 8. Código BCD

Cada dígito decimal se representa mediante 4 bits.

```text
25₁₀ en BCD = 0010 0101
25₁₀ en binario puro = 11001₂
```

BCD será importante para decodificadores y displays de 7 segmentos.

## 9. Variables digitales del proyecto

Una variable digital debe tener un significado físico claro.

Ejemplos:

| Variable | 0 lógico | 1 lógico |
|---|---|---|
| L | Iluminación suficiente | Lugar oscuro |
| P | Sin presencia | Presencia detectada |
| N | Nivel suficiente | Nivel bajo |
| T | Temperatura normal | Temperatura alta |
| E | Energía no disponible | Energía disponible |

Los nombres deben ser cortos, pero su interpretación debe quedar documentada.

## 10. Entradas y salidas

- **Entradas:** representan condiciones del entorno, sensores, interruptores o estados.
- **Salidas:** representan una decisión: alarma, indicador, habilitación, bloqueo o control de carga.

Una salida digital no activa necesariamente una carga de forma directa; puede requerir BJT, MOSFET o relé.

## 11. Ejemplo aplicado

Un sistema de iluminación debe encender una lámpara solo cuando el sitio está oscuro y hay presencia.

```text
L = 1: oscuro
P = 1: presencia
Y = 1: encender lámpara
```

La función lógica se desarrollará posteriormente, pero desde esta semana las variables deben quedar definidas sin ambigüedad.

## 12. Actividad de clase

Cada grupo deberá:

1. Revisar la situación problema escogida.
2. Definir entre 2 y 4 variables digitales de entrada.
3. Definir al menos una salida.
4. Especificar el significado de 0 y 1 para cada variable.
5. Identificar si alguna magnitud debe convertirse a una condición digital mediante sensor, comparador o interruptor.
6. Actualizar el diagrama de bloques.

## 13. Evidencia ABPr

- Tabla de variables.
- Diagrama de bloques actualizado.
- Justificación de entradas y salidas.
- Representación binaria de estados o códigos utilizados.
- Registro de correcciones de la Fase 1 que se incorporarán.

## 14. Errores comunes

- Definir variables sin relacionarlas con una condición física.
- Confundir BCD con binario puro.
- Usar demasiadas variables para una primera implementación.
- No indicar si una entrada es activa en alto o en bajo.
- Pretender controlar una carga directamente desde una compuerta lógica.

## 15. Trabajo independiente

- Realizar conversiones decimal–binario–hexadecimal–BCD.
- Completar la tabla de variables del proyecto.
- Consultar los niveles eléctricos de los circuitos integrados que podrían utilizarse.
- Preparar ejemplos de estados o conteos que requiera la solución.

## 16. Conexión con la Semana 07

La siguiente semana se estudiará aritmética binaria para comprender acarreo, préstamo, complemento y representación de datos, especialmente en proyectos que requieran conteo o comparación.

## 17. Profundización: número, código y nivel eléctrico

Un bit es una representación abstracta que en hardware se implementa mediante intervalos de tensión. Por ello, `0` y `1` no significan siempre `0 V` y `5 V`: la familia lógica define rangos garantizados de entrada y salida y una zona indeterminada. El diseño debe conservar margen de ruido y nunca dejar una entrada flotante.

Un número posicional de base `r` se interpreta como:

\[
N=\sum_{i=0}^{n-1}d_i r^i
\]

En binario `r=2`; en hexadecimal `r=16`. Cada dígito hexadecimal representa exactamente cuatro bits, de modo que la conversión binario–hexadecimal se realiza agrupando nibbles. BCD no es otra base: codifica por separado cada dígito decimal con cuatro bits. Por ejemplo, `173₁₀=10101101₂=AD₁₆`, mientras su BCD es `0001 0111 0011`. Confundir valor binario con BCD produce salidas de display erróneas.

Para `n` bits sin signo, el rango es `0≤N≤2^n-1`. El número de bits mínimo para `M` estados es `n=⌈log₂M⌉`. Esta relación permite dimensionar códigos de estados, buses y futuros contadores.

## 18. Ejemplo guiado adaptado

Un indicador de nivel cuantiza de `0` a `255` y registra `173`:

1. Divisiones sucesivas o suma de potencias: `173=128+32+8+4+1`, por tanto `10101101₂`.
2. Agrupando `1010 1101`, se obtiene `AD₁₆`.
3. Codificando dígitos decimales: `1→0001`, `7→0111`, `3→0011`; BCD usa 12 bits.
4. En binario/hexadecimal se representa el valor compacto; BCD facilita la presentación decimal, pero consume más bits.

En el ABPr, tres variables binarias `L` (nivel bajo), `H` (nivel alto) y `E` (habilitación) no forman necesariamente un número. Son un vector de condiciones. El equipo debe distinguir datos numéricos de banderas lógicas.

## 19. Procedimiento de simulación o práctica

1. Definir cada variable con nombre, unidad, rango físico y criterio para `0/1`.
2. Identificar estados imposibles o inseguros.
3. Convertir diez valores entre decimal, binario y hexadecimal; verificar con calculadora solo al final.
4. Implementar con interruptores un vector de 4 bits y observarlo en sondas lógicas o LEDs con resistencias.
5. Medir tensiones reales de ALTO y BAJO y compararlas con la hoja de datos del circuito integrado.
6. Documentar orden de bits: `MSB…LSB`; invertirlo cambia el valor aunque el cableado parezca completo.

## 20. Diagnóstico de fallas

Una lectura duplicada o invertida puede deberse a orden de bits, no a la conversión. Un código BCD entre `1010` y `1111` es inválido. Una entrada flotante puede alternar sin patrón. El diagnóstico sigue: verificar alimentación y referencia, fijar entradas conocidas (`0000`, `0001`, `1000`, `1111`), observar bits individualmente y recién después interpretar el valor.

## 21. Preguntas orientadoras y trabajo independiente

- ¿La variable es numérica, categórica o una bandera?
- ¿Cuántos estados válidos e inválidos tiene el código?
- ¿Qué resolución se obtiene con `n` bits?
- ¿Cómo se detectaría un intercambio entre MSB y LSB?
- ¿Qué tensión real garantiza la familia lógica para cada estado?

Cada grupo entregará un diccionario de entradas/salidas, una codificación de estados, cinco conversiones justificadas, identificación de códigos inválidos y una tabla que vincule condición física, nivel eléctrico y bit.

## 22. Referencias de estudio

- Floyd, 9.ª ed., cap. 1, sec. 1.2, pp. 6–13: bits, niveles lógicos, formas de onda y transferencia de datos.
- Ibid., cap. 2, secs. 2.2–2.3, pp. 56–62: números binarios y conversiones.
- Ibid., sec. 2.8, pp. 82–89; sec. 2.10, pp. 93–95; sec. 2.11, pp. 96–103: hexadecimal, BCD y códigos digitales.

## 23. Ruta de profundización recomendada

1. **Base eléctrica:** Floyd, cap. 1, sec. 1.2, pp. 6–13.
2. **Conversión obligatoria:** cap. 2, secs. 2.2–2.3, pp. 56–62, y sec. 2.8, pp. 82–89.
3. **Códigos para interfaces:** cap. 2, secs. 2.10–2.11, pp. 93–103.
4. **Ampliación:** cap. 2 completo para relacionar representación, operaciones, códigos y detección de errores antes de abordar circuitos aritméticos.
