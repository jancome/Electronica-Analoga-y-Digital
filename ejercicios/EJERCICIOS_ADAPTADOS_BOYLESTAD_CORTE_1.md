# Banco de ejercicios adaptados de Boylestad – Corte 1

## Propósito

Este banco utiliza la secuencia de análisis de **Electrónica: teoría de circuitos y dispositivos electrónicos**, de Boylestad y Nashelsky, pero presenta valores, contextos y aplicaciones propios del curso.

No contiene reproducciones literales de los problemas ni las soluciones del libro.

## Forma de entrega sugerida

Para cada ejercicio, el estudiante debe incluir:

1. datos y supuestos;
2. modelo utilizado;
3. procedimiento;
4. resultado;
5. simulación o medición;
6. interpretación en lenguaje de ingeniería;
7. relación con el proyecto ABPr, cuando aplique.

---

# Semana 01 – Diagnóstico y arquitectura

## Ejercicio 1.1 – Diagrama de bloques

Una zona de circulación utiliza iluminación aun cuando existe suficiente luz natural.

Diseñar un diagrama preliminar con:

- variable física;
- sensor;
- etapa analógica;
- condición digital;
- etapa de salida;
- indicador o carga.

Para cada bloque indicar:

1. entrada;
2. salida;
3. nivel de tensión esperado;
4. prueba necesaria;
5. riesgo principal.

## Ejercicio 1.2 – Medición y potencia

Una resistencia de `330 Ω` se conecta a una fuente de `5 V`.

1. Calcular la corriente.
2. Calcular la potencia disipada.
3. Determinar si una resistencia de `1/4 W` es adecuada.
4. Explicar dónde debe conectarse el amperímetro.
5. Explicar dónde debe conectarse el voltímetro.

---

# Semana 02 – Diodos, rectificación, filtrado y Zener

## Ejercicio 2.1 – Modelo del diodo

Una fuente de `5 V` alimenta un diodo de silicio y una resistencia de `820 Ω` en serie.

Resolver usando:

1. modelo ideal;
2. modelo práctico de caída constante;
3. comparar las corrientes obtenidas;
4. explicar cuál modelo utilizaría para una primera simulación y cuál para contrastar con una hoja de datos.

## Ejercicio 2.2 – Lectura de una curva

Para tres puntos de operación de un diodo de silicio se registran:

| Corriente | Voltaje |
|---:|---:|
| 1 mA | 0,58 V |
| 5 mA | 0,68 V |
| 20 mA | 0,79 V |

1. Calcular la resistencia estática en cada punto.
2. Comparar los resultados.
3. Explicar por qué el diodo no se comporta como una resistencia constante.
4. Estimar la resistencia dinámica entre 5 mA y 20 mA.

## Ejercicio 2.3 – Prueba con multímetro

Se tienen cuatro diodos sin identificar. Diseñar un procedimiento para:

1. identificar ánodo y cátodo;
2. comprobar conducción directa;
3. comprobar bloqueo inverso;
4. diferenciar un diodo sano, abierto y en cortocircuito;
5. registrar la caída directa medida.

## Ejercicio 2.4 – Rectificador de media onda

Una señal senoidal de `8 V RMS`, `60 Hz`, alimenta un rectificador de media onda con diodo de silicio y carga de `1 kΩ`.

1. Calcular el valor pico de entrada.
2. Estimar el pico de salida.
3. Calcular la corriente pico de carga.
4. Indicar la frecuencia de los pulsos de salida.
5. Dibujar cualitativamente entrada y salida.
6. Seleccionar un PIV mínimo razonable para el diodo.

## Ejercicio 2.5 – Puente rectificador

Repetir el ejercicio anterior utilizando un puente rectificador.

1. Calcular el pico de salida considerando dos diodos en conducción.
2. Determinar la frecuencia de rizado.
3. Comparar aprovechamiento con media onda.
4. Explicar qué dos diodos conducen en cada semiciclo.

## Ejercicio 2.6 – Filtro capacitivo

El puente del ejercicio 2.5 alimenta una carga que consume `25 mA`. Se desea un rizado aproximado máximo de `0,8 V pico a pico`.

1. Estimar la capacitancia necesaria.
2. Seleccionar un valor comercial superior.
3. Indicar el voltaje nominal mínimo del capacitor.
4. Explicar qué sucede al reducir la carga.
5. Explicar qué sucede al duplicar la capacitancia.
6. Comparar cálculo y simulación.

## Ejercicio 2.7 – LED indicador

Se desea conectar un LED rojo de caída aproximada `1,9 V` a una salida de `7 V`, con corriente de diseño de `8 mA`.

1. Calcular la resistencia.
2. Seleccionar un valor comercial.
3. Recalcular la corriente real.
4. Calcular la potencia en la resistencia.
5. Verificar si `1/4 W` es suficiente.

## Ejercicio 2.8 – Regulador Zener

Una fuente no regulada varía entre `10 V` y `13 V`. Se requiere una salida aproximada de `5,1 V` para una carga de `5 mA`. El Zener debe conservar al menos `4 mA`.

1. Calcular la resistencia serie usando la tensión mínima de entrada.
2. Verificar la corriente del Zener con la tensión máxima.
3. Calcular potencia máxima del Zener.
4. Calcular potencia máxima de la resistencia.
5. Seleccionar valores comerciales.
6. Explicar qué ocurre si se desconecta la carga.

## Ejercicio 2.9 – Diagnóstico de una fuente

Una fuente con puente, capacitor y LED presenta los siguientes síntomas:

- entrada AC correcta;
- salida del puente pulsante y de amplitud esperada;
- salida filtrada casi igual a la señal pulsante;
- LED parpadea.

1. Proponer tres causas posibles.
2. Indicar qué medición confirma cada causa.
3. Establecer el orden de diagnóstico.
4. Explicar qué síntoma produciría un diodo abierto en el puente.

---

# Semana 03 – BJT y control de cargas

## Ejercicio 3.1 – Identificación del transistor

Para un transistor NPN desconocido:

1. consultar la referencia;
2. identificar encapsulado y terminales;
3. registrar `VCEO`, `ICmáx`, `Ptot` y rango de `hFE`;
4. verificar el pinout con la hoja de datos;
5. proponer una prueba con multímetro en modo diodo.

## Ejercicio 3.2 – BJT como interruptor para LED

Un transistor NPN controla un LED que consume `15 mA` desde una fuente de `5 V`. La señal de control también es de `5 V`.

Usar una ganancia forzada de `10` y `VBE≈0,7 V`.

1. Calcular corriente de base.
2. Calcular resistencia de base.
3. Seleccionar un valor comercial.
4. Estimar `VCE(sat)` y potencia del transistor.
5. Dibujar el circuito completo.
6. Indicar las tensiones esperadas en corte y saturación.

## Ejercicio 3.3 – Control de una carga de 60 mA

Una carga resistiva de `5 V` consume `60 mA`. Se utilizará un NPN con señal de control de `3,3 V`.

1. Calcular resistencia de base con ganancia forzada de `10`.
2. Verificar la corriente que debe entregar la señal de control.
3. Calcular potencia aproximada del transistor en saturación.
4. Determinar si el diseño es razonable para una salida lógica de baja corriente.
5. Proponer una alternativa MOSFET para comparar en la semana siguiente.

## Ejercicio 3.4 – Relé y diodo de protección

Un relé de `5 V` tiene una bobina de `70 Ω`.

1. Calcular corriente de bobina.
2. Diseñar la resistencia de base para un transistor NPN con control de `5 V`.
3. Dibujar el diodo de rueda libre con polaridad correcta.
4. Explicar qué ocurre al desenergizar la bobina.
5. Explicar el riesgo de omitir el diodo.
6. Verificar la corriente y potencia del transistor seleccionado.

## Ejercicio 3.5 – Estados de tensión

Para un interruptor NPN de lado bajo se midieron:

| Estado | VB | VE | VC |
|---|---:|---:|---:|
| A | 0 V | 0 V | 5 V |
| B | 0,82 V | 0 V | 0,18 V |

1. Identificar corte y saturación.
2. Calcular `VBE` y `VCE` en cada estado.
3. Explicar qué estado enciende la carga.
4. Proponer límites de aceptación para una prueba de laboratorio.

## Ejercicio 3.6 – Diagnóstico del BJT

Una carga permanece encendida aunque la señal de control está en `0 V`.

Investigar en este orden:

1. tensión real base–emisor;
2. cortocircuito colector–emisor;
3. conexión incorrecta de terminales;
4. resistencia de base conectada al nodo equivocado;
5. fuga o camino alternativo en la carga.

Para cada causa indicar la medición que permitiría confirmarla.

## Ejercicio 3.7 – Límite de potencia

Un transistor conduce `180 mA` con `VCE=0,25 V`.

1. Calcular la potencia disipada.
2. Compararla con un límite de `500 mW` a temperatura ambiente.
3. Explicar por qué el margen de potencia no es el único criterio de selección.
4. Identificar otros límites que deben revisarse en la hoja de datos.

---

# Semana 04 – MOSFET y cierre analógico

## Ejercicio 4.1 – Umbral frente a conducción útil

Un MOSFET tiene:

```text
VGS(th) = 2,0 V a 4,0 V
RDS(on) especificada a VGS = 10 V
```

1. Explicar por qué `VGS(th)` no significa que el dispositivo pueda controlar plenamente una carga a `3,3 V`.
2. Indicar qué dato debería buscarse para usarlo con lógica de `3,3 V`.
3. Explicar el significado de un MOSFET de nivel lógico.
4. Proponer una decisión de selección justificada.

## Ejercicio 4.2 – Característica de transferencia

Para un MOSFET de enriquecimiento se utiliza:

```text
ID = k(VGS - VT)²
VT = 2 V
k = 0,20 mA/V²
```

Calcular `ID` para:

- `VGS=1 V`;
- `VGS=2 V`;
- `VGS=4 V`;
- `VGS=6 V`.

Después:

1. representar los puntos;
2. identificar la región sin conducción;
3. explicar la relación no lineal;
4. aclarar por qué este modelo no reemplaza la verificación de `RDS(on)` en conmutación real.

## Ejercicio 4.3 – Etapa MOSFET de lado bajo

Una carga de `5 V` consume `150 mA`. El MOSFET seleccionado presenta `RDS(on)=0,35 Ω` con la tensión de gate disponible.

1. Calcular la caída `VDS` aproximada.
2. Calcular potencia de conducción.
3. Comparar con un BJT que tenga `VCE(sat)=0,20 V`.
4. Determinar cuál disipa menos potencia.
5. Explicar qué otros criterios pueden cambiar la decisión.

## Ejercicio 4.4 – Resistencia de gate y pull-down

Diseñar una entrada de gate con:

- señal de control de `5 V`;
- resistencia serie entre `100 Ω` y `330 Ω`;
- resistencia pull-down entre `47 kΩ` y `220 kΩ`.

1. Seleccionar valores.
2. Explicar la función de cada resistencia.
3. Indicar qué ocurre si se omite el pull-down.
4. Explicar por qué el gate no debe dejarse flotante.

## Ejercicio 4.5 – Manejo electrostático

Elaborar un procedimiento de laboratorio para manipular MOSFET que incluya:

1. descarga electrostática del estudiante;
2. superficie de trabajo;
3. almacenamiento;
4. conexión del gate durante montaje;
5. energización segura;
6. verificación antes de conectar la carga.

## Ejercicio 4.6 – Carga inductiva con MOSFET

Una válvula de `9 V` consume `200 mA`.

1. dibujar el MOSFET de lado bajo;
2. agregar diodo de rueda libre;
3. seleccionar polaridad del diodo;
4. calcular potencia aproximada si `RDS(on)=0,25 Ω`;
5. verificar corriente y tensión nominal del MOSFET;
6. explicar qué tierra deben compartir control y etapa de potencia.

## Ejercicio 4.7 – Diagnóstico MOSFET

La carga queda encendida de forma intermitente cuando el cable de control se desconecta.

1. identificar la causa más probable;
2. proponer la corrección;
3. medir `VGS` antes y después;
4. comprobar si el MOSFET está dañado;
5. explicar cómo diferenciar una entrada flotante de un cortocircuito drenaje–fuente.

## Ejercicio 4.8 – Comparación BJT–MOSFET

Completar una matriz para una carga de `120 mA`:

| Criterio | BJT | MOSFET |
|---|---|---|
| Señal de control |  |  |
| Corriente de control |  |  |
| Caída en conducción |  |  |
| Potencia |  |  |
| Protección |  |  |
| Sensibilidad ESD |  |  |
| Facilidad de diagnóstico |  |  |
| Disponibilidad |  |  |

Concluir cuál utilizaría en el proyecto y bajo qué condiciones cambiaría la decisión.

---

# Semana 05 – Caso integrador y cierre de la Fase 1

## Ejercicio 5.1 – Sistema fotosensible de baja tensión

Diseñar la etapa analógica de un sistema que encienda un LED cuando exista oscuridad.

Debe incluir:

- fuente segura de `5 V`;
- módulo LDR o divisor fotosensible;
- umbral ajustable;
- BJT o MOSFET de salida;
- LED con resistencia;
- puntos de prueba.

El grupo debe:

1. dibujar el diagrama de bloques;
2. elaborar el esquema;
3. calcular los componentes de salida;
4. simular;
5. definir tensiones esperadas con luz y oscuridad;
6. proponer cómo conectar la etapa digital del Corte 2.

## Ejercicio 5.2 – Fuente y etapa de salida

Un sistema requiere `5 V` para la lógica y controla una carga de `9 V`.

1. separar las dos alimentaciones en el diagrama;
2. indicar cuándo debe existir tierra común;
3. seleccionar BJT o MOSFET;
4. agregar protección para carga inductiva;
5. identificar el límite de corriente de cada fuente;
6. definir cinco puntos de medición.

## Ejercicio 5.3 – Tabla de pruebas

Preparar una tabla como mínimo con:

| Prueba | Condición de entrada | Resultado esperado | Medición | Resultado obtenido | Estado |
|---|---|---|---|---|---|

Incluir:

- encendido;
- polaridad;
- fuente sin carga;
- fuente con carga;
- señal de control inactiva;
- señal de control activa;
- carga desconectada;
- recuperación después de apagar y encender.

## Ejercicio 5.4 – Falla provocada

El docente asignará una falla segura:

- diodo invertido;
- capacitor desconectado;
- resistencia incorrecta;
- pinout de transistor equivocado;
- gate o base sin referencia;
- cable abierto;
- carga sin tierra común.

El grupo debe:

1. registrar el síntoma;
2. formular hipótesis;
3. establecer un orden de medición;
4. localizar la falla;
5. corregirla;
6. repetir las pruebas;
7. explicar qué medición fue decisiva.

## Ejercicio 5.5 – Preproyecto ABPr 1

Consolidar:

1. situación problema;
2. objetivos;
3. diagrama de bloques;
4. fuente y regulación;
5. sensor o entrada;
6. etapa BJT o MOSFET;
7. cálculos;
8. simulación;
9. lista de componentes y costos;
10. tabla de pruebas;
11. riesgos y seguridad;
12. conexión prevista con la etapa digital.

## Criterio de cierre

La Fase 1 no se considera completa solo porque la simulación enciende una carga. Debe existir correspondencia entre:

```text
requisito
→ modelo
→ cálculo
→ componente
→ simulación
→ medición esperada
→ diagnóstico
```
