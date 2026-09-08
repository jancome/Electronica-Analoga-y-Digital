# Marco teórico – Semana 08

# Compuertas lógicas y primer montaje en protoboard

## Metas de aprendizaje verificables

- Pasar de requisito a tabla, expresión y circuito con compuertas.
- Verificar alimentación, umbrales, carga, fan-out y entradas no utilizadas de un CI real.
- Diagnosticar una discrepancia entre tabla, simulación y protoboard por nodos.

## 1. Propósito de la semana

Convertir las variables digitales del proyecto en una primera función de decisión e implementarla mediante compuertas lógicas, simulación y montaje en protoboard.

## 2. Resultado de aprendizaje

Al finalizar la semana, el estudiante estará en capacidad de:

- Interpretar las compuertas AND, OR, NOT, NAND, NOR, XOR y XNOR.
- Construir tablas de verdad.
- Relacionar tabla, expresión y circuito.
- Identificar alimentación, niveles lógicos y terminales de un circuito integrado.
- Simular una función lógica.
- Construir y comprobar un primer circuito en protoboard.
- Documentar la relación entre la lógica y la situación problema.

## 3. Conexión con la Fase 2 ABPr

Esta semana inicia la evidencia práctica exigida institucionalmente:

```text
Variables del proyecto
        ↓
Tabla de verdad inicial
        ↓
Compuertas
        ↓
Simulación
        ↓
Primer montaje en protoboard
```

La Fase 2 no puede quedar como un ejercicio documental. Debe llegar a una implementación funcional.

## 4. Variable y nivel lógico

Una variable booleana toma valores 0 o 1. En el circuito real estos valores corresponden a rangos de voltaje, no a números abstractos.

Antes del montaje deben revisarse:

- Voltaje de alimentación.
- Umbrales de entrada.
- Capacidad de corriente de salida.
- Compatibilidad entre familias TTL y CMOS.
- Entradas y salidas activas en alto o en bajo.

## 5. Compuertas principales

| Compuerta | Expresión | Condición de salida 1 |
|---|---|---|
| AND | `A·B` | Todas las entradas son 1. |
| OR | `A+B` | Al menos una entrada es 1. |
| NOT | `A̅` | Invierte la entrada. |
| NAND | `(A·B)̅` | Negación de AND. |
| NOR | `(A+B)̅` | Negación de OR. |
| XOR | `A⊕B` | Las entradas son diferentes. |
| XNOR | `(A⊕B)̅` | Las entradas son iguales. |

## 6. Tabla de verdad

La tabla de verdad contiene todas las combinaciones posibles. Para `n` variables existen:

```text
2ⁿ combinaciones
```

Para dos variables A y B:

| A | B | A·B | A+B | A⊕B |
|---|---|---|---|---|
| 0 | 0 | 0 | 0 | 0 |
| 0 | 1 | 0 | 1 | 1 |
| 1 | 0 | 0 | 1 | 1 |
| 1 | 1 | 1 | 1 | 0 |

## 7. Compuertas universales

NAND y NOR se consideran universales porque permiten construir cualquier función lógica.

Esta propiedad puede reducir la variedad de integrados necesarios, pero la implementación debe compararse en número de puertas, conexiones y niveles de negación.

## 8. Circuitos integrados y hoja de datos

Antes de montar se debe consultar:

- Referencia del integrado.
- Pin VCC y GND.
- Distribución de compuertas.
- Voltaje permitido.
- Corrientes de entrada y salida.
- Tabla de funcionamiento.
- Condiciones de entradas no utilizadas.

Ejemplos comunes: 7400, 7402, 7404, 7408, 7432 o equivalentes CMOS.

## 9. Entradas flotantes

Una entrada no conectada puede captar ruido y cambiar de estado. Todas las entradas deben quedar definidas mediante:

- Interruptor correctamente cableado.
- Resistencia pull-up.
- Resistencia pull-down.
- Conexión fija a un nivel permitido.

## 10. Salidas y cargas

Una compuerta puede encender un LED con resistencia, pero no debe alimentar directamente cargas de corriente elevada.

Cuando la salida deba controlar relé, motor o carga mayor, se utilizará la etapa BJT o MOSFET diseñada en el Corte 1.

## 11. Ejemplo aplicado

Una lámpara debe encender cuando el lugar está oscuro (`L=1`) y existe presencia (`P=1`):

```text
Y = L·P
```

La tabla de verdad es:

| L | P | Y |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

El circuito inicial utiliza una compuerta AND. Posteriormente se evaluará si la lógica requiere simplificación o más variables.

## 12. Procedimiento de simulación y montaje

1. Construir la tabla de verdad.
2. Dibujar el circuito.
3. Simular todas las combinaciones.
4. Consultar el pinout.
5. Montar VCC y GND.
6. Definir entradas con interruptores y resistencias.
7. Colocar LED de salida con resistencia.
8. Probar cada combinación.
9. Comparar tabla teórica, simulación y montaje.
10. Registrar fallas y correcciones.

## 13. Evidencia ABPr

- Tabla de verdad inicial.
- Expresión booleana.
- Simulación funcional.
- Fotografía del protoboard.
- Tabla de comprobación de entradas y salida.
- Hoja de datos utilizada.
- Explicación del aporte al proyecto.

## 14. Errores comunes

- Dejar entradas flotantes.
- Confundir OR con XOR.
- Conectar mal VCC o GND.
- Omitir resistencia del LED.
- Usar una salida lógica para una carga no permitida.
- No verificar si una señal es activa en bajo.
- Tomar una fotografía sin demostrar todas las combinaciones.

## 15. Preguntas orientadoras

1. ¿Qué condición física representa cada entrada?
2. ¿Cómo se comprueba que la salida coincide con la tabla?
3. ¿Qué ocurre si una entrada queda flotante?
4. ¿Por qué NAND y NOR son universales?
5. ¿Qué etapa se necesita para controlar una carga mayor?

## 16. Trabajo independiente

- Completar el Lab 01.
- Corregir el montaje.
- Documentar todas las combinaciones.
- Preparar la expresión lógica del proyecto para simplificarla en la Semana 09.

## 17. Conexión con la Semana 09

La siguiente semana se simplificará la función mediante álgebra de Boole, De Morgan y mapas de Karnaugh. Después se actualizarán la simulación y el montaje en protoboard.

## 18. Profundización funcional y eléctrica

Una puerta lógica implementa una función, pero el encapsulado real también impone alimentación, corriente, fan-out, retardo y umbrales. AND exige todas las condiciones; OR, al menos una; NOT invierte; XOR detecta diferencia o paridad impar; XNOR detecta igualdad. NAND y NOR son universales porque permiten construir cualquier función.

Para una salida que alimenta varias entradas, el fan-out debe comprobarse por corriente:

\[
FO_H=\frac{|I_{OH,max}|}{I_{IH,max}},\qquad FO_L=\frac{I_{OL,max}}{|I_{IL,max}|}
\]

Se usa el menor valor. Los márgenes de ruido se estiman con `NM_H=V_OH(min)-V_IH(min)` y `NM_L=V_IL(max)-V_OL(max)`. Estas relaciones explican por qué una salida visualmente “alta” puede no estar garantizada y por qué una carga pesada degrada el nivel.

## 19. Ejemplo guiado adaptado

Para `Y=A·B`, `A=1` significa oscuridad y `B=1` habilitación. La tabla contiene cuatro casos y solo `11` activa el LED. Con un SN74LS08:

1. Se identifica el pin de la puerta, `VCC` y `GND` en la hoja de datos.
2. Los switches fijan niveles definidos; ninguna entrada queda abierta.
3. El LED lleva resistencia y se conecta según la capacidad de source/sink de la familia.
4. Se miden las tensiones de `A`, `B` y `Y`, no solo el estado visual.

Si la salida lógica controla una carga mayor, se mantiene como señal y se utiliza la etapa BJT/MOSFET del Corte 1. Una puerta no debe accionar un relé directamente.

## 20. Procedimiento de simulación y Lab 01

1. Construir y revisar la tabla antes del esquema.
2. Simular los cuatro casos y etiquetar entradas/salida.
3. Consultar pinout, alimentación, entradas no utilizadas y límites de corriente.
4. Montar rieles de alimentación y medirlos antes de insertar el CI.
5. Aplicar combinaciones en orden Gray para cambiar un bit a la vez cuando sea útil.
6. Registrar tensión de entrada y salida de cada caso.
7. Comparar tabla, simulación y montaje.
8. Integrar la salida con la etapa de potencia mediante referencia común y niveles compatibles.

## 21. Diagnóstico sistemático

La localización de averías sigue alimentación → entradas → puerta → salida → carga. Si todas las combinaciones fallan igual, se sospecha alimentación, referencia o pinout. Si falla solo una combinación, se revisa la entrada que cambia y la tabla. Si la salida del CI es correcta pero el LED no, la falla está aguas abajo. Sustituir el integrado es la última prueba, no la primera.

## 22. Preguntas orientadoras y trabajo independiente

- ¿La expresión representa realmente el requisito verbal?
- ¿Qué entradas no usadas deben fijarse y cómo?
- ¿Son compatibles los niveles entre sensor, CI y transistor?
- ¿Cuántas cargas puede manejar la salida?
- ¿Qué patrón mínimo aísla una puerta defectuosa?

El grupo documentará tabla, expresión, CI real, pinout, límites eléctricos, simulación, cuatro mediciones y una falla provocada segura. Explicará cómo la salida se conecta a la carga sin exceder al CI.

## 23. Referencias de estudio

- Floyd, 9.ª ed., cap. 3, secs. 3.1–3.6, pp. 124–154: NOT, AND, OR, NAND, NOR, XOR y XNOR.
- Ibid., sec. 3.8, pp. 164–173; sec. 3.9, pp. 174–197: lógica de función fija y localización de averías.
- Ibid., cap. 14, secs. 14.1–14.5, pp. 884–914: niveles, disipación, retardos, fan-out, CMOS y TTL.

## 24. Ruta de profundización recomendada

1. **Funciones lógicas:** Floyd, cap. 3, secs. 3.1–3.6, pp. 124–154.
2. **Circuitos integrados reales:** cap. 3, sec. 3.8, pp. 164–173.
3. **Diagnóstico prioritario:** cap. 3, sec. 3.9, pp. 174–197.
4. **Profundización eléctrica:** cap. 14, secs. 14.1–14.5, pp. 884–914, comparando niveles, corriente, fan-out, potencia y retardo TTL/CMOS.
