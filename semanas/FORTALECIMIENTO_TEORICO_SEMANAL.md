# Fortalecimiento teórico semanal

**Asignatura:** Electrónica Analógica y Digital  
**Periodo:** 2026-2  
**Propósito:** servir como guía complementaria para fortalecer cada semana de clase con bibliografía base, recursos abiertos, conceptos clave, actividades de refuerzo y conexión entre temas.

> Este documento no reemplaza los `marco-teorico.md` de cada semana. Funciona como mapa de apoyo para preparar la clase, orientar lecturas y seleccionar ejercicios. Los libros completos protegidos por derechos de autor no deben subirse al repositorio; se pueden citar como bibliografía y orientar al estudiante a consultarlos por biblioteca o medios institucionales.

---

## Fuentes base utilizadas

### Bibliografía del curso y guías

- Boylestad, R. L., & Nashelsky, L. **Electrónica: Teoría de circuitos y dispositivos electrónicos**. Pearson.
- Floyd, T. L. **Dispositivos electrónicos** y/o **Fundamentos de sistemas digitales**, según disponibilidad institucional.
- Hayt, W. H., Kemmerly, J. E., & Durbin, S. M. **Análisis de circuitos en ingeniería**. McGraw-Hill.
- Guías de laboratorio del curso: compuertas lógicas, álgebra booleana, De Morgan, XOR, sumadores, comparadores, codificadores, decodificadores, multiplexores y demultiplexores.

### Recursos abiertos sugeridos

- All About Circuits – Direct Current: fundamentos, Ley de Ohm, series/paralelo, divisores, Kirchhoff, medición y señales de instrumentación.
- All About Circuits – Semiconductors: unión PN, diodos, rectificadores, Zener, BJT, JFET y MOSFET.
- All About Circuits – Digital Circuits: sistemas de numeración, aritmética binaria, compuertas, álgebra booleana, Karnaugh, lógica combinacional y secuencial.
- OpenStax University Physics Vol. 2: apoyo conceptual para electricidad, corriente, resistencia, circuitos DC y leyes de Kirchhoff.
- Hojas de datos de fabricantes: Texas Instruments, ON Semiconductor, STMicroelectronics, Vishay, Diodes Incorporated u otros fabricantes reconocidos.

---

# Semana 01 – Presentación, diagnóstico y fundamentos previos

## Enfoque de fortalecimiento

La primera semana debe permitir reconocer el punto de partida del grupo. Antes de entrar a electrónica analógica, el estudiante debe demostrar manejo básico de circuitos eléctricos. Por eso el diagnóstico debe incluir Ley de Ohm, potencia, circuitos serie/paralelo, divisores de voltaje, mallas, nodos, leyes de Kirchhoff y uso básico del multímetro.

## Conceptos que deben quedar claros

- Voltaje como diferencia de potencial entre dos nodos.
- Corriente como flujo de carga en un circuito cerrado.
- Resistencia como oposición al paso de corriente.
- Potencia eléctrica como variable de diseño térmico y de seguridad.
- Ley de Ohm.
- Ley de voltajes de Kirchhoff: suma de voltajes en una malla.
- Ley de corrientes de Kirchhoff: balance de corrientes en un nodo.
- Diferencia entre medir voltaje y medir corriente.
- Relación entre circuitos básicos y los futuros circuitos con diodos y transistores.

## Actividad sugerida

Aplicar un diagnóstico corto con problemas de cálculo y preguntas conceptuales. Después, resolver en clase dos ejercicios: uno de divisor de voltaje y otro de malla simple. Cerrar mostrando cómo esos mismos cálculos aparecerán en un LED con resistencia, un Zener y un BJT como interruptor.

## Bibliografía y recursos sugeridos

- Hayt, Kemmerly & Durbin: leyes de circuitos, mallas y nodos.
- Boylestad & Nashelsky: repaso de análisis de circuitos aplicado a dispositivos electrónicos.
- All About Circuits – Direct Current: Ley de Ohm, divisores, Kirchhoff y mediciones.

---

# Semana 02 – Señales, magnitudes eléctricas y medición

## Enfoque de fortalecimiento

Esta semana debe unir el diagnóstico de circuitos con el lenguaje propio de la electrónica. Una señal no debe verse solo como una forma de onda, sino como una magnitud eléctrica que existe entre nodos, transporta información y puede medirse con instrumentos.

## Conceptos que deben quedar claros

- Señal analógica: variación continua de voltaje o corriente.
- Señal digital: niveles discretos interpretados como 0 y 1.
- Diferencia entre valor instantáneo, valor pico, valor promedio y valor RMS.
- Referencia o tierra común en mediciones.
- Ruido y tolerancia de niveles lógicos.
- Uso del multímetro y, si está disponible, osciloscopio.
- Relación entre señal eléctrica, información y energía.

## Actividad sugerida

Comparar una señal senoidal, una señal DC y una señal cuadrada. Pedir al estudiante que identifique: tipo de señal, magnitud medida, referencia, posible aplicación y qué instrumento usaría.

## Puente con la Semana 03

Explicar que los semiconductores permitirán controlar el paso de corriente de forma no lineal. Es decir, ya no bastará con aplicar solo resistencias: aparecerán elementos como diodos que conducen en ciertas condiciones.

## Bibliografía y recursos sugeridos

- All About Circuits – Direct Current: señales de instrumentación, voltaje, corriente, multímetros.
- OpenStax University Physics Vol. 2: corriente, resistencia, potencia y mediciones eléctricas.
- Boylestad & Nashelsky: introducción a señales y dispositivos electrónicos.

---

# Semana 03 – Semiconductores, unión PN y diodos

## Enfoque de fortalecimiento

El objetivo es pasar de circuitos resistivos a circuitos electrónicos. La unión PN debe entenderse como la base física del diodo, pero la clase debe aterrizar rápidamente el concepto a circuitos con fuente, resistencia y medición.

## Conceptos que deben quedar claros

- Diferencia entre conductor, aislante y semiconductor.
- Silicio como material semiconductor común.
- Dopaje tipo P y tipo N.
- Formación de la región de agotamiento.
- Ánodo y cátodo.
- Polarización directa e inversa.
- Caída típica de un diodo de silicio.
- Diodo ideal, práctico y real.
- Uso de Ley de Ohm y KVL en un circuito con diodo.

## Actividad sugerida

Analizar un circuito fuente-resistencia-diodo. Primero con el modelo ideal, luego con caída aproximada de 0.7 V. Comparar corriente estimada y discutir por qué la resistencia sigue siendo necesaria.

## Puente con la Semana 04

Mostrar que si el diodo conduce en un solo sentido, puede usarse para convertir AC en DC pulsante. Esta es la base de los rectificadores.

## Bibliografía y recursos sugeridos

- Boylestad & Nashelsky: unión PN, diodos y curvas características.
- Floyd: dispositivos semiconductores y diodos.
- All About Circuits – Semiconductors: unión PN, diodos y verificación con medidor.

---

# Semana 04 – Rectificación, filtrado, LED y Zener

## Enfoque de fortalecimiento

Esta semana debe conectar la teoría del diodo con aplicaciones visibles: fuentes DC, indicadores LED y regulación básica. Es importante trabajar con formas de onda y no solo con esquemas.

## Conceptos que deben quedar claros

- Rectificador de media onda.
- Rectificador de onda completa.
- Puente rectificador.
- Voltaje pico, RMS y promedio.
- Caída de voltaje en diodos.
- Filtro capacitivo y rizado.
- LED y resistencia limitadora.
- Diodo Zener en ruptura controlada.
- Potencia en resistencia, LED y Zener.

## Actividad sugerida

Simular una fuente AC con rectificador de media onda, luego puente rectificador y finalmente capacitor. Solicitar capturas de entrada y salida. Cerrar con un cálculo de resistencia para LED y un regulador Zener simple.

## Puente con la Semana 05

Explicar que el diodo permite controlar dirección de corriente, pero el transistor permite controlar una corriente mayor con una señal pequeña.

## Bibliografía y recursos sugeridos

- Boylestad & Nashelsky: rectificadores, filtros y reguladores básicos.
- Floyd: diodos, fuentes de alimentación y Zener.
- All About Circuits – Semiconductors: diodes and rectifiers, Zener diodes.

---

# Semana 05 – BJT, FET/MOSFET y cierre analógico

## Enfoque de fortalecimiento

Esta semana debe cerrar la unidad analógica. El punto más importante es que el estudiante comprenda el transistor como dispositivo de control: una señal pequeña permite gobernar una carga. Se debe comparar BJT y MOSFET desde la perspectiva de aplicación.

## Conceptos que deben quedar claros

- BJT NPN/PNP.
- Base, colector y emisor.
- Corriente de base y corriente de colector.
- Corte, activa y saturación.
- BJT como interruptor.
- MOSFET canal N.
- Gate, Drain y Source.
- VGS, VDS e ID.
- Resistencia pull-down en MOSFET.
- Diodo flyback para cargas inductivas.
- Comparación: BJT controlado por corriente, MOSFET controlado por voltaje.

## Actividad sugerida

Resolver un caso de control de carga DC: primero con BJT y luego con MOSFET. Comparar cálculo de resistencia de base, resistencia de gate, pull-down y protección de carga inductiva.

## Cierre de corte

Realizar una matriz de integración: Ley de Ohm, Kirchhoff, diodo, Zener, BJT y MOSFET. El estudiante debe explicar qué función cumple cada dispositivo dentro de un sistema real.

## Bibliografía y recursos sugeridos

- Boylestad & Nashelsky: BJT, polarización y FET/MOSFET.
- Floyd: transistores como interruptores y amplificadores.
- All About Circuits – Semiconductors: BJT, JFET y MOSFET.

---

# Semana 06 – Sistemas numéricos

## Enfoque de fortalecimiento

Iniciar la unidad digital mostrando que los circuitos digitales trabajan con información codificada. El estudiante debe entender que binario, hexadecimal y BCD no son solo conversiones matemáticas, sino formas de representar datos en sistemas electrónicos.

## Conceptos que deben quedar claros

- Bit, nibble, byte y palabra.
- Sistema decimal.
- Sistema binario.
- Sistema hexadecimal.
- Código BCD.
- Conversión decimal-binario.
- Conversión binario-hexadecimal.
- Diferencia entre número binario y código.

## Actividad sugerida

Convertir valores usados en aplicaciones reales: número de display, dirección digital, conteo de pulsos, lectura de sensor o representación de una entrada de PLC.

## Puente con la Semana 07

Explicar que si los números se representan en binario, entonces también deben poder sumarse, restarse y manejar signo en binario.

## Bibliografía y recursos sugeridos

- Floyd: sistemas digitales y sistemas de numeración.
- All About Circuits – Digital Circuits: numeration systems.
- Guías digitales del curso: preparación para compuertas y tablas de verdad.

---

# Semana 07 – Aritmética binaria

## Enfoque de fortalecimiento

El objetivo es que el estudiante no solo haga conversiones, sino que entienda cómo un circuito digital puede realizar operaciones aritméticas. Esta semana prepara directamente los sumadores y restadores del tercer corte.

## Conceptos que deben quedar claros

- Suma binaria.
- Acarreo.
- Resta binaria.
- Complemento a 1.
- Complemento a 2.
- Números con signo.
- Overflow.
- Relación entre operación manual y circuito sumador.

## Actividad sugerida

Resolver operaciones binarias paso a paso y luego identificar qué señales serían necesarias para implementarlas en un sumador completo.

## Puente con la Semana 08

Mostrar que las operaciones binarias se construyen con compuertas lógicas básicas; por ejemplo, la suma de un bit involucra XOR y AND.

## Bibliografía y recursos sugeridos

- Floyd: aritmética binaria y códigos.
- All About Circuits – Digital Circuits: binary arithmetic.
- Boylestad & Nashelsky: apoyo para interpretación electrónica de niveles lógicos.

---

# Semana 08 – Compuertas lógicas

## Enfoque de fortalecimiento

Esta semana debe llevar al estudiante del 0/1 abstracto al circuito físico. Las compuertas tienen entradas, salidas, alimentación, tierra, niveles lógicos y limitaciones eléctricas. La práctica debe insistir en consultar hojas de datos.

## Conceptos que deben quedar claros

- AND, OR, NOT.
- NAND, NOR.
- XOR, XNOR.
- Tabla de verdad.
- Expresión booleana.
- Terminales del circuito integrado.
- VCC y GND.
- Familia TTL/CMOS.
- Niveles alto y bajo como rangos de voltaje, no valores perfectos.

## Actividad sugerida

Medir entradas y salidas de compuertas TTL con fuente de 5 V. Comparar tabla de verdad teórica con mediciones reales y calcular error o diferencia porcentual cuando aplique.

## Puente con la Semana 09

Explicar que las compuertas se pueden combinar, pero para no desperdiciar componentes se deben simplificar expresiones mediante álgebra booleana y De Morgan.

## Bibliografía y recursos sugeridos

- Guía de laboratorio 01 – Compuertas lógicas.
- Floyd: compuertas y tablas de verdad.
- All About Circuits – Digital Circuits: logic gates.
- Hojas de datos: 7400, 7402, 7404, 7408, 7432, 7420, 7451 o equivalentes.

---

# Semana 09 – Álgebra booleana, De Morgan e introducción a Karnaugh

## Enfoque de fortalecimiento

El estudiante debe pasar de armar compuertas a diseñar lógica. La simplificación no debe verse como manipulación matemática aislada, sino como una forma de reducir compuertas, conexiones, consumo, costo y probabilidad de falla.

## Conceptos que deben quedar claros

- Variable booleana.
- Suma lógica OR.
- Producto lógico AND.
- Complemento NOT.
- Identidad, nulidad, idempotencia y complemento.
- Absorción.
- Teoremas de De Morgan.
- Conversión entre circuito, tabla de verdad y expresión.
- Idea inicial de minterminos y mapas de Karnaugh.

## Actividad sugerida

Tomar una expresión no simplificada, construir su tabla de verdad, simplificarla algebraicamente y comparar el número de compuertas antes y después.

## Puente con la Semana 11

El receso corta la secuencia, por eso se debe dejar una actividad autónoma breve para repasar leyes booleanas antes de entrar a mapas de Karnaugh.

## Bibliografía y recursos sugeridos

- Guías de laboratorio 02 y 03.
- Floyd: álgebra booleana y De Morgan.
- All About Circuits – Digital Circuits: Boolean algebra y DeMorgan’s theorems.

---

# Semana 10 – Receso institucional

## Enfoque de fortalecimiento

No se debe cargar contenido nuevo. La semana debe usarse como repaso autónomo de lo ya trabajado en el segundo corte.

## Actividad autónoma sugerida

- Repasar conversiones numéricas.
- Rehacer dos ejercicios de aritmética binaria.
- Rehacer una tabla de verdad.
- Simplificar dos expresiones booleanas.
- Preparar dudas sobre De Morgan y Karnaugh.

## Producto sugerido

No asignar entregable nuevo obligatorio. Como apoyo, puede dejarse una guía opcional de repaso para quien necesite reforzar.

---

# Semana 11 – Mapas de Karnaugh y cierre del corte

## Enfoque de fortalecimiento

El mapa de Karnaugh debe presentarse como una herramienta visual para simplificar funciones lógicas a partir de tablas de verdad. Es importante explicar que las celdas se organizan en código Gray para que entre posiciones vecinas cambie solo una variable.

## Conceptos que deben quedar claros

- Minterminos.
- Maxterminos.
- Mapas de 2, 3 y 4 variables.
- Agrupaciones de 1, 2, 4 y 8.
- Condiciones de no importa.
- Obtención de expresión simplificada.
- Implementación final con compuertas.

## Actividad sugerida

Resolver un caso de control lógico de ingeniería: por ejemplo, activar una alarma cuando se cumplan ciertas condiciones de sensores. Construir tabla, mapa, expresión simplificada y circuito.

## Cierre de corte

Evaluar sistemas numéricos, aritmética binaria, compuertas, álgebra booleana, De Morgan y Karnaugh.

## Bibliografía y recursos sugeridos

- Floyd: mapas de Karnaugh y simplificación.
- All About Circuits – Digital Circuits: Karnaugh mapping.
- Guías de laboratorio 01 a 03.

---

# Semana 12 – XOR, sumadores y restadores

## Enfoque de fortalecimiento

Entrar al tercer corte mostrando aplicaciones reales de la lógica combinacional. XOR debe entenderse como detección de diferencia y como base de suma binaria.

## Conceptos que deben quedar claros

- XOR y XNOR.
- Paridad básica.
- Medio sumador.
- Sumador completo.
- Acarreo de entrada y salida.
- Restador básico.
- Relación entre aritmética binaria y circuito lógico.

## Actividad sugerida

Construir tabla de verdad de medio sumador y sumador completo. Después simular un sumador de 1 bit y explicar la función de SUM y CARRY.

## Puente con la Semana 13

Mostrar que además de sumar, los circuitos digitales comparan valores y detectan errores mediante paridad.

## Bibliografía y recursos sugeridos

- Guías de laboratorio 04 y 05.
- Floyd: XOR, sumadores y circuitos aritméticos.
- All About Circuits – Digital Circuits: combinational logic functions, half-adder y full-adder.

---

# Semana 13 – Comparadores y paridad

## Enfoque de fortalecimiento

El estudiante debe comprender que un sistema digital no solo calcula, también decide. Los comparadores permiten establecer igualdad, mayor que o menor que; la paridad ayuda a detectar errores simples.

## Conceptos que deben quedar claros

- Comparador de igualdad.
- Comparador de magnitud.
- Salidas A>B, A=B y A<B.
- Comparador de 4 bits.
- Paridad par e impar.
- Generador de paridad.
- Verificador de paridad.

## Actividad sugerida

Diseñar una lógica simple de validación: permitir acceso si un código binario coincide con una referencia o activar una alarma si hay error de paridad.

## Bibliografía y recursos sugeridos

- Guía de laboratorio 06.
- Floyd: comparadores y paridad.
- Hojas de datos: 7485, 74280, 74266 o equivalentes.

---

# Semana 14 – Codificadores y decodificadores

## Enfoque de fortalecimiento

Relacionar estos circuitos con sistemas visibles para estudiantes: displays, alarmas, teclados, selección de salidas, sensores y automatización. La meta no es memorizar pines, sino entender entradas, salidas y aplicación.

## Conceptos que deben quedar claros

- Codificador.
- Codificador con prioridad.
- Decodificador.
- BCD.
- Display de 7 segmentos.
- Entradas activas en bajo.
- Salidas activas en bajo.
- Diferencia entre codificar información y activar salidas.

## Actividad sugerida

Analizar un sistema con display de 7 segmentos. Identificar el dato BCD, el decodificador, las salidas hacia segmentos y la función de las resistencias limitadoras.

## Bibliografía y recursos sugeridos

- Guía de laboratorio 07.
- Taller individual de codificadores y descodificadores.
- Floyd: codificadores, decodificadores y displays.
- Hojas de datos: 7447, 74147, 74148, 74154 o equivalentes.

---

# Semana 15 – Multiplexores y demultiplexores

## Enfoque de fortalecimiento

Presentar el MUX como selector de datos y el DEMUX como distribuidor. Relacionarlos con selección de canales, comunicaciones, entradas de sensores, expansión de entradas/salidas y control digital.

## Conceptos que deben quedar claros

- Multiplexor.
- Demultiplexor.
- Líneas de selección.
- Entrada de habilitación.
- Salidas activas en bajo.
- Selector de datos.
- Distribuidor de datos.
- Implementación de funciones lógicas con MUX.

## Actividad sugerida

Diseñar un sistema que seleccione una de cuatro señales de sensores usando líneas de selección. Luego analizar cómo distribuir una señal hacia varias salidas mediante DEMUX.

## Bibliografía y recursos sugeridos

- Guía de laboratorio 08.
- Floyd: multiplexores y demultiplexores.
- All About Circuits – Digital Circuits: multiplexers and demultiplexers.
- Hojas de datos: 74151, 74157, 74139, 74154 o equivalentes.

---

# Semana 16 – Flip-flops, contadores y evaluación

## Enfoque de fortalecimiento

Cerrar el curso técnico mostrando la diferencia entre lógica combinacional y lógica secuencial. Aquí aparece memoria digital: la salida no depende solo de las entradas actuales, sino también del estado anterior.

## Conceptos que deben quedar claros

- Lógica combinacional vs lógica secuencial.
- Latch.
- Flip-flop SR, D, JK y T.
- Reloj.
- Flanco de subida y flanco de bajada.
- Estado almacenado.
- Contador asíncrono.
- Contador síncrono.
- Aplicaciones en conteo, temporización y automatización.

## Actividad sugerida

Simular un contador básico con flip-flops y explicar el significado de cada salida. Relacionarlo con conteo de pulsos de un sensor, encoder o final de carrera.

## Bibliografía y recursos sugeridos

- Floyd: flip-flops, registros y contadores.
- All About Circuits – Digital Circuits: multivibrators, sequential circuits and counters.
- Hojas de datos de flip-flops y contadores usados en clase.

---

# Semana 17 – Proyecto final y cierre

## Enfoque de fortalecimiento

La última semana debe evaluar integración. El estudiante debe demostrar funcionamiento, comprensión y capacidad de explicar decisiones técnicas. La sustentación individual es clave para verificar participación real.

## Conceptos que deben integrarse

- Fuente o alimentación del circuito.
- Señales de entrada.
- Procesamiento analógico o digital.
- Compuertas, codificadores, MUX/DEMUX o flip-flops, si aplica.
- Etapa de salida o potencia.
- Mediciones realizadas.
- Simulación y montaje.
- Fallas encontradas y correcciones.

## Actividad sugerida

Cada grupo debe presentar:

1. Problema que resuelve el circuito.
2. Diagrama de bloques.
3. Circuito o simulación.
4. Tabla de verdad, cálculos o lógica utilizada.
5. Evidencia de funcionamiento.
6. Explicación individual por integrante.
7. Conclusiones y mejoras posibles.

## Bibliografía y recursos sugeridos

- Modelo de informe de laboratorio del curso.
- Rúbricas del curso.
- Bibliografía usada durante el semestre.
- Hojas de datos de los componentes empleados.
- Repositorios o fuentes técnicas consultadas, cuando el proyecto lo requiera.

---

## Recomendación metodológica general

Cada semana debe cerrar con tres preguntas:

1. ¿Qué concepto nuevo aprendimos?
2. ¿Qué medición, cálculo o tabla permite comprobarlo?
3. ¿Cómo se conecta este tema con una aplicación real de ingeniería eléctrica?

Esta estructura ayuda a que la clase no sea solo teoría, sino una ruta hacia análisis, simulación, montaje, medición y sustentación técnica.
