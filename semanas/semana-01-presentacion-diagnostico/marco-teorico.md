# Marco teórico – Semana 01

# Presentación del curso, diagnóstico y situación problema ABPr

## Metas de aprendizaje verificables

- Modelar un circuito resistivo con polaridades, Ohm, Kirchhoff y potencia, y predecir sus mediciones.
- Diferenciar señal analógica, nivel lógico y etapa de potencia dentro de una arquitectura mixta.
- Formular una necesidad regional en términos de variable, rango, entrada, decisión y salida segura.

## 1. Propósito de la semana

Presentar la asignatura, socializar la situación problema institucional, conformar los grupos de trabajo y aplicar un diagnóstico breve de los fundamentos eléctricos necesarios para iniciar la unidad analógica.

La primera semana no busca desarrollar un bloque extenso de teoría. Su función es establecer el punto de partida del grupo y mostrar desde el primer día cómo la electrónica analógica y digital se integrará en un proyecto físico desarrollado por fases.

## 2. Resultado de aprendizaje

Al finalizar la semana, el estudiante estará en capacidad de:

- Diferenciar sistemas analógicos, digitales y mixtos.
- Reconocer la relación entre medición, control y uso eficiente de energía o recursos.
- Aplicar conceptos básicos de voltaje, corriente, resistencia y potencia.
- Identificar nodos, mallas y conexiones serie/paralelo.
- Comprender la estructura del proyecto ABPr y los productos esperados en cada corte.
- Proponer una primera aplicación asociada a la situación problema del curso.

## 3. Situación problema del curso

La situación problema deberá socializarse durante la primera clase:

> **¿Cómo diseñar e implementar un sistema electrónico analógico-digital, de bajo costo y bajo consumo, que permita supervisar, indicar o controlar una variable relacionada con el uso eficiente de la energía o de los recursos en Barranquilla y la región Caribe?**

Cada grupo podrá enfocar su proyecto hacia una aplicación específica, por ejemplo:

- Control eficiente de iluminación o cargas de baja potencia.
- Indicadores de nivel de agua.
- Aviso de baja tensión o condición eléctrica anormal.
- Apoyo a sistemas de riego o bombeo.
- Monitoreo básico de temperatura, luz o estado eléctrico.
- Alarmas por condiciones no permitidas.

## 4. Estrategia ABPr

La asignatura utiliza **ABPr – Aprendizaje Basado en Proyectos** porque conduce a un producto práctico.

| Fase | Corte | Producto principal |
|---|---|---|
| Fase 1 | Corte 1 | Formulación, arquitectura, etapa analógica y simulación inicial. |
| Fase 2 | Corte 2 | Lógica digital, simulación funcional y montaje en protoboard. |
| Fase 3 | Corte 3 | Prototipo físico definitivo con maqueta o base de presentación. |

Los grupos serán de **3 estudiantes**. Cada integrante deberá conocer el sistema completo y evidenciar su aporte.

## 5. Fundamentos eléctricos para el diagnóstico

### Voltaje

Es la diferencia de potencial entre dos nodos. Siempre se mide en paralelo y respecto a una referencia.

### Corriente

Es el flujo de carga eléctrica. Se mide colocando el instrumento en serie con la rama de interés.

### Resistencia

Limita la corriente y permite establecer divisores de voltaje y condiciones de operación.

### Ley de Ohm

```text
V = I × R
I = V / R
R = V / I
```

### Potencia

```text
P = V × I
P = I² × R
P = V² / R
```

La potencia es un criterio de selección y seguridad: una resistencia, diodo o transistor puede dañarse si supera su capacidad de disipación.

## 6. Leyes de Kirchhoff

### Ley de corrientes

En un nodo, la suma de las corrientes que entran es igual a la suma de las corrientes que salen.

### Ley de voltajes

En una trayectoria cerrada, la suma algebraica de voltajes es cero.

Estas leyes se usarán posteriormente para analizar diodos, rectificadores, BJT y MOSFET.

## 7. Sistemas analógicos, digitales y mixtos

- **Analógico:** trabaja con señales continuas que pueden tomar diferentes valores dentro de un rango.
- **Digital:** interpreta rangos eléctricos como estados discretos, normalmente 0 y 1.
- **Mixto:** combina medición analógica, decisión lógica y una etapa de salida o potencia.

Un proyecto del curso puede recibir una condición física, acondicionarla, interpretarla mediante lógica digital y activar un indicador o carga.

## 8. Ejemplo motivador

Un sistema de iluminación eficiente puede contener:

1. Un sensor de luz que produce una señal analógica.
2. Una condición lógica que identifica si el lugar está oscuro y ocupado.
3. Un transistor que activa una lámpara de baja potencia.
4. Un indicador del estado del sistema.

Este ejemplo conecta fundamentos eléctricos, electrónica analógica, lógica digital y control de cargas.

## 9. Actividad de clase

Cada grupo deberá:

1. Identificar una necesidad relacionada con energía o recursos.
2. Formular una primera idea de solución.
3. Identificar una posible variable de entrada y una salida.
4. Representar el sistema mediante un diagrama de bloques preliminar.
5. Indicar qué parte podría ser analógica y cuál digital.

La idea todavía puede cambiar después de recibir orientación del docente.

## 10. Evidencia de la semana

- Diagnóstico inicial corto.
- Grupo de 3 estudiantes conformado.
- Primera propuesta de aplicación.
- Diagrama de bloques preliminar.
- Registro de dudas o conocimientos que deben reforzarse.

## 11. Errores y puntos de cuidado

- Pensar que la solución debe estar completamente definida en la primera clase.
- Confundir una línea temática con una situación problema concreta.
- Proponer proyectos que no puedan construirse con los contenidos del curso.
- Ignorar límites de voltaje, corriente y potencia.
- Medir corriente con el multímetro conectado en paralelo.
- Conectar montajes estudiantiles directamente a la red de 120 V.

## 12. Trabajo independiente

- Corregir los ejercicios del diagnóstico.
- Revisar Ley de Ohm, potencia, nodos y mallas.
- Consultar una fuente técnica sobre la aplicación seleccionada.
- Mejorar el diagrama de bloques preliminar.
- Identificar materiales o sensores que podrían representar la variable escogida.

## 13. Conexión con la Semana 02

La siguiente semana inicia la construcción conceptual de la etapa común del proyecto: semiconductores, diodos, rectificación, filtrado y regulación básica con Zener. Todo montaje deberá trabajar con **AC de baja tensión**, fuente de laboratorio o simulador.

## 14. Profundización: del fenómeno físico al sistema electrónico

Un sistema de ingeniería no comienza por escoger componentes, sino por traducir una necesidad en variables medibles. La cadena mínima es `fenómeno → sensor → acondicionamiento → decisión → actuación`. En ella, una magnitud continua —iluminancia, nivel de agua, temperatura o tensión— puede conservarse como señal analógica o convertirse en estados digitales mediante un umbral. Esa frontera deberá quedar explícita en el diagrama de bloques del grupo.

El análisis eléctrico usa una convención consistente: se define una referencia de potencial, se asignan polaridades y sentidos de corriente, y solo después se escriben ecuaciones. Las relaciones fundamentales son:

\[
V=IR,\qquad P=VI=I^2R=\frac{V^2}{R}
\]

\[
\sum I_{\text{entra}}=\sum I_{\text{sale}},\qquad \sum V_k=0
\]

Kirchhoff no constituye una fórmula aislada: expresa conservación de carga en un nodo y conservación de energía en una trayectoria cerrada. Si un resultado contradice esas conservaciones, la causa suele ser una polaridad, una unidad o una conexión mal definida.

### Ejemplo guiado adaptado

Una fuente aislada de `9 V` alimenta un LED mediante `470 Ω`. Si se adopta una caída práctica de `2 V` en el LED:

1. La resistencia recibe `V_R=9-2=7 V`.
2. La corriente estimada es `I=7/470=14,9 mA`.
3. La potencia en la resistencia es `P_R=7×14,9 mA≈0,104 W`; una resistencia de `1/4 W` ofrece margen.
4. La potencia suministrada es aproximadamente `0,134 W` y se reparte entre LED y resistencia.

El cálculo debe acompañarse con una predicción de mediciones: `9 V` entre los terminales de la fuente, cerca de `2 V` en el LED y cerca de `7 V` en la resistencia. Esta tabla de valores esperados será luego una herramienta de diagnóstico.

### Procedimiento de exploración y medición

1. Dibujar el circuito y marcar referencia, polaridades y nodos.
2. Calcular valores esperados antes de montar.
3. Construir únicamente con la fuente apagada.
4. Medir continuidad sin energía; después medir tensión con el instrumento en paralelo.
5. Para corriente, abrir la rama e insertar el amperímetro en serie; nunca conectar el amperímetro directamente entre los bornes de la fuente.
6. Comparar cálculo, simulación y medición mediante error porcentual: `|medido-calculado|/|calculado|×100 %`.

### Diagnóstico razonado

Si el LED no enciende, no se cambia todo el montaje. Se comprueba en orden: tensión de la fuente, polaridad del LED, continuidad, valor de la resistencia y caída de tensión en cada elemento. Una fuente correcta con `9 V` sobre el LED y casi `0 V` sobre la resistencia sugiere circuito abierto; casi `0 V` sobre el LED puede indicar inversión, corto o medición referida a un nodo incorrecto.

## 15. Preguntas orientadoras ampliadas

- ¿Qué variable física resuelve el proyecto y en qué unidad se mide?
- ¿Qué valores representan operación normal, advertencia y alarma?
- ¿Dónde termina el dominio analógico y comienza la decisión digital?
- ¿Qué corriente y potencia exige la carga, y puede entregarlas directamente el bloque lógico?
- ¿Qué medición distinguiría una falla de alimentación de una falla de carga?

## 16. Trabajo independiente verificable

Cada grupo elaborará una hoja con: situación específica, variable y rango, diagrama de bloques, circuito resistivo de comprobación, cálculos con unidades, tabla de mediciones esperadas, tres fallas probables y una regla de seguridad. Debe incluir al menos una fuente técnica o académica y registrar las dudas surgidas en el diagnóstico.

## 17. Referencias de estudio

- Boylestad y Nashelsky, *Electrónica: teoría de circuitos y dispositivos electrónicos*, 10.ª ed., prefacio y cap. 1, sec. 1.1, p. 1: enfoque de dispositivos dentro de sistemas, aplicaciones, simulación y localización de fallas.
- Floyd, *Fundamentos de sistemas digitales*, 9.ª ed., cap. 1, sec. 1.2, pp. 6–13: niveles lógicos, impulsos y representación digital.
- La Ley de Ohm, Kirchhoff y potencia se consideran prerrequisitos que Boylestad aplica, pero no desarrolla como núcleo del cap. 1; por ello se complementan con apuntes de análisis de circuitos y prácticas de medición.

## 18. Ruta de profundización recomendada

1. **Lectura prioritaria:** Boylestad, prefacio y cap. 1, sec. 1.1, p. 1, para estudiar el dispositivo dentro de un sistema y el enfoque de medición/simulación.
2. **Puente analógico–digital:** Floyd, cap. 1, secs. 1.1–1.2, especialmente pp. 6–13, para profundizar en magnitudes, niveles, impulsos y bloques digitales.
3. **Ampliación necesaria:** un texto de análisis de circuitos para Ohm, Kirchhoff, serie/paralelo y potencia; estos son prerrequisitos, no el propósito central de Boylestad.
