# Marco teórico – Semana 07

# Aritmética binaria

## 1. Tema de la semana

Operaciones básicas con números binarios: suma, resta, complemento a 1, complemento a 2 y desbordamiento.

---

## 2. Objetivo de aprendizaje

Resolver operaciones aritméticas binarias y relacionarlas con el funcionamiento interno de circuitos sumadores, unidades aritmético-lógicas y sistemas digitales.

---

## 3. Contexto e importancia

Los sistemas digitales no solo almacenan datos en binario; también realizan operaciones con ellos. La suma y la resta binaria son la base de procesadores, calculadoras, contadores, registros y sistemas embebidos.

---

## 4. Suma binaria

Reglas básicas:

| A | B | Suma | Acarreo |
|---|---|---|---|
| 0 | 0 | 0 | 0 |
| 0 | 1 | 1 | 0 |
| 1 | 0 | 1 | 0 |
| 1 | 1 | 0 | 1 |

Cuando se suma 1 + 1, el resultado es 0 y se genera un acarreo hacia la siguiente posición.

---

## 5. Resta binaria

La resta puede realizarse directamente o usando complemento a 2. En circuitos digitales, el complemento a 2 es muy usado porque permite realizar restas usando circuitos sumadores.

---

## 6. Complemento a 1 y complemento a 2

El complemento a 1 se obtiene invirtiendo todos los bits.

Ejemplo:

```text
A = 0101
Complemento a 1 = 1010
```

El complemento a 2 se obtiene sumando 1 al complemento a 1.

```text
Complemento a 2 = 1010 + 1 = 1011
```

---

## 7. Números con signo

En complemento a 2, el bit más significativo indica el signo:

- 0: número positivo.
- 1: número negativo.

Esto permite representar valores positivos y negativos con una cantidad fija de bits.

---

## 8. Overflow

El overflow o desbordamiento ocurre cuando el resultado de una operación no puede representarse con la cantidad de bits disponibles.

Por ejemplo, con 4 bits sin signo, el mayor número posible es:

```text
1111₂ = 15₁₀
```

Si el resultado supera ese valor, se produce desbordamiento.

---

## 9. Errores comunes

- Olvidar el acarreo.
- Confundir resta directa con complemento a 2.
- Usar pocos bits para representar el resultado.
- Confundir números con signo y sin signo.
- No identificar overflow.

---

## 10. Preguntas orientadoras

1. ¿Por qué 1 + 1 en binario produce acarreo?
2. ¿Para qué sirve el complemento a 2?
3. ¿Cómo se representa un número negativo en binario?
4. ¿Qué es overflow?
5. ¿Por qué la resta puede realizarse usando un sumador?

---

## 11. Trabajo independiente

Resolver operaciones binarias de suma y resta, usando números con signo y sin signo. Prepararse para relacionar estas operaciones con sumadores en las semanas de aplicaciones digitales.
