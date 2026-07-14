# Marco teórico – Semana 03

# Semiconductores, unión PN y diodo como elemento de circuito

## 1. Tema de la semana

Fundamentos de los materiales semiconductores, dopaje tipo P y tipo N, formación de la unión PN y comportamiento básico del diodo semiconductor dentro de un circuito eléctrico real.

![Unión PN y polarización del diodo](../../recursos/imagenes/analogica/diodo-union-pn-polarizacion.svg)

---

## 2. Objetivo de aprendizaje

Comprender el funcionamiento básico de los materiales semiconductores y de la unión PN como fundamento del diodo, diferenciando el comportamiento del dispositivo en polarización directa e inversa, y aplicando Ley de Ohm y leyes de Kirchhoff para analizar circuitos simples con diodos.

---

## 3. Contexto e importancia del tema

La mayoría de los dispositivos electrónicos modernos se construyen a partir de materiales semiconductores. Diodos, transistores, circuitos integrados, microcontroladores, sensores, rectificadores, reguladores y dispositivos de potencia dependen del comportamiento controlado de los semiconductores.

Para un estudiante de ingeniería eléctrica, comprender la unión PN es clave porque permite entender cómo se comportan los rectificadores, fuentes de alimentación, protecciones electrónicas, controladores, variadores y sistemas de conversión de energía.

Esta semana marca el paso de los circuitos puramente resistivos hacia los circuitos electrónicos. En circuitos resistivos, la relación entre voltaje y corriente suele ser lineal. En cambio, el diodo introduce un comportamiento no lineal: puede bloquear corriente en un sentido y conducir en el otro a partir de cierta condición de polarización.

---

## 4. Relación con los fundamentos previos

Antes de analizar diodos, el estudiante debe recuperar tres ideas de circuitos básicos:

### Ley de Ohm

Permite calcular la corriente cuando se conoce el voltaje aplicado a una resistencia.

```text
I = V / R
```

### Ley de voltajes de Kirchhoff

En una malla, la suma de voltajes debe cerrar el balance. En un circuito con fuente, resistencia y diodo:

```text
VS = VR + VD
```

### Potencia eléctrica

Permite verificar si un componente trabaja dentro de sus límites.

```text
P = V × I
```

Estas tres herramientas serán necesarias para calcular corrientes en diodos, resistencias limitadoras, LED y diodos Zener.

---

## 5. Conceptos fundamentales

### 5.1 Material conductor

Un conductor permite el paso de corriente eléctrica con facilidad porque tiene electrones libres disponibles para moverse. Ejemplos: cobre, aluminio y plata.

### 5.2 Material aislante

Un aislante presenta alta oposición al paso de corriente eléctrica. Sus electrones están fuertemente ligados al átomo. Ejemplos: plástico, vidrio, cerámica y caucho.

### 5.3 Material semiconductor

Un semiconductor tiene una conductividad intermedia entre la de un conductor y un aislante. Su comportamiento puede modificarse mediante temperatura, luz, campos eléctricos o adición controlada de impurezas.

Los semiconductores más utilizados son:

- Silicio.
- Germanio.
- Arseniuro de galio.

En electrónica general, el silicio es el material más común.

---

## 6. Dopaje semiconductor

El dopaje consiste en agregar impurezas controladas a un semiconductor puro para modificar su comportamiento eléctrico.

### 6.1 Semiconductor tipo N

Se obtiene al agregar impurezas con cinco electrones de valencia. Esto aumenta la cantidad de electrones libres.

En un material tipo N, los portadores mayoritarios son los **electrones**.

### 6.2 Semiconductor tipo P

Se obtiene al agregar impurezas con tres electrones de valencia. Esto genera huecos, que pueden comportarse como portadores positivos.

En un material tipo P, los portadores mayoritarios son los **huecos**.

---

## 7. Unión PN

Una unión PN se forma al unir una región tipo P con una región tipo N. Al ponerse en contacto, algunos electrones de la región N se recombinan con huecos de la región P cerca de la frontera entre ambas zonas.

Como resultado se forma una zona llamada **región de agotamiento**, en la cual hay pocos portadores libres disponibles para conducir.

La unión PN es la base del diodo semiconductor.

---

## 8. Diodo semiconductor

El diodo es un dispositivo de dos terminales:

- **Ánodo:** terminal que debe estar a mayor potencial para conducción directa.
- **Cátodo:** terminal normalmente identificado físicamente con una banda.

Su característica principal es permitir el paso de corriente principalmente en un sentido y bloquearla en el sentido contrario, dentro de ciertos límites.

---

## 9. Polarización directa

Un diodo está en polarización directa cuando el ánodo se conecta al positivo de la fuente y el cátodo al negativo.

En esta condición, si el voltaje aplicado supera aproximadamente el voltaje de conducción del diodo, la unión PN permite el paso de corriente.

Para un diodo de silicio, el voltaje directo típico está alrededor de:

```text
VD ≈ 0.7 V
```

En polarización directa, el diodo puede aproximarse como un interruptor cerrado con caída de voltaje interna. Esta aproximación no es exacta, pero es útil para cálculos iniciales de laboratorio.

---

## 10. Polarización inversa

Un diodo está en polarización inversa cuando el cátodo se conecta al positivo de la fuente y el ánodo al negativo.

En esta condición, la región de agotamiento se ensancha y el diodo bloquea el paso de corriente. Solo puede circular una corriente de fuga muy pequeña.

Si el voltaje inverso supera el límite máximo del componente, puede presentarse ruptura y daño del diodo, excepto en dispositivos diseñados para operar en esa región, como el diodo Zener.

---

## 11. Modelos básicos del diodo

Para resolver problemas introductorios se pueden usar tres modelos:

### Modelo ideal

El diodo se considera como:

- Corto circuito cuando conduce.
- Circuito abierto cuando bloquea.

### Modelo práctico

El diodo se considera como un interruptor con caída fija aproximada.

Para silicio:

```text
VD ≈ 0.7 V
```

### Modelo real

Considera la curva característica del diodo, resistencia dinámica, corriente de fuga y variación con temperatura.

En el curso se inicia con el modelo práctico y luego se compara con mediciones reales.

---

## 12. Análisis de circuito con diodo y resistencia

Si se conecta una fuente DC, una resistencia y un diodo en serie, la resistencia limita la corriente del circuito.

Aplicando Kirchhoff:

```text
VS = VR + VD
```

Entonces:

```text
VR = VS - VD
```

Y por Ley de Ohm:

```text
I = VR / R
```

Este procedimiento será usado para analizar diodos rectificadores, LED y reguladores Zener.

---

## 13. Curva característica del diodo

La curva característica relaciona el voltaje aplicado al diodo con la corriente que circula por él.

En términos generales:

- En directa, la corriente aumenta rápidamente después del voltaje umbral.
- En inversa, la corriente es muy pequeña hasta llegar a la ruptura.
- En un diodo real, siempre existe una caída de voltaje en conducción.

La curva no es lineal, por eso un diodo no se comporta como una resistencia común.

---

## 14. Hoja de datos del diodo

Antes de usar un diodo real, se deben revisar datos como:

- Corriente directa máxima.
- Voltaje inverso máximo.
- Caída de voltaje directa.
- Potencia máxima.
- Encapsulado.
- Temperatura de operación.

En el laboratorio se recomienda consultar la hoja de datos del diodo utilizado, por ejemplo el 1N4007 o equivalente.

---

## 15. Aplicaciones reales

Los diodos semiconductores se utilizan en:

- Rectificadores AC/DC.
- Protección contra inversión de polaridad.
- Protección contra transitorios.
- Indicadores LED.
- Fuentes de alimentación.
- Cargadores.
- Reguladores con Zener.
- Sistemas de control industrial.
- Electrónica automotriz.

---

## 16. Ejemplo guiado

Se conecta un diodo de silicio en serie con una resistencia de 1 kΩ a una fuente de 5 V. Si el diodo está en polarización directa y se asume una caída de 0.7 V, la corriente aproximada será:

```text
VS = VR + VD
VR = VS - VD
VR = 5 V - 0.7 V
VR = 4.3 V
```

Luego:

```text
I = VR / R
I = 4.3 V / 1000 Ω
I = 4.3 mA
```

Esto significa que el diodo conduce y la resistencia limita la corriente.

---

## 17. Ejemplo comparativo: diodo invertido

Si el mismo diodo se invierte, queda en polarización inversa. En ese caso, para una fuente pequeña como 5 V, se aproxima como circuito abierto.

Por tanto:

```text
I ≈ 0 A
VR ≈ 0 V
VD ≈ VS
```

Esto permite comprobar en laboratorio la diferencia entre polarización directa e inversa.

---

## 18. Errores comunes

- Confundir ánodo y cátodo.
- Conectar un LED sin resistencia limitadora.
- Pensar que el diodo ideal y el diodo real se comportan igual.
- No aplicar Kirchhoff para calcular la corriente.
- Olvidar que la resistencia limita la corriente del diodo.
- No revisar la hoja de datos del componente.
- Exceder la corriente máxima del diodo.
- Aplicar polarización inversa superior al valor permitido.

---

## 19. Preguntas orientadoras para clase

1. ¿Por qué un semiconductor no es completamente conductor ni completamente aislante?
2. ¿Qué diferencia existe entre material tipo P y tipo N?
3. ¿Qué ocurre en la región de agotamiento?
4. ¿Por qué el diodo conduce principalmente en un solo sentido?
5. ¿Qué diferencia existe entre polarización directa e inversa?
6. ¿Por qué es necesaria una resistencia en serie con un LED?
7. ¿Cómo se aplica Kirchhoff en un circuito con fuente, resistencia y diodo?
8. ¿Qué diferencia hay entre diodo ideal, práctico y real?

---

## 20. Trabajo independiente

Antes de la siguiente clase, el estudiante debe:

1. Consultar la hoja de datos del diodo 1N4007.
2. Identificar ánodo, cátodo, corriente máxima y voltaje inverso máximo.
3. Simular un circuito simple con fuente DC, resistencia y diodo.
4. Resolver al menos tres ejercicios aplicando `VS = VR + VD`.
5. Preparar dudas para el inicio del laboratorio A01.

---

## 21. Relación con laboratorio

Este marco teórico sirve como base para la **Guía A01 – Diodos, rectificación y regulación con Zener**, especialmente en las secciones de polarización directa, polarización inversa e identificación de terminales.

El estudiante debe llegar al laboratorio entendiendo que el diodo no se analiza aislado, sino dentro de una malla donde existen una fuente, una resistencia, una corriente y una potencia que deben verificarse.