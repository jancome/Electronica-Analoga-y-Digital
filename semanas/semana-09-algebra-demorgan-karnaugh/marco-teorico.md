# Marco teórico – Semana 09

# Álgebra booleana, De Morgan y mapas de Karnaugh

## Propósito

Obtener una implementación lógica más sencilla a partir de una tabla de verdad mediante simplificación algebraica, teoremas de De Morgan y mapas de Karnaugh de hasta cuatro variables.

## Resultados de aprendizaje

- Traducir una tabla de verdad a una expresión canónica.
- Aplicar leyes booleanas y teoremas de De Morgan.
- Construir mapas de Karnaugh de 2, 3 y 4 variables.
- Formar agrupaciones válidas y obtener una expresión mínima.
- Comparar el circuito original con el simplificado.
- Aplicar la simplificación a la lógica del Preproyecto ABP 2.

## 1. Álgebra booleana

Las variables booleanas toman valores 0 o 1. Las operaciones fundamentales son complemento, producto lógico y suma lógica.

| Ley | Expresión |
|---|---|
| Identidad | A + 0 = A; A·1 = A |
| Anulación | A + 1 = 1; A·0 = 0 |
| Idempotencia | A + A = A; A·A = A |
| Complemento | A + A̅ = 1; A·A̅ = 0 |
| Absorción | A + A·B = A |
| Distributiva | A(B + C) = AB + AC |

## 2. Teoremas de De Morgan

```text
(A·B)̅ = A̅ + B̅
(A+B)̅ = A̅·B̅
```

Son esenciales para convertir implementaciones AND–OR en NAND o NOR y para interpretar correctamente señales activas en bajo.

## 3. De la tabla de verdad a minterminos

Cada fila con salida 1 genera un mintermino. Una variable aparece directa cuando vale 1 y complementada cuando vale 0.

Para A=1, B=0 y C=1:

```text
m = A·B̅·C
```

La suma de todos los minterminos activos produce la forma canónica SOP.

## 4. Mapas de Karnaugh

El mapa ordena las combinaciones mediante código Gray, de modo que celdas adyacentes solo cambian en una variable.

### Reglas de agrupación

- Los grupos contienen 1, 2, 4, 8 o 16 celdas.
- Deben ser rectangulares y contener valores 1 para una forma SOP.
- Se forman grupos tan grandes como sea posible.
- Los bordes opuestos son adyacentes.
- Una celda puede participar en más de un grupo.
- Todas las celdas con 1 deben quedar cubiertas.
- Las condiciones “no importa” pueden usarse si simplifican la función.

## 5. Ejemplo de tres variables

Sea:

```text
F(A,B,C) = Σm(1,3,5,7)
```

Los cuatro minterminos corresponden a todas las combinaciones donde C=1. Al agruparlos:

```text
F = C
```

La simplificación muestra que A y B no afectan la salida.

## 6. Ejemplo aplicado al ABP

Suponga tres entradas:

- E: energía disponible.
- N: nivel de agua bajo.
- M: modo automático.

La bomba debe habilitarse cuando hay energía, el nivel es bajo y el modo automático está activo:

```text
BOMBA = E·N·M
```

Si se agregan condiciones de bloqueo o prioridad, se construye la tabla completa, se obtiene la forma canónica y se simplifica antes del montaje.

## 7. Circuitos universales

Una función simplificada puede implementarse con NAND o NOR. De Morgan permite transformar la expresión sin cambiar la tabla de verdad. El grupo debe comparar cantidad de integrados, conexiones, entradas disponibles y niveles activos.

## 8. Errores frecuentes

- Ordenar columnas en binario natural y no en Gray.
- Agrupar en cantidades distintas a potencias de dos.
- Hacer agrupaciones diagonales.
- Omitir la adyacencia entre bordes.
- Cambiar la función al aplicar De Morgan.
- Simplificar sin comprobar la tabla de verdad final.

## 9. Conexión con Labs 02 y 03

Los laboratorios permiten comprobar equivalencias y transformaciones. El resultado no debe limitarse a una manipulación algebraica: ambos circuitos deben producir la misma salida para todas las combinaciones.

## 10. Avance del Preproyecto ABP 2

Cada grupo debe entregar:

1. Definición de entradas y salidas.
2. Tabla de verdad completa.
3. Expresión canónica.
4. Simplificación algebraica o Karnaugh.
5. Implementación propuesta.
6. Comparación entre circuito original y simplificado.
7. Evidencia de simulación.

## 11. Comprobación de aprendizaje

1. ¿Por qué el código Gray es necesario en Karnaugh?
2. ¿Qué variable se elimina dentro de una agrupación?
3. ¿Cómo se comprueba que dos circuitos son equivalentes?
4. ¿Cuándo conviene utilizar una condición “no importa”?
5. ¿Cómo reduce la simplificación el costo o la probabilidad de falla?

## Fuentes de consulta

- T. L. Floyd, *Fundamentos de sistemas digitales*.
- R. Tocci, N. Widmer y G. Moss, *Sistemas digitales: principios y aplicaciones*.
- All About Circuits, secciones de álgebra booleana y Karnaugh.
