# Marco teórico – Semana 06

# Sistemas numéricos

## 1. Tema de la semana

Representación de información digital mediante sistemas numéricos: decimal, binario, hexadecimal y BCD.

---

## 2. Objetivo de aprendizaje

Comprender cómo los sistemas digitales representan cantidades usando bits y realizar conversiones entre los sistemas decimal, binario, hexadecimal y BCD.

---

## 3. Contexto e importancia

Los circuitos digitales no procesan directamente números decimales como los usamos cotidianamente. Internamente trabajan con dos niveles eléctricos que se interpretan como 0 y 1. Por eso, para diseñar circuitos digitales es necesario comprender la representación binaria y sus equivalencias.

---

## 4. Conceptos fundamentales

- **Bit:** unidad mínima de información digital. Puede valer 0 o 1.
- **Nibble:** grupo de 4 bits.
- **Byte:** grupo de 8 bits.
- **Sistema decimal:** base 10.
- **Sistema binario:** base 2.
- **Sistema hexadecimal:** base 16.
- **BCD:** representación decimal codificada en binario.

---

## 5. Sistema binario

En el sistema binario cada posición representa una potencia de 2.

Ejemplo:

```text
1011₂ = 1×2³ + 0×2² + 1×2¹ + 1×2⁰
1011₂ = 8 + 0 + 2 + 1 = 11₁₀
```

---

## 6. Sistema hexadecimal

El sistema hexadecimal utiliza 16 símbolos:

```text
0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F
```

Cada dígito hexadecimal equivale a 4 bits. Por eso es muy usado para representar datos binarios de forma compacta.

Ejemplo:

```text
1010₂ = A₁₆
1111₂ = F₁₆
```

---

## 7. Código BCD

BCD significa **Binary Coded Decimal**. En este código cada dígito decimal se representa usando 4 bits.

Ejemplo:

```text
25₁₀ en BCD = 0010 0101
```

No es lo mismo que convertir 25 a binario puro:

```text
25₁₀ = 11001₂
```

---

## 8. Aplicaciones reales

- Displays de 7 segmentos.
- Contadores digitales.
- Calculadoras.
- Microcontroladores.
- Direcciones de memoria.
- Sistemas de comunicación digital.
- Representación interna de datos.

---

## 9. Ejemplo guiado

Convertir 45 decimal a binario:

```text
45 / 2 = 22 residuo 1
22 / 2 = 11 residuo 0
11 / 2 = 5  residuo 1
5 / 2  = 2  residuo 1
2 / 2  = 1  residuo 0
1 / 2  = 0  residuo 1
```

Leyendo los residuos de abajo hacia arriba:

```text
45₁₀ = 101101₂
```

---

## 10. Errores comunes

- Confundir BCD con binario puro.
- No indicar la base del número.
- Leer los residuos en el orden incorrecto.
- Agrupar mal los bits al convertir a hexadecimal.
- Suponer que todos los números digitales están en decimal.

---

## 11. Preguntas orientadoras

1. ¿Por qué los circuitos digitales usan 0 y 1?
2. ¿Qué diferencia hay entre binario y BCD?
3. ¿Por qué hexadecimal resulta útil en electrónica digital?
4. ¿Cuántos valores se pueden representar con 4 bits?
5. ¿Qué relación existe entre un nibble y un dígito hexadecimal?

---

## 12. Trabajo independiente

Resolver conversiones entre decimal, binario, hexadecimal y BCD, justificando el procedimiento utilizado.