# Marco teórico – Semana 12

# XOR, sumadores, restadores e integración inicial

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