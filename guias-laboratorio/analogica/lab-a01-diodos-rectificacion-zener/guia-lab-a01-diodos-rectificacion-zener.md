# EXPERIENCIA No. A01

# DIODOS SEMICONDUCTORES, RECTIFICACIÓN Y REGULACIÓN CON ZENER

**Asignatura:** Electrónica Analógica y Digital  
**Periodo:** 2026-2  
**Programa:** Ingeniería Eléctrica  
**Duración estimada:** 3 horas presenciales + trabajo independiente  

---

## 1. INTRODUCCIÓN

El diodo semiconductor es uno de los dispositivos fundamentales de la electrónica analógica. Su funcionamiento se basa en la unión PN, la cual permite el paso de corriente principalmente en un sentido cuando se encuentra polarizada directamente, y limita el paso de corriente cuando se encuentra polarizada inversamente.

Este comportamiento permite utilizar el diodo en aplicaciones como protección de polaridad, rectificación de señales, fuentes de alimentación, indicadores luminosos y regulación básica de voltaje. En ingeniería eléctrica, los diodos se encuentran presentes en cargadores, fuentes DC, sistemas de control, protecciones electrónicas, variadores, rectificadores industriales y circuitos de potencia.

En esta experiencia se estudiará el comportamiento del diodo en polarización directa e inversa. Posteriormente, se implementarán circuitos rectificadores de media onda y onda completa, se analizará el efecto de un filtro capacitivo y se comprobará el funcionamiento de un regulador básico con diodo Zener.

---

## 2. OBJETIVO

Implementar y analizar circuitos básicos con diodos semiconductores, verificando su comportamiento en polarización directa e inversa, su aplicación en rectificación de señales AC y su uso en regulación básica de voltaje mediante diodo Zener.

### Objetivos específicos

- Identificar los terminales ánodo y cátodo de un diodo semiconductor.
- Comprobar experimentalmente la polarización directa e inversa de un diodo.
- Implementar un rectificador de media onda.
- Implementar un rectificador de onda completa tipo puente.
- Analizar el efecto de un capacitor de filtrado en la señal rectificada.
- Verificar el comportamiento de un regulador básico con diodo Zener.
- Comparar valores teóricos, simulados y medidos.

---

## 3. NORMATIVA DE SEGURIDAD

Es obligatorio cumplir las normas de seguridad del laboratorio durante toda la práctica.

**PELIGRO:** Riesgo de choque eléctrico al manipular fuentes de alimentación o transformadores. Asegúrese de que el equipo esté apagado antes de realizar cualquier conexión.

**AVISO:** Riesgo de daño a componentes si se invierte la polaridad o se exceden los límites de voltaje y corriente. Revise las especificaciones de cada componente antes de energizar el circuito.

**PRECAUCIÓN:** Algunos componentes pueden calentarse durante el funcionamiento, especialmente resistencias, reguladores o diodos sometidos a corrientes elevadas.

**ELEMENTOS DE PROTECCIÓN PERSONAL:** Bata de laboratorio y gafas de seguridad cuando el laboratorio lo exija.

### Recomendaciones de seguridad

- Verifique la polaridad de la fuente antes de alimentar el circuito.
- No conecte el capacitor electrolítico con polaridad invertida.
- No alimente el circuito hasta que el docente o monitor revise el montaje.
- Utilice resistencias limitadoras de corriente para proteger diodos y LED.
- No manipule conexiones energizadas.
- Use únicamente niveles de tensión seguros para laboratorio educativo.

---

## 4. RECURSOS

### Materiales o dispositivos

- Diodos rectificadores 1N4007 o equivalentes.
- Diodo Zener de 5.1 V o 12 V.
- LED rojo, verde o amarillo.
- Resistencias de 220 Ω, 330 Ω, 1 kΩ, 2.2 kΩ y 10 kΩ.
- Capacitores electrolíticos de 100 µF, 470 µF o 1000 µF.
- Protoboard.
- Cables de conexión.
- Dip switch o cables para conexión manual, si aplica.

### Herramientas

- Pinzas de punta.
- Cortafrío, si se requiere.
- Computador con software de simulación.

### Equipos

- Fuente de corriente directa DC.
- Fuente AC de baja tensión o transformador didáctico, si está disponible.
- Multímetro digital.
- Osciloscopio, si está disponible.
- Generador de funciones, si está disponible.

### Software sugerido

- Proteus.
- Multisim.
- Tinkercad Circuits.
- Falstad Circuit Simulator.
- LTspice u otro simulador equivalente.

---

## 5. RECOMENDACIÓN PREVIA

Antes de realizar la práctica, el estudiante debe consultar la hoja de datos de los siguientes componentes:

- Diodo 1N4007.
- Diodo Zener utilizado.
- LED utilizado.
- Capacitor electrolítico utilizado.

Debe identificar:

- Terminal ánodo.
- Terminal cátodo.
- Voltaje directo aproximado.
- Corriente máxima.
- Potencia máxima.
- Polaridad de capacitores electrolíticos.

---

## 6. PROCEDIMIENTO EXPERIMENTAL

### 6.1 Identificación de terminales

1. Observe físicamente el diodo rectificador.
2. Identifique la banda que marca el cátodo.
3. Identifique el ánodo y el cátodo del LED.
4. Identifique la polaridad del capacitor electrolítico.
5. Consulte y dibuje el símbolo eléctrico de cada componente.

Complete la siguiente tabla.

| Componente | Terminal positivo o ánodo | Terminal negativo o cátodo | Observación física |
|---|---|---|---|
| Diodo 1N4007 | | | |
| LED | | | |
| Diodo Zener | | | |
| Capacitor electrolítico | | | |

---

### 6.2 Circuito 1: Polarización directa del diodo

Arme un circuito serie compuesto por fuente DC, resistencia y diodo rectificador en polarización directa.

**Valores sugeridos:**

- Fuente: 5 V DC.
- Resistencia: 1 kΩ.
- Diodo: 1N4007.

#### Procedimiento

1. Conecte el ánodo del diodo hacia el positivo de la fuente a través de la resistencia.
2. Conecte el cátodo hacia tierra.
3. Antes de energizar, revise polaridad y conexiones.
4. Mida el voltaje en el diodo.
5. Mida el voltaje en la resistencia.
6. Calcule la corriente del circuito usando la ley de Ohm.

#### Tabla 1. Polarización directa

| Fuente VS | Resistencia R | Voltaje en diodo VD | Voltaje en resistencia VR | Corriente calculada ID | Observación |
|---:|---:|---:|---:|---:|---|
| 5 V | 1 kΩ | | | | |
| 9 V | 1 kΩ | | | | |
| 12 V | 1 kΩ | | | | |

---

### 6.3 Circuito 2: Polarización inversa del diodo

Invierta la orientación del diodo del circuito anterior para que quede en polarización inversa.

#### Procedimiento

1. Conecte el cátodo del diodo hacia el positivo de la fuente.
2. Conecte el ánodo hacia tierra a través del circuito serie.
3. Energice con 5 V DC.
4. Mida el voltaje en el diodo.
5. Mida el voltaje en la resistencia.
6. Analice si circula corriente significativa.

#### Tabla 2. Polarización inversa

| Fuente VS | Resistencia R | Voltaje en diodo VD | Voltaje en resistencia VR | Corriente calculada | Observación |
|---:|---:|---:|---:|---:|---|
| 5 V | 1 kΩ | | | | |
| 9 V | 1 kΩ | | | | |
| 12 V | 1 kΩ | | | | |

---

### 6.4 Circuito 3: LED con resistencia limitadora

Arme un circuito con fuente DC, resistencia y LED.

#### Procedimiento

1. Conecte el LED en polarización directa.
2. Utilice inicialmente una resistencia de 330 Ω.
3. Mida el voltaje en el LED.
4. Mida el voltaje en la resistencia.
5. Calcule la corriente del LED.
6. Repita el procedimiento con una resistencia de 1 kΩ.

#### Tabla 3. LED con resistencia limitadora

| Fuente VS | Resistencia | Voltaje LED | Corriente calculada | Intensidad observada |
|---:|---:|---:|---:|---|
| 5 V | 330 Ω | | | |
| 5 V | 1 kΩ | | | |
| 9 V | 1 kΩ | | | |

### Cálculo sugerido

Para calcular la resistencia limitadora del LED:

```text
R = (VS - VLED) / ILED
```

Donde:

- VS es el voltaje de la fuente.
- VLED es el voltaje directo del LED.
- ILED es la corriente deseada por el LED.

---

### 6.5 Circuito 4: Rectificador de media onda

Implemente un rectificador de media onda utilizando un diodo rectificador y una resistencia de carga.

**Valores sugeridos:**

- Entrada AC: 6 V RMS o señal senoidal segura del generador.
- Diodo: 1N4007.
- Resistencia de carga: 1 kΩ.

#### Procedimiento

1. Arme el circuito rectificador de media onda.
2. Observe la señal de entrada en el osciloscopio o simulador.
3. Observe la señal de salida sobre la resistencia de carga.
4. Registre capturas de entrada y salida.
5. Mida el voltaje pico de entrada.
6. Mida el voltaje pico de salida.

#### Tabla 4. Rectificador de media onda

| Magnitud | Valor teórico | Valor simulado | Valor medido |
|---|---:|---:|---:|
| Voltaje pico de entrada | | | |
| Voltaje RMS de entrada | | | |
| Voltaje pico de salida | | | |
| Voltaje promedio aproximado | | | |
| Frecuencia de salida | | | |

---

### 6.6 Circuito 5: Rectificador de onda completa tipo puente

Implemente un puente rectificador usando cuatro diodos rectificadores.

#### Procedimiento

1. Arme el puente rectificador.
2. Conecte la resistencia de carga en la salida DC.
3. Observe la señal de entrada AC.
4. Observe la señal rectificada en la carga.
5. Compare la forma de onda con la obtenida en media onda.
6. Registre las capturas correspondientes.

#### Tabla 5. Rectificador de onda completa

| Magnitud | Valor teórico | Valor simulado | Valor medido |
|---|---:|---:|---:|
| Voltaje pico de entrada | | | |
| Voltaje pico de salida | | | |
| Voltaje promedio aproximado | | | |
| Frecuencia de rizado | | | |
| Caída aproximada en diodos | | | |

---

### 6.7 Circuito 6: Filtro capacitivo

Agregue un capacitor electrolítico en paralelo con la resistencia de carga del rectificador de onda completa.

**Valores sugeridos:**

- Capacitor 1: 100 µF.
- Capacitor 2: 470 µF.
- Capacitor 3: 1000 µF.

#### Procedimiento

1. Conecte el capacitor respetando la polaridad.
2. Observe la señal de salida filtrada.
3. Mida el voltaje DC promedio.
4. Observe el rizado.
5. Repita con diferentes valores de capacitancia.
6. Compare el efecto del aumento de capacitancia.

#### Tabla 6. Filtro capacitivo

| Capacitor | Voltaje DC de salida | Rizado observado | Comentario |
|---:|---:|---:|---|
| Sin capacitor | | | |
| 100 µF | | | |
| 470 µF | | | |
| 1000 µF | | | |

---

### 6.8 Circuito 7: Regulador básico con diodo Zener

Implemente un regulador de voltaje utilizando una resistencia serie y un diodo Zener en paralelo con la carga.

**Valores sugeridos:**

- Fuente DC: 9 V o 12 V.
- Diodo Zener: 5.1 V.
- Resistencia serie: 330 Ω, 470 Ω o 1 kΩ.
- Resistencia de carga: 1 kΩ.

#### Procedimiento

1. Conecte la resistencia serie entre la fuente y el nodo de salida.
2. Conecte el diodo Zener en polarización inversa entre la salida y tierra.
3. Conecte la resistencia de carga en paralelo con el Zener.
4. Mida el voltaje de salida.
5. Cambie el valor de la fuente de entrada.
6. Observe si el voltaje de salida se mantiene aproximadamente constante.

#### Tabla 7. Regulador con Zener

| Fuente VS | Resistencia serie | Zener nominal | Voltaje de salida medido | Corriente estimada | Observación |
|---:|---:|---:|---:|---:|---|
| 9 V | 470 Ω | 5.1 V | | | |
| 12 V | 470 Ω | 5.1 V | | | |
| 12 V | 1 kΩ | 5.1 V | | | |

---

## 7. SIMULACIÓN DE CIRCUITOS

Realice la simulación de los siguientes circuitos en el software de su preferencia:

1. Polarización directa e inversa del diodo.
2. LED con resistencia limitadora.
3. Rectificador de media onda.
4. Rectificador de onda completa tipo puente.
5. Rectificador con filtro capacitivo.
6. Regulador con diodo Zener.

### Evidencias mínimas de simulación

- Captura del circuito.
- Captura de la forma de onda de entrada y salida en rectificación.
- Captura del voltaje DC de salida con filtro.
- Captura del regulador Zener mostrando el voltaje de salida.

---

## 8. ANÁLISIS DE DATOS

Responda en el informe:

1. ¿Qué diferencia se observó entre polarización directa e inversa?
2. ¿Por qué el diodo no conduce significativamente en polarización inversa?
3. ¿Qué caída de voltaje se midió en el diodo rectificador?
4. ¿Qué caída de voltaje se midió en el LED?
5. ¿Qué diferencia existe entre rectificación de media onda y onda completa?
6. ¿Cómo cambia el rizado al aumentar el valor del capacitor?
7. ¿Qué función cumple el diodo Zener en el regulador?
8. ¿Qué diferencias se encontraron entre valores teóricos, simulados y medidos?
9. ¿Qué posibles fuentes de error pueden afectar los resultados?

---

## 9. CÁLCULOS SOLICITADOS

Incluya los siguientes cálculos en el informe:

1. Corriente del diodo en polarización directa.
2. Corriente del LED para cada resistencia utilizada.
3. Voltaje pico a partir del voltaje RMS de entrada.
4. Voltaje promedio aproximado del rectificador de media onda.
5. Voltaje promedio aproximado del rectificador de onda completa.
6. Corriente aproximada en la carga.
7. Corriente aproximada en el Zener.
8. Potencia disipada en la resistencia serie del regulador.
9. Potencia aproximada del diodo Zener.

### Fórmulas de referencia

```text
VP = VRMS × √2
```

```text
ID = (VS - VD) / R
```

```text
ILED = (VS - VLED) / R
```

```text
P = V × I
```

Para aproximaciones iniciales:

```text
VDC media onda ≈ VP / π
```

```text
VDC onda completa ≈ 2VP / π
```

---

## 10. PREGUNTAS DE PROFUNDIZACIÓN

1. ¿Por qué se recomienda usar un puente rectificador en fuentes DC?
2. ¿Qué ocurre si se conecta un capacitor electrolítico con polaridad invertida?
3. ¿Por qué el voltaje de salida del puente rectificador es menor que el voltaje pico ideal?
4. ¿Qué pasaría si se elimina la resistencia serie del regulador Zener?
5. ¿En qué aplicaciones reales de ingeniería eléctrica se utilizan rectificadores?
6. ¿Cuál es la diferencia entre usar un regulador Zener y un regulador integrado?

---

## 11. EVIDENCIAS OBLIGATORIAS

El informe debe incluir:

- Foto o captura de cada circuito implementado.
- Tablas de medición completas.
- Capturas de simulación.
- Cálculos desarrollados.
- Comparación entre teoría, simulación y medición.
- Análisis de errores.
- Conclusiones relacionadas con los objetivos.

---

## 12. CONCLUSIONES

Las conclusiones deben responder directamente a los objetivos de la práctica. No deben ser frases generales. Deben mencionar el comportamiento del diodo, los resultados de rectificación, el efecto del filtro capacitivo y el desempeño del regulador Zener.

---

## 13. BIBLIOGRAFÍA SUGERIDA

- Boylestad, R. y Nashelsky, L. *Teoría de circuitos y dispositivos electrónicos*.
- Malvino, A. *Principios de electrónica*.
- Floyd, T. *Dispositivos electrónicos*.
- Hojas de datos del diodo 1N4007.
- Hojas de datos del diodo Zener utilizado.
- Hojas de datos del LED utilizado.
