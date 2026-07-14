# Marco teórico – Semana 13

# Comparadores y paridad

## 1. Tema de la semana

Circuitos combinacionales para comparación de números binarios y detección básica de errores mediante paridad.

## 2. Objetivo de aprendizaje

Comprender el funcionamiento de comparadores digitales y circuitos de paridad, relacionándolos con aplicaciones de control y comunicación digital.

## 3. Contexto

Los sistemas digitales deben tomar decisiones. Para ello comparan valores, verifican estados y detectan errores. Los comparadores y circuitos de paridad son ejemplos de lógica combinacional aplicada a problemas reales.

## 4. Comparadores

Un comparador digital recibe dos números binarios y determina la relación entre ellos:

- A > B
- A = B
- A < B

## 5. Comparador de 1 bit

| A | B | A>B | A=B | A<B |
|---|---|---|---|---|
| 0 | 0 | 0 | 1 | 0 |
| 0 | 1 | 0 | 0 | 1 |
| 1 | 0 | 1 | 0 | 0 |
| 1 | 1 | 0 | 1 | 0 |

## 6. Paridad

La paridad agrega un bit adicional para ayudar a detectar errores simples en una palabra binaria.

- Paridad par: la cantidad total de unos debe ser par.
- Paridad impar: la cantidad total de unos debe ser impar.

## 7. Relación con XOR

La compuerta XOR es muy útil para generar y comprobar paridad porque su salida cambia cuando cambia la cantidad de unos.

## 8. Ejemplo guiado

Para la palabra 1011 hay tres unos. Si se usa paridad par, se agrega un bit 1 para que el total de unos sea cuatro.

```text
Dato: 1011
Bit de paridad par: 1
Palabra transmitida: 10111
```

## 9. Errores comunes

- Confundir comparación de igualdad con comparación de magnitud.
- No ordenar correctamente los bits más significativos.
- Confundir paridad par con paridad impar.
- Pensar que la paridad corrige errores; realmente solo ayuda a detectarlos.
- No verificar todas las combinaciones de entrada.

## 10. Preguntas orientadoras

1. ¿Qué salida se activa cuando A y B son iguales?
2. ¿Por qué se compara primero el bit más significativo?
3. ¿Qué es un bit de paridad?
4. ¿Qué tipo de error puede detectar la paridad?
5. ¿Por qué la XOR es útil en sistemas de paridad?

## 11. Trabajo independiente

Resolver ejercicios de comparación binaria y diseñar un generador de paridad para palabras de 3 o 4 bits.
