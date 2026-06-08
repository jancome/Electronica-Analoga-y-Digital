# EXPERIENCIA No. A02

# TRANSISTOR BJT COMO INTERRUPTOR Y AMPLIFICADOR BÁSICO

**Asignatura:** Electrónica Analógica y Digital  
**Periodo:** 2026-2  
**Programa:** Ingeniería Eléctrica  
**Duración estimada:** 3 horas presenciales + trabajo independiente  

---

## 1. INTRODUCCIÓN

El transistor bipolar de unión, conocido como BJT por sus siglas en inglés, es uno de los dispositivos semiconductores más importantes en la electrónica analógica y digital. Está formado por tres terminales: base, colector y emisor. Dependiendo de la forma en que se polarice, puede funcionar como interruptor electrónico, amplificador de señal o elemento de control de corriente.

En aplicaciones de ingeniería eléctrica, el transistor BJT se utiliza para activar cargas de baja y mediana potencia, adaptar señales de control, manejar relés, encender indicadores, controlar pequeñas cargas DC y construir etapas básicas de amplificación. Su principio de funcionamiento se basa en que una pequeña corriente aplicada en la base puede controlar una corriente mayor entre colector y emisor.

En esta experiencia se estudiará el transistor BJT principalmente como interruptor electrónico. Se analizarán las regiones de corte y saturación, el cálculo de la resistencia de base, la activación de un LED, el control de una carga y el uso del diodo de protección en cargas inductivas. Finalmente, se realizará una aproximación al transistor como amplificador básico en configuración de emisor común.

---

## 2. OBJETIVO

Implementar y analizar circuitos básicos con transistor BJT, verificando su funcionamiento como interruptor electrónico y observando su comportamiento en una configuración elemental de amplificación.

### Objetivos específicos

- Identificar los terminales base, colector y emisor de un transistor BJT.
- Diferenciar transistores NPN y PNP a partir de su símbolo y hoja de datos.
- Comprobar las regiones de corte y saturación del transistor.
- Calcular la resistencia de base para activar una carga mediante un BJT.
- Implementar un circuito con BJT para encender un LED.
- Implementar un circuito con BJT para activar una carga DC.
- Analizar el uso del diodo de protección en cargas inductivas.
- Observar el comportamiento de un amplificador básico en emisor común.
- Comparar resultados teóricos, simulados y medidos.

---

## 3. NORMATIVA DE SEGURIDAD

Es obligatorio cumplir las normas de seguridad del laboratorio durante toda la práctica.

**PELIGRO:** Riesgo de choque eléctrico al manipular fuentes de alimentación. Asegúrese de que el equipo esté apagado antes de realizar cualquier conexión.

**AVISO:** Riesgo de daño al transistor si se excede la corriente máxima de base, colector o la potencia permitida. Revise la hoja de datos antes de energizar el circuito.

**PRECAUCIÓN:** Las resistencias, transistores o cargas pueden calentarse si circula demasiada corriente o si se conectan incorrectamente.

**ELEMENTOS DE PROTECCIÓN PERSONAL:** Bata de laboratorio y gafas de seguridad cuando el laboratorio lo exija.

### Recomendaciones de seguridad

- Verifique el pinout del transistor antes de conectarlo.
- No conecte directamente la base del transistor a la fuente sin resistencia limitadora.
- No alimente el circuito hasta revisar las conexiones.
- Verifique la polaridad del diodo de protección cuando se utilicen cargas inductivas.
- No exceda el voltaje ni la corriente recomendada para el transistor.
- Desconecte la alimentación antes de modificar el circuito.

---

## 4. RECURSOS

### Materiales o dispositivos

- Transistor BJT NPN 2N2222, PN2222, BC547 o equivalente.
- Transistor BJT PNP, opcional para comparación.
- Diodo 1N4007 o 1N4148.
- LED rojo, verde o amarillo.
- Resistencias de 220 Ω, 330 Ω, 1 kΩ, 2.2 kΩ, 4.7 kΩ, 10 kΩ y 100 kΩ.
- Potenciómetro de 10 kΩ, opcional.
- Relé de 5 V o 12 V, si está disponible.
- Motor DC pequeño o carga resistiva, si está disponible.
- Capacitores de 1 µF, 10 µF o 100 µF para la etapa de amplificación, si aplica.
- Protoboard.
- Cables de conexión.

### Herramientas

- Pinzas de punta.
- Cortafrío, si se requiere.
- Computador con software de simulación.

### Equipos

- Fuente de corriente directa DC.
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

Antes de realizar la práctica, el estudiante debe consultar la hoja de datos del transistor que utilizará en el laboratorio.

Debe identificar:

- Tipo de transistor: NPN o PNP.
- Distribución de terminales: base, colector y emisor.
- Corriente máxima de colector.
- Voltaje máximo colector-emisor.
- Ganancia de corriente aproximada, conocida como beta o hFE.
- Potencia máxima de disipación.

Complete la siguiente tabla antes de iniciar el montaje.

| Transistor | Tipo | Pin 1 | Pin 2 | Pin 3 | IC máxima | VCE máxima | hFE aproximado |
|---|---|---|---|---|---:|---:|---:|
| 2N2222 / PN2222 / BC547 | | | | | | | |

---

## 6. PROCEDIMIENTO EXPERIMENTAL

### 6.1 Identificación de terminales del transistor

1. Observe físicamente el transistor.
2. Identifique la referencia impresa en el encapsulado.
3. Consulte el datasheet del componente.
4. Dibuje la vista frontal del transistor e indique base, colector y emisor.
5. Compare el símbolo del transistor NPN con el símbolo del transistor PNP.

#### Tabla 1. Identificación del transistor

| Parámetro | Información encontrada |
|---|---|
| Referencia del transistor | |
| Tipo NPN o PNP | |
| Terminal base | |
| Terminal colector | |
| Terminal emisor | |
| Encapsulado | |
| Aplicación típica | |

---

### 6.2 Circuito 1: BJT NPN como interruptor para LED

Arme un circuito donde el transistor BJT NPN controle el encendido de un LED conectado al colector.

**Valores sugeridos:**

- Fuente de alimentación: 5 V DC.
- Transistor: 2N2222, PN2222 o BC547.
- Resistencia del LED: 330 Ω.
- Resistencia de base: 10 kΩ inicialmente.

#### Procedimiento

1. Conecte el emisor del transistor a tierra.
2. Conecte el LED en serie con su resistencia hacia el positivo de la fuente.
3. Conecte el extremo inferior del LED al colector del transistor.
4. Conecte la base del transistor a través de una resistencia de 10 kΩ hacia 5 V.
5. Mida el voltaje base-emisor VBE.
6. Mida el voltaje colector-emisor VCE.
7. Observe si el LED enciende.
8. Retire la señal de base y observe si el LED se apaga.

#### Tabla 2. BJT como interruptor para LED

| Condición de base | VBE | VCE | Estado del LED | Región estimada del transistor |
|---|---:|---:|---|---|
| Base desconectada o en 0 V | | | | |
| Base con resistencia a 5 V | | | | |

---

### 6.3 Circuito 2: Variación de la resistencia de base

Repita el circuito anterior usando diferentes resistencias de base.

**Valores sugeridos:**

- RB1 = 100 kΩ.
- RB2 = 10 kΩ.
- RB3 = 4.7 kΩ.
- RB4 = 1 kΩ.

#### Procedimiento

1. Cambie la resistencia de base.
2. Mida VBE.
3. Mida VCE.
4. Calcule la corriente de base.
5. Observe el brillo del LED.
6. Determine si el transistor se encuentra en corte, activa o saturación.

#### Tabla 3. Efecto de la resistencia de base

| RB | VBE | VCE | IB calculada | Estado del LED | Región estimada |
|---:|---:|---:|---:|---|---|
| 100 kΩ | | | | | |
| 10 kΩ | | | | | |
| 4.7 kΩ | | | | | |
| 1 kΩ | | | | | |

### Cálculo sugerido

```text
IB = (VIN - VBE) / RB
```

Donde:

- IB es la corriente de base.
- VIN es el voltaje aplicado a la resistencia de base.
- VBE es el voltaje base-emisor.
- RB es la resistencia de base.

---

### 6.4 Circuito 3: Control de carga DC con transistor

Utilice el transistor BJT para controlar una carga diferente al LED, como un motor DC pequeño, una lámpara de baja tensión o una resistencia de carga.

**Valores sugeridos:**

- Fuente: 5 V o 9 V DC, según la carga.
- Transistor: 2N2222 o equivalente.
- Resistencia de base: 1 kΩ o 4.7 kΩ.
- Carga: motor DC pequeño o resistencia.

#### Procedimiento

1. Conecte el transistor como interruptor en configuración de lado bajo.
2. Conecte la carga entre VCC y colector.
3. Conecte el emisor a tierra.
4. Aplique señal de control en la base mediante resistencia.
5. Mida VBE.
6. Mida VCE.
7. Mida o calcule la corriente de la carga.
8. Analice si el transistor está saturado.

#### Tabla 4. Control de carga DC

| Carga utilizada | VCC | RB | VBE | VCE | Corriente de carga | Estado de la carga |
|---|---:|---:|---:|---:|---:|---|
| | | | | | | |

---

### 6.5 Circuito 4: Activación de relé con diodo de protección

Si se dispone de un relé, implemente un circuito de activación usando transistor BJT y diodo de protección en paralelo con la bobina del relé.

#### Procedimiento

1. Conecte la bobina del relé entre VCC y el colector del transistor.
2. Conecte el emisor del transistor a tierra.
3. Conecte la base mediante resistencia a la señal de control.
4. Conecte un diodo en paralelo con la bobina del relé.
5. Verifique la polaridad del diodo de protección.
6. Active y desactive el transistor.
7. Observe el comportamiento del relé.

#### Tabla 5. Activación de relé

| Condición de base | VBE | VCE | Estado del relé | Observación |
|---|---:|---:|---|---|
| Base en 0 V | | | | |
| Base activada | | | | |

### Pregunta clave

¿Qué función cumple el diodo conectado en paralelo con la bobina del relé?

---

### 6.6 Circuito 5: Medición de corrientes IB, IC e IE

Implemente un circuito básico con transistor BJT y mida o calcule las corrientes principales.

#### Procedimiento

1. Utilice el circuito del LED o de carga resistiva.
2. Calcule la corriente de base a partir de la resistencia de base.
3. Calcule la corriente de colector a partir de la resistencia de carga.
4. Mida los voltajes necesarios.
5. Calcule la ganancia aproximada.

#### Tabla 6. Corrientes del transistor

| RB | RC o carga | IB calculada | IC calculada | IE aproximada | beta aproximado IC/IB |
|---:|---:|---:|---:|---:|---:|
| | | | | | |

### Fórmulas de referencia

```text
IB = (VIN - VBE) / RB
```

```text
IC = (VCC - VCE) / RC
```

```text
β ≈ IC / IB
```

```text
IE ≈ IB + IC
```

---

### 6.7 Circuito 6: Amplificador básico en emisor común

Implemente o simule una etapa básica de amplificación en configuración de emisor común.

**Valores sugeridos para simulación:**

- VCC = 9 V o 12 V.
- RC = 2.2 kΩ o 4.7 kΩ.
- RE = 1 kΩ.
- Red de polarización de base con resistencias.
- Capacitor de acoplamiento de entrada: 1 µF o 10 µF.
- Señal de entrada: senoidal pequeña.

#### Procedimiento

1. Arme o simule el amplificador en emisor común.
2. Aplique una señal senoidal pequeña en la entrada.
3. Observe la señal de salida en el colector.
4. Compare fase de entrada y salida.
5. Mida amplitud de entrada y salida.
6. Calcule la ganancia de voltaje aproximada.

#### Tabla 7. Amplificador básico

| Vin pico | Vout pico | Ganancia aproximada AV | ¿Salida invertida? | Observación |
|---:|---:|---:|---|---|
| | | | | |

### Fórmula sugerida

```text
AV = Vout / Vin
```

---

## 7. SIMULACIÓN DE CIRCUITOS

Realice la simulación de los siguientes circuitos en el software de su preferencia:

1. BJT como interruptor para LED.
2. Variación de resistencia de base.
3. Control de carga DC con BJT.
4. Activación de relé con diodo de protección, si el software lo permite.
5. Medición de corrientes IB, IC e IE.
6. Amplificador básico en emisor común.

### Evidencias mínimas de simulación

- Captura del circuito.
- Captura de mediciones de VBE y VCE.
- Captura del estado de la carga activada y desactivada.
- Captura de la señal de entrada y salida en el amplificador, si aplica.

---

## 8. ANÁLISIS DE DATOS

Responda en el informe:

1. ¿Qué ocurre cuando la base del transistor no recibe corriente?
2. ¿Qué ocurre cuando la base recibe corriente suficiente?
3. ¿Qué valores de VBE se obtuvieron en conducción?
4. ¿Qué valor de VCE indica que el transistor está saturado?
5. ¿Cómo afecta la resistencia de base al funcionamiento del transistor?
6. ¿Por qué no se debe conectar la base directamente a la fuente?
7. ¿Qué función cumple el transistor en el control de una carga?
8. ¿Qué función cumple el diodo de protección en el relé?
9. ¿Qué diferencia existe entre usar el transistor como interruptor y como amplificador?
10. ¿Qué diferencias se encontraron entre teoría, simulación y medición?

---

## 9. CÁLCULOS SOLICITADOS

Incluya los siguientes cálculos en el informe:

1. Corriente de base para cada resistencia utilizada.
2. Corriente del LED o carga.
3. Corriente de colector.
4. Corriente de emisor aproximada.
5. Ganancia aproximada beta.
6. Potencia disipada en el transistor.
7. Potencia disipada en la resistencia de base.
8. Ganancia de voltaje del amplificador, si se implementa o simula.

### Fórmulas de referencia

```text
IB = (VIN - VBE) / RB
```

```text
IC = (VCC - VCE) / RC
```

```text
β ≈ IC / IB
```

```text
IE ≈ IC + IB
```

```text
PTRANSISTOR ≈ VCE × IC
```

```text
AV = Vout / Vin
```

---

## 10. PREGUNTAS DE PROFUNDIZACIÓN

1. ¿Por qué el transistor BJT puede funcionar como interruptor electrónico?
2. ¿Qué diferencia existe entre corte, región activa y saturación?
3. ¿Por qué se usa una resistencia en la base del transistor?
4. ¿Qué puede ocurrir si la corriente de base es insuficiente?
5. ¿Qué puede ocurrir si la corriente de base es excesiva?
6. ¿Por qué se recomienda colocar un diodo en paralelo con una bobina de relé?
7. ¿Qué aplicaciones reales tiene un transistor BJT en sistemas eléctricos?
8. ¿Qué limitaciones tiene un BJT frente a un MOSFET para controlar cargas?

---

## 11. EVIDENCIAS OBLIGATORIAS

El informe debe incluir:

- Foto o captura de cada circuito implementado.
- Tablas de medición completas.
- Capturas de simulación.
- Cálculos desarrollados.
- Identificación del pinout del transistor usado.
- Comparación entre teoría, simulación y medición.
- Análisis de errores.
- Conclusiones relacionadas con los objetivos.

---

## 12. CONCLUSIONES

Las conclusiones deben responder directamente a los objetivos de la práctica. Deben mencionar el comportamiento del transistor en corte, saturación y, si se trabajó, en región activa. También deben explicar la importancia de la resistencia de base, el uso del transistor como interruptor y la función del diodo de protección en cargas inductivas.

---

## 13. BIBLIOGRAFÍA SUGERIDA

- Boylestad, R. y Nashelsky, L. *Teoría de circuitos y dispositivos electrónicos*.
- Malvino, A. *Principios de electrónica*.
- Floyd, T. *Dispositivos electrónicos*.
- Hojas de datos del transistor 2N2222, PN2222 o BC547.
- Hojas de datos del diodo 1N4007 o 1N4148.
- Hojas de datos del relé utilizado, si aplica.
