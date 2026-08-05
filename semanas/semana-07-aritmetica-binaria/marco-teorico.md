# Marco teórico – Semana 07

# Aritmética binaria aplicada a estados y conteos

## Metas de aprendizaje verificables

- Resolver suma y resta en ancho fijo usando carry y complemento a 2.
- Interpretar un patrón con y sin signo y diferenciar carry de overflow.
- Determinar el ancho y la operación que realmente requiere el proyecto.

## 1. Propósito de la semana

Comprender cómo se realizan operaciones aritméticas con bits y relacionarlas con conteos, comparación de estados y circuitos aritméticos que podrán incorporarse al proyecto.

## 2. Resultado de aprendizaje

Al finalizar la semana, el estudiante estará en capacidad de:

- Realizar suma y resta binaria.
- Interpretar acarreo y préstamo.
- Obtener complemento a 1 y complemento a 2.
- Representar números con signo.
- Detectar desbordamiento.
- Determinar si el proyecto necesita operaciones, conteos o códigos binarios.

## 3. Conexión con la Fase 2 ABPr

No todos los proyectos necesitarán una operación aritmética, pero todos deben comprender cómo se representan los estados.

La aritmética binaria prepara el estudio de:

- Sumadores y restadores.
- Contadores.
- Comparadores de magnitud.
- Códigos de estado.
- Indicadores numéricos.

## 4. Suma binaria

| Operación | Resultado | Acarreo |
|---|---|---|
| 0 + 0 | 0 | 0 |
| 0 + 1 | 1 | 0 |
| 1 + 0 | 1 | 0 |
| 1 + 1 | 0 | 1 |
| 1 + 1 + 1 | 1 | 1 |

El acarreo se transfiere a la siguiente posición de mayor peso.

## 5. Resta binaria

La resta puede hacerse de forma directa o mediante complemento a 2.

| Operación | Resultado | Préstamo |
|---|---|---|
| 0 − 0 | 0 | 0 |
| 1 − 0 | 1 | 0 |
| 1 − 1 | 0 | 0 |
| 0 − 1 | 1 | 1 |

## 6. Complemento a 1 y complemento a 2

Complemento a 1: invertir todos los bits.

```text
1010 → 0101
```

Complemento a 2: sumar 1 al complemento a 1.

```text
1010 → 0101 + 1 = 0110
```

El complemento a 2 permite representar números negativos y realizar restas utilizando circuitos sumadores.

## 7. Número de bits y rango

Un sistema de `n` bits sin signo puede representar:

```text
0 a 2ⁿ - 1
```

Con complemento a 2:

```text
-2ⁿ⁻¹ a 2ⁿ⁻¹ - 1
```

Antes de operar debe definirse cuántos bits tiene el sistema.

## 8. Overflow

El overflow ocurre cuando el resultado no puede representarse con el número de bits disponible.

En números con signo, no debe confundirse el acarreo de salida con el overflow. Este último puede detectarse cuando se suman dos números del mismo signo y el resultado aparece con signo contrario.

## 9. Ejemplo guiado

```text
  1011
+ 0110
------
 10001
```

Si el sistema es de 4 bits, el resultado requiere un bit adicional. El diseño debe decidir si conserva el acarreo, aumenta el número de bits o interpreta la condición como desbordamiento.

## 10. Aplicación al proyecto

Ejemplos de uso:

- Contar activaciones de una carga.
- Representar cuatro niveles mediante dos bits.
- Comparar un valor actual con un límite.
- Mostrar una cantidad en un display.
- Registrar estados de operación.

## 11. Actividad de clase

Cada grupo deberá responder:

1. ¿El proyecto requiere contar eventos?
2. ¿Necesita representar más de dos estados?
3. ¿Usará un código BCD o binario?
4. ¿Qué cantidad máxima debe representarse?
5. ¿Cuántos bits serían necesarios?

Después resolverá ejercicios de suma, resta y complemento relacionados con esas decisiones.

## 12. Evidencia ABPr

- Ejercicios de aritmética binaria.
- Definición del número de bits, cuando aplique.
- Justificación de códigos o conteos utilizados.
- Actualización de la tabla de variables.
- Preparación para el Quiz 2.

## 13. Errores comunes

- Olvidar el acarreo.
- Confundir complemento a 1 y complemento a 2.
- Operar sin fijar el número de bits.
- Confundir BCD con binario puro.
- Interpretar todo acarreo como overflow.
- Agregar operaciones al proyecto sin que aporten a la solución.

## 14. Trabajo independiente

- Resolver ejercicios con diferentes cantidades de bits.
- Verificar resultados mediante conversión decimal.
- Preparar el Quiz 2.
- Revisar si el proyecto necesita suma, resta, comparación o conteo.

## 15. Conexión con la Semana 08

La siguiente semana las condiciones del proyecto se convertirán en una función lógica implementada con compuertas y se realizará el primer montaje de la Fase 2 en protoboard.

## 16. Profundización: representación finita y significado del resultado

Las reglas de suma binaria son las mismas del sistema decimal, pero con base 2: `1+1=10₂`. El bit escrito es la suma módulo 2 y el bit transferido es el acarreo. En `n` bits sin signo, un acarreo fuera del MSB indica que el resultado matemático excede `2^n-1`.

En complemento a 2, el rango es `-2^{n-1}` a `2^{n-1}-1`. Para representar `-X`, se invierten los bits de `X` y se suma uno. La resta `A-B` se ejecuta como `A+C2(B)` descartando el acarreo final. El overflow con signo no es equivalente al carry: ocurre al sumar operandos del mismo signo y obtener un resultado de signo opuesto.

Dos reglas útiles son:

\[
C_2(X)=\overline{X}+1
\]

\[
V=C_{n-1}\oplus C_n
\]

donde `V` detecta overflow mediante los acarreos de entrada y salida del bit de signo.

## 17. Ejemplo guiado adaptado

En 8 bits:

1. `00110110₂ (54) + 00011101₂ (29) = 01010011₂ (83)`: no hay carry ni overflow.
2. Para `77-27`, `27=00011011`; su complemento a 2 es `11100101`. Entonces `01001101+11100101=1 00110010`. Se descarta el carry y queda `00110010₂=50`.
3. `01100100 (100)+00111100 (60)=10100000`. Aunque cabe como patrón de 8 bits, dos positivos produjeron bit de signo 1: existe overflow con signo; `160` tampoco cabe en el rango `-128…127`.

La conclusión debe indicar formato. El mismo patrón puede significar un entero sin signo, un entero con signo o un código; una operación sin convención carece de interpretación de ingeniería.

## 18. Práctica y verificación

1. Fijar ancho y representación antes de operar.
2. Resolver manualmente por columnas, mostrando carry/borrow.
3. Verificar en decimal sin sustituir el procedimiento.
4. Simular un sumador de 4 bits y observar `Cout`.
5. Probar valores frontera: `0000`, `0111`, `1000`, `1111`.
6. Registrar por separado carry y overflow.
7. Relacionar la operación con un requisito real: conteo, diferencia de umbrales o acumulación.

## 19. Diagnóstico de errores

Los errores más frecuentes son extender signo con ceros en vez del bit de signo, olvidar sumar uno al complemento, descartar un carry que sí importa en aritmética sin signo o interpretar carry como overflow. Para aislarlos se revisan ancho, formato, operandos, columnas y condición de bandera en ese orden.

## 20. Preguntas orientadoras y trabajo independiente

- ¿Cuál es el rango de 6, 8 y 10 bits con y sin signo?
- ¿Por qué `10000000₂` representa `128` sin signo y `-128` en C2?
- ¿Cuándo un carry es válido sin que exista overflow?
- ¿Qué ancho requiere el contador del proyecto antes de reiniciarse?
- ¿Conviene restar valores o comparar directamente?

Resolver un conjunto propio con dos sumas, dos restas por C2 y dos casos frontera. Cada operación debe incluir ancho, formato, resultado decimal, carry, overflow y una interpretación dentro del ABPr.

## 21. Referencias de estudio

- Floyd, 9.ª ed., cap. 2, sec. 2.4, pp. 63–66: aritmética binaria.
- Ibid., sec. 2.5, pp. 67–68 y ejemplos 2.12–2.13, p. 68: complementos.
- Ibid., secs. 2.6–2.7, pp. 69–81: números con signo, operaciones y overflow.

## 22. Ruta de profundización recomendada

1. **Operaciones básicas:** Floyd, cap. 2, sec. 2.4, pp. 63–66.
2. **Resta y negativos:** sec. 2.5, pp. 67–68, incluidos ejemplos 2.12–2.13.
3. **Análisis prioritario:** secs. 2.6–2.7, pp. 69–81, para números con signo, extensión y overflow.
4. **Puente al Corte 3:** cap. 6, secs. 6.1–6.3, pp. 328–343, como lectura anticipada sobre la implementación física de la aritmética.
