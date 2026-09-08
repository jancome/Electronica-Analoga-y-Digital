# Marco teórico – Semana 14

# Codificadores, decodificadores, displays y primera revisión física

## Metas de aprendizaje verificables

- Diferenciar codificación, prioridad, decodificación y validez de datos.
- Interpretar señales activas en bajo y dimensionar un display con hoja de datos.
- Diseñar una interfaz visual legible y eléctricamente compatible con el prototipo.

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

## 17. Profundización: traducción entre eventos, códigos y salidas

Un codificador convierte una entrada activa entre `2^n` posibilidades en un código de `n` bits. El codificador simple presupone una sola entrada activa; si pueden coexistir varias, se necesita prioridad y, preferiblemente, una salida de validez. Un decodificador realiza la operación inversa: para cada código habilitado activa una de varias salidas.

Las burbujas y barras indican señales activas en bajo. Una salida `/Y=0` puede significar “seleccionada”, no “apagada”. Ignorar esta convención es una causa frecuente de LEDs y displays invertidos.

En un display de 7 segmentos cada LED requiere limitación de corriente:

\[
R_{seg}=\frac{V_S-V_F-V_{salida}}{I_{seg}}
\]

El controlador 74LS47 está orientado a display de ánodo común y emplea salidas activas en bajo; su corriente, pinout y pines de control se verifican en la hoja de datos. Los códigos BCD `1010…1111` no representan dígitos decimales válidos y su respuesta debe definirse o bloquearse.

## 18. Ejemplo guiado adaptado

Un proyecto declara estados `00 normal`, `01 advertencia`, `10 alarma`, `11 mantenimiento`. Un decodificador 2-a-4 genera una línea por estado. Si las salidas son activas en bajo, el LED y su resistencia se conectan de acuerdo con la capacidad de hundimiento del CI, y la tabla debe anotar `0=activo`.

Para mostrar el dígito `5`, el código BCD es `0101`; el 74LS47 activa en bajo los segmentos correspondientes. El cálculo de resistencia no se reemplaza por “usar 220 Ω” de memoria: se parte de alimentación, `V_F`, caída de salida y corriente segura.

## 19. Procedimiento de simulación y Lab 07

1. Definir código, prioridad, habilitación y validez.
2. Construir tabla con estados válidos e inválidos.
3. Confirmar polaridad activa antes de conectar indicadores.
4. Simular cada código y rotular salidas.
5. Consultar hoja de datos del CI y tipo de display.
6. Calcular resistencias por segmento y estimar corriente total.
7. Montar y verificar un estado a la vez.
8. Realizar la primera revisión física del ABPr: legibilidad, conectores, referencias y acceso a puntos de prueba.

## 20. Diagnóstico de fallas

Si todos los segmentos están invertidos, comprobar tipo de display y polaridad activa. Si un segmento nunca enciende, intercambiar prueba entre segmento, resistencia y salida para aislar la falla. Si el código mostrado no coincide, revisar orden `D C B A`, entradas de blanking/lamp test y valores BCD inválidos. En codificadores, múltiples entradas activas sin prioridad producen códigos ambiguos.

## 21. Preguntas orientadoras y trabajo independiente

- ¿Qué sucede si se activan dos entradas del codificador?
- ¿Cómo indica el circuito que ninguna entrada es válida?
- ¿Qué significa una salida activa en bajo en la tabla y el montaje?
- ¿Cuál es la corriente total en el peor dígito?
- ¿Visualizar un número aporta más que indicadores de estado en este proyecto?

El grupo entregará tabla completa, selección de CI/display, cálculo de resistencias, simulación, mediciones, prueba de código inválido y justificación de la interfaz de usuario elegida.

## 22. Referencias de estudio

- Floyd, 9.ª ed., cap. 6, sec. 6.5, pp. 348–358: decodificadores y controlador BCD–7 segmentos.
- Ibid., sec. 6.6, pp. 359–363: codificadores y prioridad.
- Ibid., sec. 6.7, pp. 364–366: convertidores de código.
- Ibid., desarrollo del 74LS47, pp. 356–358: salidas activas en bajo y display de 7 segmentos.

## 23. Ruta de profundización recomendada

1. **Decodificación y display:** Floyd, cap. 6, sec. 6.5, pp. 348–358.
2. **Caso 74LS47:** pp. 356–358, acompañado por su hoja de datos.
3. **Codificación y prioridad:** cap. 6, sec. 6.6, pp. 359–363.
4. **Conversión entre códigos:** cap. 6, sec. 6.7, pp. 364–366; volver al cap. 2, secs. 2.10–2.11, para BCD y códigos válidos.
