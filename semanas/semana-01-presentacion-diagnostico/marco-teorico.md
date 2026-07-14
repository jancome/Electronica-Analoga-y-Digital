# Marco teórico – Semana 01

# Presentación del curso e introducción a la electrónica analógica y digital

## 1. Tema de la semana

Presentación general de la asignatura **Electrónica Analógica y Digital**, diagnóstico inicial e introducción conceptual a la diferencia entre sistemas analógicos, sistemas digitales y sistemas mixtos.

## 2. Objetivo de aprendizaje

Reconocer el propósito de la asignatura y diferenciar, a nivel introductorio, los conceptos de electrónica analógica, electrónica digital y sistemas electrónicos mixtos, relacionándolos con aplicaciones propias de la ingeniería eléctrica.

## 3. Contexto e importancia del tema

La electrónica está presente en la mayoría de los sistemas modernos de ingeniería: fuentes de alimentación, sensores, sistemas de control, protecciones eléctricas, automatización, comunicaciones, instrumentación, variadores de velocidad, sistemas embebidos, cargadores, iluminación LED, equipos industriales y dispositivos de consumo.

En términos generales, la electrónica puede estudiarse desde dos enfoques complementarios:

- **Electrónica analógica:** trabaja con señales continuas que pueden tomar muchos valores dentro de un rango.
- **Electrónica digital:** trabaja con señales discretas, normalmente representadas mediante dos estados: 0 y 1.

En la práctica, muchos sistemas reales combinan ambas. Por ejemplo, un sensor puede entregar una señal analógica, un microcontrolador puede procesarla digitalmente y una etapa de potencia puede activar una carga eléctrica.

## 4. Conceptos fundamentales

### Electrónica

La electrónica es el área de la ingeniería que estudia el comportamiento, control y aplicación de dispositivos y circuitos que permiten procesar señales eléctricas o controlar energía mediante componentes como diodos, transistores, circuitos integrados, sensores y controladores.

### Señal eléctrica

Una señal eléctrica es una variación de voltaje o corriente que transporta información o representa una magnitud física. Puede representar temperatura, presión, velocidad, posición, nivel, sonido, luz o cualquier variable que pueda convertirse en una magnitud eléctrica.

### Sistema analógico

Un sistema analógico utiliza señales continuas. Esto significa que la señal puede tomar muchos valores dentro de un rango. Por ejemplo, una señal de temperatura convertida en voltaje podría variar de 0 V a 5 V de manera gradual.

Ejemplos:

- Voltaje de salida de un sensor de temperatura.
- Señal de audio.
- Variación de luz en una fotocelda.
- Señal de corriente en un transductor industrial.
- Voltaje rectificado en una fuente de alimentación.

### Sistema digital

Un sistema digital utiliza señales discretas. Normalmente trabaja con dos niveles lógicos:

- **0 lógico:** nivel bajo.
- **1 lógico:** nivel alto.

Ejemplos:

- Una compuerta lógica.
- Un contador digital.
- Un display de 7 segmentos controlado por BCD.
- Una entrada digital de un PLC.
- Una señal de encendido o apagado.

### Sistema mixto

Un sistema mixto combina etapas analógicas y digitales. Es lo más común en aplicaciones reales.

Ejemplo:

1. Un sensor mide una variable física.
2. La señal analógica se acondiciona.
3. Un convertidor ADC la transforma en dato digital.
4. Un controlador toma una decisión.
5. Una etapa de potencia activa una carga.

## 5. Comparación entre electrónica analógica y digital

| Aspecto | Electrónica analógica | Electrónica digital |
|---|---|---|
| Tipo de señal | Continua | Discreta |
| Valores posibles | Muchos valores dentro de un rango | Generalmente 0 y 1 |
| Ejemplos de componentes | Diodos, transistores, amplificadores | Compuertas, flip-flops, contadores |
| Aplicaciones | Fuentes, sensores, audio, potencia | Procesamiento lógico, control, memoria |
| Principal dificultad | Ruido, precisión y estabilidad | Temporización, niveles lógicos y codificación |

## 6. Relación con la ingeniería eléctrica

Para un ingeniero eléctrico, la electrónica analógica y digital permite comprender y diseñar sistemas de control, protección, medición y automatización. Algunos ejemplos son:

- Control de motores eléctricos.
- Fuentes de alimentación DC.
- Automatización de portones, bombas y sistemas industriales.
- Sistemas de iluminación LED.
- Sensores conectados a PLC o microcontroladores.
- Circuitos de protección y acondicionamiento de señal.
- Sistemas de medición de voltaje, corriente y potencia.

## 7. Ejemplo guiado

Suponga un sistema automático de encendido de una lámpara según la luz ambiente.

### Etapa analógica

Una fotocelda o sensor de luz cambia su resistencia o voltaje dependiendo de la iluminación.

### Etapa de comparación o decisión

Un circuito compara si el nivel de luz está por debajo de un valor establecido.

### Etapa digital

La salida puede interpretarse como:

- 0: no encender.
- 1: encender.

### Etapa de potencia

Un transistor, relé o MOSFET activa la lámpara.

Este ejemplo muestra que un sistema real puede combinar electrónica analógica, digital y potencia.

## 8. Errores comunes o puntos de cuidado

- Pensar que lo analógico y lo digital son áreas totalmente separadas.
- Creer que una señal digital no tiene voltaje real. En realidad, el 0 y el 1 se representan mediante rangos de voltaje.
- Confundir una señal variable con una señal necesariamente analógica. Algunas señales digitales también cambian en el tiempo, pero lo hacen entre niveles definidos.
- Ignorar la importancia de las tierras comunes en circuitos mixtos.
- Alimentar circuitos integrados sin revisar el pinout.

## 9. Preguntas orientadoras para la clase

1. ¿Dónde vemos electrónica analógica en sistemas eléctricos reales?
2. ¿Dónde vemos electrónica digital en sistemas eléctricos reales?
3. ¿Por qué un sistema moderno normalmente combina ambas?
4. ¿Qué ventajas tiene procesar información en forma digital?
5. ¿Qué ventajas tiene trabajar con señales analógicas para medir variables físicas?

## 10. Trabajo previo o posterior del estudiante

Para la siguiente clase, el estudiante debe identificar tres sistemas reales y clasificarlos como:

- Analógico.
- Digital.
- Mixto.

Debe explicar brevemente qué señales intervienen y qué función cumple cada etapa.

## 11. Conexión con la siguiente semana

La próxima semana se estudiarán con más detalle las señales analógicas y digitales, los niveles de voltaje, las magnitudes eléctricas básicas y la forma en que una señal puede representar información dentro de un circuito electrónico.
