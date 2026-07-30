# Marco teórico – Semana 04

# FET/MOSFET, control eficiente de cargas y cierre analógico

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