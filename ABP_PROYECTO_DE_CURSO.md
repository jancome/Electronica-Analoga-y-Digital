# Estrategia ABP – Proyecto de curso

## Sentido de la estrategia

La asignatura trabajará bajo una estrategia de **ABP – Aprendizaje Basado en Proyectos**. Esto significa que el proyecto no será una actividad aislada del final del semestre, sino un proceso que inicia desde el primer corte y se va construyendo por etapas.

La intención es que el estudiante tome mayor conciencia de su aprendizaje, relacione la teoría con una necesidad real, trabaje de forma autónoma y entienda que cada práctica de laboratorio aporta una parte del proyecto.

## Problemática general del curso

La problemática general estará orientada a la **gestión, uso eficiente y aprovechamiento responsable de la energía eléctrica en el contexto de Barranquilla y la región Caribe**.

A partir de esta línea común, cada grupo podrá enfocar su proyecto hacia una situación particular, por ejemplo:

- Monitoreo básico de consumo eléctrico.
- Control eficiente de cargas.
- Alertas por condiciones eléctricas anormales.
- Automatización de bajo consumo.
- Apoyo a sistemas de riego o bombeo de baja potencia.
- Indicadores de nivel, estado o disponibilidad de energía.
- Soluciones sencillas para ahorro energético en vivienda, comercio, campo o institución.
- Sistemas de aviso frente a baja tensión, sobrecarga o uso innecesario de cargas.

El enfoque no es hacer proyectos “por cumplir”, sino proponer una solución técnica sencilla, medible y sustentable desde los temas de la asignatura.

## Pregunta orientadora

> **¿Cómo diseñar y validar, mediante electrónica analógica y digital de baja tensión, una solución de bajo costo que permita medir, alertar o controlar una condición relacionada con el uso eficiente de energía o agua en Barranquilla y la región Caribe?**

Cada grupo debe convertir esta pregunta general en una pregunta específica, identificar un usuario o contexto y definir criterios medibles de éxito.

## Requisitos comunes

- Trabajo seguro en baja tensión.
- Problema sustentado con evidencia y fuentes confiables.
- Requisitos funcionales y restricciones explícitas.
- Etapa analógica común AC/DC.
- Decisión mediante lógica digital.
- Una salida observable o medible.
- Lista de componentes y costo estimado.
- Simulación previa al montaje.
- Bitácora de decisiones, fallas, pruebas y correcciones.
- Roles rotativos para los tres integrantes.

## Condición común para todos los grupos

Todos los grupos deberán partir de una primera etapa común:

> **Conversión de corriente alterna a corriente directa, con filtrado, regulación básica e indicadores de protección o estado.**

Esta etapa se trabajará durante el primer corte y servirá como base de alimentación o referencia para el resto del proyecto.

Por seguridad, esta etapa debe desarrollarse con **baja tensión AC proveniente de transformador, fuente de laboratorio o simulador**. No se permite conectar montajes de protoboard directamente a la red eléctrica de 120 V.

## Preproyectos y proyecto final

El proyecto se organiza mediante las siguientes entregas:

| Corte | Entrega | Sentido |
|---|---|---|
| Corte 1 | Preproyecto ABP 1 | Problema seleccionado, justificación y etapa común AC/DC. |
| Corte 2 | Preproyecto ABP 2 | Variables digitales, tabla de verdad, simplificación y lógica con compuertas. |
| Corte 3 | Proyecto ABP final | Parte final, integración completa, muestra, informe, video y sustentación. |

Los preproyectos no deben entenderse como partes acumulativas que se suman automáticamente al final. Funcionan como cortes de avance, retroalimentación y mejora. En el proyecto final se evaluará la solución corregida e integrada.

Si un grupo tuvo dificultades en el primer o segundo preproyecto, tendrá oportunidad de corregirlas. Lo importante es que en la entrega final se evidencie que la etapa fue ajustada, integrada y comprendida por los integrantes.

Los retos, entregables y rúbricas se publican desde el inicio de cada corte. Las revisiones formativas permiten recibir crítica, justificar decisiones y mejorar antes de la entrega calificada.

## Investigación por corte

Cada corte incorpora una fuente nueva en un idioma diferente del español, consultada mediante una base de datos de la universidad. El grupo registra la referencia IEEE, un resumen propio, un glosario técnico bilingüe, la evidencia de consulta y la decisión de diseño respaldada por la fuente.

## Etapas por corte

| Corte | Enfoque ABP | Producto esperado |
|---|---|---|
| Corte 1 | Etapa común analógica: conversión AC/DC, rectificación, filtrado, regulación, protección básica e indicador de estado. | Fuente DC básica simulada o montada, cálculos, mediciones y justificación de protecciones. |
| Corte 2 | Etapa digital de decisión: uso de compuertas, tablas de verdad y simplificación para responder a una condición del problema. | Lógica combinacional que active una salida, alarma, indicador o decisión según variables de entrada. |
| Corte 3 | Integración y aplicación: uso de circuitos combinacionales o secuenciales para completar la solución. | Prototipo funcional, simulación, informe, video, muestra de proyecto y sustentación individual. |

## Etapa 1 – Corte 1: base común AC/DC

Todos los grupos desarrollarán una fuente DC básica segura que incluya, según disponibilidad y criterio del docente:

1. Entrada AC de baja tensión.
2. Rectificación con diodos o puente rectificador.
3. Filtro capacitivo.
4. Regulación básica con Zener o regulador.
5. LED indicador de estado.
6. Protección o criterio de seguridad: fusible en baja tensión, resistencia limitadora, diodo de protección, revisión de polaridad o elemento equivalente.
7. Medición de voltajes antes y después de rectificar, filtrar y regular.

Esta etapa será común para todos porque fortalece la unidad analógica y permite que todos tengan una base de alimentación o referencia para el proyecto.

## Etapa 2 – Corte 2: lógica digital según la problemática

A partir del segundo corte, cada grupo comenzará a diferenciar su solución. La etapa digital debe incluir:

1. Definición de variables de entrada.
2. Tabla de verdad.
3. Expresión booleana.
4. Simplificación con álgebra booleana o mapas de Karnaugh.
5. Implementación con compuertas lógicas.
6. Salida útil: LED, alarma, habilitación de carga, indicador de estado o señal de control.

Ejemplos de variables:

- Nivel de batería bajo / normal.
- Consumo permitido / consumo alto.
- Horario permitido / horario no permitido.
- Nivel de agua bajo / suficiente.
- Temperatura alta / normal.
- Sensor activo / sensor inactivo.
- Modo manual / modo automático.

## Etapa 3 – Corte 3: integración y muestra

En el tercer corte cada grupo integrará la etapa analógica común con su lógica digital y una aplicación funcional. La solución puede incluir:

- Comparadores.
- Sumadores o contadores.
- Codificadores o decodificadores.
- Display de 7 segmentos.
- Multiplexores o demultiplexores.
- Flip-flops o contadores básicos.
- Indicadores visuales o sonoros.
- Control de una carga de baja potencia mediante BJT o MOSFET.

La muestra de proyectos se programará preferiblemente entre las **semanas 14 y 15**. Después de la muestra, los grupos podrán realizar ajustes, mejorar la presentación y preparar la sustentación final.

La muestra funciona como producto público y revisión formativa. Cada grupo recibe comentarios de otros estudiantes, del docente y, cuando sea posible, de un invitado del programa o del área. Las decisiones tomadas después de la muestra se registran en la bitácora.

## Ruta de trabajo sugerida

| Semana | Avance ABP |
|---:|---|
| 01 | Presentación de la problemática general y conformación de grupos. |
| 02 | Inicio de etapa común AC/DC: diodos, rectificación, filtrado y Zener. |
| 03 | Revisión de control de carga con BJT. |
| 04 | Revisión de control de carga con FET/MOSFET y cierre de la etapa analógica. |
| 04 | Entrega del Preproyecto ABP 1 después de la revisión formativa. |
| 05 | Corte 1: repaso y parcial, sin tema nuevo. |
| 06 | Definición de variables digitales del problema. |
| 07 | Operaciones y representación de datos si el proyecto lo requiere. |
| 08 | Implementación inicial con compuertas. |
| 09 | Simplificación de la lógica y entrega del Preproyecto ABP 2. |
| 10 | Receso y revisión autónoma. |
| 11 | Cierre del Corte 2 y parcial. |
| 12 | Integración de XOR, sumadores o restadores si aplica. |
| 13 | Comparadores, paridad o indicadores de decisión. |
| 14 | Codificadores, decodificadores o display. Primera revisión formal del prototipo. |
| 15 | Multiplexores, demultiplexores y muestra de proyectos. |
| 16 | Ajustes finales, pruebas, evidencias y preparación de sustentación. |
| 17 | Cierre, sustentación individual y entrega final. |

## Entregables mínimos por corte

### Corte 1 – Preproyecto ABP 1

- Problema seleccionado por el grupo dentro de la línea general del curso.
- Justificación de la necesidad.
- Diagrama de bloques preliminar.
- Etapa común AC/DC simulada o montada.
- Cálculos de rectificación, filtrado, regulación y resistencia de LED.
- Evidencias de medición o simulación.

### Corte 2 – Preproyecto ABP 2

- Variables de entrada y salida.
- Tabla de verdad.
- Expresión booleana.
- Simplificación.
- Circuito con compuertas.
- Simulación o evidencia de funcionamiento.
- Relación clara entre la lógica digital y la problemática seleccionada.
- Consulta técnica o académica en otro idioma, cuando aplique.

### Corte 3 – Proyecto ABP final

- Integración de etapas corregidas.
- Prototipo funcional o simulación completa.
- Informe técnico.
- Video corto de funcionamiento.
- Lista de materiales y costos.
- Roles y aportes de cada integrante.
- Muestra de proyecto.
- Sustentación individual.

## Criterio de seguridad

Los proyectos deben manejar baja tensión en protoboard y laboratorio. Cualquier trabajo asociado a red eléctrica, cargas de potencia o elementos de riesgo debe realizarse solo como simulación, diagrama, maqueta de baja tensión o bajo autorización directa del docente.
