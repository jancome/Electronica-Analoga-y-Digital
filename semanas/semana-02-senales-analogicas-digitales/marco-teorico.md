# Marco teórico – Semana 02

# Señales, magnitudes eléctricas y medición básica

## 1. Tema de la semana

Durante esta semana se estudiará cómo la información puede representarse mediante señales eléctricas y cómo dichas señales se relacionan con magnitudes básicas de circuitos: voltaje, corriente, resistencia, potencia, referencia o tierra, y medición con instrumentos.

Esta semana funciona como puente entre el diagnóstico de circuitos de la Semana 01 y el inicio formal de la electrónica analógica con semiconductores y diodos en la Semana 03.

---

## 2. Objetivo de aprendizaje

Diferenciar señales analógicas y digitales, interpretar sus características eléctricas y relacionarlas con magnitudes medibles como voltaje, corriente, frecuencia, potencia y niveles lógicos, aplicando fundamentos básicos de circuitos.

---

## 3. Contexto e importancia

La electrónica trabaja con señales. Una señal es una variación física que transporta información. En los circuitos eléctricos y electrónicos, esta información puede representarse mediante voltaje, corriente, frecuencia, pulsos o niveles lógicos.

En ingeniería eléctrica se encuentran señales analógicas en sensores, transformadores, sistemas de medición, audio, temperatura, velocidad, corriente y voltaje. También se encuentran señales digitales en sistemas de control, protecciones electrónicas, microcontroladores, PLC, comunicaciones y automatización.

Comprender una señal exige algo más que observar su forma de onda. También es necesario saber medirla, identificar su referencia, calcular corriente, estimar potencia y reconocer si el circuito opera en DC, AC o con pulsos.

---

## 4. Imagen de apoyo

![Comparación entre señal analógica y digital](../../recursos/imagenes/semana-02/senal-analogica-vs-digital.svg)

---

## 5. Conceptos fundamentales

### 5.1 Señal

Una señal es una magnitud que varía en el tiempo y que puede representar información. En electrónica, las señales más comunes son voltajes y corrientes.

### 5.2 Voltaje

El voltaje es una diferencia de potencial eléctrico entre dos puntos. Siempre debe medirse entre dos nodos. Por eso, cuando se dice que una señal es de 5 V, realmente se está comparando ese punto contra una referencia, normalmente GND.

### 5.3 Corriente

La corriente eléctrica representa el flujo de carga. En un circuito cerrado, la corriente fluye cuando existe una fuente de energía y un camino conductor.

### 5.4 Resistencia

La resistencia se opone al paso de corriente y permite limitarla o distribuir voltajes dentro de un circuito.

### 5.5 Potencia

La potencia indica cuánta energía por unidad de tiempo consume o disipa un elemento. En electrónica es importante para evitar que resistencias, diodos, transistores o reguladores se dañen por exceso de temperatura.

---

## 6. Ley de Ohm aplicada a señales

La Ley de Ohm permite relacionar voltaje, corriente y resistencia:

```text
V = I × R
```

También puede escribirse como:

```text
I = V / R
R = V / I
```

En esta semana se usará para interpretar señales eléctricas. Por ejemplo, si una salida entrega 5 V a una resistencia de 1 kΩ, la corriente aproximada será:

```text
I = 5 V / 1000 Ω
I = 5 mA
```

Esto permite comprender que una señal no solo tiene voltaje: también puede entregar corriente y disipar potencia dependiendo de la carga conectada.

---

## 7. Señal analógica

Una señal analógica puede tomar muchos valores dentro de un rango. Su variación suele ser continua.

Ejemplos:

- Voltaje de una red AC.
- Señal de audio.
- Temperatura medida por un sensor.
- Corriente en una carga.
- Velocidad de un motor.
- Voltaje de salida de una fuente rectificada.

Las señales analógicas permiten representar fenómenos físicos con detalle, pero pueden ser sensibles al ruido, variaciones de temperatura, caída de voltaje en conductores y tolerancias de componentes.

---

## 8. Señal digital

Una señal digital trabaja con valores discretos. En electrónica digital se utilizan normalmente dos niveles: nivel lógico 0 y nivel lógico 1.

Ejemplos:

- Señal de salida de un microcontrolador.
- Pulsos de un encoder.
- Señales de control en compuertas lógicas.
- Comunicación digital.
- Estados encendido/apagado.

Un nivel lógico no es un número abstracto: se representa físicamente con un rango de voltaje. Por ejemplo, en muchos sistemas de 5 V, un voltaje cercano a 0 V puede interpretarse como 0 lógico y uno cercano a 5 V como 1 lógico.

---

## 9. DC, AC y señales pulsantes

### Señal DC

Una señal DC mantiene polaridad constante. Puede ser fija o variar lentamente, pero no cambia de signo periódicamente.

Ejemplos:

- Fuente de 5 V.
- Batería de 9 V.
- Salida de un regulador.

### Señal AC

Una señal AC cambia de polaridad de forma periódica. La red eléctrica y las señales senoidales de un transformador son ejemplos comunes.

### Señal pulsante

Una señal pulsante puede provenir de un proceso de rectificación. No es completamente DC pura, porque aún puede presentar rizado o variación en el tiempo.

Este concepto será clave para entender rectificadores y filtros capacitivos.

---

## 10. Frecuencia, periodo y amplitud

En señales variables se usan tres conceptos importantes:

- **Amplitud:** valor máximo o nivel de la señal.
- **Periodo:** tiempo que tarda en repetirse un ciclo.
- **Frecuencia:** cantidad de ciclos por segundo.

```text
f = 1 / T
```

Donde:

- f es la frecuencia en hertz.
- T es el periodo en segundos.

---

## 11. Valor pico, pico a pico y RMS

En una señal senoidal se pueden diferenciar:

- **Valor pico:** máximo valor respecto a la referencia.
- **Valor pico a pico:** diferencia entre el máximo positivo y el máximo negativo.
- **Valor RMS:** valor eficaz, útil para relacionar una señal AC con su capacidad de entregar potencia.

Para una señal senoidal ideal:

```text
VP = VRMS × √2
```

Este cálculo será necesario en la Semana 04 para analizar rectificadores.

---

## 12. Tierra o referencia

GND no siempre significa ausencia absoluta de voltaje. En circuitos electrónicos, GND suele ser el punto de referencia común contra el cual se miden las señales.

Una mala referencia puede causar:

- Mediciones incorrectas.
- Fallas en comunicación digital.
- Activación errática de entradas.
- Ruido en señales analógicas.
- Problemas en sistemas mixtos.

---

## 13. Medición básica con multímetro

### Medición de voltaje

El voltaje se mide en paralelo con el elemento o entre el nodo de interés y la referencia.

### Medición de corriente

La corriente se mide colocando el instrumento en serie con la rama donde circula la corriente.

### Medición de resistencia

La resistencia se mide con el circuito desenergizado, preferiblemente aislando el componente o verificando que no existan caminos paralelos que alteren la lectura.

### Puntos de cuidado

- No medir corriente como si se midiera voltaje.
- No medir resistencia con el circuito energizado.
- Verificar escala y borne correcto del multímetro.
- Confirmar polaridad en circuitos DC.

---

## 14. Relación con Leyes de Kirchhoff

Las señales se analizan dentro de circuitos. Por eso, las leyes de Kirchhoff permiten entender cómo se distribuyen voltajes y corrientes.

### Ley de corrientes

La corriente que entra a un nodo debe ser igual a la corriente que sale.

### Ley de voltajes

En una malla, la suma de subidas y caídas de voltaje debe cerrar el balance.

Estas ideas serán usadas en diodos y transistores. Por ejemplo, en un circuito con fuente, resistencia y diodo:

```text
VS = VR + VD
```

Entonces, si se conoce VS y se estima VD, se puede calcular VR y luego la corriente.

---

## 15. Relación con aplicaciones reales

En ingeniería eléctrica y electrónica existen muchas aplicaciones mixtas:

- Un sensor de temperatura entrega una señal analógica y un controlador digital decide encender un ventilador.
- Un transformador entrega una señal AC analógica y un sistema digital supervisa si hay falla.
- Un variador de velocidad mide corrientes y voltajes analógicos, pero procesa la información digitalmente.
- Un sistema de automatización usa entradas digitales para detectar finales de carrera, pulsadores o sensores de presencia.
- Una fuente de alimentación rectifica una señal AC, la filtra y entrega una salida DC para alimentar circuitos electrónicos.

---

## 16. Ejemplo guiado

Un sensor entrega un voltaje entre 0 V y 5 V dependiendo de la temperatura. Si la temperatura es baja, entrega 1 V. Si la temperatura es alta, entrega 4.5 V. Esta señal es analógica porque puede tomar muchos valores intermedios.

Luego, un microcontrolador compara ese voltaje con un valor límite. Si supera 3 V, activa una salida digital en 1 lógico. Si está por debajo, mantiene la salida en 0 lógico.

Si la salida digital activa un LED con una resistencia de 330 Ω desde 5 V, la corriente no se puede ignorar. Debe calcularse aproximadamente con Ley de Ohm, considerando la caída del LED. Esto muestra la conexión entre señal, decisión digital y circuito analógico real.

---

## 17. Errores comunes o puntos de cuidado

- Pensar que toda señal cuadrada es necesariamente digital.
- Creer que un 1 lógico siempre equivale exactamente a 5 V.
- No considerar el ruido en señales analógicas.
- Confundir tierra o GND con nivel lógico 0 sin revisar el circuito.
- No verificar el voltaje de operación de los circuitos digitales.
- Medir corriente incorrectamente con el multímetro.
- Olvidar que una señal puede dañarse si se conecta a una carga demasiado baja.
- Analizar señales sin definir primero su referencia.

---

## 18. Preguntas orientadoras para la clase

1. ¿Qué diferencia hay entre una señal continua y una señal discreta?
2. ¿Por qué el voltaje siempre se mide entre dos puntos?
3. ¿Por qué una señal digital también es una señal eléctrica real?
4. ¿Qué diferencia hay entre valor pico, pico a pico y RMS?
5. ¿Por qué una señal analógica puede ser más sensible al ruido?
6. ¿Qué ocurre si se conecta una carga muy baja a una salida electrónica?
7. ¿Por qué la Ley de Ohm sigue siendo necesaria para estudiar electrónica?

---

## 19. Trabajo del estudiante

Antes de la siguiente clase, el estudiante debe:

1. Repasar el diagnóstico de circuitos de la Semana 01.
2. Resolver ejercicios de Ley de Ohm, potencia y divisor de voltaje.
3. Identificar tres señales reales: una analógica, una digital y una mixta.
4. Indicar cómo mediría cada señal con multímetro u osciloscopio.
5. Preparar dudas sobre voltaje, corriente, frecuencia, RMS y referencia.

---

## 20. Conexión con la Semana 03

La Semana 03 inicia el estudio de semiconductores y diodos. Para analizar un diodo no basta con saber que conduce en un sentido: también se debe calcular la corriente, la caída de voltaje, la resistencia limitadora y la potencia. Por eso, los conceptos de señales y medición de esta semana se enlazan directamente con la electrónica analógica.