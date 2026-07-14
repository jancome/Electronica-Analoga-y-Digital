# Marco teórico – Semana 15

# Multiplexores y demultiplexores

## 1. Tema de la semana

Circuitos combinacionales para selección y distribución de datos digitales.

## 2. Objetivo de aprendizaje

Comprender el funcionamiento de multiplexores y demultiplexores, relacionando sus entradas de selección con aplicaciones de comunicación, control y procesamiento digital.

## 3. Contexto

En sistemas digitales no siempre se pueden conectar todas las señales al mismo tiempo. A veces se necesita seleccionar una señal entre muchas o distribuir una señal hacia diferentes destinos. Para eso se usan multiplexores y demultiplexores.

## 4. Multiplexor

Un multiplexor, o MUX, selecciona una de varias entradas y la conecta a una única salida.

Por ejemplo, un MUX 4 a 1 tiene:

- 4 entradas de datos.
- 2 líneas de selección.
- 1 salida.

## 5. Entradas de selección

Las líneas de selección determinan cuál entrada se envía a la salida.

| S1 | S0 | Entrada seleccionada |
|---|---|---|
| 0 | 0 | I0 |
| 0 | 1 | I1 |
| 1 | 0 | I2 |
| 1 | 1 | I3 |

## 6. Demultiplexor

Un demultiplexor, o DEMUX, toma una entrada y la dirige hacia una de varias salidas, según las líneas de selección.

## 7. Aplicaciones reales

- Selección de canales de comunicación.
- Sistemas de adquisición de datos.
- Control de displays.
- Distribución de señales de control.
- Optimización de conexiones en sistemas digitales.

## 8. Ejemplo guiado

Si un MUX 4 a 1 tiene S1=1 y S0=0, la salida corresponde a la entrada I2.

```text
S1S0 = 10 → Y = I2
```

## 9. Errores comunes

- Confundir MUX con DEMUX.
- Conectar mal las líneas de selección.
- No identificar si las salidas son activas en bajo.
- No considerar la entrada de habilitación del circuito integrado.
- No verificar la hoja de datos del integrado.

## 10. Preguntas orientadoras

1. ¿Qué función cumple un multiplexor?
2. ¿Qué función cumple un demultiplexor?
3. ¿Cuántas líneas de selección necesita un MUX de 8 entradas?
4. ¿Qué significa seleccionar una entrada?
5. ¿Dónde se usan MUX y DEMUX en sistemas reales?

## 11. Trabajo independiente

Simular un MUX 4 a 1 y un DEMUX 1 a 4, completando sus tablas de funcionamiento.
