# Marco teórico – Semana 01

# Presentación del curso, diagnóstico y fundamentos previos de circuitos

## 1. Tema de la semana

Presentación general de la asignatura **Electrónica Analógica y Digital**, diagnóstico inicial e introducción conceptual a la diferencia entre sistemas analógicos, sistemas digitales y sistemas mixtos.

Además, se realiza una revisión diagnóstica de los fundamentos de circuitos eléctricos que el estudiante necesita para comprender la unidad analógica del primer corte.

---

## 2. Objetivo de aprendizaje

Reconocer el propósito de la asignatura, diferenciar los conceptos de electrónica analógica, electrónica digital y sistemas mixtos, e identificar el nivel de dominio del estudiante en fundamentos de circuitos eléctricos como Ley de Ohm, leyes de Kirchhoff, circuitos serie/paralelo, potencia y medición.

---

## 3. Contexto e importancia del tema

La electrónica está presente en la mayoría de los sistemas modernos de ingeniería: fuentes de alimentación, sensores, sistemas de control, protecciones eléctricas, automatización, comunicaciones, instrumentación, variadores de velocidad, iluminación LED, equipos industriales y dispositivos de consumo.

Sin embargo, antes de estudiar dispositivos electrónicos como diodos, transistores o compuertas lógicas, es necesario recordar que todos ellos forman parte de circuitos eléctricos. Por esta razón, la primera semana no debe limitarse a presentar el curso, sino que también debe verificar si el estudiante domina las bases mínimas para analizar circuitos.

---

## 4. Conocimientos previos esperados

El estudiante debería llegar al curso con dominio básico de:

- Voltaje, corriente y resistencia.
- Ley de Ohm.
- Potencia eléctrica.
- Resistencias en serie y paralelo.
- Divisor de voltaje.
- Ley de corrientes de Kirchhoff.
- Ley de voltajes de Kirchhoff.
- Concepto de nodo y malla.
- Uso básico del multímetro.
- Diferencia entre señales DC y AC.

Estos temas se evalúan en el archivo:

- [Diagnóstico inicial – Fundamentos de circuitos](diagnostico-inicial-circuitos.md)

---

## 5. Ley de Ohm como punto de partida

La Ley de Ohm relaciona voltaje, corriente y resistencia:

```text
V = I × R
```

De esta relación se derivan:

```text
I = V / R
R = V / I
```

Esta ley será utilizada durante todo el primer corte. Por ejemplo:

- Para calcular la corriente de un LED.
- Para determinar la resistencia limitadora de un diodo.
- Para estimar corrientes en transistores.
- Para interpretar mediciones de voltaje y corriente.
- Para calcular divisores de voltaje usados en polarización.

---

## 6. Potencia eléctrica

La potencia indica la energía eléctrica consumida o disipada por unidad de tiempo. En circuitos electrónicos es importante porque los componentes pueden dañarse si se supera su potencia máxima.

Formas comunes de cálculo:

```text
P = V × I
P = I² × R
P = V² / R
```

En electrónica analógica, este concepto será necesario para analizar resistencias, LED, diodos Zener, transistores y etapas de potencia.

---

## 7. Leyes de Kirchhoff

### Ley de corrientes de Kirchhoff

En un nodo, la suma de corrientes que entran debe ser igual a la suma de corrientes que salen.

Esta idea será importante para analizar divisores, ramas paralelas, corrientes de carga y etapas con transistores.

### Ley de voltajes de Kirchhoff

En una malla cerrada, la suma de elevaciones y caídas de voltaje debe ser igual a cero.

Esta ley será clave para comprender por qué en un circuito con fuente, resistencia y diodo se cumple:

```text
VS = VR + VD
```

Por tanto, si se conoce el voltaje de la fuente y la caída del diodo, puede calcularse el voltaje en la resistencia y luego la corriente.

---

## 8. Circuitos serie, paralelo y divisor de voltaje

### Circuito serie

En un circuito serie la corriente es la misma por todos los elementos. La resistencia equivalente se obtiene sumando las resistencias.

```text
RT = R1 + R2 + R3 + ...
```

### Circuito paralelo

En un circuito paralelo el voltaje es el mismo en cada rama. La corriente total se divide entre las ramas.

```text
1/RT = 1/R1 + 1/R2 + 1/R3 + ...
```

### Divisor de voltaje

El divisor de voltaje permite obtener una fracción del voltaje de entrada usando resistencias en serie. Este concepto se usa en sensores, polarización de transistores, referencias de voltaje y acondicionamiento de señales.

---

## 9. Electrónica analógica, digital y sistemas mixtos

En términos generales, la electrónica puede estudiarse desde dos enfoques complementarios:

- **Electrónica analógica:** trabaja con señales continuas que pueden tomar muchos valores dentro de un rango.
- **Electrónica digital:** trabaja con señales discretas, normalmente representadas mediante dos estados: 0 y 1.

En la práctica, muchos sistemas reales combinan ambas. Por ejemplo, un sensor puede entregar una señal analógica, un microcontrolador puede procesarla digitalmente y una etapa de potencia puede activar una carga eléctrica.

---

## 10. Conceptos fundamentales

### Electrónica

La electrónica estudia el comportamiento, control y aplicación de dispositivos y circuitos que permiten procesar señales eléctricas o controlar energía mediante componentes como diodos, transistores, circuitos integrados, sensores y controladores.

### Señal eléctrica

Una señal eléctrica es una variación de voltaje o corriente que transporta información o representa una magnitud física.

### Sistema analógico

Un sistema analógico utiliza señales continuas. Esto significa que la señal puede tomar muchos valores dentro de un rango.

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

---

## 11. Relación con la ingeniería eléctrica

Para un ingeniero eléctrico, la electrónica analógica y digital permite comprender y diseñar sistemas de control, protección, medición y automatización. Algunos ejemplos son:

- Control de motores eléctricos.
- Fuentes de alimentación DC.
- Automatización de portones, bombas y sistemas industriales.
- Sistemas de iluminación LED.
- Sensores conectados a PLC o microcontroladores.
- Circuitos de protección y acondicionamiento de señal.
- Sistemas de medición de voltaje, corriente y potencia.

---

## 12. Ejemplo guiado

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

Este ejemplo muestra que un sistema real puede combinar electrónica analógica, digital y potencia. También muestra por qué se necesitan conceptos previos: Ley de Ohm para limitar corriente, Kirchhoff para analizar la malla y potencia para seleccionar componentes seguros.

---

## 13. Errores comunes o puntos de cuidado

- Pensar que lo analógico y lo digital son áreas totalmente separadas.
- Creer que una señal digital no tiene voltaje real.
- Confundir GND con ausencia total de voltaje.
- Medir corriente con el multímetro en paralelo.
- Conectar un LED sin resistencia limitadora.
- Confundir circuito abierto con corto circuito.
- Aplicar fórmulas sin revisar unidades.
- Ignorar la potencia máxima de resistencias y semiconductores.

---

## 14. Preguntas orientadoras para la clase

1. ¿Por qué la electrónica necesita una base de circuitos eléctricos?
2. ¿Qué relación existe entre la Ley de Ohm y un LED con resistencia limitadora?
3. ¿Por qué una malla debe cumplir la ley de voltajes de Kirchhoff?
4. ¿Qué diferencia hay entre medir voltaje y medir corriente?
5. ¿Dónde vemos electrónica analógica en sistemas eléctricos reales?
6. ¿Dónde vemos electrónica digital en sistemas eléctricos reales?
7. ¿Por qué un sistema moderno normalmente combina ambas?

---

## 15. Trabajo previo o posterior del estudiante

Para la siguiente clase, el estudiante debe:

1. Resolver el diagnóstico inicial de circuitos.
2. Identificar tres sistemas reales y clasificarlos como analógico, digital o mixto.
3. Repasar Ley de Ohm, circuitos serie/paralelo y leyes de Kirchhoff.
4. Revisar qué conceptos del diagnóstico se le dificultaron más.

---

## 16. Conexión con la siguiente semana

La próxima semana se estudiarán con más detalle las señales analógicas y digitales, los niveles de voltaje, las magnitudes eléctricas básicas, la medición y la forma en que una señal puede representar información dentro de un circuito electrónico. Los fundamentos de Ley de Ohm, Kirchhoff y potencia serán usados para conectar las señales con circuitos reales.