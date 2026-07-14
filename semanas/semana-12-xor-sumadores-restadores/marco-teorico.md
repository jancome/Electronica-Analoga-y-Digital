# Marco teórico – Semana 12

# XOR, sumadores y restadores

## 1. Tema de la semana

Aplicaciones aritméticas de la lógica combinacional usando compuerta XOR, sumadores y restadores.

## 2. Objetivo de aprendizaje

Diseñar e interpretar circuitos básicos de suma y resta binaria a partir de compuertas lógicas.

## 3. Contexto

La aritmética digital es la base de procesadores, calculadoras, sistemas embebidos, controladores y dispositivos digitales. Aunque los circuitos reales pueden ser complejos, su fundamento parte de operaciones simples entre bits.

## 4. Compuerta XOR

La XOR produce salida 1 cuando sus entradas son diferentes.

| A | B | A⊕B |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

Esta propiedad permite usarla para sumar bits sin acarreo y para detectar diferencias.

## 5. Medio sumador

El medio sumador suma dos bits A y B.

```text
S = A ⊕ B
C = A · B
```

Donde S es la suma y C es el acarreo.

## 6. Sumador completo

El sumador completo suma A, B y un acarreo de entrada Cin.

```text
S = A ⊕ B ⊕ Cin
Cout = A·B + Cin·(A⊕B)
```

## 7. Restador básico

El medio restador compara dos bits y genera una diferencia y un préstamo.

```text
D = A ⊕ B
P = A̅ · B
```

## 8. Ejemplo guiado

Sumar A=1 y B=1 en un medio sumador:

```text
S = 1 ⊕ 1 = 0
C = 1 · 1 = 1
```

El resultado binario es 10, que equivale a 2 decimal.

## 9. Errores comunes

- Confundir acarreo con suma.
- Pensar que XOR es igual a OR.
- Olvidar el acarreo de entrada en un sumador completo.
- No verificar todas las combinaciones de la tabla de verdad.
- Conectar salidas de compuertas directamente entre sí.

## 10. Preguntas orientadoras

1. ¿Por qué la XOR es útil en circuitos aritméticos?
2. ¿Qué diferencia hay entre medio sumador y sumador completo?
3. ¿Qué representa el acarreo?
4. ¿Por qué 1+1 en binario produce 10?
5. ¿Cómo se implementa una resta usando lógica digital?

## 11. Trabajo independiente

Completar las tablas de verdad de medio sumador, sumador completo y medio restador. Simular los circuitos antes del montaje.
