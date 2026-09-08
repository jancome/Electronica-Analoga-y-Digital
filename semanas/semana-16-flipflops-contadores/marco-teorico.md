# Marco teórico – Semana 16

# Flip-flops, contadores y ajustes finales del proyecto

## Metas de aprendizaje verificables

- Interpretar estado, flanco, entradas asíncronas y restricciones temporales.
- Diseñar y comprobar una secuencia de conteo, incluidos arranque y estados no usados.
- Diagnosticar rebote, reset, reloj y retardos antes de integrar lógica secuencial.

## 1. Propósito de la semana

Introducir la lógica secuencial mediante flip-flops y contadores, evaluar su posible aporte al proyecto y completar las correcciones finales de funcionamiento, documentación y presentación física.

## 2. Resultado de aprendizaje

Al finalizar la semana, el estudiante estará en capacidad de:

- Diferenciar lógica combinacional y secuencial.
- Explicar el concepto de estado almacenado.
- Identificar las funciones básicas de flip-flops SR, D, JK y T.
- Interpretar reloj, flanco y entradas asíncronas.
- Diferenciar contadores síncronos y asíncronos.
- Relacionar conteo o memoria con aplicaciones reales.
- Decidir si un bloque secuencial aporta al proyecto.
- ejecutar pruebas finales y documentar correcciones.

## 3. Lógica combinacional y secuencial

- **Combinacional:** la salida depende de las entradas actuales.
- **Secuencial:** la salida depende de las entradas actuales y del estado previo.

La memoria permite construir contadores, registros, temporizadores y máquinas de estados.

## 4. Flip-flop

Un flip-flop almacena un bit de información.

### SR

Permite establecer o borrar el estado. Debe revisarse la condición no permitida según la implementación.

### D

Almacena el valor presente en D durante el flanco activo del reloj.

### JK

Evita la condición indeterminada del SR y puede alternar su salida cuando `J=K=1`.

### T

Alterna el estado cuando T está activa. Es útil en contadores y divisores de frecuencia.

## 5. Reloj y flancos

El reloj sincroniza los cambios de estado.

- Flanco de subida: transición 0→1.
- Flanco de bajada: transición 1→0.

Las señales mecánicas pueden producir rebote y generar múltiples pulsos. Debe considerarse antirrebote cuando se utilicen pulsadores.

## 6. Entradas asíncronas

Entradas como preset y clear pueden modificar el estado sin esperar el reloj. Frecuentemente son activas en bajo y no deben dejarse flotantes.

## 7. Contadores

Un contador avanza por una secuencia de estados.

Tipos:

- Asíncrono o ripple.
- Síncrono.
- Ascendente.
- Descendente.
- Módulo N.

Un contador de `n` flip-flops puede representar hasta `2ⁿ` estados antes de repetir, salvo que se modifique su módulo.

## 8. Aplicaciones al proyecto

- Conteo de activaciones.
- Registro de ciclos de una bomba.
- División de frecuencia.
- Secuencia de indicadores.
- Memoria de una alarma.
- Alternancia entre estados.

No debe agregarse lógica secuencial si no aporta a la situación problema.

## 9. Ejemplo aplicado

Un sistema debe contar hasta cuatro activaciones de una carga y encender una advertencia en el cuarto evento. Se puede utilizar un contador de 2 bits y una lógica de detección del estado `11`.

El diseño debe incluir:

- Fuente de pulsos.
- Antirrebote si el pulso es manual.
- Reinicio.
- Indicadores de estado.
- Interpretación física del conteo.

## 10. Actividad de clase

1. Analizar tablas de excitación básicas.
2. Simular un flip-flop.
3. Simular un contador.
4. Observar el efecto del reloj.
5. Probar reset y preset.
6. Determinar si el proyecto requiere memoria o conteo.
7. Integrar el bloque solo cuando sea útil.

## 11. Ajustes finales ABPr

El grupo deberá verificar:

- Funcionamiento estable.
- Alimentación y seguridad.
- Prototipo físico definitivo.
- Maqueta terminada y rotulada.
- Correspondencia entre simulación y montaje.
- Corrección de observaciones de la muestra.
- Lista de materiales y costos.
- Informe técnico.
- Video demostrativo.
- Roles y aportes.
- Preparación de la sustentación individual.

## 12. Pruebas finales

Como mínimo:

1. Prueba de encendido.
2. Prueba de cada entrada.
3. Prueba de cada salida.
4. Prueba de combinaciones límite.
5. Prueba repetida de funcionamiento.
6. Medición de voltajes principales.
7. Verificación de temperatura o consumo cuando aplique.
8. Prueba de recuperación después de desconexión.

## 13. Evidencia ABPr

- Simulación del circuito secuencial, cuando aplique.
- Prototipo corregido.
- Maqueta terminada.
- Tabla de pruebas.
- Registro de correcciones.
- Borrador final del informe.
- Borrador del video.
- Preparación del Quiz 3.

## 14. Errores comunes

- Confundir latch y flip-flop.
- No identificar el flanco activo.
- Dejar preset o clear flotantes.
- Ignorar el rebote de pulsadores.
- Agregar un contador sin función real.
- Realizar cambios de última hora sin repetir pruebas.
- Preparar únicamente la explicación de una parte del sistema.

## 15. Trabajo independiente

- Completar las pruebas.
- Corregir informe y video.
- Practicar la sustentación.
- Preparar respuestas individuales.
- Entregar una versión final ordenada de diagramas, simulación y evidencias.

## 16. Conexión con la Semana 17

La siguiente semana se presentará el proyecto físico definitivo con su maqueta, informe, video y sustentación grupal e individual.

## 17. Profundización: estado, tiempo y secuencia

Un circuito combinacional depende solo de entradas presentes; uno secuencial depende además del estado previo. Un latch responde a nivel, mientras un flip-flop actualiza normalmente en un flanco de reloj. Para el flip-flop D, `Q^+=D` en el flanco activo. Para T, `Q^+=T⊕Q`; con `T=1` alterna. JK evita el estado no permitido del SR y con `J=K=1` conmuta.

La temporización exige respetar setup, hold y retardo de propagación. Una entrada que cambia demasiado cerca del flanco puede producir metastabilidad; por eso señales asíncronas y pulsadores requieren sincronización o antirrebote. Las entradas preset/clear asíncronas dominan el reloj y no deben quedar flotantes.

Un contador de `n` bits posee hasta `2^n` estados. Para módulo `M`, se requiere `n=⌈log₂M⌉`; los estados restantes deben manejarse para que el circuito recupere una secuencia válida. En un contador asíncrono, los retardos se acumulan; en uno síncrono, los flip-flops comparten reloj y la lógica define qué bits cambian.

## 18. Ejemplo guiado adaptado: contador módulo 6

Para registrar ciclos de una bomba:

1. `n=⌈log₂6⌉=3` flip-flops.
2. Secuencia válida: `000→001→010→011→100→101→000`.
3. `110` y `111` son estados no usados; se diseña recuperación hacia `000`.
4. Se detecta `110` para generar reset en una realización simple, verificando la polaridad y duración requeridas.
5. Un pulsador directo puede generar múltiples conteos; se incluye antirrebote.
6. Se prueba arranque, seis pulsos, reset, estado no usado y recuperación.

Para un flip-flop D, se prepara una tabla de `D` antes de cada flanco y se predice `Q` después del retardo. Los cambios entre flancos no se almacenan hasta el siguiente evento activo.

## 19. Procedimiento de simulación y práctica

1. Dibujar diagrama de tiempos antes de conectar.
2. Definir flanco, frecuencia, reset y estado inicial.
3. Simular con reloj lento y observar `CLK`, entradas y `Q` simultáneamente.
4. Probar entradas asíncronas por separado.
5. Construir contador y recorrer toda la secuencia.
6. Forzar cada estado no usado y verificar recuperación.
7. Comparar asíncrono/síncrono observando transitorios de salidas.
8. Si se usa pulsador, demostrar el efecto del rebote y la corrección.

## 20. Diagnóstico de fallas

Si no hay conteo, verificar reloj en el pin, reset/preset y alimentación. Si salta estados, revisar rebote, orden de bits y decodificación de reset. Si inicia aleatoriamente, falta inicialización. Si un LED parece mostrar códigos breves inesperados, medir retardos y distinguir transitorios de una secuencia lógica incorrecta.

## 21. Preguntas orientadoras y trabajo independiente

- ¿Qué información debe persistir y durante cuánto tiempo?
- ¿La señal de reloj está limpia y dentro de límites?
- ¿Qué sucede al encender y desde estados no usados?
- ¿Cuál contador tolera mejor la decodificación de salidas?
- ¿Memoria o conteo aporta una función necesaria al ABPr?

Entregar diagrama de tiempos, tabla de estados, cálculo de módulo, simulación de recuperación, prueba de antirrebote, mediciones y justificación de inclusión o exclusión del bloque secuencial.

## 22. Referencias de estudio

- Floyd, 9.ª ed., cap. 7, secs. 7.1–7.4, pp. 412–440: latches, flip-flops y aplicaciones.
- Ibid., sec. 7.6, pp. 448–453: temporizador 555 como ampliación opcional.
- Ibid., cap. 8, secs. 8.1–8.3, pp. 476–498: contadores asíncronos, síncronos y ascendente/descendente.
- Ibid., secs. 8.5–8.7, pp. 509–522: cascada, decodificación y aplicaciones; cap. 14, pp. 884–914: retardos y límites eléctricos.

## 23. Ruta de profundización recomendada

1. **Memoria elemental:** Floyd, cap. 7, secs. 7.1–7.4, pp. 412–440.
2. **Reloj opcional:** cap. 7, sec. 7.6, pp. 448–453, para temporizador 555.
3. **Conteo obligatorio:** cap. 8, secs. 8.1–8.3, pp. 476–498.
4. **Profundización de sistema:** cap. 8, secs. 8.5–8.7, pp. 509–522, y cap. 14 para retardos; comparar arranque, cascada, decodificación y recuperación.
