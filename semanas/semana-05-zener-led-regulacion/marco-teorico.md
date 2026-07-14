# Marco teórico – Semana 05

# Transistores BJT, FET/MOSFET y cierre de la unidad analógica

## 1. Tema de la semana

Transistores como dispositivos de control en circuitos electrónicos: BJT como interruptor controlado por corriente y MOSFET como interruptor controlado por voltaje. Esta semana también sirve para cerrar la unidad analógica del primer corte.

![BJT vs MOSFET como interruptor](../../recursos/imagenes/analogica/bjt-vs-mosfet-interruptor.svg)

---

## 2. Objetivo de aprendizaje

Analizar el funcionamiento básico de transistores BJT y MOSFET como elementos de conmutación, relacionándolos con aplicaciones de control de cargas, indicadores, motores pequeños, relés y etapas electrónicas de potencia baja o media.

---

## 3. Contexto e importancia

Los diodos permiten conducir corriente principalmente en un sentido, rectificar señales y regular voltajes simples. Sin embargo, muchos sistemas electrónicos necesitan algo más: **controlar una carga a partir de una señal pequeña**.

Ahí aparecen los transistores. Un transistor puede actuar como interruptor electrónico o como amplificador. En sistemas reales se utiliza para encender luces, activar relés, controlar motores, excitar zumbadores, adaptar señales, manejar cargas desde microcontroladores y construir etapas de amplificación.

En ingeniería eléctrica, los transistores aparecen en fuentes, variadores, tarjetas de control, sistemas de protección, electrónica de potencia, automatismos, drivers de motores y circuitos de mando.

---

## 4. Transistor BJT

El BJT, o transistor bipolar de unión, es un dispositivo semiconductor de tres terminales:

- **Base (B)**.
- **Colector (C)**.
- **Emisor (E)**.

En un BJT NPN, una pequeña corriente que entra por la base permite controlar una corriente mayor entre colector y emisor.

Por eso se dice que el BJT es un dispositivo **controlado por corriente**.

---

## 5. Regiones de operación del BJT

Para esta asignatura se trabajarán principalmente tres regiones:

| Región | Comportamiento | Aplicación típica |
|---|---|---|
| Corte | No circula corriente significativa por el colector | Interruptor apagado |
| Activa | La corriente de colector depende de la corriente de base | Amplificación |
| Saturación | El transistor conduce al máximo posible según la carga | Interruptor encendido |

Cuando se usa como interruptor, normalmente se busca trabajar entre **corte** y **saturación**.

---

## 6. BJT como interruptor

Un BJT puede controlar una carga conectada al colector. La base recibe una señal de control a través de una resistencia.

Si no hay corriente de base:

```text
IB = 0  →  IC ≈ 0
```

El transistor está en corte y la carga permanece apagada.

Si hay corriente suficiente en la base:

```text
IB suficiente  →  transistor saturado  →  carga encendida
```

La resistencia de base es importante porque limita la corriente que entra a la base y protege tanto la señal de control como el transistor.

---

## 7. Ganancia de corriente

La relación aproximada entre la corriente de colector y la corriente de base se representa con beta:

```text
β = IC / IB
```

Donde:

- **β** es la ganancia de corriente.
- **IC** es la corriente de colector.
- **IB** es la corriente de base.

En diseño como interruptor no se debe depender únicamente del valor ideal de beta, porque este puede variar entre dispositivos. Por eso se fuerza una corriente de base suficiente para asegurar saturación.

---

## 8. Transistor FET/MOSFET

El MOSFET es un transistor de efecto de campo. Sus terminales principales son:

- **Gate (G)** o compuerta.
- **Drain (D)** o drenador.
- **Source (S)** o fuente.

A diferencia del BJT, el MOSFET se controla principalmente mediante voltaje entre compuerta y fuente:

```text
VGS = VG - VS
```

Por eso se dice que es un dispositivo **controlado por voltaje**.

---

## 9. MOSFET como interruptor

En un MOSFET canal N usado como interruptor de lado bajo:

- La carga se conecta entre el positivo de la fuente y el drenador.
- El source va a tierra.
- La compuerta recibe la señal de control.

Si el voltaje de compuerta es bajo:

```text
VGS = 0 V  →  MOSFET apagado
```

Si el voltaje de compuerta es suficiente:

```text
VGS suficiente  →  MOSFET encendido
```

En conducción, un MOSFET adecuado presenta una resistencia baja entre drenador y source, conocida como:

```text
RDS(on)
```

Mientras menor sea esa resistencia, menor será la pérdida de potencia.

---

## 10. Comparación BJT vs MOSFET

| Aspecto | BJT | MOSFET |
|---|---|---|
| Variable de control | Corriente de base | Voltaje gate-source |
| Terminales | Base, colector, emisor | Gate, drain, source |
| Uso como interruptor | Corte y saturación | Apagado y conducción |
| Pérdida típica | VCE(sat) × IC | I² × RDS(on) |
| Ventaja | Económico y fácil de entender | Alta eficiencia y bajo consumo de control |
| Cuidado principal | Limitar corriente de base | No dejar la compuerta flotante |

---

## 11. Aplicaciones reales

- Encendido de LED o tiras LED.
- Activación de relés.
- Control de motores DC pequeños.
- Drivers de cargas desde microcontroladores.
- Tarjetas de control de portones, bombas o automatismos.
- Fuentes conmutadas.
- Etapas de protección y control.

---

## 12. Ejemplo guiado

Se desea encender un LED de 20 mA usando un transistor BJT NPN como interruptor. La señal de control es de 5 V y se asume:

```text
VBE ≈ 0.7 V
IB deseada = 2 mA
```

La resistencia de base se calcula así:

```text
RB = (VIN - VBE) / IB
RB = (5 V - 0.7 V) / 0.002 A
RB = 4.3 V / 0.002 A
RB = 2150 Ω
```

Se puede seleccionar un valor comercial cercano, por ejemplo 2.2 kΩ.

---

## 13. Errores comunes

- Conectar mal los terminales del transistor.
- No usar resistencia de base en el BJT.
- Confundir colector y emisor.
- No colocar resistencia pull-down en la compuerta del MOSFET.
- Usar un MOSFET que no enciende correctamente con 5 V en la compuerta.
- No usar diodo de protección al controlar relés o motores.
- No calcular corriente ni potencia de la carga.

---

## 14. Preguntas orientadoras para clase

1. ¿Por qué un transistor permite controlar una carga con una señal pequeña?
2. ¿Qué diferencia existe entre controlar por corriente y controlar por voltaje?
3. ¿Qué significa que un BJT esté en corte?
4. ¿Qué significa que un BJT esté en saturación?
5. ¿Por qué un MOSFET no debe dejar la compuerta flotante?
6. ¿Qué transistor sería más conveniente para controlar una carga de mayor corriente?
7. ¿Por qué se utiliza un diodo en paralelo con cargas inductivas?

---

## 15. Trabajo independiente

El estudiante debe:

1. Revisar la Guía A02 sobre transistor BJT.
2. Revisar la Guía A03 sobre FET/MOSFET.
3. Simular un BJT controlando un LED.
4. Simular un MOSFET controlando una carga DC.
5. Comparar ambos circuitos en una tabla.
6. Prepararse para la evaluación del primer corte.

---

## 16. Relación con laboratorio

Este marco teórico se relaciona con:

- **Lab A02:** Transistor BJT como interruptor y amplificador básico.
- **Lab A03:** Transistor FET/MOSFET como dispositivo de control.

Por tiempo de corte, estas guías pueden manejarse como práctica orientada, simulación o trabajo complementario, manteniendo el énfasis en el análisis del transistor como dispositivo de control.
