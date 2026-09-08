# Marco teórico – Semana 09

# Álgebra booleana, De Morgan y mapas de Karnaugh

## Metas de aprendizaje verificables

- Obtener formas canónicas desde una tabla y simplificarlas por álgebra y Karnaugh.
- Demostrar equivalencia exhaustiva y cuantificar la reducción de puertas, conexiones y niveles.
- Tratar estados imposibles o “no importa” con criterio de seguridad del proyecto.

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

## 20. Profundización: equivalencia y minimización verificable

El álgebra de Boole transforma expresiones sin cambiar su tabla de verdad. Entre las identidades más útiles están `X+X=X`, `XX=X`, `X+XY=X`, `X(X+Y)=X` y distributividad. De Morgan permite mover una negación a través de una operación: `\overline{XY}=\bar X+\bar Y` y `\overline{X+Y}=\bar X\bar Y`. Estas relaciones son esenciales al implementar solo con NAND o NOR.

Una suma de productos canónica contiene un mintermino por cada fila donde `F=1`. El mapa de Karnaugh organiza celdas en código Gray, de manera que las adyacentes difieren en una variable. Los grupos deben contener `1,2,4,8…` celdas, pueden envolver bordes y deben hacerse tan grandes como sea posible. Cada variable que cambia dentro del grupo desaparece.

La minimización persigue menor costo, potencia y probabilidad de error, pero no garantiza por sí sola menor retardo o ausencia de riesgos dinámicos. En este curso se comprobará equivalencia exhaustiva para hasta cuatro variables.

## 21. Ejemplo guiado adaptado

Para `F(A,B,C)=Σm(1,2,3,5,7)`:

1. Se escriben los minterminos `001,010,011,101,111`.
2. En el mapa se agrupan `1,3,5,7`, donde `C=1`, obteniendo `C`.
3. El mintermino `2` se agrupa con `3`, donde `A=0` y `B=1`, obteniendo `\bar AB`.
4. Resultado: `F=C+\bar AB`.
5. La forma canónica usa cinco términos de tres literales; la simplificada usa dos términos y menos conexiones.
6. Se prueban las ocho combinaciones y se confirma que ambas salidas coinciden.

## 22. Procedimiento de simulación y Labs 02–03

1. Traducir el requisito a variables y decidir estados imposibles; no asignar “no importa” sin justificación física.
2. Construir tabla y forma canónica.
3. Simplificar algebraicamente y con Karnaugh.
4. Implementar original y simplificada en simulación.
5. Crear una señal `E=F_original XOR F_simplificada`; equivalencia exige `E=0` en todas las filas.
6. Montar la solución simplificada, fijando entradas no usadas.
7. Contar CIs, puertas, conexiones y niveles de propagación.
8. Registrar una falla de cableado y aislarla por nodos intermedios.

## 23. Diagnóstico de fallas

Si la tabla esperada es incorrecta, ninguna simplificación corregirá el requisito. Si expresión y mapa difieren, se revisan numeración de minterminos y orden de variables. Si simulación funciona y protoboard no, se comprueban niveles, negaciones, entradas flotantes y pinout. Medir términos intermedios permite ubicar el primer nodo divergente.

## 24. Preguntas orientadoras y trabajo independiente

- ¿Qué filas son físicamente posibles y cuáles son condiciones de seguridad?
- ¿Puede un “no importa” convertirse en peligro si aparece en hardware?
- ¿Cuánto reduce la forma simplificada el número de literales y niveles?
- ¿Cómo se demuestra equivalencia sin depender de inspección visual?
- ¿Conviene implementación NAND–NAND o NOR–NOR con los CIs disponibles?

El grupo entregará requisito verbal, tabla, forma canónica, dos métodos de simplificación, comparación cuantitativa, prueba de equivalencia y diagnóstico de una salida errónea.

## 25. Referencias de estudio

- Floyd, 9.ª ed., cap. 4, secs. 4.1–4.7, pp. 200–227: operaciones, leyes, De Morgan, formas estándar y tablas.
- Ibid., secs. 4.8–4.10, pp. 228–246; ejemplos 4.30 y 4.33, pp. 243–245: mapas y minimización.
- Ibid., cap. 5, ejemplos 5.5–5.6, pp. 282–283: reducción de circuitos combinacionales.

## 26. Ruta de profundización recomendada

1. **Álgebra y De Morgan:** Floyd, cap. 4, secs. 4.1–4.5, pp. 200–216.
2. **De tabla a forma estándar:** secs. 4.6–4.7, pp. 217–227; revisar el ejemplo 4.20, p. 227.
3. **Minimización obligatoria:** secs. 4.8–4.10, pp. 228–246; analizar ejemplos 4.30 y 4.33, pp. 243–245.
4. **Profundización de diseño:** cap. 5, especialmente ejemplos 5.5–5.6, pp. 282–283, para comparar circuitos antes y después de reducirlos.
