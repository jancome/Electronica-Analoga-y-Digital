# Marco teórico – Semana 11

# Cierre de la Fase 2 ABPr y evaluación de lógica combinacional

## Metas de aprendizaje verificables

- Demostrar coherencia entre requisito, tabla, expresión, simplificación, simulación y hardware.
- Ejecutar una prueba completa y diagnosticar una falla segura con mediciones.
- Transformar retroalimentación del Preproyecto 2 en un plan verificable para la Fase 3.

## 1. Propósito de la semana

Cerrar el segundo corte mediante integración conceptual, presentación del Preproyecto ABPr 2, retroalimentación y aplicación del Parcial 2.

Esta semana **no introduce contenido nuevo**. Los mapas de Karnaugh, la simplificación y el montaje deben haberse desarrollado antes del cierre.

## 2. Resultado de aprendizaje

Al finalizar la semana, el estudiante estará en capacidad de:

- Explicar la relación entre variables, tabla, expresión y circuito.
- Demostrar una simulación funcional.
- Demostrar un montaje funcional en protoboard.
- Comparar la lógica original y la lógica simplificada.
- Identificar fallas y correcciones.
- Justificar cómo la etapa digital responde a la situación problema.
- Presentar su aporte individual.

## 3. Integración conceptual del Corte 2

```text
Situación problema
        ↓
Variables digitales
        ↓
Tabla de verdad
        ↓
Expresión canónica
        ↓
Álgebra / De Morgan / Karnaugh
        ↓
Circuito simplificado
        ↓
Simulación
        ↓
Protoboard
        ↓
Pruebas y mediciones
```

## 4. Preproyecto ABPr 2

La entrega debe incluir:

1. Situación problema y objetivos actualizados.
2. Diagrama de bloques actualizado.
3. Variables y significado de sus estados.
4. Tabla de verdad completa.
5. Expresión canónica.
6. Simplificación algebraica o por Karnaugh.
7. Circuito lógico final.
8. Simulación funcional.
9. Montaje funcional en protoboard.
10. Comprobación de todas las combinaciones.
11. Mediciones y evidencias.
12. Consulta de hojas de datos.
13. Roles y aportes.
14. Registro de retroalimentación y mejoras.
15. Relación explícita con la situación problema.

## 5. Demostración mínima

El grupo deberá mostrar:

- La entrada correspondiente a cada variable.
- La salida para cada combinación relevante.
- Coincidencia con la tabla de verdad.
- Alimentación y referencia correctas.
- Ausencia de entradas flotantes.
- Uso de una etapa de control si la carga supera la capacidad de la compuerta.

## 6. Criterios de calidad

### Coherencia lógica

La tabla, la expresión, la simulación y el montaje deben producir el mismo resultado.

### Funcionalidad

El circuito debe responder de manera repetible a las entradas.

### Calidad del montaje

Se valoran orden, conexiones verificables, identificación de señales y seguridad.

### Comprensión

Cada integrante debe explicar la función completa y su aporte.

### Mejora

El grupo debe mostrar qué corrigió después de la retroalimentación.

## 7. Preparación para el Parcial 2

La evaluación individual puede incluir:

- Conversiones entre sistemas numéricos.
- Aritmética binaria.
- Tablas de verdad.
- Interpretación de compuertas.
- Expresiones booleanas.
- Leyes del álgebra de Boole.
- Teoremas de De Morgan.
- Minterminos.
- Mapas de Karnaugh de 2, 3 y 4 variables.
- Diseño e interpretación de circuitos combinacionales.

## 8. Retroalimentación para la Fase 3

La entrega de la Fase 2 tiene nota propia, pero el proyecto final se evaluará por su versión definitiva.

Cada grupo deberá completar:

| Observación | Corrección para Fase 3 | Responsable | Evidencia |
|---|---|---|---|
|  |  |  |  |

## 9. Actividad de cierre

Cada integrante responderá preguntas como:

1. ¿Qué condición representa cada variable?
2. ¿Cómo se obtuvo la tabla?
3. ¿Qué método de simplificación se utilizó?
4. ¿Qué cambió entre la expresión original y la final?
5. ¿Cómo se comprobó el protoboard?
6. ¿Qué falla fue la más importante?
7. ¿Qué se integrará físicamente en el tercer corte?

## 10. Evidencias de la semana

- Preproyecto ABPr 2.
- Simulación funcional.
- Protoboard funcional.
- Registro de mediciones.
- Registro de retroalimentación.
- Parcial 2 individual.

## 11. Errores comunes

- Entregar solo simulación sin protoboard.
- Mostrar un protoboard sin tabla ni explicación.
- No probar todas las combinaciones.
- Dejar entradas flotantes.
- No evidenciar correcciones.
- Presentar un montaje que no se relaciona con el problema.

## 12. Conexión con el Corte 3

La Fase 3 integrará la etapa analógica y la lógica digital con aplicaciones combinacionales o secuenciales. El producto definitivo deberá ser físico y presentarse en una maqueta, estructura o base organizada.

## 13. Profundización integradora sin tema nuevo

El cierre del Corte 2 evalúa una cadena completa: `requisito → variables → tabla → expresión → simplificación → CI → simulación → protoboard → medición`. La fortaleza de una solución no depende solo de que la salida coincida una vez, sino de la trazabilidad entre todos esos artefactos y de la cobertura de estados normales, límite, inválidos y de seguridad.

## 14. Caso integrador adaptado: control de agua

Se definen `L` (nivel bajo detectado), `H` (nivel alto detectado) y `E` (habilitación), con salidas `P` (bomba) y `A` (alarma). El equipo debe:

1. declarar la física de los sensores y estados imposibles;
2. construir tablas independientes para `P` y `A`;
3. obtener expresiones canónicas y simplificadas;
4. comprobar que una condición incoherente no active la bomba;
5. implementar, simular y montar;
6. medir niveles en cada combinación;
7. provocar una entrada abierta o cable mal ubicado y diagnosticarlo.

El caso adapta la metodología de análisis de sistemas combinacionales de Floyd al uso eficiente del agua en la región Caribe. No se copia un circuito del texto y no se exige que todos los proyectos sean de tanque.

## 15. Matriz de validación del Preproyecto ABPr 2

| Dimensión | Pregunta de control |
|---|---|
| requisito | ¿cada salida responde a una condición inequívoca? |
| lógica | ¿tabla, expresión y Karnaugh son equivalentes? |
| eléctrica | ¿alimentación, umbrales, fan-out y cargas son compatibles? |
| cobertura | ¿se probaron todas las combinaciones y casos inválidos? |
| trazabilidad | ¿cada captura/foto indica caso, nodo y resultado? |
| mejora | ¿la retroalimentación de Fase 1 aparece resuelta o justificada? |

## 16. Procedimiento de demostración y diagnóstico

1. Mostrar estado inicial seguro.
2. Aplicar casos normales y uno límite en un orden anunciado.
3. Medir entradas y salida de al menos un caso, no depender solo de LEDs.
4. Comparar en vivo con la fila correspondiente de la tabla.
5. Introducir una falla segura previamente definida.
6. Formular dos hipótesis y elegir una medición que las separe.
7. Corregir, repetir el caso y registrar la evidencia.

Si la salida diverge en simulación y hardware, se identifica primero cuál coincide con la tabla. Esto separa un error lógico de un problema físico.

## 17. Preguntas orientadoras y trabajo independiente

- ¿Qué evidencia prueba equivalencia y no solo coincidencia parcial?
- ¿Qué estado inválido merece una salida segura?
- ¿Cuál es el primer nodo donde medición y predicción divergen?
- ¿Qué costo eléctrico y de cableado tuvo la simplificación?
- ¿Qué bloque del Corte 3 aporta valor real, en vez de complejidad ornamental?

Después de la retroalimentación, el grupo elaborará un plan de Fase 3 con observación, causa, corrección, responsable, fecha y prueba de cierre. Cada integrante prepara una explicación individual de una decisión lógica y una decisión eléctrica.

## 18. Referencias de repaso

- Floyd, 9.ª ed., cap. 5, pp. 270–325: análisis e implementación de lógica combinacional y aplicación de control de tanque.
- Ibid., cap. 5, sec. 5.7: localización de averías en circuitos combinacionales.
- Ibid., cap. 3, sec. 3.9, pp. 174–197: método de diagnóstico en circuitos de puertas.
- Ibid., cap. 14, pp. 884–914: niveles y límites prácticos TTL/CMOS.

## 19. Ruta de profundización recomendada

1. **Integración combinacional:** Floyd, cap. 5, pp. 270–325.
2. **Caso de sistema:** aplicación de control de tanque del cap. 5, analizada como método requisito–tabla–circuito–prueba.
3. **Diagnóstico:** cap. 5, sec. 5.7, complementado con cap. 3, sec. 3.9, pp. 174–197.
4. **Profundización según falla:** volver al cap. 2 para representación, cap. 4 para simplificación o cap. 14 para compatibilidad eléctrica.
