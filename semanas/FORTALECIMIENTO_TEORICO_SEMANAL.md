# Fortalecimiento teórico semanal

**Asignatura:** Electrónica Analógica y Digital  
**Periodo:** 2026-2

## Propósito

Este documento complementa los marcos teóricos semanales con conceptos clave, aplicaciones, actividades de refuerzo y relación con las fases del **ABPr – Aprendizaje Basado en Proyectos**.

> Este archivo es una vista panorámica. La versión desarrollada y canónica de cada tema está en el `marco-teorico.md` de su semana, donde se incluyen ecuaciones, ejemplo guiado, práctica, diagnóstico, preguntas, trabajo independiente, referencias por página y ruta de capítulos para profundizar. Consulte el [índice semanal](README.md) para el mapa bibliográfico completo.

## Situación problema

> **¿Cómo diseñar e implementar un sistema electrónico analógico-digital, de bajo costo y bajo consumo, que permita supervisar, indicar o controlar una variable relacionada con el uso eficiente de la energía o de los recursos en Barranquilla y la región Caribe?**

## Fases del ABPr

| Fase | Corte | Producto |
|---|---|---|
| Fase 1 | Corte 1 | Formulación, arquitectura, etapa analógica y simulación inicial. |
| Fase 2 | Corte 2 | Diseño lógico, simulación funcional y montaje en protoboard. |
| Fase 3 | Corte 3 | Integración física, maqueta, informe, video y sustentación. |

Los preproyectos permiten retroalimentación y corrección. El proyecto final se evalúa por su versión definitiva.

## Fuentes base

- Boylestad y Nashelsky, *Electrónica: teoría de circuitos y dispositivos electrónicos*.
- Floyd, *Dispositivos electrónicos* y *Fundamentos de sistemas digitales*.
- Hayt, Kemmerly y Durbin, *Análisis de circuitos en ingeniería*.
- All About Circuits: Direct Current, Semiconductors y Digital Circuits.
- OpenStax University Physics Vol. 2.
- Hojas de datos de fabricantes reconocidos.

---

# Semana 01 – Inicio, diagnóstico y situación problema

## Conceptos

- Propósito de la asignatura.
- Diferencia entre ABPr y ABP.
- Ley de Ohm, potencia, nodos, mallas y medición básica.
- Señales analógicas y digitales.

## Actividad

Aplicar diagnóstico y analizar necesidades del contexto relacionadas con energía, agua, riego, iluminación o control de cargas.

## Conexión ABPr

Socializar la situación problema, conformar grupos de 3 estudiantes y seleccionar posibles aplicaciones.

---

# Semana 02 – Diodos, rectificación y Zener

## Conceptos

- Unión PN.
- Polarización directa e inversa.
- Media onda y puente rectificador.
- Filtro capacitivo.
- LED y resistencia limitadora.
- Regulación con Zener.

## Actividad

Simular una fuente AC/DC en baja tensión y registrar voltajes por etapa.

## Conexión ABPr

Inicio de la etapa analógica y de la simulación del Preproyecto ABPr 1.

---

# Semana 03 – BJT y control de cargas

## Conceptos

- BJT NPN y PNP.
- Corte, activa y saturación.
- Resistencia de base.
- Diodo de protección.

## Actividad

Diseñar y probar el control de un LED, relé o carga DC de baja potencia.

## Conexión ABPr

Incorporar una etapa de salida o accionamiento a la arquitectura del proyecto.

---

# Semana 04 – MOSFET y cierre analógico

## Conceptos

- MOSFET canal N.
- Gate, Drain y Source.
- Resistencia de compuerta y pull-down.
- Comparación BJT–MOSFET.

## Actividad

Comparar dos alternativas de control de carga y justificar la selección.

## Conexión ABPr

Cerrar cálculos, simulación inicial y arquitectura de la Fase 1.

---

# Semana 05 – Cierre de Fase 1

## Integración

- Rectificación, filtrado y regulación.
- Indicadores y protección.
- BJT o MOSFET.
- Seguridad en baja tensión.

## Producto

**Preproyecto ABPr 1:** problema, objetivos, diagrama de bloques, cálculos, simulación inicial, materiales y roles.

---

# Semana 06 – Sistemas numéricos y variables

## Conceptos

- Decimal, binario, hexadecimal y BCD.
- Bit, nibble y byte.
- Diferencia entre número y código.
- Variables digitales de entrada y salida.

## Actividad

Definir estados binarios del proyecto: alto/bajo, activo/inactivo, suficiente/insuficiente o permitido/bloqueado.

## Conexión ABPr

Inicio del diseño lógico de la Fase 2.

---

# Semana 07 – Aritmética binaria

## Conceptos

- Suma y resta binaria.
- Acarreo.
- Complemento a 1 y a 2.
- Overflow.

## Actividad

Resolver operaciones relacionadas con conteos, niveles o códigos de la aplicación.

## Conexión ABPr

Determinar si el proyecto requiere conteo, comparación o representación numérica.

---

# Semana 08 – Compuertas lógicas

## Conceptos

- AND, OR, NOT, NAND, NOR, XOR y XNOR.
- Tabla de verdad.
- Expresión booleana.
- VCC, GND y niveles lógicos.

## Actividad

Construir el primer circuito de decisión y comprobarlo en protoboard.

## Conexión ABPr

Primer avance físico obligatorio de la Fase 2.

---

# Semana 09 – Álgebra, De Morgan y Karnaugh

## Conceptos

- Leyes del álgebra de Boole.
- Teoremas de De Morgan.
- Minterminos.
- Mapas de Karnaugh.

## Actividad

Simplificar la función real del proyecto, simularla y ajustar el montaje en protoboard.

## Conexión ABPr

Preparación de la simulación y el protoboard funcional del Preproyecto ABPr 2.

---

# Semana 10 – Receso institucional

No se introduce contenido nuevo.

## Trabajo autónomo

- Revisar tabla de verdad.
- Corregir simplificación.
- Comparar simulación y protoboard.
- Preparar evidencias y dudas.

---

# Semana 11 – Cierre de Fase 2

## Integración

- Sistemas numéricos.
- Aritmética binaria.
- Compuertas.
- Tablas de verdad.
- Álgebra, De Morgan y Karnaugh.

## Producto

**Preproyecto ABPr 2:** simulación funcional, montaje en protoboard, mediciones, evidencias y plan de corrección.

---

# Semana 12 – XOR, sumadores y restadores

## Conceptos

- XOR y XNOR.
- Medio sumador y sumador completo.
- Restador.

## Actividad

Analizar si la aplicación requiere detección de diferencia, suma, resta o generación de acarreo.

## Conexión ABPr

Inicio de la integración física definitiva.

---

# Semana 13 – Comparadores y paridad

## Conceptos

- Comparadores de igualdad y magnitud.
- Salidas mayor, igual y menor.
- Paridad par e impar.

## Actividad

Incorporar una decisión, validación o alarma útil al proyecto.

## Conexión ABPr

Avance funcional del prototipo físico.

---

# Semana 14 – Codificadores, decodificadores y display

## Conceptos

- Codificadores y prioridad.
- Decodificadores.
- BCD y display de 7 segmentos.
- Entradas o salidas activas en bajo.

## Actividad

Diseñar una forma clara de visualizar estados o datos.

## Conexión ABPr

Primera revisión física del prototipo y de la distribución de la maqueta.

---

# Semana 15 – Multiplexores, demultiplexores y muestra

## Conceptos

- Selector y distribuidor de datos.
- Líneas de selección.
- Habilitación.

## Actividad

Revisar selección de señales y presentar un prototipo preliminar.

## Conexión ABPr

Muestra de proyectos y revisión de la maqueta o base de presentación.

---

# Semana 16 – Flip-flops, contadores y ajustes

## Conceptos

- Lógica combinacional y secuencial.
- Flip-flops SR, D, JK y T.
- Reloj y estado almacenado.
- Contadores.

## Actividad

Aplicar memoria o conteo cuando sea pertinente y ejecutar pruebas finales.

## Conexión ABPr

Corregir el prototipo, terminar maqueta, informe y video.

---

# Semana 17 – Proyecto final ABPr

## Evidencias

- Prototipo físico funcional.
- Maqueta o base organizada.
- Simulación actualizada.
- Mediciones y pruebas.
- Informe y video.
- Registro de correcciones.
- Sustentación grupal e individual.

## Criterio de cierre

La valoración se centra en el estado definitivo del proyecto, la calidad de la integración y el dominio técnico demostrado.

## Preguntas de cierre semanal

1. ¿Qué concepto se aprendió?
2. ¿Cómo se comprobó mediante cálculo, simulación, protoboard o medición?
3. ¿Qué aporta al proyecto?
4. ¿Qué debe corregirse antes de la siguiente fase?
