# Parcial 1 – Unidad analógica

**Corte:** 1  
**Semana de aplicación:** Semana 05  
**Peso:** 20% de la nota final  
**Modalidad:** individual  
**Tiempo sugerido:** 90 a 120 minutos  

## Temas evaluados

- Fundamentos básicos de circuitos.
- Señales y medición.
- Diodos y unión PN.
- LED y resistencia limitadora.
- Rectificación y filtrado.
- Diodo Zener.
- BJT como interruptor.
- FET/MOSFET como dispositivo de control.

---

## Indicaciones para el estudiante

- Responda de forma clara y ordenada.
- Justifique todos los procedimientos.
- Use unidades en cada resultado numérico.
- Cuando sea necesario, dibuje el circuito o diagrama de apoyo.
- No basta con escribir el resultado final; se evaluará el procedimiento.
- El uso de calculadora básica queda sujeto a indicación del docente.

---

# Parte A – Fundamentos de circuitos y medición

## 1. Circuito resistivo y Ley de Ohm

Se tiene una fuente de **12 V DC** conectada a dos resistencias en serie:

```text
R1 = 1 kΩ
R2 = 2.2 kΩ
```

Calcule:

1. Resistencia equivalente.
2. Corriente total.
3. Voltaje en cada resistencia.
4. Potencia disipada en cada resistencia.

**Valor:** 1.0 punto

---

## 2. Medición eléctrica

Explique cómo se debe conectar un multímetro para medir voltaje en una resistencia y cómo se debe conectar para medir corriente en una rama del circuito.

Incluya una precaución importante para cada medición.

**Valor:** 0.5 puntos

---

# Parte B – Señales y rectificación

## 3. Valor RMS y valor pico

Una señal senoidal tiene un valor de **9 V RMS**.

Calcule el valor pico aproximado.

Use:

```text
VP = VRMS × √2
```

Explique por qué este valor es importante al analizar un rectificador.

**Valor:** 0.6 puntos

---

## 4. Rectificador de media onda

Explique qué ocurre con una señal AC cuando pasa por un rectificador de media onda con un diodo ideal.

Luego indique qué diferencia habría si se considera un diodo de silicio real.

**Valor:** 0.6 puntos

---

## 5. Rectificador de onda completa con filtro

En una fuente básica se utiliza un puente rectificador y un capacitor de filtrado.

Explique:

1. Qué función cumple el puente rectificador.
2. Qué función cumple el capacitor.
3. Qué significa rizado.
4. Qué ocurre con el rizado cuando se aumenta la capacitancia.

**Valor:** 0.8 puntos

---

# Parte C – Diodo, LED y Zener

## 6. Circuito con diodo de silicio

Se tiene el siguiente circuito:

```text
Fuente = 5 V DC
Resistencia = 1 kΩ
Diodo de silicio en polarización directa
VD ≈ 0.7 V
```

Calcule:

1. Voltaje en la resistencia.
2. Corriente aproximada del circuito.
3. Potencia en la resistencia.

Explique por qué la resistencia es necesaria.

**Valor:** 0.9 puntos

---

## 7. LED con resistencia limitadora

Se desea encender un LED usando una fuente de **12 V**.

Datos:

```text
VLED = 2 V
ILED = 15 mA
```

Calcule:

1. Resistencia limitadora.
2. Valor comercial cercano recomendado.
3. Potencia aproximada en la resistencia.

**Valor:** 0.8 puntos

---

## 8. Regulador con Zener

Explique el funcionamiento básico de un regulador con diodo Zener.

Debe incluir:

1. Forma de conexión del Zener.
2. Función de la resistencia serie.
3. Condición para que el Zener regule.
4. Riesgo de exceder la potencia del Zener.

**Valor:** 0.7 puntos

---

# Parte D – BJT como interruptor

## 9. Identificación y función de terminales

En un transistor BJT NPN, explique la función de:

1. Base.
2. Colector.
3. Emisor.

**Valor:** 0.5 puntos

---

## 10. Cálculo de resistencia de base

Se desea controlar una carga pequeña con un BJT NPN usando una señal de control de **5 V**.

Datos:

```text
VBE ≈ 0.7 V
IB deseada = 2 mA
```

Calcule la resistencia de base aproximada.

**Valor:** 0.8 puntos

---

## 11. Corte y saturación

Explique qué significa que un BJT esté en:

1. Corte.
2. Saturación.

Relacione ambos estados con el uso del transistor como interruptor.

**Valor:** 0.6 puntos

---

# Parte E – FET/MOSFET como dispositivo de control

## 12. Terminales del MOSFET

En un MOSFET canal N, explique la función de:

1. Gate.
2. Drain.
3. Source.

**Valor:** 0.5 puntos

---

## 13. Comparación BJT vs MOSFET

Complete la siguiente tabla:

| Característica | BJT | MOSFET |
|---|---|---|
| Variable principal de control | | |
| Terminal de control | | |
| Aplicación como interruptor | | |
| Precaución básica | | |

**Valor:** 0.8 puntos

---

## 14. Resistencia pull-down y carga inductiva

Explique:

1. Para qué se usa una resistencia pull-down en la compuerta de un MOSFET.
2. Por qué se recomienda usar un diodo de protección cuando se controla un relé o motor DC.

**Valor:** 0.6 puntos

---

## 15. Aplicación integradora

Proponga un circuito básico para controlar una carga DC desde una señal de control.

Puede usar BJT o MOSFET. Debe indicar:

1. Dispositivo seleccionado.
2. Componentes necesarios.
3. Función de cada componente.
4. Una aplicación real en ingeniería eléctrica.

**Valor:** 0.8 puntos

---

# Total

**10.0 puntos**

---

# Distribución sugerida

| Parte | Tema | Valor |
|---|---|---:|
| A | Fundamentos y medición | 1.5 |
| B | Señales y rectificación | 2.0 |
| C | Diodo, LED y Zener | 2.4 |
| D | BJT | 1.9 |
| E | MOSFET e integración | 2.2 |
| **Total** |  | **10.0** |

---

# Rúbrica general

| Criterio | Peso |
|---|---:|
| Procedimiento y análisis | 35% |
| Resultados numéricos correctos | 25% |
| Manejo conceptual | 25% |
| Unidades, orden y claridad | 15% |

---

# Guía de respuestas para el docente

> Esta sección es de apoyo docente. Puede retirarse antes de entregar el parcial.

## Respuestas orientadoras

1. `Req = 3.2 kΩ`; `I = 12 V / 3200 Ω = 3.75 mA`; `VR1 = 3.75 V`; `VR2 = 8.25 V`; `P1 ≈ 14.1 mW`; `P2 ≈ 30.9 mW`.
2. Voltaje en paralelo; corriente en serie abriendo la rama. Precaución: escala adecuada, no medir corriente en paralelo con la fuente.
3. `VP = 9 × 1.414 ≈ 12.73 V`. Importa porque el capacitor puede cargarse cerca del pico menos caídas en diodos.
4. Media onda deja pasar un semiciclo y bloquea el otro. Con diodo real hay caída aproximada de 0.7 V y pérdidas.
5. Puente rectifica ambos semiciclos; capacitor suaviza la salida; rizado es variación residual; al aumentar capacitancia normalmente disminuye el rizado.
6. `VR = 5 - 0.7 = 4.3 V`; `I = 4.3 mA`; `P = 4.3 V × 0.0043 A ≈ 18.5 mW`. La resistencia limita corriente.
7. `R = (12 - 2) / 0.015 = 666.7 Ω`; valor comercial cercano 680 Ω; `P ≈ 10 V × 0.015 A = 0.15 W`, usar 1/4 W o superior.
8. Zener en inversa con resistencia serie; regula si tiene corriente suficiente y no supera potencia; resistencia limita corriente.
9. Base controla, colector conecta la carga, emisor va a referencia en NPN de lado bajo.
10. `RB = (5 - 0.7) / 0.002 = 2150 Ω`; valor cercano 2.2 kΩ.
11. Corte: apagado, sin corriente significativa. Saturación: encendido, conduce al máximo permitido por la carga.
12. Gate controla, Drain recibe corriente desde la carga, Source va a referencia en canal N de lado bajo.
13. BJT: control por corriente, base, corte/saturación, resistencia de base. MOSFET: control por voltaje VGS, gate, apagado/encendido, evitar gate flotante y respetar VGS máximo.
14. Pull-down evita que la compuerta quede flotante; diodo de protección descarga energía de cargas inductivas.
15. Respuesta abierta: debe incluir dispositivo, resistencia de control, carga, fuente, tierra común, diodo si carga inductiva y aplicación real.
