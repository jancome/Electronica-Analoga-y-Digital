# Fortalecimiento teórico semanal

**Asignatura:** Electrónica Analógica y Digital  
**Periodo:** 2026-2  
**Propósito:** servir como guía complementaria para fortalecer cada semana de clase con bibliografía base, recursos abiertos, conceptos clave, actividades de refuerzo y conexión con el proyecto ABP.

> Este documento no reemplaza los `marco-teorico.md` de cada semana. Funciona como mapa de apoyo para preparar la clase, orientar lecturas y seleccionar ejercicios. Los libros completos protegidos por derechos de autor no deben subirse al repositorio; se pueden citar como bibliografía y orientar al estudiante a consultarlos por biblioteca o medios institucionales.

---

## Enfoque ABP del curso

La asignatura se trabajará bajo la estrategia **ABP – Aprendizaje Basado en Proyectos**. La teoría, los laboratorios y las evaluaciones deben conectarse con una problemática común:

> **Gestión, uso eficiente y aprovechamiento responsable de la energía eléctrica en Barranquilla y la región Caribe.**

Los **preproyectos ABP** conectan el fortalecimiento teórico con decisiones reales del proyecto y evitan que los temas se estudien como contenidos aislados.

| Corte | Enfoque del proyecto | Entrega asociada |
|---|---|---|
| Corte 1 | Etapa común AC/DC en baja tensión: rectificación, filtrado, regulación básica, protección e indicador de estado. | Preproyecto ABP 1 |
| Corte 2 | Variables digitales, tabla de verdad, expresión booleana, simplificación y lógica con compuertas. | Preproyecto ABP 2 |
| Corte 3 | Integración, muestra, correcciones, informe, video y sustentación. | Proyecto ABP final |

Los preproyectos sirven para recibir retroalimentación. El proyecto final no será una suma automática de esas entregas; en el cierre se evaluará la integración final, el funcionamiento, las correcciones y la sustentación individual.

---

## Fuentes base utilizadas

### Bibliografía del curso y guías

- Boylestad, R. L., & Nashelsky, L. **Electrónica: Teoría de circuitos y dispositivos electrónicos**. Pearson.
- Floyd, T. L. **Dispositivos electrónicos** y/o **Fundamentos de sistemas digitales**, según disponibilidad institucional.
- Hayt, W. H., Kemmerly, J. E., & Durbin, S. M. **Análisis de circuitos en ingeniería**. McGraw-Hill.
- Guías de laboratorio del curso: diodos, BJT, FET/MOSFET, compuertas lógicas, álgebra booleana, De Morgan, XOR, sumadores, comparadores, codificadores, decodificadores, multiplexores y demultiplexores.

### Recursos abiertos sugeridos

- All About Circuits – Direct Current: fundamentos, Ley de Ohm, series/paralelo, divisores, Kirchhoff, medición y señales de instrumentación.
- All About Circuits – Semiconductors: unión PN, diodos, rectificadores, Zener, BJT, JFET y MOSFET.
- All About Circuits – Digital Circuits: sistemas de numeración, aritmética binaria, compuertas, álgebra booleana, Karnaugh, lógica combinacional y secuencial.
- OpenStax University Physics Vol. 2: apoyo conceptual para electricidad, corriente, resistencia, circuitos DC y leyes de Kirchhoff.
- Hojas de datos de fabricantes: Texas Instruments, ON Semiconductor, STMicroelectronics, Vishay, Diodes Incorporated u otros fabricantes reconocidos.

---

# Semana 01 – Presentación, diagnóstico y problemática ABP

## Enfoque de fortalecimiento

La primera semana debe presentar la asignatura, aplicar un diagnóstico corto y explicar la problemática ABP. El estudiante debe entender que el proyecto inicia desde el primer corte y que cada laboratorio aportará una pieza de la solución.

## Conceptos que deben quedar claros

- Propósito de la asignatura.
- Problemática general: uso eficiente y responsable de la energía eléctrica.
- Organización de grupos de 3 estudiantes.
- Ley de Ohm, potencia, nodos, mallas y medición básica.
- Diferencia entre señal analógica y señal digital.
- Relación entre circuitos básicos y el futuro proyecto ABP.

## Actividad sugerida

Aplicar un diagnóstico corto con ejercicios de circuitos básicos. Después, presentar posibles problemas del contexto: ahorro energético, control de cargas, aviso de baja tensión, monitoreo básico o apoyo a sistemas de riego de baja potencia.

## Conexión ABP

Cada grupo debe empezar a pensar qué situación real quiere abordar dentro de la línea del curso.

---

# Semana 02 – Diodos, rectificación básica y Zener

## Enfoque de fortalecimiento

Esta semana inicia la etapa común AC/DC del proyecto. Los diodos no se estudian solo como componentes, sino como la base para rectificar, proteger, indicar estado y construir una fuente DC básica en baja tensión.

## Conceptos que deben quedar claros

- Unión PN.
- Polarización directa e inversa.
- Rectificación de media onda y puente rectificador.
- Filtrado capacitivo introductorio.
- LED y resistencia limitadora.
- Regulación básica con Zener.
- Medición de voltaje antes y después de rectificar, filtrar y regular.

## Actividad sugerida

Simular o montar una fuente AC de baja tensión con rectificación, filtro, LED indicador y regulación básica. Registrar voltajes y explicar qué cambia en cada etapa.

## Conexión ABP

Avance del **Preproyecto ABP 1**: inicio de la etapa común AC/DC segura.

---

# Semana 03 – BJT y control de cargas

## Enfoque de fortalecimiento

El BJT debe presentarse como un dispositivo que permite controlar una carga usando una señal pequeña. Esta idea conecta directamente con soluciones de ahorro, alarmas o control básico dentro del proyecto.

## Conceptos que deben quedar claros

- BJT NPN/PNP.
- Base, colector y emisor.
- Corriente de base y corriente de colector.
- Corte, activa y saturación.
- BJT como interruptor.
- Resistencia de base.
- Diodo de protección para cargas inductivas.

## Actividad sugerida

Diseñar un circuito que active un LED, relé o carga DC de baja potencia mediante BJT. Calcular resistencia de base y explicar cuándo el transistor está en corte o saturación.

## Conexión ABP

Avance del **Preproyecto ABP 1**: control de una salida o indicador usando la etapa AC/DC del proyecto.

---

# Semana 04 – FET/MOSFET y cierre de etapa analógica

## Enfoque de fortalecimiento

El MOSFET debe compararse con el BJT como alternativa de control de carga. La semana cierra la etapa analógica del proyecto y prepara el Preproyecto ABP 1.

## Conceptos que deben quedar claros

- MOSFET canal N.
- Gate, Drain y Source.
- VGS, VDS e ID.
- MOSFET como interruptor.
- Resistencia de compuerta y pull-down.
- Control de carga de baja potencia.
- Comparación BJT vs MOSFET.

## Actividad sugerida

Resolver un caso de control de carga primero con BJT y luego con MOSFET. Comparar ventajas, cálculos y cuidados de conexión.

## Conexión ABP

Preparación del **Preproyecto ABP 1**: etapa AC/DC, indicador, protección y posible control de carga.

---

# Semana 05 – Parcial 1 y cierre del Corte 1

## Enfoque de fortalecimiento

La semana no introduce tema nuevo. Se usa para repasar la unidad analógica, aplicar el Parcial 1 y revisar las correcciones derivadas del Preproyecto ABP 1 ya entregado.

## Conceptos que deben integrarse

- Ley de Ohm y potencia.
- Medición de voltaje y corriente.
- Diodos, LED, Zener y rectificación.
- Filtrado básico.
- BJT y MOSFET como interruptores.
- Seguridad en baja tensión.

## Producto ABP

El Preproyecto ABP 1 debe incluir problema seleccionado, justificación, diagrama de bloques preliminar, etapa común AC/DC, cálculos, simulación o mediciones iniciales y correcciones pendientes.

---

# Semana 06 – Sistemas numéricos y variables del proyecto

## Enfoque de fortalecimiento

Iniciar la unidad digital mostrando que las condiciones del proyecto pueden representarse con estados 0 y 1. Los sistemas numéricos ayudan a codificar datos, estados, conteos o niveles.

## Conceptos que deben quedar claros

- Bit, nibble, byte y palabra.
- Decimal, binario, hexadecimal y BCD.
- Conversión entre sistemas.
- Diferencia entre número binario y código.
- Variables digitales de entrada y salida.

## Actividad sugerida

Cada grupo debe proponer posibles variables digitales para su proyecto: consumo alto/bajo, nivel suficiente/bajo, horario permitido/no permitido, sensor activo/inactivo o energía disponible/no disponible.

## Conexión ABP

Inicio del **Preproyecto ABP 2**: definición de entradas y salidas digitales.

---

# Semana 07 – Aritmética binaria

## Enfoque de fortalecimiento

La aritmética binaria permite representar conteos, comparaciones y estados dentro de un sistema digital. No debe verse solo como operación manual, sino como base de circuitos aritméticos.

## Conceptos que deben quedar claros

- Suma binaria.
- Acarreo.
- Resta binaria.
- Complemento a 1 y complemento a 2.
- Números con signo.
- Overflow.
- Relación entre operación binaria y circuito sumador.

## Actividad sugerida

Resolver operaciones binarias asociadas a conteo de eventos, niveles o estados. Relacionar los resultados con posibles indicadores o decisiones del proyecto.

## Conexión ABP

Apoyo al Preproyecto ABP 2 cuando el proyecto requiera conteo, códigos o comparación de valores.

---

# Semana 08 – Compuertas lógicas

## Enfoque de fortalecimiento

Esta semana debe llevar al estudiante del 0/1 abstracto al circuito físico. Las compuertas se usarán como primera implementación de una decisión digital del proyecto.

## Conceptos que deben quedar claros

- AND, OR, NOT.
- NAND, NOR.
- XOR, XNOR.
- Tabla de verdad.
- Expresión booleana.
- VCC y GND en circuitos integrados.
- Niveles alto y bajo como rangos de voltaje.

## Actividad sugerida

Tomar dos o tres variables del proyecto y construir una tabla de verdad que active una salida: alarma, indicador, habilitación o bloqueo de carga.

## Conexión ABP

Avance del **Preproyecto ABP 2**: primer circuito lógico con compuertas.

---

# Semana 09 – Álgebra booleana, De Morgan y Karnaugh

## Enfoque de fortalecimiento

La simplificación se presenta como una forma de reducir compuertas, conexiones, consumo, costo y probabilidad de falla. Debe aplicarse a la lógica real propuesta por cada grupo.

## Conceptos que deben quedar claros

- Variable booleana.
- Suma lógica, producto lógico y complemento.
- Leyes básicas del álgebra de Boole.
- Teoremas de De Morgan.
- Minterminos.
- Introducción a mapas de Karnaugh.
- Equivalencia entre tabla, expresión y circuito.

## Actividad sugerida

Cada grupo debe tomar su tabla de verdad, escribir una expresión booleana inicial, simplificarla y comparar el circuito antes y después.

## Conexión ABP

Preparación del **Preproyecto ABP 2**: lógica digital simplificada y justificada.

---

# Semana 10 – Receso institucional

## Enfoque de fortalecimiento

No se debe cargar contenido nuevo. La semana puede usarse para revisar la lógica del proyecto, corregir tablas de verdad, mejorar expresiones booleanas y preparar dudas.

## Actividad autónoma sugerida

- Repasar conversiones numéricas.
- Rehacer una tabla de verdad.
- Simplificar expresiones booleanas.
- Revisar el circuito lógico del proyecto.
- Preparar el Preproyecto ABP 2.

---

# Semana 11 – Parcial 2 y cierre del Corte 2

## Enfoque de fortalecimiento

La semana no introduce tema nuevo. Se usa para cerrar la unidad digital, aplicar el Parcial 2 y revisar las correcciones del Preproyecto ABP 2 entregado antes del receso.

## Conceptos que deben integrarse

- Sistemas numéricos.
- Aritmética binaria.
- Compuertas lógicas.
- Tablas de verdad.
- Álgebra booleana.
- De Morgan.
- Karnaugh introductorio.

## Producto ABP

El Preproyecto ABP 2 debe incluir variables de entrada y salida, tabla de verdad, expresión booleana, simplificación, circuito con compuertas y relación clara con la problemática seleccionada.

---

# Semana 12 – XOR, sumadores y restadores

## Enfoque de fortalecimiento

Entrar al tercer corte mostrando aplicaciones reales de la lógica combinacional. XOR debe entenderse como detección de diferencia y como base de suma binaria.

## Conceptos que deben quedar claros

- XOR y XNOR.
- Medio sumador.
- Sumador completo.
- Acarreo.
- Restador básico.
- Relación entre aritmética binaria y circuito lógico.

## Actividad sugerida

Revisar si el proyecto requiere detectar diferencia, sumar estados, contar eventos o comparar entradas. Integrar la función cuando tenga sentido técnico.

## Conexión ABP

Inicio de la integración final del proyecto ABP.

---

# Semana 13 – Comparadores y paridad

## Enfoque de fortalecimiento

Los comparadores permiten tomar decisiones: mayor, menor, igual o condición válida. La paridad ayuda a detectar errores simples.

## Conceptos que deben quedar claros

- Comparador de igualdad.
- Comparador de magnitud.
- Salidas A>B, A=B y A<B.
- Paridad par e impar.
- Generador y verificador de paridad.

## Actividad sugerida

Aplicar un comparador o una lógica de validación al proyecto: por ejemplo, activar aviso por nivel bajo, condición fuera de rango o combinación incorrecta.

## Conexión ABP

Avance funcional para la solución final.

---

# Semana 14 – Codificadores, decodificadores y primera revisión

## Enfoque de fortalecimiento

Relacionar estos circuitos con sistemas visibles: displays, alarmas, teclados, selección de salidas, sensores y automatización. Esta semana sirve como primera revisión formal del prototipo.

## Conceptos que deben quedar claros

- Codificador.
- Codificador con prioridad.
- Decodificador.
- BCD.
- Display de 7 segmentos.
- Entradas y salidas activas en bajo.

## Actividad sugerida

Analizar cómo mostrar estados del proyecto en LED o display. Revisar el diagrama completo del sistema y detectar correcciones antes de la muestra.

## Conexión ABP

Primera revisión formal del prototipo.

---

# Semana 15 – Multiplexores, demultiplexores y muestra de proyectos

## Enfoque de fortalecimiento

Presentar el MUX como selector de datos y el DEMUX como distribuidor. Relacionarlos con selección de señales, sensores, modos de operación y expansión de entradas/salidas.

## Conceptos que deben quedar claros

- Multiplexor.
- Demultiplexor.
- Líneas de selección.
- Entrada de habilitación.
- Selector de datos.
- Distribuidor de datos.
- Implementación de funciones lógicas con MUX.

## Actividad sugerida

Realizar la muestra de proyectos. Cada grupo debe explicar su problemática, etapa AC/DC, lógica digital, estado del prototipo, fallas detectadas y ajustes pendientes.

## Conexión ABP

Muestra de proyectos y retroalimentación para la entrega final.

---

# Semana 16 – Flip-flops, contadores y ajustes finales

## Enfoque de fortalecimiento

Cerrar el curso técnico mostrando la diferencia entre lógica combinacional y lógica secuencial. La semana también se usa para ajustes finales del proyecto.

## Conceptos que deben quedar claros

- Lógica combinacional vs lógica secuencial.
- Latch.
- Flip-flop SR, D, JK y T.
- Reloj.
- Estado almacenado.
- Contador asíncrono y síncrono.
- Aplicaciones en conteo, temporización y automatización.

## Actividad sugerida

Simular un contador básico o revisar si el proyecto requiere memoria, conteo o temporización. Ajustar el prototipo, preparar evidencias, video e informe.

## Conexión ABP

Correcciones finales antes de la sustentación.

---

# Semana 17 – Proyecto ABP final y cierre

## Enfoque de fortalecimiento

La última semana evalúa integración. El estudiante debe demostrar funcionamiento, comprensión, correcciones realizadas y capacidad de explicar decisiones técnicas.

## Conceptos que deben integrarse

- Problemática seleccionada.
- Etapa AC/DC corregida si fue necesario.
- Señales de entrada.
- Lógica digital de decisión.
- Aplicaciones combinacionales o secuenciales.
- Etapa de salida o control de carga.
- Simulación, montaje, mediciones y evidencia de funcionamiento.
- Fallas encontradas y correcciones.

## Actividad sugerida

Cada grupo debe presentar:

1. Problema que resuelve el circuito.
2. Diagrama de bloques.
3. Circuito o simulación.
4. Tabla de verdad, cálculos o lógica utilizada.
5. Evidencia de funcionamiento.
6. Mejoras realizadas frente a los preproyectos.
7. Explicación individual por integrante.
8. Conclusiones y mejoras posibles.

## Criterio de cierre

El proyecto final se califica por el estado final integrado. Los preproyectos anteriores sirvieron para avanzar y corregir, pero no se suman automáticamente como partes del proyecto final.

---

## Recomendación metodológica general

Cada semana debe cerrar con cuatro preguntas:

1. ¿Qué concepto nuevo aprendimos?
2. ¿Qué medición, cálculo o tabla permite comprobarlo?
3. ¿Cómo se conecta este tema con una aplicación real de ingeniería eléctrica?
4. ¿Qué parte del proyecto ABP ayuda a mejorar o construir?

Esta estructura ayuda a que la clase no sea solo teoría, sino una ruta hacia análisis, simulación, montaje, medición, corrección y sustentación técnica.
