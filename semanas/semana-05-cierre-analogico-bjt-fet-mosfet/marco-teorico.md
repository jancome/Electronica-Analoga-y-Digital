# Marco teórico – Semana 05

# Cierre de la Fase 1 ABPr y evaluación de la unidad analógica

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