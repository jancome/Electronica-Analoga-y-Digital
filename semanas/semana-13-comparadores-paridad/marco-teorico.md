# Marco teórico – Semana 13

# Comparadores, paridad y decisiones de control

## Metas de aprendizaje verificables

- Comparar palabras por igualdad y magnitud respetando prioridad de bits.
- Generar y comprobar paridad y demostrar experimentalmente su limitación.
- Traducir resultados de comparación o error en acciones seguras del proyecto.

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

## 16. Profundización: prioridad de magnitud e integridad básica

Para un bit, la igualdad es `E=A XNOR B`, mientras `G=A\bar B` indica `A>B` y `L=\bar AB` indica `A<B`. En palabras de varios bits, decide primero el bit más significativo donde los operandos difieren. Para dos bits:

\[
A=B=(A_1\odot B_1)(A_0\odot B_0)
\]

\[
A>B=A_1\bar B_1+(A_1\odot B_1)A_0\bar B_0
\]

donde `⊙` representa XNOR. Las tres salidas deben ser mutuamente excluyentes para datos válidos.

La paridad agrega un bit que hace par o impar el número total de unos. Para datos `D_0…D_{n-1}`, el bit de paridad par puede expresarse `P_e=D_0⊕D_1⊕…⊕D_{n-1}`. El receptor recalcula XOR; una discrepancia detecta cualquier número impar de errores, pero puede omitir dos, cuatro u otro número par. La paridad detecta; no localiza ni corrige el bit.

## 17. Ejemplos guiados adaptados

### Comparación

Consumo actual `A=1010₂ (10)` y límite `B=1001₂ (9)`. Los MSB `1` y `1` empatan; en el siguiente bit también; en el bit 1, `1>0`, de modo que `A>B` sin necesidad de bits inferiores. La salida puede activar una advertencia, pero una etapa BJT/MOSFET maneja la carga.

### Paridad

La palabra `1011010` contiene cuatro unos, por tanto para paridad par `P=0`. Si se invierte un bit, el total se vuelve impar y el comprobador señala error. Si se invierten dos bits, la cantidad puede volver a ser par y el error pasar inadvertido. Esta prueba debe documentarse para no atribuir a la paridad una seguridad que no ofrece.

## 18. Procedimiento de simulación y Lab 06

1. Definir ancho, orden de bits y formato de los operandos.
2. Probar igualdad, diferencia en MSB y diferencia solo en LSB.
3. Confirmar que exactamente una salida de comparación esté activa.
4. Generar paridad para palabras con número par e impar de unos.
5. Inyectar un error de un bit y luego uno de dos bits.
6. Montar con entradas definidas y medir salidas.
7. Relacionar cada salida con una acción segura y con la capacidad eléctrica del indicador.

## 19. Diagnóstico de fallas

Si `A=B` funciona pero magnitud está invertida, revisar orden MSB/LSB o cruce de operandos. Si dos salidas se activan, hay error de lógica, habilitación o cascada. Si la paridad no detecta un error simple, verificar si se diseñó paridad par o impar y si el bit de paridad fue incluido en la comprobación.

## 20. Preguntas orientadoras y trabajo independiente

- ¿Qué bit decide primero la magnitud y por qué?
- ¿Cómo se comparan palabras con signo?
- ¿Qué acción corresponde a `A=B`, `A>B` y `A<B`?
- ¿Qué tipos de error no detecta la paridad?
- ¿La aplicación necesita integridad de datos o una decisión de umbral?

El grupo entregará ecuaciones, tabla de casos representativos, simulación, pruebas de error simple/doble, mediciones y una decisión razonada sobre qué bloque aporta a su ABPr.

## 21. Referencias de estudio

- Floyd, 9.ª ed., cap. 6, sec. 6.4, pp. 344–347: comparadores.
- Ibid., sec. 6.10, pp. 379–382: generación y comprobación de paridad.
- Ibid., cap. 2, sec. 2.12, pp. 104–121: detección y corrección de errores y límites de los códigos.

## 22. Ruta de profundización recomendada

1. **Comparación:** Floyd, cap. 6, sec. 6.4, pp. 344–347.
2. **Paridad:** cap. 6, sec. 6.10, pp. 379–382.
3. **Fundamento de integridad:** cap. 2, sec. 2.12, pp. 104–121, para distinguir detección, localización y corrección.
4. **Ampliación aplicada:** contrastar los límites de paridad con los requisitos reales de seguridad o confiabilidad del ABPr.
