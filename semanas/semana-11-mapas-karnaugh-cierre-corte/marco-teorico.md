# Marco teórico – Semana 11

# Mapas de Karnaugh y cierre del Corte 2

## 1. Tema de la semana

Simplificación de funciones lógicas mediante mapas de Karnaugh.

## 2. Objetivo de aprendizaje

Construir e interpretar mapas de Karnaugh para simplificar funciones de 2, 3 y 4 variables, obteniendo expresiones lógicas reducidas.

## 3. Contexto

Los mapas de Karnaugh permiten simplificar funciones digitales de forma visual. Son especialmente útiles cuando una expresión proviene de una tabla de verdad y se desea implementar con la menor cantidad posible de compuertas.

## 4. Conceptos fundamentales

- Mintermino: combinación específica de variables que produce salida 1.
- Maxtermino: combinación específica de variables que produce salida 0.
- Adyacencia: celdas vecinas que difieren en una sola variable.
- Agrupación: unión de celdas con valor 1 para simplificar la función.
- Condición de no importa: combinación que puede tomarse como 0 o 1 según convenga.

## 5. Reglas básicas de agrupación

- Se agrupan cantidades de celdas en potencias de 2: 1, 2, 4, 8 o 16.
- Los grupos deben ser lo más grandes posible.
- Una celda puede pertenecer a más de un grupo si ayuda a simplificar.
- Los bordes del mapa se consideran adyacentes.
- Cada grupo elimina variables que cambian dentro del grupo.

## 6. Ejemplo guiado

Si una función de dos variables vale 1 para:

```text
A=0, B=1
A=1, B=1
```

En ambos casos B permanece en 1 y A cambia. Por tanto, la función simplificada es:

```text
F = B
```

## 7. Relación con circuitos

Una expresión simplificada implica menos compuertas, menos conexiones, menor posibilidad de error en el montaje y una implementación más clara.

## 8. Errores comunes

- Agrupar cantidades que no son potencias de 2.
- No considerar adyacencia por los bordes.
- Agrupar celdas que no tienen valor 1.
- No usar condiciones de no importa cuando están disponibles.
- Obtener la expresión sin verificarla con tabla de verdad.

## 9. Preguntas orientadoras

1. ¿Por qué Karnaugh facilita la simplificación?
2. ¿Qué significa que dos celdas sean adyacentes?
3. ¿Por qué se agrupa en potencias de 2?
4. ¿Cuándo se puede usar una condición de no importa?
5. ¿Cómo se verifica que la expresión simplificada es correcta?

## 10. Trabajo independiente

Resolver mapas de 2, 3 y 4 variables y preparar la evaluación o actividad de cierre del segundo corte.
