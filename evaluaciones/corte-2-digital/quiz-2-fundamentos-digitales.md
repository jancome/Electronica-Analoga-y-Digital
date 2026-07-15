# Quiz 2 – Fundamentos digitales

**Corte:** 2  
**Semana sugerida:** Semana 07  
**Peso:** 2% de la nota final  
**Modalidad:** individual  
**Tiempo sugerido:** 20 a 25 minutos

## Indicaciones para el estudiante

- Responda de forma ordenada.
- Muestre el procedimiento en conversiones y operaciones.
- No se permite el uso de celular durante el quiz, salvo autorización del docente.
- El quiz está orientado principalmente a ejercicios cortos de sistemas numéricos y aritmética binaria.

---

## Ejercicios

### 1. Decimal a binario

Convierta el número **25₁₀** a binario.

**Valor:** 0.5 puntos

---

### 2. Binario a decimal

Convierta el número **101101₂** a decimal.

**Valor:** 0.5 puntos

---

### 3. Binario a hexadecimal

Convierta **11110010₂** a hexadecimal.

**Valor:** 0.5 puntos

---

### 4. Código BCD

Escriba en BCD los números:

- 59
- 408

**Valor:** 0.7 puntos

---

### 5. Suma binaria

Realice la siguiente suma binaria:

```text
1011 + 0110
```

**Valor:** 0.6 puntos

---

### 6. Resta con complemento a 2

Realice la operación **13 - 5** usando representación binaria de 4 bits y complemento a 2.

**Valor:** 0.8 puntos

---

### 7. Overflow

Determine si hay overflow en la siguiente suma de 4 bits:

```text
0111 + 0011
```

Explique brevemente su respuesta.

**Valor:** 0.5 puntos

---

### 8. Tabla de verdad

Complete la tabla de verdad de la función:

```text
F = A · B
```

| A | B | F |
|---|---|---|
| 0 | 0 |   |
| 0 | 1 |   |
| 1 | 0 |   |
| 1 | 1 |   |

**Valor:** 0.5 puntos

---

### 9. De Morgan

Aplique el teorema de De Morgan a la siguiente expresión:

```text
(A + B)̅
```

**Valor:** 0.4 puntos

---

### 10. Evaluación de expresión lógica

Para la expresión:

```text
F = A + B̅
```

Determine el valor de **F** cuando **A = 0** y **B = 1**.

**Valor:** 0.5 puntos

---

## Total

**5.0 puntos**

---

# Respuestas orientadoras para el docente

> Esta sección puede retirarse antes de entregar el quiz.

1. `25₁₀ = 11001₂`.
2. `101101₂ = 45₁₀`.
3. `11110010₂ = F2₁₆`.
4. `59 = 0101 1001`; `408 = 0100 0000 1000`.
5. `1011 + 0110 = 10001`.
6. `13 = 1101`, `5 = 0101`, complemento a 2 de 5: `1011`; `1101 + 1011 = 1000` descartando acarreo externo. Resultado: `1000₂ = 8₁₀`.
7. `0111 + 0011 = 1010`. En 4 bits con signo hay overflow porque se suman dos positivos y el resultado queda con bit de signo 1.
8. AND: 0, 0, 0, 1.
9. `(A + B)̅ = A̅ · B̅`.
10. `B̅ = 0`; `F = 0 + 0 = 0`.
