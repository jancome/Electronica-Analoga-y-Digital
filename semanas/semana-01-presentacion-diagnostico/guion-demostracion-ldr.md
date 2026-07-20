# Guion de demostración – Iluminación automática con LDR

## Para qué se usa

El montaje abre la clase con un sistema que los estudiantes pueden observar, cuestionar y medir antes de recibir una explicación formal. La intención no es presentar el circuito terminado, sino convertirlo en una situación de investigación:

> Al cambiar la iluminación sobre el sensor, el circuito modifica el estado de un LED. ¿Qué variable cambió, dónde se tomó la decisión y cómo podríamos comprobarlo?

## Montaje sugerido

- Protoboard.
- Fuente regulada de 5 V.
- Fotoresistencia LDR.
- Resistencia fija de 10 kΩ para formar un divisor de voltaje.
- Módulo comparador LM393 o un comparador equivalente.
- Potenciómetro de ajuste, si el módulo lo incorpora.
- LED y resistencia limitadora de 220 Ω a 1 kΩ.
- Multímetro.
- Cables de conexión.

> Trabajar únicamente con baja tensión. Verificar polaridad, continuidad de las líneas de alimentación y resistencia del LED antes de energizar.

## Secuencia de preguntas

### 1. Observar sin explicar

Cubra y descubra la LDR. No mencione todavía el nombre de los componentes.

- ¿Qué cambió en el entorno?
- ¿Qué cambió en la salida del circuito?
- ¿El LED cambia gradualmente o conmuta entre dos estados?
- ¿Qué parte del montaje creen que detecta la luz?
- ¿Qué evidencia necesitaríamos para respaldar la respuesta?

Registre en el tablero dos o tres hipótesis sin indicar cuál es correcta.

### 2. Predecir antes de medir

Muestre la LDR y el divisor de voltaje.

- Si la resistencia de la LDR disminuye cuando recibe más luz, ¿qué debería ocurrir con el voltaje del nodo de medición?
- ¿La respuesta cambia si la LDR está arriba o abajo en el divisor?
- ¿En qué punto conectarían el voltímetro?
- ¿Qué referencia usarían para la medición?

Cada estudiante escribe una predicción. Luego la contrasta con su equipo de tres integrantes.

### 3. Medir y contrastar

Asigne roles rotativos: una persona modifica la luz, otra mide y otra registra.

Mida como mínimo:

| Condición | Resistencia aproximada de la LDR | Voltaje del sensor | Estado del LED |
|---|---:|---:|---|
| Luz intensa | | | |
| Luz ambiente | | | |
| Oscuridad | | | |

Preguntas para la puesta en común:

- ¿Los datos confirman la predicción?
- ¿Qué relación observan entre luz, resistencia y voltaje?
- ¿Dónde aparece la Ley de Ohm?
- ¿Qué corriente circula por el LED y cómo se limita?
- ¿Qué diferencias existen entre lo calculado y lo medido?

### 4. Identificar la decisión

Explique el papel del LM393 después de que los equipos hayan interpretado sus datos.

- ¿Qué dos voltajes compara el circuito?
- ¿Qué significa ajustar el potenciómetro?
- ¿La señal del sensor es analógica o digital?
- ¿La salida del comparador es analógica o digital?
- ¿Qué ocurre cuando el voltaje del sensor cruza el valor de referencia?
- ¿Qué podría provocar encendidos y apagados repetitivos cerca del umbral?

La idea central se resume así:

```text
Condición de luz → LDR y divisor → comparación con una referencia → acción del LED
```

### 5. Conectar con el ABP

- ¿En qué lugar de Barranquilla o la región Caribe sería útil encender una carga solo cuando se necesita?
- ¿Qué problema de energía, agua o seguridad podría observarse con un sensor?
- ¿Cuál sería la variable de entrada?
- ¿Qué decisión debería tomar el circuito?
- ¿Cuál sería la acción de salida?
- ¿Qué indicador demostraría que la solución funciona o ahorra energía?

Cada equipo completa esta frase:

> Queremos ayudar a ________. Mediremos ________. El sistema actuará cuando ________. Sabremos que funciona si ________.

## Cierre de la demostración

Pida una explicación de un minuto que incluya cinco palabras: **luz, resistencia, voltaje, comparación y acción**. La conclusión debe enlazar el montaje con el proyecto:

> Una necesidad del entorno puede convertirse en una variable medible; esa variable se compara con un criterio y produce una acción que debe validarse con datos.

## Evidencias de aprendizaje

- Predicción individual.
- Tabla de mediciones del equipo.
- Explicación oral breve.
- Respuesta del diagnóstico en Microsoft Forms.
- Primera formulación del reto ABP.
