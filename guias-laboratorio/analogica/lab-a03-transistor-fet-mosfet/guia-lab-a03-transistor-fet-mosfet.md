# EXPERIENCIA No. A03

# TRANSISTOR FET/MOSFET COMO DISPOSITIVO DE CONTROL

**Asignatura:** Electrónica Analógica y Digital  
**Periodo:** 2026-2  
**Programa:** Ingeniería Eléctrica  

---

## 1. INTRODUCCIÓN

El transistor de efecto de campo, conocido como FET por sus siglas en inglés, es un dispositivo semiconductor controlado principalmente por voltaje. A diferencia del transistor BJT, que requiere corriente de base para controlar la corriente de colector, el FET controla la corriente entre drenador y fuente mediante el voltaje aplicado en la compuerta.

Dentro de esta familia, el MOSFET es uno de los dispositivos más utilizados en circuitos electrónicos modernos debido a su alta impedancia de entrada, rápida conmutación y eficiencia en el control de cargas. En aplicaciones reales de ingeniería eléctrica y electrónica, los MOSFET se encuentran en fuentes conmutadas, variadores, controladores de motores, sistemas de iluminación LED, inversores, cargadores, protecciones electrónicas y sistemas embebidos.

En esta experiencia se estudiará el MOSFET como interruptor electrónico para controlar cargas DC. Se analizarán los terminales Gate, Drain y Source, el voltaje de compuerta-fuente VGS, el voltaje drenador-fuente VDS, la corriente de drenador ID y el comportamiento del dispositivo en estado de corte y conducción. Finalmente, se realizará una comparación técnica entre el BJT y el MOSFET como dispositivos de control.

---

## 2. OBJETIVO

Implementar y analizar circuitos básicos con transistor FET/MOSFET, verificando su funcionamiento como dispositivo de control de carga y comparando su comportamiento con el transistor BJT.

### Objetivos específicos

- Identificar los terminales Gate, Drain y Source de un MOSFET.
- Diferenciar un MOSFET de canal N y uno de canal P a partir del símbolo y hoja de datos.
- Comprobar el comportamiento del MOSFET en corte y conducción.
- Implementar un circuito con MOSFET canal N para controlar un LED.
- Implementar un circuito con MOSFET para controlar una carga DC.
- Analizar el uso de resistencia de compuerta y resistencia pull-down.
- Medir o estimar VGS, VDS e ID en diferentes condiciones de operación.
- Comparar técnicamente el uso de BJT y MOSFET para control de cargas.
- Realizar una simulación básica de control PWM, si el software o los equipos lo permiten.

---

## 3. NORMATIVA DE SEGURIDAD

Es obligatorio cumplir las normas de seguridad del laboratorio durante toda la práctica.

**PELIGRO:** Riesgo de choque eléctrico al manipular fuentes de alimentación. Asegúrese de que los equipos estén apagados antes de realizar cualquier conexión.

**AVISO:** Riesgo de daño al MOSFET si se conecta incorrectamente la compuerta, el drenador o la fuente. Revise cuidadosamente el pinout del componente antes de energizar el circuito.

**PRECAUCIÓN:** El MOSFET puede calentarse si se controla una carga con corriente elevada, si no entra completamente en conducción o si se excede su potencia máxima de disipación.

**ELEMENTOS DE PROTECCIÓN PERSONAL:** Bata de laboratorio y gafas de seguridad cuando el laboratorio lo exija.

### Recomendaciones de seguridad

- Verifique el pinout del MOSFET antes de conectarlo.
- No deje la compuerta del MOSFET flotante.
- Utilice una resistencia pull-down entre compuerta y fuente.
- Utilice resistencia de compuerta cuando se conecte a señales de control.
- Use diodo de protección cuando controle cargas inductivas como relés o motores.
- No exceda el voltaje máximo VGS del dispositivo.
- Desconecte la fuente antes de modificar conexiones.

### Alcance de la práctica

- **Preparación previa:** hoja de datos, pinout, VGS(th), RDS(on) y simulación del interruptor.
- **Montaje esencial:** control de LED, efecto de VGS y control protegido de una carga.
- **Profundización:** comparación extendida con BJT y control PWM.
- **Aplicación ABP:** seleccionar y justificar el dispositivo de control del proyecto.

PWM se desarrolla cuando exista generador, microcontrolador o simulador disponible. No constituye un requisito universal del montaje esencial.

---

## 4. RECURSOS

### Materiales o dispositivos

- MOSFET canal N IRLZ44N, IRFZ44N, 2N7000, BS170 o equivalente.
- Transistor BJT NPN 2N2222 o BC547 para comparación, opcional.
- Diodo 1N4007 o 1N4148 para protección de cargas inductivas.
- LED rojo, verde o amarillo.
- Motor DC pequeño, relé o carga resistiva, si está disponible.
- Resistencias de 220 Ω, 330 Ω, 1 kΩ, 10 kΩ y 100 kΩ.
- Potenciómetro de 10 kΩ, opcional.
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
- Generador de funciones o placa Arduino/ESP32 para PWM, si está disponible.

### Software sugerido

- Proteus.
- Multisim.
- Tinkercad Circuits.
- Falstad Circuit Simulator.
- LTspice u otro simulador equivalente.

---

## 5. RECOMENDACIÓN PREVIA

Antes de realizar la práctica, el estudiante debe consultar la hoja de datos del MOSFET que utilizará.

Debe identificar:

- Tipo de MOSFET: canal N o canal P.
- Distribución de terminales: Gate, Drain y Source.
- Voltaje máximo drenador-fuente VDS.
- Corriente máxima de drenador ID.
- Voltaje máximo compuerta-fuente VGS.
- Resistencia de conducción RDS(on).
- Voltaje umbral VGS(th).
- Potencia máxima de disipación.

Complete la siguiente tabla antes de iniciar el montaje.

| MOSFET | Tipo | Pin 1 | Pin 2 | Pin 3 | VDS máx. | ID máx. | VGS(th) | RDS(on) |
|---|---|---|---|---|---:|---:|---:|---:|
| IRLZ44N / IRFZ44N / 2N7000 / BS170 | | | | | | | | |

---

## 6. PROCEDIMIENTO EXPERIMENTAL

### 6.1 Identificación de terminales del MOSFET

1. Observe físicamente el MOSFET.
2. Identifique la referencia impresa en el encapsulado.
3. Consulte el datasheet del componente.
4. Dibuje la vista frontal del MOSFET e indique Gate, Drain y Source.
5. Dibuje el símbolo eléctrico de un MOSFET canal N.
6. Compare el símbolo del MOSFET canal N con el del MOSFET canal P.

#### Tabla 1. Identificación del MOSFET

| Parámetro | Información encontrada |
|---|---|
| Referencia del MOSFET | |
| Tipo canal N o canal P | |
| Terminal Gate | |
| Terminal Drain | |
| Terminal Source | |
| Encapsulado | |
| VGS(th) | |
| RDS(on) | |
| Aplicación típica | |

---

### 6.2 Circuito 1: MOSFET canal N como interruptor para LED

Arme un circuito donde el MOSFET canal N controle el encendido de un LED conectado al drenador.

**Valores sugeridos:**

- Fuente de alimentación: 5 V DC.
- MOSFET: 2N7000, BS170, IRLZ44N o equivalente.
- Resistencia del LED: 330 Ω.
- Resistencia de compuerta: 1 kΩ.
- Resistencia pull-down: 100 kΩ.

#### Procedimiento

1. Conecte la fuente del MOSFET a tierra.
2. Conecte el LED en serie con su resistencia hacia el positivo de la fuente.
3. Conecte el extremo inferior del LED al drenador del MOSFET.
4. Conecte una resistencia pull-down de 100 kΩ entre Gate y Source.
5. Aplique una señal de 0 V en la compuerta y observe el estado del LED.
6. Aplique una señal de 5 V en la compuerta mediante una resistencia de 1 kΩ.
7. Mida VGS.
8. Mida VDS.
9. Observe si el LED enciende.

#### Tabla 2. MOSFET como interruptor para LED

| Condición de Gate | VGS | VDS | Estado del LED | Región estimada |
|---|---:|---:|---|---|
| Gate en 0 V | | | | |
| Gate en 5 V | | | | |

---

### 6.3 Circuito 2: Efecto del voltaje de compuerta VGS

Utilice el circuito anterior, pero varíe el voltaje aplicado a la compuerta del MOSFET.

**Valores sugeridos:**

- VGS = 0 V.
- VGS = 2 V.
- VGS = 3.3 V.
- VGS = 5 V.

#### Procedimiento

1. Aplique diferentes valores de voltaje en la compuerta.
2. Mida VGS.
3. Mida VDS.
4. Observe el estado del LED o la carga.
5. Determine a partir de qué voltaje el MOSFET empieza a conducir.
6. Compare el resultado con el valor VGS(th) de la hoja de datos.

#### Tabla 3. Variación de VGS

| VGS aplicado | VGS medido | VDS medido | Estado de la carga | Observación |
|---:|---:|---:|---|---|
| 0 V | | | | |
| 2 V | | | | |
| 3.3 V | | | | |
| 5 V | | | | |

### Nota importante

El voltaje umbral VGS(th) no siempre significa que el MOSFET esté completamente encendido. Para controlar cargas con baja resistencia de conducción, se debe verificar el valor de RDS(on) indicado en la hoja de datos para el VGS utilizado.

---

### 6.4 Circuito 3: Control de carga DC con MOSFET

Utilice el MOSFET para controlar una carga diferente al LED, como un motor DC pequeño, una lámpara de baja tensión o una resistencia de potencia.

**Valores sugeridos:**

- Fuente: 5 V, 9 V o 12 V DC según la carga.
- MOSFET canal N.
- Resistencia de compuerta: 1 kΩ.
- Resistencia pull-down: 100 kΩ.
- Carga: motor DC pequeño o resistencia.

#### Procedimiento

1. Conecte el MOSFET como interruptor en configuración de lado bajo.
2. Conecte la carga entre VCC y Drain.
3. Conecte Source a tierra.
4. Conecte la resistencia pull-down entre Gate y Source.
5. Aplique señal de control en Gate.
6. Mida VGS.
7. Mida VDS.
8. Mida o calcule la corriente de la carga.
9. Analice si el MOSFET conduce adecuadamente.

#### Tabla 4. Control de carga DC con MOSFET

| Carga utilizada | VCC | VGS | VDS | Corriente de carga ID | Estado de la carga |
|---|---:|---:|---:|---:|---|
| | | | | | |

---

### 6.5 Circuito 4: Control de motor DC con diodo de protección

Si se dispone de un motor DC pequeño, implemente un control de encendido y apagado mediante MOSFET. Conecte un diodo de protección en paralelo con el motor.

#### Procedimiento

1. Conecte el motor entre VCC y Drain del MOSFET.
2. Conecte Source a tierra.
3. Conecte la compuerta mediante resistencia de 1 kΩ.
4. Conecte resistencia pull-down de 100 kΩ entre Gate y Source.
5. Conecte un diodo de protección en paralelo con el motor.
6. Active y desactive el MOSFET.
7. Observe el comportamiento del motor.
8. Mida VGS y VDS.

#### Tabla 5. Control de motor DC

| Condición de Gate | VGS | VDS | Estado del motor | Observación |
|---|---:|---:|---|---|
| Gate en 0 V | | | | |
| Gate activado | | | | |

### Pregunta clave

¿Qué función cumple el diodo conectado en paralelo con el motor?

---

### 6.6 Circuito 5: Comparación BJT vs MOSFET como interruptor

Implemente o simule dos circuitos de control de carga: uno usando BJT y otro usando MOSFET. Use la misma carga si es posible.

#### Procedimiento

1. Arme o simule un circuito de control con BJT.
2. Arme o simule un circuito de control con MOSFET.
3. Mida la señal requerida en la entrada de control.
4. Mida la caída de voltaje en el dispositivo de control.
5. Compare el comportamiento de ambos circuitos.
6. Analice cuál dispositivo resulta más conveniente para controlar la carga.

#### Tabla 6. Comparación BJT vs MOSFET

| Criterio | BJT | MOSFET |
|---|---|---|
| Variable de control | Corriente de base | Voltaje de compuerta |
| Terminales principales | Base, colector, emisor | Gate, Drain, Source |
| Caída en conducción | | |
| Corriente de entrada requerida | | |
| Facilidad de control | | |
| Aplicación recomendada | | |

---

### 6.7 Circuito 6: Control PWM con MOSFET

Realice una simulación o montaje en el cual el MOSFET controle la intensidad de un LED o la velocidad de un motor DC mediante una señal PWM.

**Opciones para generar PWM:**

- Generador de funciones.
- Arduino.
- ESP32.
- Simulador.

#### Procedimiento

1. Aplique una señal PWM a la compuerta del MOSFET mediante resistencia de compuerta.
2. Conecte resistencia pull-down entre Gate y Source.
3. Conecte la carga controlada por el MOSFET.
4. Varíe el ciclo de trabajo de la señal PWM.
5. Observe el cambio en brillo del LED o velocidad del motor.
6. Registre al menos tres condiciones de ciclo de trabajo.

#### Tabla 7. Control PWM con MOSFET

| Ciclo de trabajo PWM | VGS observado | Estado de la carga | Observación |
|---:|---:|---|---|
| 25% | | | |
| 50% | | | |
| 75% | | | |

---

## 7. SIMULACIÓN DE CIRCUITOS

Realice la simulación de los siguientes circuitos en el software de su preferencia:

1. MOSFET como interruptor para LED.
2. Variación del voltaje VGS.
3. Control de carga DC con MOSFET.
4. Control de motor DC con diodo de protección.
5. Comparación BJT vs MOSFET.
6. Control PWM con MOSFET, si el software lo permite.

### Evidencias mínimas de simulación

- Captura del circuito.
- Captura de mediciones de VGS y VDS.
- Captura del estado de la carga activada y desactivada.
- Captura de la señal PWM aplicada a Gate, si aplica.
- Captura del efecto del cambio de ciclo de trabajo.

---

## 8. ANÁLISIS DE DATOS

Responda en el informe:

1. ¿Qué ocurre cuando la compuerta del MOSFET está en 0 V?
2. ¿Qué ocurre cuando la compuerta recibe un voltaje positivo suficiente?
3. ¿Qué función cumple la resistencia pull-down?
4. ¿Qué función cumple la resistencia de compuerta?
5. ¿Qué valor de VGS permitió activar la carga correctamente?
6. ¿Por qué VGS(th) no siempre garantiza conducción completa?
7. ¿Qué valor de VDS se obtiene cuando el MOSFET está conduciendo?
8. ¿Qué función cumple el diodo de protección en motores o relés?
9. ¿Qué diferencias se observaron entre BJT y MOSFET como interruptores?
10. ¿Qué ventajas tiene el MOSFET para controlar cargas mediante PWM?

---

## 9. CÁLCULOS SOLICITADOS

Incluya los siguientes cálculos en el informe:

1. Corriente de la carga controlada por el MOSFET.
2. Potencia aproximada disipada por la carga.
3. Potencia aproximada disipada por el MOSFET.
4. Comparación de caída de voltaje en conducción entre BJT y MOSFET.
5. Corriente promedio estimada en PWM para diferentes ciclos de trabajo, si aplica.
6. Potencia promedio estimada en PWM, si aplica.

### Fórmulas de referencia

```text
ID = VLOAD / RLOAD
```

```text
PLOAD = VLOAD × ID
```

```text
PMOSFET ≈ VDS × ID
```

```text
P ≈ I² × RDS(on)
```

Para PWM ideal:

```text
Vpromedio ≈ D × VCC
```

Donde D es el ciclo de trabajo expresado en forma decimal.

---

## 10. PREGUNTAS DE PROFUNDIZACIÓN

1. ¿Por qué se dice que el MOSFET es un dispositivo controlado por voltaje?
2. ¿Qué diferencia existe entre VGS(th) y el voltaje necesario para plena conducción?
3. ¿Por qué no se recomienda dejar la compuerta del MOSFET flotante?
4. ¿Qué ventajas tiene el MOSFET frente al BJT en control de cargas?
5. ¿Qué precauciones deben tomarse al controlar motores con MOSFET?
6. ¿Por qué un MOSFET lógico puede ser más conveniente que un MOSFET común en circuitos de 5 V o 3.3 V?
7. ¿Qué aplicaciones reales tienen los MOSFET en sistemas eléctricos?
8. ¿Qué ocurre si se supera el voltaje máximo VGS permitido por el fabricante?

---

## 11. EVIDENCIAS OBLIGATORIAS

El informe debe incluir:

- Foto o captura de cada circuito implementado.
- Tablas de medición completas.
- Capturas de simulación.
- Cálculos desarrollados.
- Identificación del pinout del MOSFET usado.
- Comparación entre teoría, simulación y medición.
- Comparación técnica BJT vs MOSFET.
- Análisis de errores.
- Conclusiones relacionadas con los objetivos.

---

## 12. CONCLUSIONES

Las conclusiones deben responder directamente a los objetivos de la práctica. Deben mencionar el comportamiento del MOSFET en corte y conducción, la importancia del voltaje VGS, el uso de la resistencia pull-down, la función del diodo de protección y la comparación con el transistor BJT.

---

## 13. BIBLIOGRAFÍA SUGERIDA

- Boylestad, R. y Nashelsky, L. *Teoría de circuitos y dispositivos electrónicos*.
- Malvino, A. *Principios de electrónica*.
- Floyd, T. *Dispositivos electrónicos*.
- Hojas de datos del MOSFET utilizado.
- Hojas de datos del transistor BJT utilizado para comparación.
- Hojas de datos del diodo 1N4007 o 1N4148.
