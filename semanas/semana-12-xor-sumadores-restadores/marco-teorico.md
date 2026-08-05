# Marco teórico – Semana 12

# XOR, sumadores, restadores e integración inicial

## Metas de aprendizaje verificables

- Derivar y comprobar XOR/XNOR, medio sumador y sumador completo.
- Seguir carry/borrow entre etapas e identificar el primer bit divergente.
- Integrar aritmética o detección de diferencia solo si responde a un requisito real.

## 1. Propósito de la semana

Iniciar la Fase 3 integrando aplicaciones aritméticas de la lógica combinacional al proyecto, cuando aporten una función real de conteo, diferencia, validación o procesamiento.

No todos los proyectos deben incluir un sumador. El circuito seleccionado debe responder a una necesidad de la solución y no añadirse únicamente para cumplir una lista de componentes.

## 2. Resultado de aprendizaje

Al finalizar la semana, el estudiante estará en capacidad de:

- Explicar la función de XOR y XNOR.
- Diseñar medio sumador y sumador completo.
- Interpretar acarreo de entrada y salida.
- Diseñar un medio restador básico.
- Identificar aplicaciones de detección de diferencia.
- Determinar si estos circuitos aportan al proyecto.
- Integrar una aplicación combinacional al prototipo físico.

## 3. Conexión con la Fase 3 ABPr

La Fase 3 debe transformar el montaje de laboratorio en una solución física integrada:

```text
Etapa analógica corregida
        +
Lógica digital simplificada
        +
Aplicación combinacional o secuencial
        ↓
Prototipo físico definitivo
        ↓
Maqueta y sustentación
```

## 4. Compuerta XOR

La XOR produce 1 cuando sus entradas son diferentes.

| A | B | A⊕B |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

Aplicaciones:

- Detección de diferencia.
- Suma de bits.
- Generación de paridad.
- Inversión controlada.

## 5. Compuerta XNOR

La XNOR produce 1 cuando las entradas son iguales. Puede utilizarse como comparador elemental de igualdad.

```text
A XNOR B = (A⊕B)̅
```

## 6. Medio sumador

Suma dos bits:

```text
S = A⊕B
C = A·B
```

- `S`: bit de suma.
- `C`: acarreo de salida.

## 7. Sumador completo

Suma A, B y un acarreo de entrada:

```text
S = A⊕B⊕Cin
Cout = A·B + Cin·(A⊕B)
```

Los sumadores completos pueden conectarse en cascada para operar con varios bits.

## 8. Medio restador

```text
D = A⊕B
P = A̅·B
```

- `D`: diferencia.
- `P`: préstamo.

## 9. Ejemplo aplicado

Un sistema necesita comparar dos estados y activar una alarma cuando sean diferentes. Una XOR puede realizar esta función sin necesidad de un sumador completo.

Esto demuestra que debe seleccionarse el bloque más simple que resuelva la necesidad.

## 10. Criterios para incorporar el tema al proyecto

El grupo debe responder:

1. ¿La solución requiere sumar, restar o detectar diferencia?
2. ¿Qué entradas representan los bits?
3. ¿Qué significado tiene el acarreo o préstamo?
4. ¿La función puede implementarse con menos compuertas?
5. ¿Cómo se integrará físicamente?

## 11. Actividad de clase y Labs 04–05

1. Construir tablas de medio sumador, sumador completo y medio restador.
2. Simular los circuitos.
3. Montar el circuito asignado.
4. Probar todas las combinaciones.
5. Identificar una posible aplicación en el proyecto.
6. Integrar solo el bloque que aporte valor.
7. Actualizar el diagrama del prototipo.

## 12. Evidencia ABPr

- Tabla de verdad.
- Expresiones.
- Simulación.
- Montaje de laboratorio.
- Decisión justificada de integración o no integración.
- Diagrama de bloques actualizado.
- Fotografía del primer ensamblaje físico de la Fase 3.

## 13. Errores comunes

- Confundir OR con XOR.
- Confundir suma con acarreo.
- Omitir `Cin` en el sumador completo.
- Incorporar un circuito que no aporta al problema.
- Conectar salidas entre sí.
- No considerar la capacidad eléctrica de las salidas.

## 14. Trabajo independiente

- Completar Labs 04 y 05.
- Corregir el montaje.
- Documentar si el proyecto utilizará XOR, sumador o restador.
- Diseñar la distribución física preliminar del prototipo y la maqueta.

## 15. Conexión con la Semana 13

La siguiente semana se estudiarán comparadores y paridad, útiles para tomar decisiones entre valores y verificar información digital.

## 16. Profundización: de la diferencia lógica a la aritmética

XOR vale uno cuando sus entradas son diferentes: `A⊕B=\bar AB+A\bar B`. XNOR vale uno cuando son iguales. Esta propiedad permite detectar cambio, generar paridad y producir el bit de suma de dos operandos.

El medio sumador tiene:

\[
S=A\oplus B,\qquad C=AB
\]

El sumador completo incluye acarreo de entrada:

\[
S=A\oplus B\oplus C_{in}
\]

\[
C_{out}=AB+C_{in}(A\oplus B)
\]

El medio restador produce diferencia `D=A⊕B` y préstamo `B_{out}=\bar AB`. En palabras de varios bits, cada etapa debe propagar carry o borrow. El retardo acumulado limita la velocidad de un sumador de acarreo serie; Floyd introduce el acarreo anticipado para reducir ese problema, aunque el montaje básico del curso prioriza comprensión funcional.

## 17. Ejemplo guiado adaptado

Para el sumador completo con `A=1`, `B=1`, `Cin=0`:

1. `A⊕B=0`.
2. `S=0⊕0=0`.
3. `Cout=AB+Cin(A⊕B)=1+0=1`.
4. La salida `10₂` representa `2`, coherente con `1+1+0`.

Para `A=0`, `B=1`, `Cin=1`, `S=0` y `Cout=1`: nuevamente `0+1+1=2`. Probar solo el primer caso no demuestra el circuito; un sumador completo exige las ocho combinaciones.

En un proyecto, XOR puede indicar discrepancia entre orden y realimentación: `F=ORDEN⊕ESTADO`. `F=1` señala que la carga no coincide con lo esperado. Esta aplicación suele ser más pertinente que agregar un sumador sin requerimiento numérico.

## 18. Procedimiento de simulación y Labs 04–05

1. Construir tablas de XOR/XNOR y del bloque aritmético.
2. Derivar expresiones y subdividir el sumador completo en dos medios sumadores.
3. Simular ocho casos con sondas para `S` y `Cout`.
4. En palabras de varios bits, observar el carry de cada etapa.
5. Consultar pinout, alimentación y límites de los CIs.
6. Montar y medir niveles; no evaluar solo LEDs.
7. Aplicar un vector que genere propagación de carry, por ejemplo `1111+0001`.
8. Integrar al ABPr únicamente si satisface una función trazable.

## 19. Diagnóstico de fallas

Si `S` falla cuando `A=B`, revisar XOR o inversión; si `Cout` falla solo con `Cin=1`, revisar la segunda rama de acarreo. En cascada, medir el carry entre etapas localiza el primer bit incorrecto. Un resultado correcto en bits bajos y erróneo en altos suele indicar propagación abierta, orden de bits o ancho insuficiente.

## 20. Preguntas orientadoras y trabajo independiente

- ¿XOR detecta cualquier cambio o solo diferencia instantánea?
- ¿Qué diferencia funcional existe entre carry y overflow?
- ¿Qué caso prueba mejor la propagación entre etapas?
- ¿El proyecto necesita aritmética o basta comparación/alarma?
- ¿Cómo se valida que un bloque añadido aporta valor?

Entregar tabla, derivación, simulación de todos los casos, dos mediciones físicas, diagnóstico de un carry interrumpido y una decisión justificada sobre su integración al proyecto.

## 21. Referencias de estudio

- Floyd, 9.ª ed., cap. 3, sec. 3.6, pp. 151–154: XOR y XNOR.
- Ibid., cap. 6, sec. 6.1, pp. 328–331: medio sumador y sumador completo.
- Ibid., secs. 6.2–6.3, pp. 332–343: sumadores en paralelo y acarreo serie/anticipado.

## 22. Ruta de profundización recomendada

1. **XOR/XNOR:** Floyd, cap. 3, sec. 3.6, pp. 151–154.
2. **Bloques básicos:** cap. 6, sec. 6.1, pp. 328–331.
3. **Palabras de varios bits:** cap. 6, sec. 6.2, pp. 332–339.
4. **Profundización temporal:** cap. 6, sec. 6.3, pp. 340–343, para comparar acarreo serie y anticipado.
