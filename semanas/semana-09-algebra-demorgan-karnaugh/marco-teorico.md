# Marco teórico – Semana 09

# Álgebra booleana, De Morgan e introducción a Karnaugh

## 1. Tema de la semana

Simplificación de expresiones lógicas mediante álgebra booleana y teoremas de De Morgan, con introducción al método gráfico de Karnaugh.

## 2. Objetivo de aprendizaje

Aplicar reglas booleanas para simplificar expresiones y reconocer cuándo conviene usar mapas de Karnaugh para obtener circuitos lógicos más simples.

## 3. Contexto

En los sistemas digitales, una misma función puede implementarse con diferentes cantidades de compuertas. Simplificar una expresión reduce componentes, conexiones, consumo, fallas y complejidad de montaje.

## 4. Conceptos fundamentales

- Variable booleana: solo toma valores 0 o 1.
- Producto lógico: operación AND.
- Suma lógica: operación OR.
- Complemento: negación de una variable.
- Expresión booleana: representación matemática de una función lógica.
- Circuito equivalente: circuito que produce la misma tabla de verdad que otro.

## 5. Leyes básicas

| Ley | Forma |
|---|---|
| Identidad OR | A + 0 = A |
| Identidad AND | A · 1 = A |
| Anulación OR | A + 1 = 1 |
| Anulación AND | A · 0 = 0 |
| Idempotencia | A + A = A ; A · A = A |
| Complemento | A + A̅ = 1 ; A · A̅ = 0 |
| Doble negación | (A̅)̅ = A |
| Absorción | A + A·B = A |

## 6. Teoremas de De Morgan

```text
(A + B)̅ = A̅ · B̅
```

```text
(A · B)̅ = A̅ + B̅
```

Estos teoremas permiten transformar expresiones negadas y son útiles para implementar funciones con compuertas NAND o NOR.

## 7. Introducción a Karnaugh

El mapa de Karnaugh organiza la tabla de verdad de forma gráfica, permitiendo agrupar unos o ceros adyacentes para simplificar expresiones de 2, 3 o 4 variables.

En esta semana solo se introduce el concepto; la aplicación completa se desarrolla en la Semana 11 después del receso.

## 8. Ejemplo guiado

Simplificar:

```text
F = A + A·B
```

Aplicando absorción:

```text
F = A
```

Esto significa que el circuito completo puede reemplazarse por una conexión directa de A a la salida.

## 9. Errores comunes

- Confundir suma lógica con suma aritmética.
- Aplicar De Morgan sin cambiar la operación.
- Olvidar negar todas las variables al aplicar De Morgan.
- Simplificar expresiones sin verificar con tabla de verdad.
- Pensar que el mapa de Karnaugh reemplaza la comprensión del álgebra.

## 10. Preguntas orientadoras

1. ¿Por qué simplificar una función lógica?
2. ¿Cómo se sabe que dos expresiones son equivalentes?
3. ¿Qué cambia cuando se aplica De Morgan?
4. ¿Qué ventaja tienen las compuertas NAND y NOR?
5. ¿Por qué Karnaugh se considera un método visual de simplificación?

## 11. Trabajo independiente

Resolver ejercicios de simplificación algebraica, completar Labs 02 y 03, y preparar preguntas para retomar Karnaugh después del receso.
