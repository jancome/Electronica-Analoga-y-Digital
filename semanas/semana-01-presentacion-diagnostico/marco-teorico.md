# Marco teórico – Semana 01

# Presentación del curso, diagnóstico y situación problema ABPr

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