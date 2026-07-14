# Marco teórico – Semana 06

# Sistemas numéricos

## 1. Tema de la semana

Representación de información numérica en electrónica digital mediante los sistemas decimal, binario, hexadecimal y BCD.

---

## 2. Objetivo de aprendizaje

Realizar conversiones entre sistemas numéricos y explicar por qué el sistema binario es la base de los circuitos digitales.

---

## 3. Contexto e importancia

Los circuitos digitales trabajan con dos niveles de voltaje que se interpretan como 0 y 1. Por eso, la información debe representarse en binario. Sin embargo, los humanos usamos decimal y muchos sistemas electrónicos usan hexadecimal para simplificar la lectura de grupos de bits.

Comprender estos sistemas es fundamental antes de estudiar compuertas, aritmética binaria, registros, memorias, microcontroladores y comunicaciones digitales.

---

## 4. Conceptos fundamentales

### Sistema decimal

Usa diez símbolos:

```text
0, 1, 2, 3, 4, 5, 6, 7, 8, 9
```

Es un sistema de base 10.

### Sistema binario

Usa dos símbolos:

```text
0 y 1
```

Es un sistema de base 2 y es el lenguaje básico de los circuitos digitales.

### Sistema hexadecimal

Usa dieciséis símbolos:

```text
0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F
```

Es un sistema de base 16. Cada dígito hexadecimal equivale a 4 bits.

### BCD

BCD significa **Binary Coded Decimal**. En BCD, cada dígito decimal se representa usando 4 bits.

---

## 5. Conversión decimal a binario

Para convertir un número decimal a binario se divide sucesivamente entre 2 y se toman los residuos.

Ejemplo:

```text
13 / 2 = 6 residuo 1
6 / 2 = 3 residuo 0
3 / 2 = 1 residuo 1
1 / 2 = 0 residuo 1
```

Leyendo los residuos de abajo hacia arriba:

```text
13 decimal = 1101 binario
```

---

## 6. Conversión binario a decimal

Cada posición binaria representa una potencia de 2.

Ejemplo:

```text
1011₂ = 1×2³ + 0×2² + 1×2¹ + 1×2⁰
1011₂ = 8 + 0 + 2 + 1
1011₂ = 11₁₀
```

---

## 7. Conversión binario a hexadecimal

Se agrupan los bits de cuatro en cuatro desde la derecha.

Ejemplo:

```text
10101100₂ = 1010 1100
1010 = A
1100 = C
```

Por tanto:

```text
10101100₂ = AC₁₆
```

---

## 8. Errores comunes

- Leer un número binario como si fuera decimal.
- Olvidar que cada posición representa una potencia de la base.
- Confundir hexadecimal con decimal cuando aparecen letras.
- No completar grupos de 4 bits al convertir a hexadecimal.
- Confundir binario puro con BCD.

---

## 9. Preguntas orientadoras

1. ¿Por qué los sistemas digitales usan binario?
2. ¿Qué ventaja tiene el sistema hexadecimal?
3. ¿Cuál es la diferencia entre 1001₂ y 1001₁₀?
4. ¿Qué diferencia hay entre binario puro y BCD?
5. ¿Dónde se utiliza hexadecimal en electrónica o programación?

---

## 10. Trabajo independiente

Resolver ejercicios de conversión entre decimal, binario, hexadecimal y BCD. Prepararse para la Semana 07, donde estos números se usarán en operaciones aritméticas binarias.
