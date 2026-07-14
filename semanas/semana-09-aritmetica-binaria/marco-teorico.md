# Marco teórico – Semana 09

# Álgebra booleana, De Morgan e introducción a Karnaugh

## 1. Tema de la semana

Uso del álgebra booleana para representar, analizar y simplificar circuitos lógicos combinacionales.

---

## 2. Objetivo de aprendizaje

Simplificar expresiones booleanas mediante leyes algebraicas y teoremas de De Morgan, reconociendo la necesidad de métodos gráficos como los mapas de Karnaugh.

---

## 3. Contexto e importancia

Un mismo comportamiento lógico puede implementarse con diferentes circuitos. La simplificación permite reducir el número de compuertas, conexiones, costo, consumo y posibilidades de error.

---

## 4. Variables booleanas

Una variable booleana solo puede tomar dos valores:

```text
0 o 1
```

Las operaciones principales son:

- Suma lógica: OR.
- Producto lógico: AND.
- Complemento: NOT.

---

## 5. Leyes básicas

| Ley | Expresión |
|---|---|
| Identidad OR | A + 0 = A |
| Identidad AND | A·1 = A |
| Dominación OR | A + 1 = 1 |
| Dominación AND | A·0 = 0 |
| Idempotencia | A + A = A ; A·A = A |
| Complemento | A + A̅ = 1 ; A·A̅ = 0 |
| Doble negación | (A̅)̅ = A |

---

## 6. Teoremas de De Morgan

Los teoremas de De Morgan permiten transformar expresiones negadas:

```text
(A + B)̅ = A̅ · B̅
```

```text
(A · B)̅ = A̅ + B̅
```

Son fundamentales para implementar circuitos usando NAND o NOR.

---

## 7. Introducción a Karnaugh

Cuando las expresiones tienen muchas variables, la simplificación algebraica puede volverse extensa. Los mapas de Karnaugh permiten simplificar funciones de forma visual agrupando unos o ceros adyacentes.

---

## 8. Errores comunes

- Aplicar mal la negación de una suma o producto.
- Confundir suma lógica con suma aritmética.
- No respetar la prioridad de operaciones.
- No comprobar la expresión simplificada con tabla de verdad.

---

## 9. Preguntas orientadoras

1. ¿Por qué simplificar una función lógica?
2. ¿Qué diferencia hay entre A+B y A·B?
3. ¿Cómo se niega una suma lógica?
4. ¿Cómo se niega un producto lógico?
5. ¿Cuándo conviene usar Karnaugh?

---

## 10. Trabajo independiente

Resolver ejercicios de simplificación y preparar la Semana 11, donde se trabajarán mapas de Karnaugh después del receso institucional.
