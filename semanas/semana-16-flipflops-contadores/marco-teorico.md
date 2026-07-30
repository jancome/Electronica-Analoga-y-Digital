# Marco teórico – Semana 16

# Flip-flops, contadores y ajustes finales del proyecto

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