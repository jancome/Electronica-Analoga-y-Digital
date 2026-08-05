# Marco teórico – Semana 02

# Semiconductores, diodos, rectificación, filtrado y Zener

## Metas de aprendizaje verificables

- Explicar la unión PN y elegir conscientemente un modelo ideal, práctico o de hoja de datos.
- Calcular y comprobar pico, rectificación, rizado, limitación LED y regulación Zener en baja tensión.
- Diagnosticar la etapa AC/DC mediante formas de onda y puntos de prueba definidos.

## 1. Propósito de la semana

Comprender el diodo como dispositivo semiconductor y utilizarlo para iniciar la etapa común AC/DC de la Fase 1 del proyecto ABPr.

Esta semana integra fundamentos que antes aparecían separados: unión PN, polarización del diodo, rectificación, filtrado, LED y regulación básica con Zener.

## 2. Resultado de aprendizaje

Al finalizar la semana, el estudiante estará en capacidad de:

- Explicar de forma básica la formación de una unión PN.
- Diferenciar polarización directa e inversa.
- Analizar circuitos simples con diodos mediante Ley de Ohm y Kirchhoff.
- Comparar rectificación de media onda y onda completa.
- Explicar el efecto de un capacitor de filtrado.
- Dimensionar una resistencia para LED.
- Reconocer el funcionamiento básico de un regulador Zener.
- Simular la etapa común AC/DC del Preproyecto ABPr 1.

## 3. Conexión con la Fase 1 ABPr

Todos los grupos desarrollarán una base analógica común:

```text
AC de baja tensión
        ↓
Rectificación
        ↓
Filtrado
        ↓
Regulación / protección
        ↓
Indicador de estado
```

Esta etapa deberá diseñarse y simularse antes de cualquier montaje físico.

## 4. Materiales semiconductores y unión PN

Un semiconductor tiene una conductividad intermedia entre un conductor y un aislante. Su comportamiento puede modificarse mediante dopaje.

- **Tipo N:** predominan electrones como portadores mayoritarios.
- **Tipo P:** predominan huecos como portadores mayoritarios.

Al unir regiones P y N aparece una **región de agotamiento**, que condiciona el paso de corriente.

## 5. Diodo semiconductor

El diodo tiene dos terminales:

- **Ánodo.**
- **Cátodo**, normalmente identificado mediante una banda.

### Polarización directa

El diodo conduce cuando el ánodo se encuentra a mayor potencial que el cátodo y se supera su tensión de conducción.

Para un diodo de silicio, en un modelo práctico:

```text
VD ≈ 0.7 V
```

### Polarización inversa

El diodo bloquea la corriente, salvo una pequeña fuga, mientras no se supere su tensión inversa máxima.

## 6. Análisis con Ley de Ohm y Kirchhoff

En una malla formada por fuente, resistencia y diodo:

```text
VS = VR + VD
VR = VS - VD
I = VR / R
```

El diodo nunca debe analizarse aislado: la resistencia, la fuente y la carga determinan la corriente real.

## 7. Señales AC, RMS y valor pico

Para una señal senoidal ideal:

```text
VP = VRMS × √2
```

El valor pico permite estimar el máximo voltaje disponible después de la rectificación, antes de considerar las caídas en los diodos.

## 8. Rectificación

### Media onda

Utiliza un diodo y aprovecha un solo semiciclo de la señal AC.

- Circuito sencillo.
- Mayor rizado.
- Menor aprovechamiento de la energía disponible.

### Puente rectificador

Utiliza cuatro diodos y aprovecha ambos semiciclos. En cada semiciclo conducen dos diodos.

```text
Vsalida,pico ≈ VP - 2VD
```

Para diodos de silicio, la caída aproximada del puente es de 1.4 V.

## 9. Filtrado capacitivo

El capacitor se conecta en paralelo con la carga. Se carga cerca del valor máximo de la señal rectificada y entrega energía cuando el voltaje de entrada disminuye.

Al aumentar la capacitancia:

- Disminuye el rizado.
- La salida se aproxima más a una DC constante.
- Puede aumentar la corriente inicial de carga.

Una aproximación útil del rizado es:

```text
ΔV ≈ Iload / (frizado × C)
```

En un puente de onda completa, la frecuencia de rizado es aproximadamente el doble de la frecuencia de la señal AC.

## 10. LED y resistencia limitadora

Un LED requiere una resistencia en serie:

```text
R = (VS - VLED) / ILED
```

También debe verificarse la potencia:

```text
PR = ILED² × R
```

## 11. Regulación básica con Zener

El Zener se utiliza en polarización inversa dentro de su zona de ruptura controlada. Con una resistencia serie puede mantener una tensión aproximadamente constante.

La resistencia debe limitar la corriente total:

```text
Rserie = (Vin - VZ) / (IZ + Iload)
```

Se debe comprobar:

```text
PZ = VZ × IZ
```

## 12. Ejemplo aplicado

Para una fuente de 6 V RMS:

```text
VP ≈ 6 × 1.414 = 8.48 V
```

Después de un puente de silicio:

```text
Vsalida,pico ≈ 8.48 - 1.4 = 7.08 V
```

La salida real dependerá de la corriente de carga, el capacitor y la regulación utilizada.

## 13. Actividad de clase y laboratorio

Cada grupo deberá:

1. Seleccionar una tensión AC segura de baja tensión.
2. Simular media onda y puente rectificador.
3. Comparar formas de onda.
4. Agregar un capacitor y medir el rizado.
5. Incorporar un LED indicador.
6. Proponer regulación básica con Zener o regulador autorizado.
7. Registrar voltajes en cada bloque.

## 14. Evidencia ABPr de la semana

- Esquema de la etapa AC/DC.
- Simulación funcional.
- Cálculos de voltaje pico, resistencias y potencia.
- Capturas de las formas de onda.
- Primera lista de componentes.
- Explicación del aporte de esta etapa al proyecto.

## 15. Seguridad

- No conectar protoboard directamente a la red de 120 V.
- Utilizar transformador de baja tensión, fuente de laboratorio o simulador.
- Verificar polaridad del capacitor y del LED.
- Descargar capacitores antes de modificar el circuito.
- Revisar el voltaje nominal de los componentes.

## 16. Errores comunes

- Confundir voltaje RMS con voltaje pico.
- Olvidar las caídas del puente rectificador.
- Suponer que la señal rectificada ya es DC constante.
- Invertir el capacitor electrolítico.
- Conectar un LED sin resistencia.
- Usar el Zener sin limitar corriente.

## 17. Trabajo independiente

- Completar la simulación de la etapa común.
- Consultar las hojas de datos de los diodos y Zener seleccionados.
- Registrar preguntas y diferencias entre cálculo y simulación.
- Preparar el Lab A01 y el avance del Preproyecto ABPr 1.

## 18. Conexión con la Semana 03

La siguiente semana se estudiará el BJT como interruptor para controlar una carga de baja potencia a partir de una señal pequeña.

## 19. Profundización del modelo físico y eléctrico

En un semiconductor puro, la energía térmica puede generar pares electrón-hueco. El dopaje crea material tipo `n`, con electrones mayoritarios, o tipo `p`, con huecos mayoritarios. Al unirlos aparece una región de agotamiento y una barrera interna. La polarización directa reduce esa barrera y permite corriente apreciable; la inversa la amplía y deja solo una corriente muy pequeña hasta la ruptura. Este modelo explica por qué el diodo no es una resistencia lineal.

Para resolver circuitos se escogerá deliberadamente uno de tres modelos: ideal, caída constante o curva/hoja de datos. La ecuación exponencial `I_D≈I_S(e^{V_D/(nV_T)}-1)` describe la tendencia física, pero el curso prioriza el modelo adecuado al propósito y la validación.

Para una senoidal `V_p=√2V_RMS`. En un puente conducen dos diodos: `V_p,carga≈V_p-2V_D`. Con filtro capacitivo y carga casi constante:

\[
\Delta V\approx\frac{I_L}{f_rC}
\]

donde `f_r=f_red` en media onda y `f_r=2f_red` en onda completa. Para regulación Zener:

\[
R_S=\frac{V_{in}-V_Z}{I_L+I_Z},\qquad P_Z=V_ZI_Z
\]

Se comprueban extremos de entrada y carga; diseñar solo con valores nominales puede sacar al Zener de regulación o exceder su potencia.

## 20. Ejemplo guiado adaptado

Una fuente aislada entrega `9 V RMS`, `60 Hz`. Se usa puente de silicio, filtro de `470 µF` y carga de `680 Ω`.

1. `V_p=9√2=12,73 V`.
2. Después del puente, `V_max≈12,73-1,4=11,33 V`.
3. `I_L≈11,33/680=16,7 mA`.
4. Como `f_r=120 Hz`, `ΔV≈0,0167/(120×470 µF)=0,296 Vpp`.
5. `V_DC≈V_max-ΔV/2≈11,18 V`.

El cálculo es iterativo porque la corriente depende de la tensión media. En simulación se medirán máximo, mínimo y periodo del rizado; en laboratorio se compararán los mismos puntos y los límites de los diodos.

## 21. Procedimiento de simulación y Lab A01

1. Simular la fuente y confirmar amplitud, frecuencia y referencia.
2. Añadir el rectificador sin capacitor; observar polaridad y frecuencia de pulsos.
3. Incorporar carga y filtro; medir `Vmax`, `Vmin`, `VDC` y `ΔV`.
4. Variar carga y capacitor para explicar la tendencia.
5. Añadir LED con `R=(V_S-V_F)/I_F`.
6. Evaluar el Zener en carga mínima y máxima y calcular `P_Z`.
7. Montar con la fuente desconectada y energizar por bloques.
8. Registrar cálculo, simulación y medición en una misma tabla con unidades.

## 22. Diagnóstico de fallas

| Síntoma | Hipótesis | Medición discriminante |
|---|---|---|
| No hay salida | fuente ausente, puente abierto o referencia incorrecta | medir AC de entrada y DC después del puente |
| Salida negativa | polaridad del puente o puntas invertidas | comprobar polaridad en capacitor |
| Rizado excesivo | capacitor bajo/abierto o carga excesiva | medir `ΔV` y corriente de carga |
| Zener no regula | `I_Z` insuficiente o conexión invertida | medir tensión en `R_S` y calcular corriente |
| LED no enciende | polaridad, resistor incorrecto o corriente insuficiente | medir `V_F` y caída en resistor |

## 23. Preguntas orientadoras y trabajo independiente

- ¿Qué cambia entre valor RMS, pico y valor medio después de rectificar?
- ¿Por qué un puente pierde aproximadamente dos caídas directas?
- ¿Qué condición de carga produce el mayor rizado?
- ¿Cuál es el peor caso de potencia del Zener?
- ¿Qué punto de prueba separa una falla de rectificación de una de filtrado?

Cada grupo recalculará su etapa con tolerancia de capacitor, extremos de carga y margen de potencia; entregará formas de onda etiquetadas, tabla comparativa, selección por hoja de datos y tres fallas con su prueba confirmatoria.

## 24. Referencias de estudio

- Boylestad y Nashelsky, 10.ª ed., cap. 1, secs. 1.2–1.9, pp. 2–27: semiconductores, unión PN, modelos y resistencias del diodo.
- Ibid., secs. 1.12 y 1.14–1.16, pp. 32, 36–41: hoja de datos, prueba, Zener y LED.
- Ibid., cap. 2, secs. 2.2–2.7 y 2.10, pp. 60–92: redes, rectificación y aplicaciones Zener.
- Ibid., cap. 15, secs. 15.2–15.7, pp. 774–796: filtros, regulación y fuentes, como ampliación.

## 25. Ruta de profundización recomendada

1. **Fundamento físico:** Boylestad, cap. 1, secs. 1.2–1.9, pp. 2–27.
2. **Dispositivos reales:** cap. 1, secs. 1.12 y 1.14–1.16, pp. 32 y 36–41, con énfasis en hoja de datos, prueba, Zener y LED.
3. **Análisis obligatorio:** cap. 2, secs. 2.2–2.7 y 2.10, pp. 60–92, para recta de carga, redes y rectificación.
4. **Profundización aplicada:** cap. 2, sec. 2.12, p. 103, y cap. 15, secs. 15.2–15.7, pp. 774–796, para filtros y fuentes prácticas.
