# Instrumentos de evaluación por corte

**Asignatura:** Electrónica Analógica y Digital  
**Periodo:** 2026-2  
**Programa:** Ingeniería Eléctrica  

---

## 1. Estructura general de la nota

La nota final del estudiante se organizará así:

| Componente | Peso sobre nota final |
|---|---:|
| Corte 1 – Unidad analógica | 30% |
| Corte 2 – Fundamentos digitales y lógica combinacional | 30% |
| Corte 3 – Aplicaciones digitales y secuenciales | 30% |
| Examen institucional de la universidad | 10% |
| **Total** | **100%** |

El docente desarrolla y califica el **90% correspondiente a la asignatura**. El **10% restante** corresponde a un examen institucional de la universidad, externo a la planeación del docente.

---

## 2. Distribución interna sugerida por corte

Cada corte se propone con esta distribución sobre la nota final:

| Instrumento | Peso sobre nota final | Propósito |
|---|---:|---|
| Quiz del corte | 2% | Verificar conceptos mínimos de la unidad. |
| Taller 1 – Aplicación y cálculo | 2% | Fortalecer análisis, procedimientos y solución de problemas. |
| Taller 2 – Investigación académica en otro idioma | 2% | Consultar bases de datos institucionales y relacionar la teoría con aplicaciones actuales. |
| Guías de laboratorio / actividad práctica | 4% | Evidenciar simulación, montaje, medición, análisis y conclusiones. |
| Parcial del corte | 20% | Evaluar integralmente la unidad. |
| **Total por corte** | **30%** |  |

---

## 3. Condiciones del taller investigativo en otro idioma

En cada corte, uno de los talleres debe involucrar búsqueda académica en bases de datos de la universidad en un idioma diferente al español, preferiblemente **inglés**.

### Bases de datos o fuentes institucionales sugeridas

El estudiante debe consultar las bases disponibles en la biblioteca o plataforma institucional, por ejemplo:

- IEEE Xplore.
- ScienceDirect.
- SpringerLink.
- Scopus.
- EBSCOhost.
- ProQuest.
- Taylor & Francis.
- Wiley Online Library.
- Libros electrónicos de Pearson, McGraw-Hill, Cengage u otros proveedores institucionales.

### Producto mínimo esperado

Cada taller investigativo debe incluir:

1. Título del artículo, capítulo o recurso consultado.
2. Base de datos utilizada.
3. Referencia en formato IEEE.
4. Resumen en español, redactado por el estudiante.
5. Cinco términos técnicos en el idioma original con su traducción.
6. Explicación de cómo el recurso se relaciona con el tema del corte.
7. Una aplicación en ingeniería eléctrica.
8. Evidencia de consulta: captura de la base de datos, DOI, enlace institucional o ficha bibliográfica.

### Criterios éticos

- No se debe copiar y pegar el resumen del artículo.
- La traducción automática puede usarse como apoyo, pero el análisis debe ser propio.
- El uso de IA debe declararse si se emplea para apoyo de redacción, traducción o corrección.
- Las fuentes deben ser académicas o técnicas; no se aceptan blogs sin respaldo técnico como fuente principal.

---

# Corte 1 – Unidad analógica

## Temas del corte

- Fundamentos de circuitos eléctricos para electrónica.
- Ley de Ohm, potencia, nodos, mallas y leyes de Kirchhoff.
- Señales, magnitudes eléctricas y medición básica.
- Semiconductores, unión PN y diodos.
- Rectificación, filtrado, LED y Zener.
- Transistores BJT y FET/MOSFET como dispositivos de control.

## Guías asociadas

- Guía A01 – Diodos, rectificación y regulación con Zener.
- Guía A02 – Transistor BJT como interruptor y amplificador básico.
- Guía A03 – Transistor FET/MOSFET como dispositivo de control.

---

## Quiz 1 – Unidad analógica

**Peso:** 2% de la nota final.  
**Duración sugerida:** 20 a 30 minutos.  
**Tipo:** individual.  

### Objetivo

Verificar que el estudiante maneja los conceptos mínimos necesarios para analizar circuitos electrónicos analógicos básicos.

### Preguntas sugeridas

1. Explique brevemente la diferencia entre voltaje y corriente.
2. Una resistencia de 1 kΩ se conecta a una fuente de 5 V. Calcule la corriente.
3. ¿Por qué una resistencia puede limitar la corriente en un LED?
4. Enuncie la ley de voltajes de Kirchhoff para una malla.
5. ¿Qué diferencia existe entre una señal DC y una señal AC?
6. ¿Qué es una señal analógica?
7. ¿Qué es una unión PN?
8. ¿Qué ocurre con un diodo en polarización directa?
9. ¿Qué ocurre con un diodo en polarización inversa?
10. Compare brevemente BJT y MOSFET como dispositivos de control.

### Criterios de calificación

| Criterio | Peso |
|---|---:|
| Conceptos correctos | 40% |
| Cálculos básicos correctos | 30% |
| Claridad de explicación | 20% |
| Orden y unidades | 10% |

---

## Taller 1 – Aplicación y cálculo: circuitos analógicos básicos

**Peso:** 2% de la nota final.  
**Tipo:** individual o parejas.  

### Objetivo

Reforzar los fundamentos de circuitos eléctricos necesarios para analizar señales y circuitos con diodos, LED, Zener, BJT y MOSFET.

### Actividades

1. Para una fuente de 12 V y resistencias de 1 kΩ y 2.2 kΩ en serie, calcule resistencia equivalente, corriente total, caída de voltaje y potencia en cada resistencia.
2. Diseñe un divisor de voltaje que entregue aproximadamente 5 V a partir de una fuente de 12 V. Justifique los valores elegidos.
3. Explique cómo se conecta un multímetro para medir voltaje y cómo se conecta para medir corriente.
4. Dibuje una señal DC, una señal senoidal y una señal cuadrada. Indique cuál puede ser analógica, digital o ambas según el contexto.
5. Analice un circuito compuesto por fuente de 5 V, resistencia de 1 kΩ y diodo de silicio en polarización directa. Calcule la corriente aproximada suponiendo VD = 0.7 V.
6. Diseñe un circuito LED con fuente de 9 V, LED rojo de 2 V y corriente deseada de 10 mA. Calcule la resistencia comercial recomendada y su potencia.
7. Diseñe un circuito con BJT NPN como interruptor para encender un LED o relé de baja corriente. Identifique base, colector, emisor y resistencia de base.
8. Diseñe un MOSFET canal N como interruptor para controlar una carga DC. Incluya resistencia de gate, resistencia pull-down y diodo de protección si la carga es inductiva.

### Producto esperado

Documento con cálculos, esquemas, unidades, análisis y conclusiones.

---

## Taller 2 – Investigación académica en inglés: dispositivos semiconductores

**Peso:** 2% de la nota final.  
**Tipo:** grupos de máximo 3 estudiantes.  
**Idioma de consulta:** inglés.  

### Objetivo

Relacionar los dispositivos semiconductores estudiados en el primer corte con una aplicación actual documentada en literatura académica o técnica.

### Tema sugerido

Seleccionar uno de los siguientes temas:

1. Diodos rectificadores en fuentes de alimentación.
2. Diodos Zener como referencia o protección de voltaje.
3. BJT como interruptor o amplificador básico.
4. MOSFET en control de cargas DC o electrónica de potencia.
5. Uso de semiconductores en sistemas de energía, automatización o control eléctrico.

### Instrucciones

1. Buscar un artículo, capítulo de libro o documento técnico en inglés en una base de datos institucional.
2. El recurso debe estar relacionado con uno de los temas del corte.
3. Elaborar una ficha académica con referencia IEEE.
4. Escribir un resumen en español de 250 a 400 palabras.
5. Extraer cinco términos técnicos en inglés y traducirlos al español.
6. Explicar cómo el tema se conecta con una práctica de laboratorio del corte.
7. Proponer una aplicación real en ingeniería eléctrica.

### Producto esperado

Ficha académica, resumen, glosario técnico, análisis de aplicación y evidencia de consulta.

### Rúbrica sugerida

| Criterio | Peso |
|---|---:|
| Fuente académica pertinente | 20% |
| Resumen propio y claro | 25% |
| Relación con el corte | 20% |
| Glosario técnico bilingüe | 15% |
| Aplicación en ingeniería eléctrica | 10% |
| Referencia IEEE y evidencia de consulta | 10% |

---

## Parcial 1 – Unidad analógica

**Peso:** 20% de la nota final.  
**Duración sugerida:** 90 a 120 minutos.  
**Tipo:** individual.  

### Objetivo

Evaluar la capacidad del estudiante para analizar circuitos básicos de electrónica analógica aplicando fundamentos de circuitos, semiconductores, diodos, rectificación, regulación y transistores.

### Estructura sugerida

| Sección | Tema | Peso dentro del parcial |
|---|---|---:|
| A | Fundamentos de circuitos, Ley de Ohm, Kirchhoff y medición | 20% |
| B | Señales, valores eléctricos y análisis básico | 15% |
| C | Diodos, polarización y rectificación | 25% |
| D | LED, Zener y potencia | 20% |
| E | BJT/MOSFET como interruptores | 20% |

### Preguntas sugeridas

1. En un circuito serie con fuente de 12 V, R1 = 1 kΩ y R2 = 2.2 kΩ, calcule corriente, voltajes y potencias.
2. Explique la diferencia entre valor pico y valor RMS en una señal AC.
3. Analice un circuito con fuente de 5 V, resistencia de 1 kΩ y diodo de silicio. Calcule la corriente en polarización directa.
4. Para una entrada de 12 V RMS, estime el voltaje pico y describa la salida de un rectificador de onda completa.
5. Calcule la resistencia para un LED alimentado con 12 V, con VLED = 2 V e ILED = 15 mA.
6. Diseñe de forma básica un regulador Zener de 5.1 V. Explique función de la resistencia serie y verificación de potencia.
7. Explique cuándo un BJT trabaja en corte y saturación.
8. Compare BJT y MOSFET en una aplicación de control de carga DC.

---

# Corte 2 – Fundamentos digitales y lógica combinacional

## Temas del corte

- Sistemas numéricos.
- Aritmética binaria.
- Compuertas lógicas.
- Tablas de verdad.
- Álgebra booleana.
- Teoremas de De Morgan.
- Mapas de Karnaugh.

## Guías asociadas

- Lab 01 – Compuertas lógicas.
- Lab 02 – Álgebra booleana.
- Lab 03 – Teorema de De Morgan.

---

## Quiz 2 – Fundamentos digitales

**Peso:** 2% de la nota final.  
**Duración sugerida:** 20 a 30 minutos.  
**Tipo:** individual.

### Objetivo

Verificar que el estudiante comprende la representación binaria de información y el funcionamiento básico de compuertas lógicas.

### Preguntas sugeridas

1. Convierta el número decimal 25 a binario.
2. Convierta el número binario 101101 a decimal.
3. ¿Qué es un bit?
4. ¿Qué es un nibble?
5. Realice la suma binaria: 1011 + 0110.
6. Escriba la tabla de verdad de una compuerta AND de dos entradas.
7. Escriba la tabla de verdad de una compuerta OR de dos entradas.
8. ¿Qué hace una compuerta NOT?
9. Enuncie uno de los teoremas de De Morgan.
10. ¿Para qué sirve un mapa de Karnaugh?

---

## Taller 1 – Aplicación y cálculo: sistemas numéricos y lógica básica

**Peso:** 2% de la nota final.  
**Tipo:** individual o parejas.

### Objetivo

Fortalecer la representación de información en sistemas digitales y el uso de tablas de verdad, compuertas y simplificación lógica.

### Actividades

1. Convierta a binario los siguientes números decimales: 13, 27, 45, 64 y 127.
2. Convierta a decimal los siguientes números binarios: 1010, 1111, 10010, 110101 y 1111111.
3. Convierta a hexadecimal: 10101100, 11110000 y 00111101.
4. Represente en BCD los números 25, 79 y 408.
5. Realice tres sumas binarias y dos restas usando complemento a 2.
6. Construya la tabla de verdad de una función lógica de tres variables propuesta por el docente.
7. Simplifique una expresión booleana usando leyes básicas y De Morgan.
8. Resuelva un mapa de Karnaugh de 3 o 4 variables y dibuje el circuito lógico final.

---

## Taller 2 – Investigación académica en inglés: lógica digital y simplificación

**Peso:** 2% de la nota final.  
**Tipo:** grupos de máximo 3 estudiantes.  
**Idioma de consulta:** inglés.

### Objetivo

Relacionar la lógica digital básica con aplicaciones documentadas en literatura académica o técnica.

### Tema sugerido

Seleccionar uno de los siguientes temas:

1. Aplicaciones de lógica combinacional en sistemas de control.
2. Uso de compuertas lógicas en electrónica industrial.
3. Métodos de simplificación lógica en diseño digital.
4. Mapas de Karnaugh en diseño de circuitos combinacionales.
5. Implementación de lógica digital en sistemas embebidos o PLC.

### Instrucciones

1. Buscar un artículo, capítulo o documento técnico en inglés en una base de datos institucional.
2. Identificar el problema o aplicación que aborda el documento.
3. Elaborar la referencia en formato IEEE.
4. Redactar un resumen en español de 250 a 400 palabras.
5. Extraer cinco términos técnicos en inglés relacionados con lógica digital y traducirlos.
6. Explicar cómo la investigación se relaciona con compuertas, tablas de verdad, De Morgan o Karnaugh.
7. Proponer un ejemplo de aplicación en ingeniería eléctrica.

### Producto esperado

Ficha académica, resumen, glosario técnico, ejemplo de aplicación y evidencia de consulta.

---

## Parcial 2 – Fundamentos digitales y lógica combinacional

**Peso:** 20% de la nota final.  
**Duración sugerida:** 90 a 120 minutos.  
**Tipo:** individual.

### Objetivo

Evaluar la capacidad del estudiante para representar información digital, operar en binario, analizar compuertas, construir tablas de verdad y simplificar funciones lógicas.

### Estructura sugerida

| Sección | Tema | Peso dentro del parcial |
|---|---|---:|
| A | Sistemas numéricos y códigos | 20% |
| B | Aritmética binaria | 20% |
| C | Compuertas y tablas de verdad | 20% |
| D | Álgebra booleana y De Morgan | 20% |
| E | Mapas de Karnaugh | 20% |

### Preguntas sugeridas

1. Realice conversiones entre decimal, binario, hexadecimal y BCD.
2. Resuelva operaciones binarias con y sin signo.
3. Construya una tabla de verdad a partir de una condición lógica.
4. Obtenga la expresión booleana de una tabla de verdad.
5. Simplifique una expresión usando leyes booleanas.
6. Aplique De Morgan para transformar una expresión.
7. Simplifique una función usando Karnaugh.
8. Dibuje el circuito final con compuertas lógicas.

---

# Corte 3 – Aplicaciones digitales y secuenciales

## Temas del corte

- XOR y XNOR.
- Sumadores y restadores.
- Comparadores y paridad.
- Codificadores y decodificadores.
- Multiplexores y demultiplexores.
- Flip-flops y contadores.
- Proyecto final.

## Guías asociadas

- Lab 04 – XOR y aplicaciones.
- Lab 05 – Sumadores y aplicaciones.
- Lab 06 – Comparadores y paridad.
- Lab 07 – Codificadores y decodificadores.
- Lab 08 – Multiplexores y demultiplexores.

---

## Quiz 3 – Aplicaciones digitales

**Peso:** 2% de la nota final.  
**Duración sugerida:** 20 a 30 minutos.  
**Tipo:** individual.

### Objetivo

Verificar conceptos clave de circuitos combinacionales y secuenciales básicos.

### Preguntas sugeridas

1. ¿Qué función cumple una compuerta XOR?
2. ¿Qué diferencia existe entre medio sumador y sumador completo?
3. ¿Qué es el acarreo de salida?
4. ¿Qué hace un comparador de magnitud?
5. ¿Qué es paridad par?
6. ¿Qué diferencia existe entre codificador y decodificador?
7. ¿Para qué sirve un multiplexor?
8. ¿Para qué sirve un demultiplexor?
9. ¿Qué diferencia existe entre lógica combinacional y lógica secuencial?
10. ¿Qué función cumple un flip-flop?

---

## Taller 1 – Aplicación y diseño: circuitos combinacionales y secuenciales

**Peso:** 2% de la nota final.  
**Tipo:** grupos de máximo 3 estudiantes.

### Objetivo

Diseñar y analizar aplicaciones digitales combinacionales y secuenciales básicas.

### Actividades

1. Construya la tabla de verdad de un medio sumador y un sumador completo.
2. Diseñe un circuito comparador de dos números de 2 bits.
3. Diseñe un generador de paridad par para un dato de 3 bits.
4. Explique el funcionamiento de un decodificador BCD a 7 segmentos.
5. Proponga una aplicación con multiplexor para seleccionar una de cuatro señales.
6. Proponga una aplicación con demultiplexor para activar una de varias salidas.
7. Explique la diferencia entre un latch y un flip-flop.
8. Simule o describa un contador básico y relacione su uso con automatización.

---

## Taller 2 – Investigación académica en inglés: aplicaciones digitales en ingeniería eléctrica

**Peso:** 2% de la nota final.  
**Tipo:** grupos de máximo 3 estudiantes.  
**Idioma de consulta:** inglés.

### Objetivo

Investigar una aplicación actual de circuitos digitales combinacionales o secuenciales en ingeniería eléctrica, automatización, control, medición o sistemas embebidos.

### Tema sugerido

Seleccionar uno de los siguientes temas:

1. Aplicaciones de sumadores o ALU en sistemas digitales.
2. Comparadores digitales en medición, control o protección.
3. Codificadores y decodificadores en interfaces hombre-máquina.
4. Multiplexores en adquisición de datos o comunicaciones.
5. Flip-flops y contadores en automatización o instrumentación.
6. Aplicaciones digitales en sistemas embebidos usados en ingeniería eléctrica.

### Instrucciones

1. Buscar un artículo, capítulo, paper de conferencia o documento técnico en inglés en una base de datos institucional.
2. Identificar el circuito digital o concepto principal usado.
3. Elaborar la referencia en formato IEEE.
4. Redactar un resumen en español de 300 a 500 palabras.
5. Extraer cinco términos técnicos en inglés con traducción y definición corta.
6. Relacionar el documento con una guía del tercer corte.
7. Proponer una mejora, variante o aplicación didáctica que pueda implementarse en clase o simulación.

### Producto esperado

Ficha académica, resumen, glosario técnico, relación con laboratorio, propuesta de aplicación y evidencia de consulta.

---

## Parcial 3 – Aplicaciones digitales y secuenciales

**Peso:** 20% de la nota final.  
**Duración sugerida:** 90 a 120 minutos.  
**Tipo:** individual.

### Objetivo

Evaluar la capacidad del estudiante para analizar y diseñar circuitos digitales combinacionales y secuenciales básicos.

### Estructura sugerida

| Sección | Tema | Peso dentro del parcial |
|---|---|---:|
| A | XOR, sumadores y restadores | 20% |
| B | Comparadores y paridad | 20% |
| C | Codificadores y decodificadores | 20% |
| D | Multiplexores y demultiplexores | 20% |
| E | Flip-flops y contadores | 20% |

### Preguntas sugeridas

1. Diseñe un medio sumador usando compuertas lógicas.
2. Construya la tabla de verdad de un sumador completo.
3. Diseñe un comparador simple de igualdad para dos bits.
4. Explique cómo se detecta error usando paridad.
5. Analice el funcionamiento de un decodificador BCD a 7 segmentos.
6. Explique cómo un multiplexor puede implementar una función lógica.
7. Proponga una aplicación de un demultiplexor en automatización.
8. Compare lógica combinacional y lógica secuencial.
9. Explique la función de un flip-flop D.
10. Analice un contador básico y describa sus salidas.

---

## 4. Observaciones para aplicación

- El docente puede cambiar los ejercicios numéricos conservando la misma estructura.
- El taller investigativo debe mantener el componente de consulta en otro idioma y base de datos institucional.
- Las guías pueden evaluarse como informes completos, simulaciones, evidencias de montaje o sustentaciones cortas.
- El parcial debe ser individual.
- Los trabajos en grupo deben incluir sustentación o preguntas individuales para validar participación.
