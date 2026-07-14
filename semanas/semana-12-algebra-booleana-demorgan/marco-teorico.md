# Marco teórico – Semana 12

# XOR, sumadores y restadores

## 1. Tema de la semana

Aplicaciones de la compuerta XOR en circuitos aritméticos combinacionales.

---

## 2. Objetivo de aprendizaje

Diseñar y analizar circuitos de suma y resta binaria usando compuertas lógicas.

---

## 3. Contexto e importancia

Los sumadores son bloques fundamentales de calculadoras, procesadores, contadores, unidades aritmético-lógicas y sistemas embebidos. La compuerta XOR es clave porque permite obtener la suma sin acarreo en operaciones binarias.

---

## 4. Compuerta XOR

La salida de una XOR es 1 cuando las entradas son diferentes.

| A | B | A XOR B |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

---

## 5. Medio sumador

El medio sumador suma dos bits A y B.

```text
S = A XOR B
C = A · B
```

Donde S es la suma y C es el acarreo.

---

## 6. Sumador completo

El sumador completo suma tres bits: A, B y acarreo de entrada Cin.

```text
S = A XOR B XOR Cin
```

El acarreo de salida se activa cuando al menos dos entradas valen 1.

---

## 7. Restadores

La resta binaria puede implementarse con restadores directos o mediante complemento a 2. Los restadores directos utilizan señales de préstamo.

---

## 8. Errores comunes

- Confundir suma aritmética con OR lógico.
- Olvidar el acarreo de entrada en un sumador completo.
- No diferenciar suma y acarreo.
- No construir la tabla de verdad antes del circuito.

---

## 9. Preguntas orientadoras

1. ¿Por qué XOR es útil para sumar bits?
2. ¿Cuál es la diferencia entre medio sumador y sumador completo?
3. ¿Qué representa el acarreo?
4. ¿Cómo se relaciona la resta con el complemento a 2?
5. ¿Dónde se usan sumadores en sistemas reales?

---

## 10. Trabajo independiente

Simular un medio sumador y un sumador completo, completar sus tablas de verdad y preparar el informe de los Labs 04 y 05.
