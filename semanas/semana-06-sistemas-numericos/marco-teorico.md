# Marco teórico – Semana 06

# Sistemas numéricos y definición de variables del proyecto

## 1. Propósito de la semana

Iniciar la Fase 2 del ABPr mostrando cómo un sistema digital representa cantidades, estados y condiciones mediante bits.

El objetivo no es realizar conversiones de forma aislada, sino utilizarlas para definir las variables de entrada y salida del proyecto.

## 2. Resultado de aprendizaje

Al finalizar la semana, el estudiante estará en capacidad de:

- Diferenciar decimal, binario, hexadecimal y BCD.
- Realizar conversiones básicas entre sistemas.
- Diferenciar número binario y código.
- Definir variables digitales relacionadas con la situación problema.
- Establecer qué condición física representa 0 y qué condición representa 1.
- Actualizar el diagrama de bloques para iniciar la etapa lógica.

## 3. Conexión con la Fase 2 ABPr

La Fase 2 debe producir una solución digital funcional:

```text
Condiciones del problema
        ↓
Variables digitales
        ↓
Tabla de verdad
        ↓
Expresión y simplificación
        ↓
Simulación
        ↓
Montaje en protoboard
```

## 4. Conceptos fundamentales

- **Bit:** unidad mínima de información, con valores 0 o 1.
- **Nibble:** conjunto de 4 bits.
- **Byte:** conjunto de 8 bits.
- **Palabra:** grupo de bits tratado como una unidad.
- **Base:** cantidad de símbolos utilizados por un sistema numérico.

## 5. Sistema decimal

Utiliza diez símbolos, del 0 al 9. Cada posición representa una potencia de 10.

## 6. Sistema binario

Utiliza 0 y 1. Cada posición representa una potencia de 2.

```text
1011₂ = 1×2³ + 0×2² + 1×2¹ + 1×2⁰ = 11₁₀
```

## 7. Sistema hexadecimal

Utiliza los símbolos 0–9 y A–F. Cada dígito hexadecimal equivale a 4 bits.

```text
1010₂ = A₁₆
1111₂ = F₁₆
```

Es útil para representar patrones binarios de manera compacta.

## 8. Código BCD

Cada dígito decimal se representa mediante 4 bits.

```text
25₁₀ en BCD = 0010 0101
25₁₀ en binario puro = 11001₂
```

BCD será importante para decodificadores y displays de 7 segmentos.

## 9. Variables digitales del proyecto

Una variable digital debe tener un significado físico claro.

Ejemplos:

| Variable | 0 lógico | 1 lógico |
|---|---|---|
| L | Iluminación suficiente | Lugar oscuro |
| P | Sin presencia | Presencia detectada |
| N | Nivel suficiente | Nivel bajo |
| T | Temperatura normal | Temperatura alta |
| E | Energía no disponible | Energía disponible |

Los nombres deben ser cortos, pero su interpretación debe quedar documentada.

## 10. Entradas y salidas

- **Entradas:** representan condiciones del entorno, sensores, interruptores o estados.
- **Salidas:** representan una decisión: alarma, indicador, habilitación, bloqueo o control de carga.

Una salida digital no activa necesariamente una carga de forma directa; puede requerir BJT, MOSFET o relé.

## 11. Ejemplo aplicado

Un sistema de iluminación debe encender una lámpara solo cuando el sitio está oscuro y hay presencia.

```text
L = 1: oscuro
P = 1: presencia
Y = 1: encender lámpara
```

La función lógica se desarrollará posteriormente, pero desde esta semana las variables deben quedar definidas sin ambigüedad.

## 12. Actividad de clase

Cada grupo deberá:

1. Revisar la situación problema escogida.
2. Definir entre 2 y 4 variables digitales de entrada.
3. Definir al menos una salida.
4. Especificar el significado de 0 y 1 para cada variable.
5. Identificar si alguna magnitud debe convertirse a una condición digital mediante sensor, comparador o interruptor.
6. Actualizar el diagrama de bloques.

## 13. Evidencia ABPr

- Tabla de variables.
- Diagrama de bloques actualizado.
- Justificación de entradas y salidas.
- Representación binaria de estados o códigos utilizados.
- Registro de correcciones de la Fase 1 que se incorporarán.

## 14. Errores comunes

- Definir variables sin relacionarlas con una condición física.
- Confundir BCD con binario puro.
- Usar demasiadas variables para una primera implementación.
- No indicar si una entrada es activa en alto o en bajo.
- Pretender controlar una carga directamente desde una compuerta lógica.

## 15. Trabajo independiente

- Realizar conversiones decimal–binario–hexadecimal–BCD.
- Completar la tabla de variables del proyecto.
- Consultar los niveles eléctricos de los circuitos integrados que podrían utilizarse.
- Preparar ejemplos de estados o conteos que requiera la solución.

## 16. Conexión con la Semana 07

La siguiente semana se estudiará aritmética binaria para comprender acarreo, préstamo, complemento y representación de datos, especialmente en proyectos que requieran conteo o comparación.