# Marco teórico – Semana 05

# Cierre de la Fase 1 ABPr y evaluación de la unidad analógica

## Metas de aprendizaje verificables

- Integrar cálculos, simulación, hoja de datos, seguridad y diagnóstico sin introducir un tema nuevo.
- Defender la trazabilidad entre necesidad, arquitectura, etapa analógica y mediciones esperadas.
- Convertir la retroalimentación del Preproyecto 1 en correcciones comprobables para la Fase 2.

## 1. Propósito de la semana

Cerrar el primer corte mediante integración conceptual, retroalimentación del proyecto, entrega del Preproyecto ABPr 1 y aplicación del Parcial 1.

Esta semana **no introduce tema nuevo**. El marco funciona como guía de síntesis y verificación.

## 2. Resultado de aprendizaje

Al finalizar la semana, el estudiante estará en capacidad de:

- Explicar el funcionamiento de la etapa analógica diseñada.
- Relacionar cálculos, simulación y aplicación del proyecto.
- Justificar la selección de diodos, Zener, BJT o MOSFET.
- Identificar limitaciones, riesgos y mejoras pendientes.
- Presentar una arquitectura preliminar coherente con la situación problema.
- Reconocer la retroalimentación como insumo para las fases siguientes.

## 3. Integración conceptual del Corte 1

La unidad debe comprenderse como una cadena de decisiones de ingeniería:

```text
Situación problema
        ↓
Requerimientos básicos
        ↓
Entrada AC de baja tensión
        ↓
Rectificación y filtrado
        ↓
Regulación / protección / indicador
        ↓
Control de carga con BJT o MOSFET
        ↓
Medición, simulación y verificación
```

## 4. Conceptos que deben dominarse

### Circuitos y medición

- Ley de Ohm.
- Potencia.
- Leyes de Kirchhoff.
- Medición de voltaje y corriente.
- Referencia GND.

### Diodos y fuentes

- Unión PN.
- Polarización directa e inversa.
- Media onda y puente rectificador.
- Valor RMS y valor pico.
- Caídas de voltaje.
- Filtrado y rizado.
- LED y resistencia limitadora.
- Regulación básica con Zener.

### Control de cargas

- BJT: corte, activa y saturación.
- Resistencia de base.
- MOSFET: `VGS`, `RDS(on)`, Gate y pull-down.
- Comparación BJT–MOSFET.
- Diodo de protección para cargas inductivas.

## 5. Preproyecto ABPr 1

La entrega debe contener como mínimo:

1. Título provisional.
2. Situación específica y justificación.
3. Objetivo general y objetivos específicos.
4. Integrantes, roles y aportes.
5. Diagrama de bloques.
6. Etapa AC/DC en baja tensión.
7. Rectificación, filtrado, regulación e indicador.
8. Protección o criterio de seguridad.
9. Posible etapa de control con BJT o MOSFET.
10. Cálculos de voltaje, corriente, resistencia y potencia.
11. Simulación inicial.
12. Mediciones o montaje preliminar, cuando aplique.
13. Lista inicial de materiales y costos.
14. Fuente técnica consultada.
15. Fallas encontradas y correcciones pendientes.

## 6. Criterios de calidad de la Fase 1

La entrega no debe calificarse solo por tener capturas. Debe existir coherencia entre:

- El problema escogido.
- La arquitectura propuesta.
- Los cálculos.
- Los componentes.
- La simulación.
- La seguridad.
- El trabajo realizado por cada integrante.

## 7. Retroalimentación formativa

La nota del Preproyecto ABPr 1 pertenece al Corte 1, pero sus errores no se arrastran mecánicamente al proyecto final.

La retroalimentación debe transformarse en un **registro de mejora**:

| Observación recibida | Corrección propuesta | Responsable | Evidencia futura |
|---|---|---|---|
|  |  |  |  |

Las correcciones se demostrarán en las fases 2 y 3.

## 8. Preparación para el Parcial 1

La evaluación individual puede incluir:

- Análisis de circuitos con diodos.
- Cálculo de resistencia para LED.
- RMS, pico y salida de rectificadores.
- Interpretación de rizado y filtrado.
- Regulación con Zener.
- Diseño básico de BJT como interruptor.
- Selección básica de MOSFET.
- Potencia y seguridad.
- Interpretación de hojas de datos.

## 9. Actividad de cierre

Cada grupo realizará una explicación breve de su diagrama de bloques y responderá:

1. ¿Qué problema se está resolviendo?
2. ¿Qué función cumple la etapa analógica?
3. ¿Qué valores fueron calculados?
4. ¿Qué se comprobó en simulación?
5. ¿Qué limitación debe corregirse?
6. ¿Qué parte desarrolló cada integrante?

## 10. Evidencias de la semana

- Preproyecto ABPr 1.
- Registro de retroalimentación.
- Parcial 1 individual.
- Lista de correcciones para la Fase 2.

## 11. Errores comunes

- Presentar una fuente genérica sin relación con la situación problema.
- Entregar capturas sin cálculos ni interpretación.
- Copiar un circuito sin revisar límites eléctricos.
- No indicar el aporte individual.
- Ocultar fallas en lugar de analizarlas.
- Conectar montajes directamente a la red de 120 V.

## 12. Conexión con el Corte 2

La Fase 2 convertirá las condiciones del problema en variables digitales. El grupo construirá una tabla de verdad, simplificará la función, la simulará y realizará un montaje funcional en protoboard.

## 13. Profundización integradora sin tema nuevo

La semana no agrega otro dispositivo; consolida una forma de razonar. Cada bloque debe tener entrada, salida, función, ecuación de diseño, condición límite y punto de prueba:

```text
requisito → arquitectura → cálculo → componente → simulación
          → medición esperada → prueba → diagnóstico → mejora
```

Una simulación que “enciende” no demuestra diseño. Se debe comprobar el peor caso de entrada, carga y tolerancia; verificar corriente y potencia; identificar referencias comunes; y explicar qué decisión deriva de cada resultado.

## 14. Caso integrador guiado adaptado

Considérese una fuente aislada de `9 V RMS` con puente, `470 µF`, indicador LED y una carga de `5 V/60 mA` accionada por transistor.

1. Calcular `V_p`, caídas del puente y rizado con `ΔV≈I/(f_rC)`.
2. Definir salida regulada y comprobar el peor caso de potencia.
3. Para BJT, calcular `I_B`, `R_B` y `P_Q`; para MOSFET, verificar `R_DS(on)` a la tensión real y `P≈I²R_DS(on)`.
4. Ubicar puntos de prueba antes/después de puente, filtro, regulación, control y carga.
5. Construir una tabla de estados con tensiones esperadas.
6. Provocar una falla segura y diagnosticarla por mediciones.

La entrega debe mostrar continuidad entre el problema regional y el circuito: no basta con presentar una fuente y un transistor sin explicar qué variable se supervisa y qué acción eficiente produce.

## 15. Auditoría técnica del Preproyecto ABPr 1

| Pregunta | Evidencia exigida |
|---|---|
| ¿La arquitectura resuelve la necesidad? | diagrama con señales y rangos |
| ¿La fuente soporta la carga? | balance de tensión, corriente, rizado y potencia |
| ¿Los semiconductores tienen margen? | hoja de datos y peor caso |
| ¿La simulación es reproducible? | esquema, parámetros y puntos de medición |
| ¿Se puede diagnosticar? | valores esperados y árbol de fallas |
| ¿Es segura? | baja tensión aislada, límites y procedimiento |

## 16. Procedimiento de revisión y retroalimentación

1. Otro equipo reconstruye la lógica del diseño con diagrama y cálculos.
2. Marca toda entrada sin rango, salida sin carga o componente sin referencia.
3. Comprueba unidades, márgenes y coherencia entre esquema y BOM.
4. Ejecuta dos casos normales y uno límite en simulación.
5. El autor clasifica cada observación como aceptada, rechazada con evidencia o pendiente.
6. Se registra la corrección que pasa a la Fase 2.

## 17. Diagnóstico, preguntas y trabajo independiente

Ante una salida incorrecta se divide el sistema por bloques. Si la tensión filtrada es correcta pero la regulada no, se investiga regulación, no el puente. Si el control es válido pero la carga no responde, se mide conmutación y carga.

- ¿Qué supuesto domina la incertidumbre?
- ¿Cuál es el componente más exigido y qué margen conserva?
- ¿Qué diferencia cálculo–simulación es aceptable?
- ¿Qué falla única explica el síntoma?
- ¿Qué señal entregará la etapa analógica a la lógica digital?

El trabajo independiente consiste en corregir el Preproyecto 1, completar una matriz requisito–evidencia y preparar una explicación individual de dos minutos y un caso de diagnóstico.

## 18. Referencias de repaso

- Boylestad y Nashelsky, 10.ª ed., cap. 2, sec. 2.12, p. 103: aplicaciones prácticas de diodos.
- Ibid., cap. 4, secs. 4.15–4.18, pp. 206–228: conmutación, fallas y aplicaciones BJT.
- Ibid., cap. 7, secs. 7.12 y 7.15, pp. 445–462: diagnóstico y aplicaciones FET.
- Ibid., cap. 15, secs. 15.2–15.7, pp. 774–796: filtrado, regulación y fuentes.

## 19. Ruta de profundización recomendada

1. **Cadena de alimentación:** Boylestad, caps. 1–2 y cap. 15, secs. 15.2–15.7.
2. **Conmutación BJT:** caps. 3–4, priorizando cap. 4, secs. 4.15–4.18.
3. **Conmutación MOSFET:** caps. 6–7, priorizando cap. 7, secs. 7.8, 7.11, 7.12 y 7.15.
4. **Lectura integradora:** comparar las aplicaciones y procedimientos de fallas de los caps. 2, 4, 7 y 15; profundizar por el bloque más débil del Preproyecto 1, no por cantidad de páginas.
