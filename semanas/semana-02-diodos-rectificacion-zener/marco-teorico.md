# Marco teórico – Semana 02

# Semiconductores, diodos, rectificación, filtrado y Zener

## 1. Propósito de la semana

Comprender el diodo como dispositivo semiconductor y utilizarlo para iniciar la etapa común AC/DC de la Fase 1 del proyecto ABPr.

Esta semana integra fundamentos que antes aparecían separados: unión PN, polarización del diodo, rectificación, filtrado, LED y regulación básica con Zener.

## 2. Resultado de aprendizaje

Al finalizar la semana, el estudiante estará en capacidad de:

- Explicar de forma básica la formación de una unión PN.
- Diferenciar polarización directa e inversa.
- Analizar circuitos simples con diodos mediante Ley de Ohm y Kirchhoff.
- Comparar rectificación de media onda y onda completa.
- Explicar el efecto de un capacitor de filtrado.
- Dimensionar una resistencia para LED.
- Reconocer el funcionamiento básico de un regulador Zener.
- Simular la etapa común AC/DC del Preproyecto ABPr 1.

## 3. Conexión con la Fase 1 ABPr

Todos los grupos desarrollarán una base analógica común:

```text
AC de baja tensión
        ↓
Rectificación
        ↓
Filtrado
        ↓
Regulación / protección
        ↓
Indicador de estado
```

Esta etapa deberá diseñarse y simularse antes de cualquier montaje físico.

## 4. Materiales semiconductores y unión PN

Un semiconductor tiene una conductividad intermedia entre un conductor y un aislante. Su comportamiento puede modificarse mediante dopaje.

- **Tipo N:** predominan electrones como portadores mayoritarios.
- **Tipo P:** predominan huecos como portadores mayoritarios.

Al unir regiones P y N aparece una **región de agotamiento**, que condiciona el paso de corriente.

## 5. Diodo semiconductor

El diodo tiene dos terminales:

- **Ánodo.**
- **Cátodo**, normalmente identificado mediante una banda.

### Polarización directa

El diodo conduce cuando el ánodo se encuentra a mayor potencial que el cátodo y se supera su tensión de conducción.

Para un diodo de silicio, en un modelo práctico:

```text
VD ≈ 0.7 V
```

### Polarización inversa

El diodo bloquea la corriente, salvo una pequeña fuga, mientras no se supere su tensión inversa máxima.

## 6. Análisis con Ley de Ohm y Kirchhoff

En una malla formada por fuente, resistencia y diodo:

```text
VS = VR + VD
VR = VS - VD
I = VR / R
```

El diodo nunca debe analizarse aislado: la resistencia, la fuente y la carga determinan la corriente real.

## 7. Señales AC, RMS y valor pico

Para una señal senoidal ideal:

```text
VP = VRMS × √2
```

El valor pico permite estimar el máximo voltaje disponible después de la rectificación, antes de considerar las caídas en los diodos.

## 8. Rectificación

### Media onda

Utiliza un diodo y aprovecha un solo semiciclo de la señal AC.

- Circuito sencillo.
- Mayor rizado.
- Menor aprovechamiento de la energía disponible.

### Puente rectificador

Utiliza cuatro diodos y aprovecha ambos semiciclos. En cada semiciclo conducen dos diodos.

```text
Vsalida,pico ≈ VP - 2VD
```

Para diodos de silicio, la caída aproximada del puente es de 1.4 V.

## 9. Filtrado capacitivo

El capacitor se conecta en paralelo con la carga. Se carga cerca del valor máximo de la señal rectificada y entrega energía cuando el voltaje de entrada disminuye.

Al aumentar la capacitancia:

- Disminuye el rizado.
- La salida se aproxima más a una DC constante.
- Puede aumentar la corriente inicial de carga.

Una aproximación útil del rizado es:

```text
ΔV ≈ Iload / (frizado × C)
```

En un puente de onda completa, la frecuencia de rizado es aproximadamente el doble de la frecuencia de la señal AC.

## 10. LED y resistencia limitadora

Un LED requiere una resistencia en serie:

```text
R = (VS - VLED) / ILED
```

También debe verificarse la potencia:

```text
PR = ILED² × R
```

## 11. Regulación básica con Zener

El Zener se utiliza en polarización inversa dentro de su zona de ruptura controlada. Con una resistencia serie puede mantener una tensión aproximadamente constante.

La resistencia debe limitar la corriente total:

```text
Rserie = (Vin - VZ) / (IZ + Iload)
```

Se debe comprobar:

```text
PZ = VZ × IZ
```

## 12. Ejemplo aplicado

Para una fuente de 6 V RMS:

```text
VP ≈ 6 × 1.414 = 8.48 V
```

Después de un puente de silicio:

```text
Vsalida,pico ≈ 8.48 - 1.4 = 7.08 V
```

La salida real dependerá de la corriente de carga, el capacitor y la regulación utilizada.

## 13. Actividad de clase y laboratorio

Cada grupo deberá:

1. Seleccionar una tensión AC segura de baja tensión.
2. Simular media onda y puente rectificador.
3. Comparar formas de onda.
4. Agregar un capacitor y medir el rizado.
5. Incorporar un LED indicador.
6. Proponer regulación básica con Zener o regulador autorizado.
7. Registrar voltajes en cada bloque.

## 14. Evidencia ABPr de la semana

- Esquema de la etapa AC/DC.
- Simulación funcional.
- Cálculos de voltaje pico, resistencias y potencia.
- Capturas de las formas de onda.
- Primera lista de componentes.
- Explicación del aporte de esta etapa al proyecto.

## 15. Seguridad

- No conectar protoboard directamente a la red de 120 V.
- Utilizar transformador de baja tensión, fuente de laboratorio o simulador.
- Verificar polaridad del capacitor y del LED.
- Descargar capacitores antes de modificar el circuito.
- Revisar el voltaje nominal de los componentes.

## 16. Errores comunes

- Confundir voltaje RMS con voltaje pico.
- Olvidar las caídas del puente rectificador.
- Suponer que la señal rectificada ya es DC constante.
- Invertir el capacitor electrolítico.
- Conectar un LED sin resistencia.
- Usar el Zener sin limitar corriente.

## 17. Trabajo independiente

- Completar la simulación de la etapa común.
- Consultar las hojas de datos de los diodos y Zener seleccionados.
- Registrar preguntas y diferencias entre cálculo y simulación.
- Preparar el Lab A01 y el avance del Preproyecto ABPr 1.

## 18. Conexión con la Semana 03

La siguiente semana se estudiará el BJT como interruptor para controlar una carga de baja potencia a partir de una señal pequeña.