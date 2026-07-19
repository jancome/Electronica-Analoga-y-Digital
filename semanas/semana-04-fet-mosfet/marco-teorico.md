# Marco teórico – Semana 04

# MOSFET como interruptor y comparación con BJT

## Propósito

Diseñar y analizar una etapa de control de carga con MOSFET canal N, interpretar los parámetros básicos de su hoja de datos y comparar su uso con el BJT.

## Resultados de aprendizaje

- Identificar Gate, Drain y Source en el MOSFET seleccionado.
- Diferenciar VGS(th) del voltaje necesario para una conducción eficiente.
- Implementar resistencia de compuerta y resistencia pull-down.
- Estimar pérdidas de conducción mediante RDS(on).
- Proteger cargas inductivas y justificar la selección del dispositivo.
- Comparar BJT y MOSFET para una aplicación concreta.

## 1. Principio de control

El MOSFET es un dispositivo controlado por voltaje. En un MOSFET canal N, el voltaje entre Gate y Source controla la corriente que puede circular entre Drain y Source.

Sus terminales son:

- **Gate (G):** entrada de control.
- **Drain (D):** terminal conectado normalmente hacia la carga.
- **Source (S):** referencia del voltaje de compuerta.

![Comparación BJT vs MOSFET](../../recursos/imagenes/analogica/bjt-vs-mosfet-interruptor.svg)

## 2. VGS(th) no significa encendido completo

El parámetro VGS(th) indica la condición en la que comienza a circular una corriente pequeña de prueba. No garantiza que el MOSFET pueda controlar una carga con bajas pérdidas.

Para seleccionar el dispositivo se debe buscar en la hoja de datos el valor de RDS(on) especificado para el VGS disponible. Un MOSFET lógico puede tener RDS(on) especificada a 4,5 V o menos; otros requieren cerca de 10 V.

## 3. Interruptor de lado bajo

En una configuración típica:

1. La carga se conecta entre VCC y Drain.
2. Source se conecta a GND.
3. Gate recibe la señal de control por medio de una resistencia.
4. Una resistencia pull-down une Gate y Source.

La resistencia pull-down mantiene el dispositivo apagado cuando la señal de control está desconectada. La resistencia de Gate limita corrientes transitorias de carga y descarga de la capacitancia de entrada.

## 4. Pérdidas de conducción

Cuando el MOSFET está completamente activado, puede aproximarse:

```text
VDS(on) ≈ ID · RDS(on)
Pcond ≈ ID² · RDS(on)
```

### Ejemplo

Para una carga de 0,5 A y RDS(on) = 0,08 Ω:

```text
VDS(on) ≈ 0,5 A · 0,08 Ω = 0,04 V
Pcond ≈ (0,5 A)² · 0,08 Ω = 0,02 W
```

Estos valores solo son válidos si RDS(on) corresponde al VGS real y a condiciones térmicas compatibles.

## 5. Protección de cargas inductivas

Motores, relés y bobinas almacenan energía en un campo magnético. Al apagar el MOSFET aparece un pico de tensión. Se utiliza un diodo de rueda libre en antiparalelo con la carga, igual que en el control con BJT.

También debe verificarse que el MOSFET soporte VDS, ID, potencia y temperatura.

## 6. PWM

La modulación por ancho de pulso conmuta rápidamente el MOSFET. Al variar el ciclo de trabajo se controla el valor promedio aplicado a una carga, por ejemplo el brillo de un LED o la velocidad de un motor.

```text
Ciclo de trabajo = ton / T · 100 %
```

PWM es una actividad de profundización cuando se disponga de generador, microcontrolador o simulador.

## 7. BJT frente a MOSFET

| Criterio | BJT | MOSFET |
|---|---|---|
| Variable de control | Corriente de base | Voltaje Gate–Source |
| Estado activado | Saturación | Baja RDS(on) |
| Entrada | Requiere corriente continua | Principalmente carga/descarga capacitiva |
| Diseño | Resistencia de base | Gate, pull-down y VGS adecuado |
| Uso típico | Control sencillo de baja corriente | Conmutación eficiente y PWM |

La elección depende de la carga, la señal disponible, las pérdidas permitidas, la velocidad de conmutación y la disponibilidad del componente.

## 8. Errores frecuentes

- Suponer el pinout por la forma del encapsulado.
- Usar un IRFZ44N con 3,3 V sin verificar RDS(on).
- Dejar Gate flotante.
- Confundir VGS con el voltaje de Gate respecto a cualquier punto.
- Omitir GND común.
- Omitir el diodo de protección.
- Interpretar VGS(th) como voltaje de conducción plena.

## 9. Conexión con el Lab A03 y el ABP

El Lab A03 debe comprobar como núcleo el control de LED, la variación de VGS y el control protegido de una carga. PWM y la comparación extendida con BJT pueden desarrollarse como profundización.

Para cerrar el Preproyecto ABP 1, el grupo debe justificar:

- Dispositivo escogido.
- Voltaje de control disponible.
- Corriente de carga.
- RDS(on) o VCE(sat), según el dispositivo.
- Protección implementada.
- Mediciones que demuestran estado activado y desactivado.

## 10. Comprobación de aprendizaje

1. ¿Por qué VGS(th) no garantiza control eficiente de una carga?
2. ¿Qué función cumple la resistencia pull-down?
3. ¿Cómo se estiman las pérdidas de conducción?
4. ¿Qué criterio usaría para escoger entre BJT y MOSFET?
5. ¿Qué mediciones comprobarían que el MOSFET está correctamente activado?

## Fuentes de consulta

- R. L. Boylestad y L. Nashelsky, *Teoría de circuitos y dispositivos electrónicos*.
- T. L. Floyd, *Dispositivos electrónicos*.
- Hoja de datos del MOSFET empleado.
- All About Circuits, secciones de MOSFET y transistores de efecto de campo.

