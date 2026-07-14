# Marco teórico – Semana 03

# Semiconductores y unión PN

## 1. Tema de la semana

Fundamentos de los materiales semiconductores, dopaje tipo P y tipo N, formación de la unión PN y comportamiento básico del diodo semiconductor.

![Unión PN y polarización del diodo](../../recursos/imagenes/analogica/diodo-union-pn-polarizacion.svg)

---

## 2. Objetivo de aprendizaje

Comprender el funcionamiento básico de los materiales semiconductores y de la unión PN como fundamento del diodo, diferenciando el comportamiento del dispositivo en polarización directa e inversa.

---

## 3. Contexto e importancia del tema

La mayoría de los dispositivos electrónicos modernos se construyen a partir de materiales semiconductores. Diodos, transistores, circuitos integrados, microcontroladores, sensores, rectificadores, reguladores y dispositivos de potencia dependen del comportamiento controlado de los semiconductores.

Para un estudiante de ingeniería eléctrica, comprender la unión PN es clave porque permite entender cómo se comportan los rectificadores, fuentes de alimentación, protecciones electrónicas, controladores, variadores y sistemas de conversión de energía.

---

## 4. Conceptos fundamentales

### 4.1 Material conductor

Un conductor permite el paso de corriente eléctrica con facilidad porque tiene electrones libres disponibles para moverse. Ejemplos: cobre, aluminio y plata.

### 4.2 Material aislante

Un aislante presenta alta oposición al paso de corriente eléctrica. Sus electrones están fuertemente ligados al átomo. Ejemplos: plástico, vidrio, cerámica y caucho.

### 4.3 Material semiconductor

Un semiconductor tiene una conductividad intermedia entre la de un conductor y un aislante. Su comportamiento puede modificarse mediante temperatura, luz, campos eléctricos o adición controlada de impurezas.

Los semiconductores más utilizados son:

- Silicio.
- Germanio.
- Arseniuro de galio.

En electrónica general, el silicio es el material más común.

---

## 5. Dopaje semiconductor

El dopaje consiste en agregar impurezas controladas a un semiconductor puro para modificar su comportamiento eléctrico.

### 5.1 Semiconductor tipo N

Se obtiene al agregar impurezas con cinco electrones de valencia. Esto aumenta la cantidad de electrones libres.

En un material tipo N, los portadores mayoritarios son los **electrones**.

### 5.2 Semiconductor tipo P

Se obtiene al agregar impurezas con tres electrones de valencia. Esto genera huecos, que pueden comportarse como portadores positivos.

En un material tipo P, los portadores mayoritarios son los **huecos**.

---

## 6. Unión PN

Una unión PN se forma al unir una región tipo P con una región tipo N. Al ponerse en contacto, algunos electrones de la región N se recombinan con huecos de la región P cerca de la frontera entre ambas zonas.

Como resultado se forma una zona llamada **región de agotamiento**, en la cual hay pocos portadores libres disponibles para conducir.

La unión PN es la base del diodo semiconductor.

---

## 7. Diodo semiconductor

El diodo es un dispositivo de dos terminales:

- **Ánodo:** terminal positivo del diodo.
- **Cátodo:** terminal negativo del diodo, normalmente identificado físicamente con una banda.

Su característica principal es permitir el paso de corriente en un sentido y bloquearla en el sentido contrario, dentro de ciertos límites.

---

## 8. Polarización directa

Un diodo está en polarización directa cuando el ánodo se conecta al positivo de la fuente y el cátodo al negativo.

En esta condición, si el voltaje aplicado supera aproximadamente el voltaje de conducción del diodo, la unión PN permite el paso de corriente.

Para un diodo de silicio, el voltaje directo típico está alrededor de:

```text
VD ≈ 0.7 V
```

En polarización directa, el diodo se comporta aproximadamente como un interruptor cerrado, aunque con una caída de voltaje interna.

---

## 9. Polarización inversa

Un diodo está en polarización inversa cuando el cátodo se conecta al positivo de la fuente y el ánodo al negativo.

En esta condición, la región de agotamiento se ensancha y el diodo bloquea el paso de corriente. Solo puede circular una corriente de fuga muy pequeña.

Si el voltaje inverso supera el límite máximo del componente, puede presentarse ruptura y daño del diodo, excepto en dispositivos diseñados para operar en esa región, como el diodo Zener.

---

## 10. Curva característica del diodo

La curva característica relaciona el voltaje aplicado al diodo con la corriente que circula por él.

En términos generales:

- En directa, la corriente aumenta rápidamente después del voltaje umbral.
- En inversa, la corriente es muy pequeña hasta llegar a la ruptura.
- En un diodo real, siempre existe una caída de voltaje en conducción.

---

## 11. Aplicaciones reales

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

## 12. Ejemplo guiado

Se conecta un diodo de silicio en serie con una resistencia de 1 kΩ a una fuente de 5 V. Si el diodo está en polarización directa y se asume una caída de 0.7 V, la corriente aproximada será:

```text
I = (VS - VD) / R
I = (5 V - 0.7 V) / 1000 Ω
I = 4.3 mA
```

Esto significa que el diodo conduce y la resistencia limita la corriente.

---

## 13. Errores comunes

- Confundir ánodo y cátodo.
- Conectar un LED sin resistencia limitadora.
- Pensar que el diodo ideal y el diodo real se comportan igual.
- No revisar la hoja de datos del componente.
- Exceder la corriente máxima del diodo.
- Aplicar polarización inversa superior al valor permitido.

---

## 14. Preguntas orientadoras para clase

1. ¿Por qué un semiconductor no es completamente conductor ni completamente aislante?
2. ¿Qué diferencia existe entre material tipo P y tipo N?
3. ¿Qué ocurre en la región de agotamiento?
4. ¿Por qué el diodo conduce en un solo sentido?
5. ¿Qué diferencia existe entre polarización directa e inversa?
6. ¿Por qué es necesaria una resistencia en serie con un LED?

---

## 15. Trabajo independiente

Antes de la siguiente clase, el estudiante debe:

1. Consultar la hoja de datos del diodo 1N4007.
2. Identificar ánodo, cátodo, corriente máxima y voltaje inverso máximo.
3. Simular un circuito simple con fuente DC, resistencia y diodo.
4. Preparar dudas para el inicio del laboratorio A01.

---

## 16. Relación con laboratorio

Este marco teórico sirve como base para la **Guía A01 – Diodos, rectificación y regulación con Zener**, especialmente en las secciones de polarización directa, polarización inversa e identificación de terminales.
