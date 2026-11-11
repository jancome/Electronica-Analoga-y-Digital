# Marco teórico – Semana 14

# 3.4 Aplicaciones con multiplexores y demultiplexores

## 1. Propósito de la semana

Comprender la selección y distribución de señales mediante MUX y DEMUX y revisar la integración del prototipo ABPr.

La primera revisión física permite detectar fallas. La muestra formativa con maqueta se realiza en la semana 15.

## 2. Resultado de aprendizaje

Al finalizar la semana, el estudiante estará en capacidad de:

- Explicar el funcionamiento de un multiplexor.
- Explicar el funcionamiento de un demultiplexor.
- Calcular la cantidad de líneas de selección.
- Interpretar habilitaciones y salidas activas en bajo.
- Seleccionar o distribuir señales dentro de una aplicación.
- Determinar si MUX o DEMUX aporta al proyecto.
- Presentar un prototipo físico funcional y recibir retroalimentación.

## 3. Conexión con la Fase 3 ABPr

Un MUX o DEMUX puede optimizar conexiones, pero no debe incorporarse sin necesidad.

Ejemplos:

- Seleccionar una de varias señales de sensores.
- Elegir modos de operación.
- Compartir una línea de visualización.
- Distribuir una señal de control a diferentes salidas.

## 4. Multiplexor

Un multiplexor selecciona una de varias entradas y la conecta a una salida.

Para un MUX de `2ⁿ` entradas se requieren `n` líneas de selección.

Ejemplo MUX 4 a 1:

| S1 | S0 | Salida |
|---|---|---|
| 0 | 0 | `Y=I0` |
| 0 | 1 | `Y=I1` |
| 1 | 0 | `Y=I2` |
| 1 | 1 | `Y=I3` |

## 5. Entrada de habilitación

Muchos integrados tienen una entrada Enable. Puede ser activa en alto o activa en bajo.

Si la habilitación no está en el estado correcto, el circuito no funcionará aunque las líneas de selección estén bien conectadas.

## 6. Demultiplexor

Un DEMUX recibe una entrada y la dirige hacia una de varias salidas según las líneas de selección.

Puede utilizarse para:

- Distribuir pulsos.
- Seleccionar actuadores.
- Dirigir una señal de habilitación.
- Activar indicadores por canal.

## 7. Decodificador utilizado como DEMUX

Algunos decodificadores pueden utilizarse como demultiplexores si su entrada de habilitación recibe la señal de datos. La hoja de datos debe confirmar el comportamiento y la polaridad de las salidas.

## 8. Implementación de funciones con MUX

Un multiplexor también puede implementar funciones lógicas conectando sus entradas de datos a 0, 1 o variables.

El procedimiento incluye:

1. Elegir variables de selección.
2. Analizar la tabla de verdad.
3. Determinar el valor de cada entrada de datos.
4. Verificar la función resultante.

## 9. Ejemplo aplicado

Un sistema debe mostrar alternativamente el estado de cuatro sensores en una sola línea de visualización. Un MUX 4 a 1 permite seleccionar el sensor mediante dos líneas.

La aplicación es válida solo si la selección mejora el diseño o reduce recursos.

## 10. Actividad de clase y Lab 08

1. Completar tablas de MUX y DEMUX.
2. Simular un MUX 4 a 1.
3. Simular o montar un DEMUX 1 a 4.
4. Verificar la habilitación.
5. Probar todas las selecciones.
6. Evaluar si el bloque aporta al proyecto.
7. Integrarlo cuando sea pertinente.

## 11. Primera revisión física y evidencias

Presentar la etapa analógica, la lógica digital, el diagrama actualizado, la alimentación y las entradas/salidas identificadas. Registrar las pruebas del Lab 08 y las correcciones pendientes. La maqueta puede estar en construcción.

## 12. Continuidad

La semana 15 desarrolla el tema 3.5, teclado matricial y display de 7 segmentos, junto con la muestra formativa del proyecto.
