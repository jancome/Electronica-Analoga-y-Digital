# Marco teórico – Semana 15

# Multiplexores, demultiplexores y muestra de prototipos

## Metas de aprendizaje verificables

- Seleccionar y distribuir señales mediante selectores y habilitación documentados.
- Comprobar todos los canales e implementar una función con MUX cuando sea ventajoso.
- Convertir la muestra formativa en correcciones técnicas verificables.

## 1. Propósito de la semana

Comprender la selección y distribución de señales mediante MUX y DEMUX y realizar una muestra formativa del prototipo ABPr con su maqueta o base de presentación.

La muestra no es necesariamente la entrega definitiva. Su propósito es detectar fallas y orientar las correcciones finales.

## 2. Resultado de aprendizaje

Al finalizar la semana, el estudiante estará en capacidad de:

- Explicar el funcionamiento de un multiplexor.
- Explicar el funcionamiento de un demultiplexor.
- Calcular la cantidad de líneas de selección.
- Interpretar habilitaciones y salidas activas en bajo.
- Seleccionar o distribuir señales dentro de una aplicación.
- Determinar si MUX o DEMUX aporta al proyecto.
- Presentar un prototipo físico funcional y recibir retroalimentación.

## 3. Conexión con la Fase 3 ABPr

Un MUX o DEMUX puede optimizar conexiones, pero no debe incorporarse sin necesidad.

Ejemplos:

- Seleccionar una de varias señales de sensores.
- Elegir modos de operación.
- Compartir una línea de visualización.
- Distribuir una señal de control a diferentes salidas.

## 4. Multiplexor

Un multiplexor selecciona una de varias entradas y la conecta a una salida.

Para un MUX de `2ⁿ` entradas se requieren `n` líneas de selección.

Ejemplo MUX 4 a 1:

| S1 | S0 | Salida |
|---|---|---|
| 0 | 0 | `Y=I0` |
| 0 | 1 | `Y=I1` |
| 1 | 0 | `Y=I2` |
| 1 | 1 | `Y=I3` |

## 5. Entrada de habilitación

Muchos integrados tienen una entrada Enable. Puede ser activa en alto o activa en bajo.

Si la habilitación no está en el estado correcto, el circuito no funcionará aunque las líneas de selección estén bien conectadas.

## 6. Demultiplexor

Un DEMUX recibe una entrada y la dirige hacia una de varias salidas según las líneas de selección.

Puede utilizarse para:

- Distribuir pulsos.
- Seleccionar actuadores.
- Dirigir una señal de habilitación.
- Activar indicadores por canal.

## 7. Decodificador utilizado como DEMUX

Algunos decodificadores pueden utilizarse como demultiplexores si su entrada de habilitación recibe la señal de datos. La hoja de datos debe confirmar el comportamiento y la polaridad de las salidas.

## 8. Implementación de funciones con MUX

Un multiplexor también puede implementar funciones lógicas conectando sus entradas de datos a 0, 1 o variables.

El procedimiento incluye:

1. Elegir variables de selección.
2. Analizar la tabla de verdad.
3. Determinar el valor de cada entrada de datos.
4. Verificar la función resultante.

## 9. Ejemplo aplicado

Un sistema debe mostrar alternativamente el estado de cuatro sensores en una sola línea de visualización. Un MUX 4 a 1 permite seleccionar el sensor mediante dos líneas.

La aplicación es válida solo si la selección mejora el diseño o reduce recursos.

## 10. Actividad de clase y Lab 08

1. Completar tablas de MUX y DEMUX.
2. Simular un MUX 4 a 1.
3. Simular o montar un DEMUX 1 a 4.
4. Verificar la habilitación.
5. Probar todas las selecciones.
6. Evaluar si el bloque aporta al proyecto.
7. Integrarlo cuando sea pertinente.

## 11. Muestra formativa del proyecto

Cada grupo deberá presentar:

- Situación problema.
- Diagrama de bloques.
- Etapa analógica.
- Lógica digital.
- Aplicación combinacional o secuencial seleccionada.
- Prototipo físico funcional o parcialmente funcional.
- Maqueta, estructura o base de presentación.
- Simulación actualizada.
- Evidencias y mediciones.
- Fallas abiertas y plan de corrección.

## 12. Retroalimentación de la muestra

La revisión debe responder:

1. ¿El proyecto resuelve la situación propuesta?
2. ¿La integración analógica–digital es coherente?
3. ¿El prototipo funciona de manera repetible?
4. ¿La maqueta permite comprender la aplicación?
5. ¿La alimentación es segura?
6. ¿Las entradas y salidas están identificadas?
7. ¿Qué debe corregirse antes de la sustentación?

## 13. Evidencia ABPr

- Lab 08.
- Tabla de selección o distribución.
- Simulación o montaje del MUX/DEMUX.
- Prototipo presentado.
- Maqueta o base física.
- Registro de retroalimentación.
- Plan de mejora con responsables y fechas.

## 14. Errores comunes

- Confundir MUX con DEMUX.
- No conectar correctamente la habilitación.
- Ignorar salidas activas en bajo.
- Incorporar un MUX sin necesidad.
- Mostrar una maqueta sin circuito funcional.
- Presentar un circuito funcional sin explicar el problema.
- Ocultar fallas en lugar de registrarlas.

## 15. Trabajo independiente

- Aplicar la retroalimentación de la muestra.
- Completar la maqueta.
- Mejorar orden, rotulado y conexiones.
- Actualizar informe, simulación y video.
- Preparar el Quiz 3 y las pruebas finales.

## 16. Conexión con la Semana 16

La siguiente semana se estudiarán flip-flops y contadores y se realizarán los ajustes finales de funcionamiento, documentación y presentación.

## 17. Profundización: compartir rutas sin perder trazabilidad

Un multiplexor selecciona una de `2^n` entradas mediante `n` líneas de selección. Para un MUX 4-a-1:

\[
Y=\bar S_1\bar S_0I_0+\bar S_1S_0I_1+S_1\bar S_0I_2+S_1S_0I_3
\]

La habilitación puede ser activa en alto o bajo y domina la salida cuando está deshabilitada. Un demultiplexor dirige una entrada a una salida seleccionada; un decodificador puede cumplir esa función si su Enable actúa como dato, pero las polaridades deben coincidir.

El MUX también implementa funciones: se escogen algunas variables como selectores y se conectan las entradas de datos a `0`, `1`, una variable o su complemento según la tabla. Esta técnica reduce puertas, pero puede dificultar diagnóstico si no se documenta la correspondencia de canales.

## 18. Ejemplo guiado adaptado

Cuatro señales `I0…I3` representan nivel, temperatura, estado de carga y modo manual. `S1S0` selecciona qué señal observar en `Y`:

| `S1S0` | salida |
|---|---|
| `00` | `I0` |
| `01` | `I1` |
| `10` | `I2` |
| `11` | `I3` |

Para probar el enrutamiento se aplica un patrón distinguible, por ejemplo `I0I1I2I3=1010`, y se recorre la selección. Luego se invierte una sola entrada para confirmar que no existe conexión cruzada. El proyecto debe explicar quién genera `S1S0` y qué ocurre si Enable está inactivo.

## 19. Procedimiento de simulación y Lab 08

1. Leer tabla funcional y polaridades del CI.
2. Fijar Enable en estado activo y comprobar todos los canales.
3. Probar estado deshabilitado y registrar la salida definida por el fabricante.
4. Aplicar patrones que permitan distinguir canales.
5. Medir selectores, dato seleccionado y salida.
6. Para DEMUX, seguir una entrada por todas las rutas y verificar que las no seleccionadas permanezcan inactivas.
7. Comparar implementación con puertas frente a MUX por CIs, cableado y retardo.
8. Incorporar la retroalimentación de la muestra de prototipos a una lista verificable.

## 20. Diagnóstico de fallas

Una salida fija suele indicar Enable incorrecto, selector flotante o alimentación. Un orden de canales desplazado apunta a `S0/S1` intercambiados. Si aparecen varias salidas activas en DEMUX, revisar polaridad y conexiones del decodificador. Se diagnostica fijando datos conocidos, recorriendo selección binaria y midiendo los selectores antes de sospechar el CI.

## 21. Preguntas orientadoras y trabajo independiente

- ¿Quién controla las líneas de selección y con qué estado inicial?
- ¿Qué salida produce el modo deshabilitado?
- ¿MUX reduce realmente componentes y cableado en el prototipo?
- ¿Cómo se evita que una selección transitoria active una salida insegura?
- ¿La aplicación necesita compartir una ruta o distribuir una orden?

El grupo entregará tabla de selección, simulación completa, mediciones, diagnóstico de selectores cruzados y análisis de utilidad. Además, convertirá la retroalimentación de la muestra en acciones con responsable y prueba de cierre.

## 22. Referencias de estudio

- Floyd, 9.ª ed., cap. 6, sec. 6.8, pp. 367–376: multiplexores e implementación de funciones.
- Ibid., sec. 6.9, pp. 377–378: demultiplexores.
- Ibid., ejercicios de aplicación del cap. 6 con 74LS151: metodología para realizar funciones, sin reproducir sus soluciones.

## 23. Ruta de profundización recomendada

1. **Selección de datos:** Floyd, cap. 6, sec. 6.8, pp. 367–376.
2. **Realización de funciones:** revisar en esa sección el método con MUX y los ejercicios del 74LS151, resolviendo valores propios.
3. **Distribución de datos:** cap. 6, sec. 6.9, pp. 377–378.
4. **Ampliación:** relacionar decodificadores de la sec. 6.5 con DEMUX y comparar polaridades, Enable y número de líneas.
