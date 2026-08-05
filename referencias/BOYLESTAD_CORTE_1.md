# Guía de uso de Boylestad para el Corte 1

## Fuente principal

Robert L. Boylestad y Louis Nashelsky, **Electrónica: teoría de circuitos y dispositivos electrónicos**, 10.ª edición, Pearson Prentice Hall, 2009.

Esta guía relaciona el libro con la Fase 1 de la asignatura. No reemplaza los marcos teóricos semanales: indica qué capítulos respaldan cada tema, qué ejemplos pueden adaptarse y cómo conectar la teoría con el proyecto ABPr.

> Las páginas indicadas corresponden a la numeración impresa del libro, no necesariamente al número mostrado por el lector PDF.

## Uso académico y derechos de autor

- No se publicarán capítulos completos, escaneos, figuras ni soluciones extensas del libro.
- Se citarán capítulo, sección y página de la edición utilizada.
- Los ejercicios del repositorio son **adaptaciones propias**: cambian valores, contexto, variables y aplicación.
- Las imágenes o gráficas del texto se analizarán en clase, pero no se reproducirán de manera masiva en el repositorio.
- El estudiante debe calcular, simular, medir e interpretar; no basta con copiar una solución.

---

# Corte 1 – Electrónica analógica básica

## Semana 01 – Inicio, diagnóstico y arquitectura analógico-digital

### Alcance real de Boylestad

Boylestad es un texto de dispositivos electrónicos y presupone conocimientos previos de Ley de Ohm, Kirchhoff, potencia, circuitos serie/paralelo y manejo básico de instrumentos. Por tanto, **no será la única fuente de la Semana 01**.

### Aporte útil

- Prefacio: enfoque de sistemas, aplicaciones prácticas, simulación y solución de fallas.
- Capítulo 1, Sección 1.1: introducción a la evolución y función de los dispositivos semiconductores, p. 1.
- El libro insiste en relacionar el dispositivo con la red completa, la fuente, la carga y las mediciones.

### Aplicación al curso

La primera arquitectura del proyecto debe separar:

```text
variable física
      ↓
sensor o entrada
      ↓
acondicionamiento analógico
      ↓
decisión lógica
      ↓
etapa de salida
      ↓
carga o indicador
```

### Actividad adaptada

Para una aplicación de iluminación eficiente:

1. identificar qué señal es analógica;
2. definir qué condición se convertirá en 0 o 1;
3. proponer el bloque de alimentación;
4. seleccionar un indicador o carga de baja tensión;
5. marcar qué bloques se estudiarán en las semanas 2, 3 y 4.

---

## Semana 02 – Diodos, rectificación, filtrado y Zener

### Base en Boylestad

#### Capítulo 1 – Diodos semiconductores

- Secciones 1.2–1.5: materiales semiconductores, enlace covalente, bandas de energía y materiales tipo n y p, pp. 2–9.
- Sección 1.6: unión p-n, polarización directa e inversa, pp. 10–19.
- Sección 1.7: modelo ideal frente al modelo práctico, p. 20.
- Sección 1.8: resistencia estática y dinámica, pp. 21–26.
- Sección 1.9: circuitos equivalentes del diodo, p. 27.
- Sección 1.12: hojas de especificaciones, p. 32.
- Sección 1.14: prueba de un diodo, p. 36.
- Sección 1.15: diodo Zener, p. 38.
- Sección 1.16: LED, p. 41.

#### Capítulo 2 – Aplicaciones del diodo

- Sección 2.2: análisis mediante recta de carga, p. 60.
- Secciones 2.3 y 2.4: diodos en serie, paralelo y redes mixtas, pp. 65–75.
- Sección 2.6: rectificación de media onda, p. 76.
- Sección 2.7: rectificación de onda completa, p. 79.
- Sección 2.10: aplicaciones del Zener, p. 92.
- Sección 2.12: aplicaciones prácticas, p. 103.

#### Capítulo 15 – Fuentes de alimentación, como ampliación

- Sección 15.2: consideraciones generales sobre filtros, p. 774.
- Sección 15.3: filtro de capacitor, p. 776.
- Sección 15.4: filtro RC, p. 779.
- Sección 15.6: reguladores integrados, p. 788.
- Sección 15.7: aplicaciones prácticas, p. 793.

### Aporte al marco teórico

El texto permite pasar por tres niveles de modelo:

```text
diodo ideal
→ caída práctica aproximada
→ curva real y hoja de datos
```

Esta progresión evita aplicar siempre `0,7 V` sin revisar corriente, temperatura, material y condiciones de operación.

### Ejemplos del libro útiles como metodología

- Ejemplo 1.2: lectura de curvas de diodos de Ge, Si y GaAs para diferentes corrientes, p. 18.
- Ejemplos 1.3 y 1.4: resistencia de cd y resistencia dinámica a partir de la curva, pp. 22–24.
- Los análisis de los capítulos 1 y 2 muestran cómo seleccionar el modelo del diodo antes de aplicar Kirchhoff.

### Ejemplo docente adaptado

Para una fuente de `9 V RMS` y puente de silicio:

1. calcular el valor pico;
2. estimar el pico después del puente;
3. conectar una carga de `680 Ω`;
4. calcular la corriente aproximada;
5. elegir un capacitor para limitar el rizado a un valor definido;
6. agregar un LED indicador;
7. verificar corriente, potencia y tensión inversa de los diodos.

### Conexión ABPr

Cada grupo debe justificar:

- fuente segura de baja tensión;
- rectificación utilizada;
- valor del capacitor;
- tensión y corriente requeridas por la carga;
- protección o regulación;
- puntos de medición antes y después de cada bloque.

### Restricción de seguridad

Boylestad describe fuentes conectadas a la línea dentro de sus aplicaciones prácticas. **Esos circuitos no se construirán en protoboard durante el curso.** Solo se usarán fuentes aisladas de baja tensión o simulación.

---

## Semana 03 – BJT y control de cargas

### Base en Boylestad

#### Capítulo 3 – Transistores de unión bipolar

- Secciones 3.2 y 3.3: construcción y operación, p. 132.
- Sección 3.5: acción amplificadora, p. 138.
- Sección 3.6: configuración en emisor común, p. 139.
- Sección 3.8: límites de operación, p. 146.
- Sección 3.9: hojas de especificaciones, p. 147.
- Sección 3.10: prueba de un transistor, p. 151.
- Sección 3.11: encapsulado e identificación de terminales, p. 153.

#### Capítulo 4 – Polarización de cd de los BJT

- Sección 4.2: punto de operación, p. 162.
- Sección 4.11: operaciones de diseño, p. 194.
- Sección 4.15: redes de conmutación con transistores, p. 206.
- Sección 4.16: técnicas de solución de fallas, p. 210.
- Sección 4.18: aplicaciones prácticas, p. 220.

### Aporte al marco teórico

Para el curso el BJT se estudiará principalmente como interruptor:

```text
corte → carga apagada
saturación → carga encendida
```

No es suficiente afirmar que `IC = βIB`. En conmutación se debe asegurar corriente de base suficiente, verificar `VCE(sat)`, corriente de colector, potencia y límites de la hoja de datos.

### Ejemplo docente adaptado

Controlar un LED de potencia baja o un relé didáctico de `5 V` que consume `60 mA` mediante un transistor NPN:

1. seleccionar una corriente de colector de diseño;
2. usar una ganancia forzada conservadora;
3. calcular la resistencia de base;
4. calcular potencia del transistor;
5. agregar diodo de rueda libre si la carga es inductiva;
6. medir `VB`, `VC`, `VE`, `VBE` y `VCE` en corte y saturación.

### Diagnóstico inspirado en Boylestad

1. inspección visual;
2. comprobar alimentación y tierra;
3. verificar pinout real del encapsulado;
4. medir base, emisor y colector respecto a tierra;
5. comparar con estados esperados;
6. comprobar continuidad de carga y resistencia;
7. probar el transistor fuera de circuito cuando sea necesario.

### Conexión ABPr

El BJT puede actuar como:

- etapa de salida de una compuerta;
- controlador de relé;
- amplificador de corriente para un LED;
- interfaz entre sensor y carga;
- bloque de protección o inversión, cuando esté justificado.

---

## Semana 04 – MOSFET y cierre analógico

### Base en Boylestad

#### Capítulo 6 – Transistores de efecto de campo

- Sección 6.8: MOSFET tipo enriquecimiento, p. 392.
- Sección 6.9: manejo del MOSFET, p. 399.
- Sección 6.10: VMOS, p. 400.
- Sección 6.11: CMOS, p. 401.
- Sección 6.13: tabla de resumen, p. 405.

#### Capítulo 7 – Polarización de los FET

- Sección 7.8: polarización del MOSFET tipo enriquecimiento, p. 433.
- Sección 7.11: diseño, p. 442.
- Sección 7.12: solución de fallas, p. 445.
- Sección 7.15: aplicaciones prácticas, p. 451.

### Alcance real del libro

Boylestad desarrolla con profundidad las características y la polarización de los FET. Para nuestro montaje se seleccionarán de esas secciones los conceptos necesarios para usar el MOSFET tipo enriquecimiento como interruptor de baja tensión. La topología de conmutación completa será una adaptación de curso, no una reproducción literal de un ejemplo del texto.

### Aporte al marco teórico

- La compuerta se controla por tensión.
- Existe un voltaje umbral, pero `VGS(th)` no garantiza conducción plena de una carga.
- La corriente depende de la región de operación y de las características del dispositivo.
- El MOSFET puede dañarse por electricidad estática.
- Deben verificarse `VDS`, `ID`, potencia, resistencia de encendido y tensión real disponible en gate.

### Ejemplo del libro útil como metodología

La sección de MOSFET de enriquecimiento construye la característica de transferencia a partir de los datos del dispositivo y utiliza la relación entre `ID` y `VGS`. Este análisis ayuda a explicar por qué no basta con conocer únicamente el voltaje umbral.

### Ejemplo docente adaptado

Diseñar una etapa de conmutación de lado bajo para una carga de `5 V` y `150 mA`:

1. comprobar que el MOSFET sea adecuado para la tensión de control disponible;
2. seleccionar resistencia serie de gate;
3. colocar resistencia pull-down;
4. agregar diodo de protección si la carga es inductiva;
5. calcular potencia aproximada en conducción;
6. medir `VGS` y `VDS` con la carga encendida;
7. comparar pérdidas con una alternativa BJT.

### Conexión ABPr

Cada grupo debe comparar BJT y MOSFET con criterios de:

- corriente de control;
- caída de tensión;
- potencia disipada;
- compatibilidad con la señal lógica;
- costo y disponibilidad;
- protección requerida;
- facilidad de diagnóstico.

---

## Semana 05 – Integración y cierre de la Fase 1

### Base en Boylestad

- Capítulo 2, Sección 2.12: aplicaciones prácticas de diodos, p. 103.
- Capítulo 4, Secciones 4.15, 4.16 y 4.18: conmutación, fallas y aplicaciones BJT, pp. 206–228.
- Capítulo 7, Secciones 7.12 y 7.15: fallas y aplicaciones FET, pp. 445–462.
- Capítulo 15, Secciones 15.2–15.7: filtrado, regulación y fuentes prácticas, pp. 774–796.

### Aclaración

Boylestad no presenta exactamente nuestro proyecto ABPr de integración analógico-digital. El caso integrador será diseñado por el curso utilizando la metodología del libro: modelar, calcular, simular, medir, comparar y diagnosticar.

### Caso integrador adaptado

```text
fuente aislada de baja tensión
        ↓
rectificación y filtrado
        ↓
regulación o protección
        ↓
sensor o señal de control
        ↓
BJT o MOSFET
        ↓
LED, relé didáctico o carga de baja tensión
```

El grupo deberá entregar:

1. propósito de cada bloque;
2. cálculos;
3. simulación;
4. valores nominales de componentes;
5. mediciones esperadas;
6. riesgos eléctricos;
7. lista de fallas probables;
8. procedimiento de diagnóstico;
9. BOM inicial;
10. conexión con la futura etapa digital.

### Secuencia de verificación

1. comprobar fuente;
2. observar forma de onda rectificada;
3. medir rizado;
4. verificar regulación;
5. comprobar señal de control;
6. medir la etapa de salida;
7. probar la carga;
8. comparar cálculo y simulación;
9. provocar una falla segura;
10. localizarla mediante mediciones.

---

# Temas de Boylestad que quedan como ampliación

Los siguientes contenidos son valiosos, pero no deben desplazar los temas oficiales del primer corte:

- análisis de ca y amplificadores BJT, Capítulo 5;
- amplificadores con FET, Capítulo 8;
- respuesta en frecuencia, Capítulo 9;
- amplificadores operacionales, Capítulos 10 y 11;
- amplificadores de potencia, Capítulo 12;
- temporizadores, conversión y PLL, Capítulo 13;
- osciladores, Capítulo 14;
- dispositivos optoelectrónicos y de potencia, Capítulos 16 y 17.

# Recomendación metodológica

Cada marco teórico del primer corte debe incluir:

1. **Modelo físico:** qué ocurre dentro del dispositivo.
2. **Modelo de circuito:** ideal, práctico o basado en hoja de datos.
3. **Ejemplo guiado:** cálculo con valores propios del curso.
4. **Simulación:** forma de onda y puntos de operación.
5. **Medición:** voltajes y corrientes en nodos definidos.
6. **Diagnóstico:** falla probable, medición que la confirma y corrección.
7. **Conexión ABPr:** función del bloque dentro del proyecto.

Así Boylestad se utiliza como base rigurosa sin convertir el repositorio en una reproducción del libro.