# Marco teórico – Semana 07

# Aritmética binaria

## 1. Tema de la semana

Operaciones aritméticas en sistema binario: suma, resta, complemento a 1, complemento a 2 y representación de números con signo.

---

## 2. Objetivo de aprendizaje

Aplicar reglas de suma y resta binaria para resolver operaciones digitales, comprendiendo el uso del complemento a 2 y el concepto de desbordamiento.

---

## 3. Contexto e importancia

Los computadores, microcontroladores y circuitos digitales realizan operaciones matemáticas usando bits. Los sumadores, restadores, contadores y unidades aritméticas trabajan con reglas binarias. Por eso, dominar la aritmética binaria es indispensable antes de estudiar sumadores y circuitos combinacionales.

---

## 4. Reglas de suma binaria

| Operación | Resultado | Acarreo |
|---|---|---|
| 0 + 0 | 0 | 0 |
| 0 + 1 | 1 | 0 |
| 1 + 0 | 1 | 0 |
| 1 + 1 | 0 | 1 |
| 1 + 1 + 1 | 1 | 1 |

El acarreo se traslada a la siguiente posición, igual que ocurre en decimal, pero usando base 2.

---

## 5. Resta binaria

La resta binaria puede hacerse directamente o usando complemento a 2. En circuitos digitales, el complemento a 2 es muy importante porque permite realizar restas mediante sumadores.

---

## 6. Complemento a 1 y complemento a 2

El **complemento a 1** se obtiene invirtiendo todos los bits:

```text
1010 → 0101
```

El **complemento a 2** se obtiene sumando 1 al complemento a 1:

```text
1010 → complemento a 1: 0101
0101 + 1 = 0110
```

---

## 7. Números con signo

En muchos sistemas digitales se utiliza el bit más significativo para representar el signo:

- 0: número positivo.
- 1: número negativo.

El complemento a 2 facilita representar números negativos y operar con ellos.

---

## 8. Overflow

El overflow ocurre cuando el resultado de una operación excede la cantidad de bits disponibles.

Ejemplo: si se trabaja con 4 bits, solo se pueden representar 16 combinaciones diferentes. Si el resultado requiere más bits, se produce desbordamiento.

---

## 9. Aplicaciones reales

- Sumadores digitales.
- Restadores.
- Contadores.
- Microprocesadores.
- Unidades aritmético-lógicas.
- Cálculos internos de controladores y sistemas embebidos.

---

## 10. Ejemplo guiado

Sumar:

```text
  1011
+ 0110
------
 10001
```

El resultado requiere 5 bits. Si el sistema solo permite 4 bits, el bit adicional representa acarreo de salida.

---

## 11. Errores comunes

- Olvidar el acarreo.
- Confundir complemento a 1 con complemento a 2.
- No definir cuántos bits tiene el sistema.
- Ignorar el overflow.
- Mezclar binario puro con BCD.

---

## 12. Preguntas orientadoras

1. ¿Qué ocurre cuando se suma 1 + 1 en binario?
2. ¿Por qué el complemento a 2 permite restar usando suma?
3. ¿Qué significa que un sistema sea de 4 bits?
4. ¿Cuándo se presenta overflow?
5. ¿Por qué la aritmética binaria es base para los sumadores digitales?

---

## 13. Trabajo independiente

Resolver ejercicios de suma, resta y complemento a 2, indicando el número de bits utilizado y verificando si existe overflow.