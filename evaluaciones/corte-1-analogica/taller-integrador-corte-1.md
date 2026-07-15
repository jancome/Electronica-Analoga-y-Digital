# Taller integrador – Corte 1

**Unidad:** Electrónica analógica  
**Semana de entrega:** Semana 02  
**Peso:** 4% de la nota final  
**Modalidad:** grupos de 3 estudiantes  

## Propósito

Reforzar los fundamentos mínimos necesarios para iniciar el trabajo con dispositivos semiconductores, relacionando circuitos básicos, señales, medición, diodos, LED, Zener y una consulta técnica breve en otro idioma.

Este taller reemplaza la división entre taller aplicado y taller investigativo del primer corte. Por eso integra cálculo, análisis y una consulta técnica corta en inglés.

---

## Indicaciones

- El taller se entrega en grupos de 3 estudiantes.
- Debe incluir portada, nombres completos, grupo, fecha y roles de cada integrante.
- Las respuestas deben estar justificadas.
- Todos los cálculos deben tener unidades.
- Las simulaciones pueden realizarse en Proteus, Multisim, Tinkercad, Falstad, LTspice u otro simulador autorizado.
- La consulta técnica debe hacerse en una fuente académica o técnica en inglés.
- La entrega puede ser en PDF o documento digital según indique el docente.

---

# Parte A – Fundamentos de circuitos

## 1. Circuito resistivo en serie

Se tiene una fuente de **12 V DC** conectada a dos resistencias en serie:

```text
R1 = 1 kΩ
R2 = 2.2 kΩ
```

Calcule:

1. Resistencia equivalente.
2. Corriente total del circuito.
3. Voltaje en R1.
4. Voltaje en R2.
5. Potencia disipada en cada resistencia.

## 2. Divisor de voltaje

Diseñe un divisor de voltaje que entregue aproximadamente **5 V** a partir de una fuente de **12 V**.

Debe incluir:

1. Valores seleccionados de resistencias.
2. Cálculo del voltaje de salida.
3. Justificación de los valores escogidos.
4. Comentario sobre qué ocurre si se conecta una carga en la salida del divisor.

## 3. Medición con multímetro

Explique cómo se conecta el multímetro para medir:

1. Voltaje.
2. Corriente.
3. Resistencia.

Incluya una advertencia de seguridad para cada caso.

---

# Parte B – Señales y medición

## 4. Identificación de señales

Dibuje o simule las siguientes señales:

1. Señal DC.
2. Señal senoidal.
3. Señal cuadrada.

Para cada una indique:

- Si puede considerarse analógica, digital o depende del contexto.
- Qué instrumento usaría para medirla.
- Una aplicación real.

## 5. Valor pico y valor RMS

Una señal senoidal tiene un valor de **6 V RMS**.

Calcule el valor pico aproximado.

Use:

```text
VP = VRMS × √2
```

Explique por qué esta diferencia es importante al analizar rectificadores.

---

# Parte C – Diodo, LED y Zener

## 6. Diodo en polarización directa

Analice un circuito compuesto por:

```text
Fuente = 5 V DC
Resistencia = 1 kΩ
Diodo de silicio en polarización directa
VD ≈ 0.7 V
```

Calcule:

1. Voltaje en la resistencia.
2. Corriente aproximada del circuito.
3. Potencia en la resistencia.
4. Explique por qué no debe conectarse el diodo directamente a la fuente.

## 7. LED con resistencia limitadora

Diseñe un circuito LED con los siguientes datos:

```text
Fuente = 9 V
VLED = 2 V
ILED deseada = 10 mA
```

Calcule:

1. Resistencia limitadora.
2. Valor comercial recomendado.
3. Potencia aproximada en la resistencia.
4. Explique qué ocurriría si se usa una resistencia demasiado pequeña.

## 8. Diodo Zener como regulador básico

Se desea obtener una salida regulada aproximada de **5.1 V** usando un diodo Zener.

Explique:

1. Cómo debe conectarse el Zener.
2. Qué función cumple la resistencia serie.
3. Qué ocurre si la corriente por el Zener es demasiado baja.
4. Qué ocurre si la corriente por el Zener es demasiado alta.

---

# Parte D – Simulación corta

## 9. Simulación de circuito con diodo o LED

Realice una simulación de uno de los siguientes circuitos:

- Diodo en polarización directa.
- LED con resistencia limitadora.
- Regulador básico con Zener.

Incluya:

1. Captura del circuito.
2. Valores de fuente y componentes.
3. Voltaje medido en el diodo o LED.
4. Corriente calculada o medida.
5. Comentario comparando teoría y simulación.

---

# Parte E – Consulta técnica en inglés

## 10. Consulta breve de hoja de datos o recurso técnico

Busque una fuente técnica en inglés relacionada con uno de estos componentes:

- Diodo 1N4007.
- LED.
- Diodo Zener de 5.1 V.
- Transistor BJT 2N2222 o BC547.
- MOSFET 2N7000, IRLZ44N o equivalente.

Puede consultar hoja de datos de fabricante, libro electrónico institucional, IEEE Xplore, ScienceDirect, SpringerLink, EBSCO, ProQuest u otra base autorizada por la universidad.

### Producto mínimo

Incluya:

1. Nombre del componente o tema consultado.
2. Fuente o base de datos utilizada.
3. Referencia en formato IEEE básico.
4. Cinco términos técnicos en inglés con traducción al español.
5. Resumen propio en español de 120 a 180 palabras.
6. Relación con una práctica del primer corte.

---

# Entrega

El documento final debe incluir:

1. Portada.
2. Desarrollo de las partes A, B, C, D y E.
3. Cálculos con unidades.
4. Captura de simulación.
5. Fuente técnica consultada.
6. Conclusiones individuales breves de cada integrante.
7. Roles de trabajo.

---

# Rúbrica

| Criterio | Peso |
|---|---:|
| Cálculos de circuitos básicos | 25% |
| Análisis de señales y medición | 15% |
| Análisis de diodo, LED y Zener | 25% |
| Simulación y comparación con teoría | 15% |
| Consulta técnica en inglés | 15% |
| Orden, unidades, roles y presentación | 5% |

---

# Nota para el docente

Este taller se ubica en la Semana 02 para adelantar parte del trabajo de análisis del primer corte. Las preguntas sobre BJT y MOSFET se manejan como consulta técnica inicial, no como desarrollo profundo, porque esos temas se trabajan después en las semanas 03 y 04.
