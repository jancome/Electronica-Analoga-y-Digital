# Quiz 3 – Aplicaciones digitales

**Corte:** 3  
**Semana sugerida:** Semana 16  
**Peso:** 2% de la nota final  
**Modalidad:** individual  
**Tiempo sugerido:** 20 a 25 minutos

## Indicaciones para el estudiante

- Responda de forma ordenada.
- Complete tablas o salidas cuando se solicite.
- No se permite el uso de celular durante el quiz, salvo autorización del docente.
- El quiz está orientado principalmente a ejercicios cortos de circuitos combinacionales y secuenciales.

---

## Ejercicios

### 1. Compuerta XOR

Complete la tabla de verdad de una compuerta XOR de dos entradas.

| A | B | F = A ⊕ B |
|---|---|---|
| 0 | 0 |   |
| 0 | 1 |   |
| 1 | 0 |   |
| 1 | 1 |   |

**Valor:** 0.5 puntos

---

### 2. Medio sumador

Para un medio sumador con **A = 1** y **B = 1**, determine:

- Suma.
- Carry.

**Valor:** 0.5 puntos

---

### 3. Sumador completo

Para un sumador completo con **A = 1**, **B = 0** y **Cin = 1**, determine:

- Suma.
- Cout.

**Valor:** 0.6 puntos

---

### 4. Comparador

Compare los números:

```text
A = 10₂
B = 11₂
```

Indique cuál salida se activa:

- A > B
- A = B
- A < B

**Valor:** 0.5 puntos

---

### 5. Paridad

Para el dato **1011**, agregue un bit de paridad par.

**Valor:** 0.5 puntos

---

### 6. Multiplexor

En un MUX 4:1 se tienen las siguientes entradas:

```text
I0 = 0
I1 = 1
I2 = 0
I3 = 1
```

Si la selección es **S1S0 = 01**, indique la salida.

**Valor:** 0.5 puntos

---

### 7. Demultiplexor

En un DEMUX 1:4 la entrada es **D = 1** y la selección es **S1S0 = 10**.

Indique qué salida se activa.

**Valor:** 0.5 puntos

---

### 8. Flip-flop D

En un flip-flop tipo D, si **D = 1** en el flanco activo del reloj, indique el valor siguiente de **Q**.

**Valor:** 0.4 puntos

---

### 9. Contador

Un contador binario de 3 bits se encuentra en el estado **011**.

Indique el siguiente estado.

**Valor:** 0.5 puntos

---

### 10. Aplicación

Proponga una aplicación breve de un contador en un sistema eléctrico, electrónico o de automatización.

**Valor:** 0.5 puntos

---

## Total

**5.0 puntos**

---

# Respuestas orientadoras para el docente

> Esta sección puede retirarse antes de entregar el quiz.

1. XOR: 0, 1, 1, 0.
2. Medio sumador con A=1 y B=1: Suma = 0, Carry = 1.
3. A=1, B=0, Cin=1: Suma = 0, Cout = 1.
4. `10₂ = 2`, `11₂ = 3`; se activa `A < B`.
5. `1011` tiene tres unos; para paridad par se agrega `1`.
6. Selección `01` toma `I1`; salida = 1.
7. Selección `10` activa la salida `Y2`, según convención de numeración usada en clase.
8. `Q` toma el valor de `D`; por tanto `Q = 1`.
9. Después de `011` sigue `100`.
10. Conteo de pulsos de sensor, contador de piezas, ciclos de una máquina, pulsos de encoder, temporización o secuencia de semáforo.
