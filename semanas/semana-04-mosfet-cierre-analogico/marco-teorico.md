# Marco teórico – Semana 04

# FET/MOSFET, control eficiente de cargas y cierre analógico

## Metas de aprendizaje verificables

- Explicar por qué `VGS(th)` no equivale a conducción plena y seleccionar un MOSFET compatible.
- Estimar caída, pérdidas y temperatura y justificar gate, pull-down y protección inductiva.
- Comparar BJT y MOSFET con evidencia eléctrica y escoger la etapa del ABPr.

## 1. Propósito de la semana

Comprender el MOSFET como interruptor controlado por voltaje, compararlo con el BJT y seleccionar una alternativa apropiada para controlar cargas de baja potencia en el proyecto ABPr.

La semana también se utiliza para cerrar técnicamente la etapa analógica y preparar el Preproyecto ABPr 1.

## 2. Resultado de aprendizaje

Al finalizar la semana, el estudiante estará en capacidad de:

- Identificar Gate, Drain y Source.
- Explicar la importancia de `VGS` y `RDS(on)`.
- Diferenciar un MOSFET de canal N de uno de canal P.
- Implementar un MOSFET canal N como interruptor de baja conexión.
- Seleccionar resistencias de Gate y pull-down.
- Comparar BJT y MOSFET con criterios eléctricos.
- Verificar corriente, potencia y temperatura.
- Consolidar la arquitectura y la simulación de la Fase 1.

## 3. Conexión con la Fase 1 ABPr

El proyecto puede utilizar BJT o MOSFET para accionar una salida:

```text
Etapa AC/DC
     ↓
Condición o señal de control
     ↓
BJT / MOSFET
     ↓
Indicador o carga de baja potencia
```

El componente no debe elegirse por costumbre. La selección debe justificarse según voltaje de control, corriente de carga, pérdidas y disponibilidad.

## 4. Estructura del MOSFET

Terminales principales:

- **Gate (G):** compuerta de control.
- **Drain (D):** drenador.
- **Source (S):** fuente.

En un MOSFET canal N de baja conexión, la carga se ubica entre la alimentación y el Drain, mientras el Source se conecta a GND.

## 5. Control mediante voltaje Gate–Source

La variable de control es:

```text
VGS = VG - VS
```

El dato `VGS(th)` de la hoja de datos indica el inicio de una conducción pequeña, no necesariamente la condición adecuada para manejar la corriente nominal.

Para utilizar señales de 3.3 V o 5 V debe seleccionarse un MOSFET **logic level** cuya `RDS(on)` esté especificada al voltaje de control disponible.

## 6. Resistencia de Gate y pull-down

### Resistencia de Gate

Limita los picos de corriente durante la carga y descarga de la capacitancia de compuerta y ayuda a controlar oscilaciones.

### Resistencia pull-down

Mantiene el Gate en 0 V cuando la señal de control está desconectada o en alta impedancia.

Sin pull-down, la carga almacenada en el Gate puede producir encendidos no deseados.

## 7. Pérdidas por conducción

Una aproximación de la potencia disipada es:

```text
PMOSFET ≈ ID² × RDS(on)
```

La resistencia `RDS(on)` depende de `VGS`, temperatura y dispositivo. Debe consultarse la hoja de datos.

## 8. Protección de cargas inductivas

Al igual que con el BJT, una bobina requiere una ruta de descarga. Para cargas DC se utiliza un diodo de rueda libre conectado en paralelo con la bobina.

El diodo interno del MOSFET no reemplaza automáticamente la protección de la carga; la topología completa debe analizarse.

## 9. Comparación BJT y MOSFET

| Criterio | BJT | MOSFET |
|---|---|---|
| Variable de control | Corriente de base | Voltaje Gate–Source |
| Corriente de entrada permanente | Sí | Muy pequeña en estado estable |
| Pérdida principal | `VCE(sat) × IC` | `ID² × RDS(on)` |
| Selección de control | Resistencia de base | Nivel lógico, resistencia Gate y pull-down |
| Aplicación introductoria | Cargas pequeñas | Control eficiente de cargas DC |

## 10. Ejemplo guiado

Una carga consume 0.5 A y el MOSFET presenta:

```text
RDS(on) = 0.08 Ω
```

La pérdida aproximada es:

```text
P = (0.5 A)² × 0.08 Ω
P = 0.02 W
```

El cálculo debe repetirse con el valor de `RDS(on)` correspondiente al `VGS` y a la temperatura reales.

## 11. Actividad de clase y Lab A03

Cada grupo deberá:

1. Identificar el pinout del MOSFET.
2. Consultar `VGS(th)`, `RDS(on)`, corriente y potencia máximas.
3. Simular el control de una carga.
4. Agregar resistencia de Gate y pull-down.
5. Incorporar protección si la carga es inductiva.
6. Comparar el circuito con la alternativa BJT.
7. Seleccionar justificadamente la etapa de salida de su proyecto.

## 12. Cierre técnico de la Fase 1

Antes de la entrega, el grupo debe verificar:

- Situación específica y justificación.
- Objetivos.
- Diagrama de bloques.
- Etapa AC/DC simulada.
- Cálculos de rectificación, filtrado y regulación.
- Indicador y protección.
- Posible etapa de control con BJT o MOSFET.
- Lista de materiales.
- Roles de los integrantes.
- Fallas pendientes y plan de corrección.

## 13. Evidencia ABPr

- Simulación consolidada de la etapa analógica.
- Comparación técnica BJT–MOSFET.
- Hoja de datos consultada.
- Cálculos y capturas.
- Diagrama de bloques actualizado.
- Decisión de diseño justificada.

## 14. Errores comunes

- Elegir un MOSFET únicamente por su corriente máxima anunciada.
- Interpretar `VGS(th)` como voltaje de encendido completo.
- No usar resistencia pull-down.
- Confundir Drain y Source.
- Ignorar la disipación térmica.
- No compartir GND cuando el circuito lo requiere.
- Superar límites de la fuente o la carga.

## 15. Trabajo independiente

- Completar el informe del Lab A03.
- Consolidar el Preproyecto ABPr 1.
- Corregir cálculos y simulación.
- Preparar una explicación individual del bloque trabajado.
- Repasar los temas para el Quiz 1 y el Parcial 1.

## 16. Conexión con la Semana 05

La Semana 05 no introduce contenido nuevo. Se utilizará para integración conceptual, retroalimentación, entrega del Preproyecto ABPr 1 y aplicación del Parcial 1.

## 17. Profundización: MOSFET como interruptor real

En un MOSFET de enriquecimiento canal N, una `V_GS` positiva forma el canal conductor. La compuerta aislada demanda corriente continua casi nula, aunque en cada transición se carga o descarga su capacitancia. Una resistencia serie limita picos y oscilaciones; la pull-down fija `V_GS=0` si la señal queda desconectada.

`V_GS(th)` solo identifica el comienzo de conducción con una corriente de ensayo pequeña. La selección debe basarse en `R_DS(on)` especificada a una `V_GS` compatible con el control:

\[
P_{cond}\approx I_D^2R_{DS(on)},\qquad V_{DS(on)}\approx I_DR_{DS(on)}
\]

El cálculo térmico preliminar usa `T_J≈T_A+P_Dθ_JA`. También se revisan `V_DS(max)`, `V_GS(max)`, `I_D`, área segura y protección ESD.

## 18. Ejemplo guiado adaptado y comparación

Una carga de `5 V`, `150 mA` se controla con `3,3 V`. Un MOSFET logic-level especifica `R_DS(on)=0,20 Ω` a `V_GS=2,5 V`.

1. `V_DS(on)≈0,15×0,20=0,030 V`.
2. `P_cond≈0,15²×0,20=4,5 mW`.
3. Con `100 Ω` en gate y `100 kΩ` pull-down, la entrada queda definida al arrancar.
4. Si la carga es inductiva, se añade el diodo de rueda libre.

Un BJT con `V_CE(sat)≈0,2 V` disiparía cerca de `30 mW` y requeriría corriente de base. Esto favorece al MOSFET, pero la elección final incluye tensión de gate, costo, disponibilidad y robustez.

## 19. Procedimiento de simulación y Lab A03

1. Verificar terminales `G`, `D`, `S` y parámetros a la tensión real.
2. Simular apagado/encendido y medir `V_GS`, `V_DS` e `I_D`.
3. Desconectar virtualmente la entrada para demostrar la necesidad del pull-down.
4. Comparar modelo genérico con el componente escogido.
5. Montar con manejo ESD y alimentación desconectada.
6. Medir primero sin carga y luego con carga resistiva segura.
7. Incorporar la carga final y observar calentamiento y caída de tensión.
8. Documentar la decisión BJT/MOSFET con una matriz de criterios.

## 20. Diagnóstico de fallas

| Síntoma | Causa probable | Prueba |
|---|---|---|
| carga se activa sola | gate flotante | medir `V_GS`; comprobar pull-down |
| MOSFET calienta | `V_GS` insuficiente, pinout o selección incorrecta | medir `V_GS`, `V_DS` e `I_D` |
| carga no enciende | tierras separadas, dispositivo invertido o señal ausente | medir terminales respecto a source |
| daño al apagar bobina | diodo ausente o invertido | revisar polaridad y sobretensión |
| simula bien y monta mal | modelo ideal o parámetro incompatible | contrastar `R_DS(on)` a `V_GS` real |

## 21. Preguntas orientadoras y trabajo independiente

- ¿La hoja de datos especifica `R_DS(on)` a la tensión disponible?
- ¿Qué garantiza el apagado durante el arranque?
- ¿Cuál es la diferencia entre umbral y conducción plena?
- ¿Qué pérdidas dominan a baja y alta frecuencia?
- ¿Qué medición separa una falla de gate de una de carga?

El grupo entregará cálculos, selección por hoja de datos, simulación con falla de gate flotante, matriz BJT–MOSFET y justificación de la etapa elegida.

## 22. Referencias de estudio

- Boylestad y Nashelsky, 10.ª ed., cap. 6, secs. 6.8–6.13, pp. 392–405: MOSFET de enriquecimiento, manejo y síntesis FET.
- Ibid., cap. 7, secs. 7.8 y 7.11, pp. 433 y 442: polarización y diseño.
- Ibid., cap. 7, secs. 7.12 y 7.15, pp. 445–462: fallas y aplicaciones prácticas.

## 23. Ruta de profundización recomendada

1. **Fundamento del dispositivo:** Boylestad, cap. 6, sec. 6.8, p. 392 en adelante, para MOSFET de enriquecimiento.
2. **Manejo y familias:** cap. 6, secs. 6.9–6.13, pp. 399–405.
3. **Diseño obligatorio:** cap. 7, secs. 7.8 y 7.11, pp. 433 y 442.
4. **Profundización aplicada:** cap. 7, secs. 7.12 y 7.15, pp. 445–462, para fallas y aplicaciones; contrastar siempre con la hoja de datos del MOSFET escogido.
