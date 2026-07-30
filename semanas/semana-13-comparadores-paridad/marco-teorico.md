# Marco teórico – Semana 13

# Comparadores, paridad y decisiones de control

## 1. Propósito de la semana

Utilizar circuitos combinacionales para comparar valores, detectar igualdad o diferencia y verificar datos mediante paridad, relacionando estas funciones con decisiones reales del proyecto ABPr.

## 2. Resultado de aprendizaje

Al finalizar la semana, el estudiante estará en capacidad de:

- Diseñar un comparador de 1 bit.
- Interpretar las salidas `A>B`, `A=B` y `A<B`.
- Explicar la comparación de palabras binarias.
- Generar y verificar paridad par o impar.
- Diferenciar detección y corrección de errores.
- Seleccionar una función de comparación útil para el prototipo.
- Comprobar la integración física del circuito.

## 3. Conexión con la Fase 3 ABPr

Los comparadores permiten convertir valores o estados en decisiones:

```text
Valor medido / estado
        ↓
Comparación con referencia
        ↓
Mayor, igual o menor
        ↓
Alarma, indicador o control
```

La paridad puede utilizarse para comprobar información digital, pero no corrige automáticamente los errores.

## 4. Comparador de 1 bit

| A | B | A>B | A=B | A<B |
|---|---|---|---|---|
| 0 | 0 | 0 | 1 | 0 |
| 0 | 1 | 0 | 0 | 1 |
| 1 | 0 | 1 | 0 | 0 |
| 1 | 1 | 0 | 1 | 0 |

Expresiones básicas:

```text
A>B = A·B̅
A<B = A̅·B
A=B = A XNOR B
```

## 5. Comparador de varios bits

En una palabra binaria se compara primero el bit más significativo. Si es igual, se revisa el siguiente.

Circuitos como el 7485 permiten comparar palabras de 4 bits y conectar varios integrados en cascada.

## 6. Comparación aplicada

Ejemplos de interpretación:

- Nivel actual mayor que límite permitido.
- Conteo igual a valor de referencia.
- Prioridad entre dos estados.
- Activación cuando una magnitud codificada supera un umbral.

En un proyecto puramente lógico, las entradas pueden generarse mediante interruptores. Para una variable analógica real puede requerirse un comparador analógico o una etapa de conversión antes de ingresar a la lógica digital.

## 7. Paridad

La paridad agrega un bit para que la cantidad total de unos sea:

- **Paridad par:** número par.
- **Paridad impar:** número impar.

La XOR es útil para generar y verificar paridad.

Ejemplo para `1011`, que contiene tres unos:

```text
Bit de paridad par = 1
Palabra transmitida = 10111
```

## 8. Límites de la paridad

La paridad:

- Puede detectar ciertos cambios en uno o un número impar de bits.
- No identifica cuál bit cambió.
- No corrige el error.
- Puede no detectar errores que cambien una cantidad par de bits.

## 9. Ejemplo aplicado al ABPr

Un sistema de nivel tiene dos bits que representan cuatro estados. El grupo puede comparar el estado actual con un código de nivel bajo y activar una alarma cuando exista coincidencia.

Debe explicarse por qué se usa comparación y qué valor físico representa cada código.

## 10. Actividad de clase y Lab 06

1. Construir un comparador de 1 bit.
2. Probar todas las combinaciones.
3. Analizar un comparador de varios bits.
4. Diseñar un generador de paridad.
5. Simular y montar el circuito asignado.
6. Determinar si el proyecto necesita comparación o paridad.
7. Integrar el bloque elegido al prototipo.
8. Registrar mediciones y fallas.

## 11. Evidencia ABPr

- Tabla y expresiones del comparador.
- Simulación.
- Montaje funcional.
- Aplicación escogida.
- Diagrama de bloques actualizado.
- Fotografía del avance físico.
- Registro de prueba y corrección.

## 12. Errores comunes

- Confundir igualdad con comparación de magnitud.
- Comparar primero el bit menos significativo.
- Confundir paridad par e impar.
- Afirmar que la paridad corrige errores.
- Incorporar comparadores sin definir códigos o referencias.
- No distinguir entre una entrada analógica y una entrada digital.

## 13. Preguntas orientadoras

1. ¿Qué salida se activa cuando A y B son iguales?
2. ¿Por qué se compara primero el bit más significativo?
3. ¿Qué representa la referencia en el proyecto?
4. ¿Qué errores puede detectar la paridad?
5. ¿Qué etapa convierte una magnitud física en un estado digital?

## 14. Trabajo independiente

- Completar el Lab 06.
- Documentar la aplicación de comparación o paridad.
- Corregir el prototipo.
- Preparar la primera revisión física de la Semana 14.

## 15. Conexión con la Semana 14

La siguiente semana se estudiarán codificadores, decodificadores y display de 7 segmentos para representar o visualizar estados del sistema.