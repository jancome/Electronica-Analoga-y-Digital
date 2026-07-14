# Marco teórico – Semana 08

# Compuertas lógicas

## 1. Tema de la semana

Compuertas lógicas básicas y universales: AND, OR, NOT, NAND, NOR, XOR y XNOR.

---

## 2. Objetivo de aprendizaje

Interpretar tablas de verdad y relacionarlas con el comportamiento eléctrico de circuitos lógicos digitales.

---

## 3. Contexto e importancia

Las compuertas lógicas son los bloques básicos de los sistemas digitales. Con ellas se construyen comparadores, sumadores, multiplexores, memorias, procesadores y sistemas de control.

---

## 4. Niveles lógicos

En electrónica digital se trabaja con dos estados principales:

```text
0 lógico: nivel bajo
1 lógico: nivel alto
```

Estos estados se representan mediante rangos de voltaje, no por un único valor exacto.

---

## 5. Compuertas básicas

| Compuerta | Operación | Descripción |
|---|---|---|
| AND | A·B | La salida es 1 solo si todas las entradas son 1 |
| OR | A+B | La salida es 1 si al menos una entrada es 1 |
| NOT | A̅ | Invierte el valor de entrada |

---

## 6. Compuertas universales

Las compuertas NAND y NOR se llaman universales porque con ellas se puede implementar cualquier función lógica.

| Compuerta | Función |
|---|---|
| NAND | Salida negada de AND |
| NOR | Salida negada de OR |

---

## 7. XOR y XNOR

La compuerta XOR entrega 1 cuando las entradas son diferentes. La XNOR entrega 1 cuando las entradas son iguales.

Son útiles en comparadores, sumadores, detectores de paridad y sistemas de verificación.

---

## 8. Errores comunes

- Confundir OR con XOR.
- Olvidar alimentar correctamente los circuitos integrados.
- Dejar entradas flotantes.
- No verificar hoja de datos del CI.
- Interpretar niveles lógicos como valores ideales exactos.

---

## 9. Preguntas orientadoras

1. ¿Cuál es la diferencia entre AND y OR?
2. ¿Por qué NAND y NOR son universales?
3. ¿Cuándo la salida de XOR vale 1?
4. ¿Qué ocurre si una entrada queda flotante?
5. ¿Por qué se deben medir los niveles de voltaje en laboratorio?

---

## 10. Trabajo independiente

Completar tablas de verdad y simular compuertas básicas antes del Lab 01.
