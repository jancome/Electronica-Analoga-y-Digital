# Marco teórico – Semana 10

# Receso institucional y mejora autónoma de la Fase 2

## Metas de aprendizaje verificables

- Autoevaluar representación, aritmética, lógica, simplificación y montaje ya estudiados.
- Identificar vacíos con evidencia y preparar preguntas concretas para el cierre del corte.
- Mejorar de forma opcional el Preproyecto 2 sin contenido ni entrega nueva.

## 1. Propósito de la semana

No se introduce contenido nuevo ni se asigna una entrega obligatoria nueva. La semana puede utilizarse para consolidar aprendizajes, corregir la simulación y mejorar el montaje en protoboard antes del cierre del Corte 2.

## 2. Resultados de autoevaluación

El estudiante debe comprobar si puede:

- Convertir entre decimal, binario, hexadecimal y BCD.
- Realizar suma y resta binaria.
- Interpretar compuertas y tablas de verdad.
- Obtener una expresión booleana a partir de una tabla.
- Aplicar De Morgan.
- Resolver mapas de Karnaugh de 2, 3 y 4 variables.
- Verificar equivalencia entre tabla, expresión y circuito.
- Montar compuertas sin dejar entradas flotantes.

## 3. Ruta autónoma de revisión

1. Revisar las observaciones del docente.
2. Corregir la tabla de verdad.
3. Repetir la simplificación.
4. Verificar el mapa de Karnaugh.
5. Actualizar la simulación.
6. Revisar VCC, GND, entradas y salidas del protoboard.
7. Probar todas las combinaciones.
8. Organizar fotografías, videos y mediciones.
9. Preparar la explicación individual.
10. Completar el registro de mejoras.

## 4. Lista de verificación del Preproyecto ABPr 2

- [ ] Situación problema y objetivos actualizados.
- [ ] Diagrama de bloques actualizado.
- [ ] Variables de entrada y salida definidas.
- [ ] Significado de 0 y 1 documentado.
- [ ] Tabla de verdad completa.
- [ ] Expresión canónica.
- [ ] Simplificación algebraica o mediante Karnaugh.
- [ ] Simulación funcional.
- [ ] Montaje funcional en protoboard.
- [ ] Prueba de todas las combinaciones.
- [ ] Evidencias de medición.
- [ ] Roles y aportes individuales.
- [ ] Registro de fallas y correcciones.

## 5. Preguntas de autoevaluación

1. ¿La salida del montaje coincide con todas las filas de la tabla?
2. ¿La expresión simplificada es equivalente a la original?
3. ¿Las entradas están eléctricamente definidas?
4. ¿El circuito integrado está alimentado según su hoja de datos?
5. ¿La salida lógica requiere una etapa BJT o MOSFET?
6. ¿Puedo explicar cada conexión del protoboard?
7. ¿Qué se corrigió después de la retroalimentación?

## 6. Seguridad

- Trabajar únicamente con baja tensión.
- Desenergizar antes de modificar conexiones.
- Verificar polaridad y referencia GND.
- No cortocircuitar salidas lógicas.
- No conectar cargas de corriente elevada directamente a una compuerta.

## 7. Producto de la semana

No se exige un entregable nuevo. El producto esperado es una **versión mejorada** de la simulación y del protoboard que será presentada en la Semana 11.

## 8. Alcance académico: consolidación, no contenido nuevo

El receso del **5 al 11 de octubre de 2026** se conserva sin clase, evaluación ni entrega nueva. La ruta siguiente es opcional y sirve para que cada estudiante detecte vacíos antes del cierre del Corte 2. No reemplaza descanso ni introduce mapas, dispositivos o aplicaciones que no se hayan estudiado.

## 9. Ruta de autoauditoría

1. **Representación:** convertir un valor decimal a binario, hexadecimal y BCD, explicando por qué BCD no equivale al binario puro.
2. **Aritmética:** resolver una suma y una resta en 8 bits, indicando carry, signo y overflow.
3. **Función:** leer una situación del proyecto y reconstruir variables y tabla de verdad.
4. **Simplificación:** obtener forma canónica y reducción por álgebra o Karnaugh.
5. **Comprobación:** probar todas las combinaciones en simulación y comparar con el protoboard.
6. **Diagnóstico:** escoger una discrepancia real y registrar síntoma, hipótesis, medición y corrección.

La autoevaluación es satisfactoria solo cuando el estudiante explica el procedimiento sin depender de una captura o de la respuesta de un compañero.

## 10. Caso de repaso integrador adaptado

Un control de agua usa `L` (nivel bajo), `H` (nivel alto) y `E` (habilitación). Antes de simplificar, el estudiante debe establecer qué significa cada bit y si `L=1,H=1` es válido para el tipo de sensores empleado. Luego propone `P` para bomba y `A` para alarma, construye tablas y verifica que ninguna combinación insegura active la bomba.

El valor de esta actividad no está en una fórmula única, sino en documentar supuestos. Dos equipos pueden obtener tablas diferentes si definen sensores de manera distinta; solo es aceptable la que sea coherente con la arquitectura declarada.

## 11. Diagnóstico autónomo

Antes de mover cables: comprobar `VCC` y `GND`; fijar entradas; comparar salida con tabla; medir un nodo intermedio; revisar una negación a la vez. Si la simulación también falla, volver a requisitos y expresión. Si solo falla el montaje, revisar pinout, entradas flotantes, continuidad y límites eléctricos.

## 12. Preguntas de control y trabajo independiente opcional

- ¿Puedo explicar la diferencia entre número, código y nivel eléctrico?
- ¿Identifico overflow sin confundirlo con carry?
- ¿Puedo pasar del requisito a la tabla y de la tabla al circuito?
- ¿Verifiqué todas las filas, incluidas las que no esperaba usar?
- ¿Mi registro permite repetir y confirmar la corrección?

El producto opcional es una página de autoauditoría con tres fortalezas, tres vacíos, dos evidencias y un plan concreto para la Semana 11. No se califica como entrega nueva.

## 13. Referencias de repaso

- Floyd, 9.ª ed., cap. 2, pp. 56–103: sistemas numéricos, aritmética y códigos.
- Ibid., cap. 3, pp. 124–197: compuertas, circuitos integrados y averías.
- Ibid., cap. 4, pp. 200–246: álgebra, De Morgan, formas estándar y Karnaugh.
- Ibid., cap. 14, pp. 884–914: comportamiento eléctrico TTL/CMOS.

## 14. Ruta de profundización recomendada

No se asigna lectura nueva. Según el vacío detectado, escoger una sola ruta de Floyd: cap. 2, pp. 56–103, para representación y aritmética; cap. 3, pp. 124–197, para compuertas y fallas; cap. 4, pp. 200–246, para álgebra/Karnaugh; o cap. 14, pp. 884–914, para problemas eléctricos. La prioridad es corregir comprensión, no adelantar contenido del Corte 3.
