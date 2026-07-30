# Marco teórico – Semana 09

# Álgebra booleana, De Morgan y mapas de Karnaugh

## 1. Propósito de la semana

Simplificar la función lógica del proyecto, comprobar su equivalencia y actualizar la simulación y el montaje en protoboard de la Fase 2 ABPr.

Los mapas de Karnaugh se desarrollan completamente durante esta semana para que la Semana 11 pueda reservarse al cierre, la entrega y el Parcial 2.

## 2. Resultado de aprendizaje

Al finalizar la semana, el estudiante estará en capacidad de:

- Aplicar leyes del álgebra de Boole.
- Utilizar correctamente los teoremas de De Morgan.
- Obtener minterminos a partir de una tabla de verdad.
- Construir mapas de Karnaugh de 2, 3 y 4 variables.
- Formar agrupaciones válidas y obtener una expresión simplificada.
- Verificar equivalencia entre tabla, expresión, simulación y montaje.
- Reducir componentes y conexiones en el protoboard.

## 3. Conexión con la Fase 2 ABPr

La simplificación debe producir una mejora visible:

```text
Tabla de verdad
      ↓
Expresión canónica
      ↓
Álgebra / De Morgan / Karnaugh
      ↓
Expresión simplificada
      ↓
Simulación actualizada
      ↓
Protoboard corregido
```

## 4. Operaciones booleanas

- **Suma lógica:** OR.
- **Producto lógico:** AND.
- **Complemento:** NOT.

La suma lógica no es suma aritmética y el producto lógico no es multiplicación convencional.

## 5. Leyes básicas

| Ley | Expresión |
|---|---|
| Identidad OR | `A + 0 = A` |
| Identidad AND | `A·1 = A` |
| Anulación OR | `A + 1 = 1` |
| Anulación AND | `A·0 = 0` |
| Idempotencia | `A+A=A`, `A·A=A` |
| Complemento | `A+A̅=1`, `A·A̅=0` |
| Doble negación | `(A̅)̅=A` |
| Absorción | `A+A·B=A` |
| Distributiva | `A(B+C)=AB+AC` |

## 6. Teoremas de De Morgan

```text
(A + B)̅ = A̅·B̅
(A·B)̅ = A̅ + B̅
```

Al aplicar De Morgan deben realizarse dos acciones:

1. Negar cada variable.
2. Cambiar AND por OR o OR por AND.

Estos teoremas son útiles para implementar funciones con NAND o NOR.

## 7. Forma canónica y minterminos

Cada fila de la tabla con salida 1 puede expresarse como un mintermino.

Ejemplo para `A=1`, `B=0`, `C=1`:

```text
m5 = A·B̅·C
```

La función puede escribirse como suma de minterminos:

```text
F(A,B,C) = Σm(1,3,5,7)
```

## 8. Organización de Karnaugh

Las celdas se ordenan mediante código Gray para que entre posiciones vecinas cambie una sola variable.

Reglas:

- Agrupar 1, 2, 4, 8 o 16 celdas.
- Formar grupos lo más grandes posible.
- Los grupos pueden superponerse.
- Los bordes opuestos son adyacentes.
- Las esquinas pueden ser adyacentes.
- Cada 1 debe quedar cubierto.
- Las condiciones `X` pueden utilizarse cuando ayuden a simplificar.

## 9. Mapas de 2 variables

Un mapa de 2 variables contiene cuatro celdas. Cada agrupación elimina las variables que cambian.

Si la salida vale 1 cuando `B=1`, sin importar A:

```text
F = B
```

## 10. Mapas de 3 variables

Contienen ocho celdas. El orden de las columnas debe seguir código Gray:

```text
00, 01, 11, 10
```

Una agrupación de cuatro elimina dos variables.

## 11. Mapas de 4 variables

Contienen dieciséis celdas. Las filas y columnas usan código Gray. Debe revisarse especialmente la adyacencia por bordes y esquinas.

## 12. Ejemplo aplicado

Suponga que una alarma se activa cuando:

```text
F(A,B,C) = Σm(3,5,6,7)
```

El procedimiento es:

1. Construir la tabla.
2. Ubicar los unos en el mapa.
3. Crear las agrupaciones mayores.
4. Obtener los términos simplificados.
5. Verificar la función con todas las combinaciones.
6. Redibujar el circuito.

La expresión final dependerá de las agrupaciones realizadas, pero debe producir exactamente la misma tabla de verdad.

## 13. Verificación de equivalencia

Una simplificación solo es válida si:

```text
Tabla original = expresión original = expresión simplificada = circuito final
```

La comprobación debe realizarse con:

- Tabla de verdad.
- Simulación.
- Prueba física de todas las combinaciones.

## 14. Impacto en el montaje

Simplificar puede reducir:

- Cantidad de compuertas.
- Circuitos integrados.
- Cableado.
- Consumo.
- Costo.
- Posibilidad de errores.

El grupo debe mostrar una comparación antes–después.

## 15. Actividad de clase y Labs 02–03

Cada grupo deberá:

1. Construir la tabla definitiva de su proyecto.
2. Obtener la expresión canónica.
3. Simplificar algebraicamente.
4. Aplicar De Morgan cuando aporte valor.
5. Resolver el mapa de Karnaugh.
6. Comparar los resultados.
7. Simular la función simplificada.
8. Actualizar el protoboard.
9. Medir y comprobar todas las combinaciones.
10. Registrar los cambios realizados.

## 16. Evidencia ABPr

- Tabla de verdad definitiva.
- Expresión canónica.
- Desarrollo algebraico.
- Mapa de Karnaugh.
- Expresión simplificada.
- Comparación de cantidad de compuertas.
- Simulación funcional.
- Montaje en protoboard actualizado.
- Fotografías o video.
- Registro de fallas y correcciones.

## 17. Errores comunes

- Agrupar cantidades que no son potencias de 2.
- Usar orden binario normal en lugar de código Gray.
- Ignorar adyacencia por los bordes.
- Aplicar De Morgan sin cambiar la operación.
- Simplificar sin verificar la tabla.
- Presentar simulación sin montaje.
- Presentar protoboard sin comprobar todas las combinaciones.

## 18. Trabajo independiente

- Completar Labs 02 y 03.
- Corregir simulación y montaje.
- Preparar evidencias para el Preproyecto ABPr 2.
- Elaborar un registro de retroalimentación y plan de mejora.
- Repasar los temas del Corte 2.

## 19. Conexión con la Semana 10

La Semana 10 es receso institucional. No tendrá contenido nuevo ni entrega obligatoria nueva. Puede utilizarse para corregir el protoboard y preparar la entrega de la Fase 2.