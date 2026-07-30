# Marco teórico – Semana 07

# Aritmética binaria aplicada a estados y conteos

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