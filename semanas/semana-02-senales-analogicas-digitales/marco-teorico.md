# Marco teórico – Semana 02

# Señales analógicas y señales digitales

## 1. Tema de la semana

Durante esta semana se estudiará la diferencia entre señales analógicas y digitales, entendiendo cómo se representa la información mediante voltaje, corriente y niveles lógicos.

## 2. Objetivo de aprendizaje

Diferenciar señales analógicas y digitales, identificando sus características, formas de representación, ventajas, limitaciones y aplicaciones en sistemas eléctricos y electrónicos.

## 3. Contexto e importancia

La electrónica trabaja con señales. Una señal es una variación física que transporta información. En los circuitos eléctricos y electrónicos, esta información puede representarse mediante voltaje, corriente, frecuencia, pulsos o niveles lógicos.

En ingeniería eléctrica se encuentran señales analógicas en sensores, transformadores, sistemas de medición, audio, temperatura, velocidad, corriente y voltaje. También se encuentran señales digitales en sistemas de control, protecciones electrónicas, microcontroladores, PLC, comunicaciones y automatización.

Comprender la diferencia entre ambos tipos de señales es fundamental para avanzar en el curso, porque la asignatura integra electrónica analógica y electrónica digital.

## 4. Imagen de apoyo

![Comparación entre señal analógica y digital](../../recursos/imagenes/semana-02/senal-analogica-vs-digital.svg)

## 5. Conceptos fundamentales

### Señal

Una señal es una magnitud que varía en el tiempo y que puede representar información. En electrónica, las señales más comunes son voltajes y corrientes.

### Señal analógica

Una señal analógica puede tomar infinitos valores dentro de un rango. Su variación suele ser continua. Un ejemplo típico es una onda senoidal de voltaje.

Ejemplos:

- Voltaje de una red AC.
- Señal de audio.
- Temperatura medida por un sensor.
- Corriente en una carga.
- Velocidad de un motor.

### Señal digital

Una señal digital trabaja con valores discretos. En electrónica digital se utilizan normalmente dos niveles: nivel lógico 0 y nivel lógico 1.

Ejemplos:

- Señal de salida de un microcontrolador.
- Pulsos de un encoder.
- Señales de control en compuertas lógicas.
- Comunicación digital.
- Estados encendido/apagado.

### Nivel lógico

Un nivel lógico es un rango de voltaje interpretado como 0 o como 1. Por ejemplo, en muchos sistemas digitales de 5 V, un voltaje cercano a 0 V puede representar 0 lógico y un voltaje cercano a 5 V puede representar 1 lógico.

## 6. Explicación teórica principal

La diferencia central entre una señal analógica y una digital está en la forma en que representan la información.

Una señal analógica representa la información mediante una variación continua. Esto permite describir fenómenos físicos con gran detalle, pero también hace que la señal sea más sensible al ruido y a las perturbaciones.

Una señal digital representa la información mediante niveles discretos. Esta forma de representación es más robusta frente al ruido, porque el circuito no necesita interpretar todos los valores intermedios, sino decidir si la señal corresponde a un 0 o a un 1.

En la práctica, muchos sistemas modernos son mixtos. Un sensor puede entregar una señal analógica, un conversor analógico-digital puede transformarla en datos digitales y un microcontrolador puede tomar decisiones con base en esa información.

## 7. Relación con aplicaciones reales

En ingeniería eléctrica y electrónica existen muchas aplicaciones mixtas:

- Un sensor de temperatura entrega una señal analógica y un controlador digital decide encender un ventilador.
- Un transformador entrega una señal AC analógica y un sistema digital supervisa si hay falla.
- Un variador de velocidad mide corrientes y voltajes analógicos, pero procesa la información digitalmente.
- Un sistema de automatización usa entradas digitales para detectar finales de carrera, pulsadores o sensores de presencia.

## 8. Ejemplo guiado

Un sensor entrega un voltaje entre 0 V y 5 V dependiendo de la temperatura. Si la temperatura es baja, entrega 1 V. Si la temperatura es alta, entrega 4.5 V. Esta señal es analógica porque puede tomar muchos valores intermedios.

Luego, un microcontrolador compara ese voltaje con un valor límite. Si supera 3 V, activa una salida digital en 1 lógico. Si está por debajo, mantiene la salida en 0 lógico.

En este ejemplo, el sistema combina una entrada analógica con una decisión digital.

## 9. Errores comunes o puntos de cuidado

- Pensar que toda señal cuadrada es necesariamente digital. Una onda cuadrada puede ser analógica si se analiza como forma de onda continua.
- Creer que un 1 lógico siempre equivale exactamente a 5 V. En realidad, depende de la familia lógica o del dispositivo.
- No considerar el ruido en señales analógicas.
- Confundir tierra o GND con nivel lógico 0 sin revisar el circuito.
- No verificar el voltaje de operación de los circuitos digitales.

## 10. Preguntas orientadoras para la clase

1. ¿Qué diferencia hay entre una señal continua y una señal discreta?
2. ¿Por qué las señales digitales son útiles en sistemas de control?
3. ¿Qué ventajas tiene una señal analógica para representar fenómenos físicos?
4. ¿Qué ejemplos de sistemas mixtos se encuentran en la ingeniería eléctrica?
5. ¿Qué ocurre si una señal digital queda en un valor intermedio entre 0 y 1?

## 11. Trabajo del estudiante

Antes de la siguiente clase, el estudiante debe identificar tres sistemas reales donde existan señales analógicas, digitales o mixtas, y explicar brevemente qué información transporta cada señal.
