# Marco teórico – Semana 14

# Codificadores, decodificadores, displays y primera revisión física

## 1. Propósito de la semana

Comprender cómo los sistemas digitales transforman y presentan información mediante codificadores, decodificadores y displays, utilizando estos bloques para mejorar la interfaz del proyecto ABPr.

La semana incluye la **primera revisión formal del prototipo físico**.

## 2. Resultado de aprendizaje

Al finalizar la semana, el estudiante estará en capacidad de:

- Diferenciar codificación y decodificación.
- Interpretar un codificador con prioridad.
- Analizar un decodificador de `n` entradas a `2ⁿ` salidas.
- Diferenciar binario puro y BCD.
- Conectar un decodificador BCD a display de 7 segmentos.
- Identificar señales activas en alto y activas en bajo.
- Verificar compatibilidad entre integrado y tipo de display.
- Incorporar una interfaz visual útil al proyecto.

## 3. Conexión con la Fase 3 ABPr

La visualización debe ayudar al usuario a interpretar el sistema:

```text
Estado o código interno
        ↓
Decodificador / lógica de interfaz
        ↓
LED, display o indicadores
        ↓
Información comprensible
```

No es obligatorio usar display si no aporta a la solución. Puede emplearse una combinación de indicadores claramente identificados.

## 4. Codificador

Un codificador convierte una entrada activa entre varias posibilidades en un código binario.

Ejemplo: un codificador 8 a 3 representa ocho entradas mediante tres bits.

La versión elemental supone que solo una entrada está activa a la vez.

## 5. Codificador con prioridad

Cuando varias entradas se activan simultáneamente, el codificador con prioridad entrega el código correspondiente a la entrada definida como más importante.

Aplicaciones:

- Gestión de alarmas.
- Solicitudes múltiples.
- Identificación de eventos prioritarios.
- Teclados o entradas de selección.

## 6. Decodificador

Un decodificador recibe un código y activa una salida específica.

Ejemplo: un decodificador 2 a 4 posee dos entradas y cuatro salidas posibles.

Debe comprobarse:

- Entrada de habilitación.
- Polaridad de las salidas.
- Estados no utilizados.
- Capacidad de corriente.

## 7. Código BCD

BCD representa cada dígito decimal mediante cuatro bits.

```text
5₁₀ = 0101 BCD
9₁₀ = 1001 BCD
```

Las combinaciones 1010 a 1111 no representan dígitos decimales válidos en BCD.

## 8. Display de 7 segmentos

Los segmentos se identifican normalmente como `a, b, c, d, e, f, g`.

Tipos:

- **Ánodo común.**
- **Cátodo común.**

La selección del decodificador debe ser compatible con el display y con la polaridad de sus salidas.

Cada segmento requiere limitación de corriente.

```text
Rsegmento = (VCC - VF) / Isegmento
```

## 9. Señales activas en bajo

Una burbuja en el símbolo o una barra sobre el nombre indica que la función se activa con 0 lógico.

Ejemplo de notación:

```text
E̅ = habilitación activa en bajo
```

Debe evitarse interpretar una salida activa en bajo como una falla del circuito.

## 10. Ejemplo aplicado

Un sistema posee cuatro estados codificados en dos bits:

| Código | Estado |
|---|---|
| 00 | Normal |
| 01 | Advertencia |
| 10 | Alarma |
| 11 | Mantenimiento |

Un decodificador puede activar un indicador diferente para cada estado. La solución debe asegurar que el usuario entienda el significado de cada salida.

## 11. Actividad de clase y Lab 07

1. Analizar un codificador y un decodificador.
2. Completar tablas de funcionamiento.
3. Consultar hojas de datos.
4. Simular un decodificador BCD–7 segmentos.
5. Montar el circuito con resistencias.
6. Identificar ánodo o cátodo común.
7. Probar códigos válidos y no válidos.
8. Seleccionar una interfaz útil para el proyecto.

## 12. Primera revisión física del prototipo

El grupo debe presentar:

- Etapa analógica corregida.
- Lógica combinacional funcional.
- Integración parcial en una base física.
- Alimentación segura.
- Entradas claramente identificadas.
- Salidas o indicadores visibles.
- Diagrama de bloques actualizado.
- Lista de correcciones pendientes.

La maqueta todavía puede estar en construcción, pero debe existir una propuesta física concreta.

## 13. Evidencia ABPr

- Lab 07.
- Tabla de codificación o decodificación.
- Simulación y montaje.
- Cálculo de resistencias.
- Fotografías de la primera revisión física.
- Boceto o diseño de la maqueta.
- Retroalimentación recibida.

## 14. Errores comunes

- Confundir codificador y decodificador.
- Confundir BCD con binario puro.
- No identificar salidas activas en bajo.
- Conectar un display sin resistencias.
- Usar decodificador y display incompatibles.
- Sobrecargar las salidas del integrado.
- Añadir una pantalla que no mejora la comprensión del proyecto.

## 15. Trabajo independiente

- Completar el Lab 07.
- Corregir el prototipo según la revisión.
- Avanzar en la maqueta o base de presentación.
- Preparar una explicación breve para la muestra de la Semana 15.

## 16. Conexión con la Semana 15

La siguiente semana se estudiarán multiplexores y demultiplexores y se realizará la muestra de prototipos con revisión de la maqueta.