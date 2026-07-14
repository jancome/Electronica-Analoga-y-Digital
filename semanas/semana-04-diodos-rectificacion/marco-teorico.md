# Marco teórico – Semana 04

# Diodos y rectificación

## 1. Tema de la semana

Uso del diodo semiconductor como rectificador para convertir señales de corriente alterna en señales de corriente directa pulsante.

![Rectificación y filtrado](../../recursos/imagenes/analogica/rectificacion-y-filtrado.svg)

---

## 2. Objetivo de aprendizaje

Analizar el funcionamiento de los rectificadores de media onda y onda completa, comprendiendo la forma de onda de salida, el efecto de la caída de voltaje en los diodos y la importancia del filtrado capacitivo.

---

## 3. Contexto e importancia del tema

Muchos equipos electrónicos necesitan alimentación en corriente directa, pero la energía disponible en la red eléctrica normalmente se suministra en corriente alterna. Por esta razón, las fuentes de alimentación deben convertir AC en DC.

El primer paso de esa conversión es la rectificación. Los diodos permiten que la corriente circule en un solo sentido, por lo que son fundamentales para construir rectificadores.

En ingeniería eléctrica, los rectificadores se encuentran en cargadores, fuentes DC, variadores, UPS, sistemas de control, equipos industriales, inversores y sistemas de potencia.

---

## 4. Conceptos fundamentales

### 4.1 Corriente alterna AC

Una señal AC cambia de polaridad periódicamente. En una señal senoidal, el voltaje aumenta, disminuye, cruza por cero y cambia de signo de forma repetitiva.

Sus magnitudes principales son:

- Voltaje pico.
- Voltaje pico a pico.
- Voltaje RMS.
- Frecuencia.
- Periodo.

### 4.2 Corriente directa DC

Una señal DC mantiene una polaridad definida. Puede ser constante o presentar variaciones pequeñas llamadas rizado.

Una fuente DC ideal mantiene su voltaje constante en el tiempo.

---

## 5. Voltaje RMS y voltaje pico

En una señal senoidal, el voltaje RMS representa el valor efectivo de la señal. El voltaje pico se puede calcular aproximadamente como:

```text
VP = VRMS × √2
```

Por ejemplo, si una señal AC tiene 6 V RMS:

```text
VP = 6 V × 1.414
VP ≈ 8.48 V
```

Este valor pico es importante porque determina el máximo voltaje disponible antes de considerar las caídas en los diodos.

---

## 6. Rectificador de media onda

Un rectificador de media onda utiliza un solo diodo en serie con la carga.

Durante el semiciclo positivo de la señal AC, el diodo queda en polarización directa y permite el paso de corriente. Durante el semiciclo negativo, el diodo queda en polarización inversa y bloquea la corriente.

Por eso, la señal de salida conserva solo una mitad de la señal de entrada.

### Características

- Usa un solo diodo.
- El aprovechamiento de la señal AC es bajo.
- La salida tiene alto rizado.
- La frecuencia del rizado es igual a la frecuencia de entrada.
- Es sencillo, pero poco eficiente para fuentes de alimentación.

---

## 7. Rectificador de onda completa

Un rectificador de onda completa aprovecha ambos semiciclos de la señal AC. Puede implementarse con transformador con derivación central o con un puente de cuatro diodos.

En el puente rectificador, dos diodos conducen durante el semiciclo positivo y otros dos conducen durante el semiciclo negativo. La corriente por la carga siempre mantiene el mismo sentido.

### Características

- Usa cuatro diodos en configuración de puente.
- Aprovecha ambos semiciclos de la señal AC.
- La salida tiene menor rizado que la media onda.
- La frecuencia del rizado es el doble de la frecuencia de entrada.
- Es ampliamente usado en fuentes de alimentación.

---

## 8. Caída de voltaje en los diodos

En un diodo real existe una caída de voltaje en conducción. Para diodos de silicio, esta caída suele estar alrededor de 0.7 V.

En un puente rectificador, durante cada semiciclo conducen dos diodos, por lo que la caída total aproximada es:

```text
Vcaída ≈ 2 × 0.7 V
Vcaída ≈ 1.4 V
```

Esto significa que el voltaje de salida será menor que el voltaje pico ideal.

---

## 9. Filtro capacitivo

Después de la rectificación, la señal de salida todavía no es una DC completamente constante. Presenta pulsos o variaciones periódicas. A estas variaciones se les llama rizado.

El capacitor de filtrado se conecta en paralelo con la carga. Su función es cargarse cuando el voltaje rectificado sube y descargarse lentamente cuando el voltaje baja, reduciendo la variación de la salida.

### Efecto de aumentar la capacitancia

Cuando se aumenta el valor del capacitor:

- La salida se vuelve más suave.
- Disminuye el rizado.
- Aumenta el voltaje DC promedio.
- Puede aumentar la corriente inicial de carga del capacitor.

---

## 10. Rizado

El rizado es la variación residual de voltaje que queda después de rectificar y filtrar una señal AC.

Una fuente DC real no siempre es perfectamente constante. El objetivo del filtro es reducir el rizado a un nivel aceptable para el circuito que se desea alimentar.

En onda completa, el rizado es menor que en media onda porque el capacitor se recarga con mayor frecuencia.

---

## 11. Aplicaciones reales

Los rectificadores se utilizan en:

- Cargadores de baterías.
- Fuentes de alimentación DC.
- Variadores de frecuencia.
- UPS.
- Equipos de audio.
- Controladores industriales.
- Fuentes de computadores.
- Sistemas de automatización.
- Electrónica de potencia.

---

## 12. Ejemplo guiado

Una fuente AC de 6 V RMS alimenta un puente rectificador. El voltaje pico de entrada es:

```text
VP = 6 V × 1.414
VP ≈ 8.48 V
```

Como en el puente conducen dos diodos, se resta aproximadamente 1.4 V:

```text
Vsalida pico ≈ 8.48 V - 1.4 V
Vsalida pico ≈ 7.08 V
```

Por lo tanto, la salida máxima real del puente será menor que el valor pico ideal de la señal AC.

---

## 13. Errores comunes

- Confundir voltaje RMS con voltaje pico.
- Olvidar la caída de voltaje en los diodos.
- Conectar incorrectamente el puente rectificador.
- Invertir la polaridad del capacitor.
- Usar un capacitor con voltaje nominal insuficiente.
- Pensar que una señal rectificada ya es una DC perfectamente constante.

---

## 14. Preguntas orientadoras para clase

1. ¿Por qué se necesita rectificar una señal AC?
2. ¿Cuál es la diferencia entre media onda y onda completa?
3. ¿Por qué el puente rectificador usa cuatro diodos?
4. ¿Por qué el voltaje de salida es menor que el voltaje pico ideal?
5. ¿Qué función cumple el capacitor en paralelo con la carga?
6. ¿Qué es el rizado y por qué debe reducirse?

---

## 15. Trabajo independiente

Antes de la siguiente clase, el estudiante debe:

1. Simular un rectificador de media onda.
2. Simular un puente rectificador.
3. Comparar las formas de onda de entrada y salida.
4. Repetir la simulación agregando un capacitor de filtrado.
5. Registrar capturas para usarlas en el informe del laboratorio A01.

---

## 16. Relación con laboratorio

Este marco teórico sirve como base para la **Guía A01 – Diodos, rectificación y regulación con Zener**, especialmente en las secciones de rectificador de media onda, rectificador de onda completa y filtro capacitivo.
