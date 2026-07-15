# Quiz 1 – Unidad analógica

**Corte:** 1  
**Semana de aplicación:** Semana 04, al inicio de la clase  
**Peso:** 2% de la nota final  
**Modalidad:** individual  
**Tiempo sugerido:** 20 a 25 minutos

## Indicaciones para el estudiante

- Responda con letra clara y ordenada.
- Justifique los cálculos.
- Use unidades en todas las respuestas numéricas.
- No se permite el uso de celular durante el quiz, salvo autorización del docente.
- El quiz está orientado principalmente a ejercicios cortos de aplicación.

---

## Ejercicios

### 1. Ley de Ohm y potencia

Una resistencia de **1 kΩ** se conecta a una fuente de **5 V DC**.

Calcule:

- Corriente del circuito.
- Potencia disipada en la resistencia.

**Valor:** 0.6 puntos

---

### 2. Circuito serie

En un circuito serie se conectan una fuente de **12 V**, una resistencia de **1 kΩ** y una resistencia de **2.2 kΩ**.

Calcule:

- Resistencia equivalente.
- Corriente total.
- Voltaje en cada resistencia.

**Valor:** 0.7 puntos

---

### 3. LED con resistencia limitadora

Se desea encender un LED rojo con una fuente de **9 V**. El LED tiene una caída aproximada de **2 V** y se desea una corriente de **10 mA**.

Calcule:

- Resistencia limitadora.
- Potencia aproximada en la resistencia.

**Valor:** 0.7 puntos

---

### 4. Diodo en polarización directa

Un circuito tiene una fuente de **5 V**, una resistencia de **1 kΩ** y un diodo de silicio en polarización directa. Suponga una caída en el diodo de **0.7 V**.

Calcule la corriente aproximada del circuito.

**Valor:** 0.5 puntos

---

### 5. Señal AC y rectificación

Una señal de **6 V RMS** entra a un rectificador.

Calcule el voltaje pico aproximado de entrada.

**Valor:** 0.5 puntos

---

### 6. Regulador con Zener

Un regulador básico usa una fuente de **12 V**, un diodo Zener de **5.1 V** y una resistencia serie de **330 Ω**. Suponga que no hay carga conectada.

Calcule la corriente aproximada por la resistencia serie.

**Valor:** 0.6 puntos

---

### 7. Resistencia de base en BJT

Se desea activar un BJT NPN desde una señal de control de **5 V**. Suponga **VBE = 0.7 V** y una corriente de base deseada de **2 mA**.

Calcule la resistencia de base aproximada.

**Valor:** 0.7 puntos

---

### 8. MOSFET como control de carga

Un MOSFET canal N controla una carga de **12 V** y **120 Ω**.

Calcule:

- Corriente de la carga.
- Explique brevemente por qué se recomienda usar una resistencia pull-down en la compuerta.

**Valor:** 0.7 puntos

---

## Total

**5.0 puntos**

---

# Rúbrica de calificación

| Criterio | Peso |
|---|---:|
| Procedimiento y planteamiento | 30% |
| Cálculos correctos | 40% |
| Uso de unidades | 15% |
| Interpretación breve de resultados | 15% |

---

# Versión con respuestas orientadoras para el docente

> Esta sección es de apoyo docente. Puede retirarse antes de entregar el quiz a los estudiantes.

## Respuestas esperadas

1. `I = V/R = 5 V / 1000 Ω = 0.005 A = 5 mA`. `P = V × I = 5 V × 0.005 A = 0.025 W = 25 mW`.
2. `Req = 3.2 kΩ`. `I = 12 V / 3200 Ω = 3.75 mA`. `VR1 = 3.75 V`. `VR2 = 8.25 V`.
3. `R = (9 V - 2 V) / 0.01 A = 700 Ω`. Potencia: `P = 7 V × 0.01 A = 0.07 W`. Puede usarse valor comercial cercano verificando corriente.
4. `I = (5 V - 0.7 V) / 1000 Ω = 4.3 mA`.
5. `VP = VRMS × √2 = 6 V × 1.414 ≈ 8.48 V`.
6. `I = (12 V - 5.1 V) / 330 Ω ≈ 20.9 mA`.
7. `RB = (5 V - 0.7 V) / 0.002 A = 2150 Ω`. Valor comercial cercano: `2.2 kΩ`.
8. `I = 12 V / 120 Ω = 0.1 A = 100 mA`. La resistencia pull-down evita que la compuerta quede flotante y que el MOSFET se active por ruido o carga residual.
