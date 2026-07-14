# Marco teórico – Semana 11

# Mapas de Karnaugh y cierre del segundo corte

## 1. Tema de la semana

Simplificación de funciones lógicas mediante mapas de Karnaugh de 2, 3 y 4 variables.

---

## 2. Objetivo de aprendizaje

Usar mapas de Karnaugh para obtener expresiones booleanas simplificadas y relacionarlas con circuitos combinacionales más eficientes.

---

## 3. Contexto e importancia

El álgebra booleana permite simplificar expresiones, pero cuando aumenta el número de variables el proceso puede ser largo. Los mapas de Karnaugh ofrecen una herramienta visual para agrupar combinaciones lógicas y reducir funciones.

---

## 4. Conceptos fundamentales

- Tabla de verdad.
- Mintermino.
- Variable complementada y no complementada.
- Adyacencia lógica.
- Agrupación de 1, 2, 4, 8 o 16 celdas.

---

## 5. Regla general de agrupación

Los grupos deben formarse con cantidades que sean potencias de 2:

```text
1, 2, 4, 8, 16
```

Mientras más grande sea el grupo, más simple será el término resultante.

---

## 6. Procedimiento básico

1. Construir la tabla de verdad.
2. Ubicar los unos en el mapa.
3. Agrupar unos adyacentes.
4. Identificar las variables que no cambian dentro de cada grupo.
5. Escribir la expresión simplificada.
6. Verificar el resultado.

---

## 7. Errores comunes

- Agrupar celdas que no son adyacentes.
- Olvidar que los bordes del mapa también son adyacentes.
- Hacer grupos que no son potencia de 2.
- No buscar grupos grandes.
- No comprobar la expresión simplificada.

---

## 8. Preguntas orientadoras

1. ¿Qué ventaja tiene Karnaugh frente a la simplificación algebraica?
2. ¿Por qué los grupos deben ser de tamaño 1, 2, 4, 8 o 16?
3. ¿Qué significa que una variable no cambie dentro de un grupo?
4. ¿Por qué los bordes del mapa se consideran adyacentes?
5. ¿Cómo se verifica una expresión simplificada?

---

## 9. Trabajo independiente

Resolver mapas de Karnaugh de 2, 3 y 4 variables. Prepararse para el tercer corte, donde se aplicarán estas funciones en sumadores, comparadores, codificadores y multiplexores.
