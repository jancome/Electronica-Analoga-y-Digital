# Marco teórico – Semana 05

# Cierre analógico: BJT y FET/MOSFET

## 1. Tema de la semana

Transistores BJT y FET/MOSFET como dispositivos de control dentro de circuitos electrónicos analógicos básicos.

![Comparación BJT vs MOSFET](../../recursos/imagenes/analogica/bjt-vs-mosfet-interruptor.svg)

---

## 2. Objetivo de aprendizaje

Analizar el funcionamiento básico de los transistores BJT y MOSFET como interruptores electrónicos, identificando sus terminales, variables de control, regiones de operación y aplicaciones en cargas de baja potencia.

---

## 3. Contexto e importancia

Los transistores son dispositivos fundamentales en electrónica. Permiten controlar corrientes mayores a partir de señales pequeñas, por lo que se utilizan en automatización, tarjetas electrónicas, control de motores, fuentes, sensores, relés, amplificadores y sistemas digitales.

En este curso se estudian como cierre de la unidad analógica, porque permiten conectar los conceptos de semiconductores, diodos, polarización, corriente y potencia con aplicaciones reales de control.

---

## 4. Conceptos fundamentales

### BJT

El transistor BJT tiene tres terminales:

- **Base:** terminal de control.
- **Colector:** terminal por donde entra la corriente principal en un NPN.
- **Emisor:** terminal por donde sale la corriente principal.

En un BJT, una pequeña corriente de base puede controlar una corriente mayor entre colector y emisor.

### MOSFET

El MOSFET tiene tres terminales principales:

- **Gate:** compuerta de control.
- **Drain:** drenador.
- **Source:** fuente.

En un MOSFET, el control se realiza principalmente por voltaje entre Gate y Source.

---

## 5. BJT como interruptor

Cuando el BJT se usa como interruptor, se trabaja principalmente en dos estados:

- **Corte:** no circula corriente significativa entre colector y emisor. La carga está apagada.
- **Saturación:** el transistor conduce completamente. La carga está encendida.

Una aplicación típica es activar un LED, un relé o una carga DC usando una señal de control pequeña.

---

## 6. MOSFET como interruptor

El MOSFET canal N puede utilizarse como interruptor de baja conexión, ubicándolo entre la carga y tierra. Cuando el voltaje Gate-Source es suficiente, el MOSFET conduce y permite el paso de corriente por la carga.

Una ventaja del MOSFET es su alta impedancia de entrada. Esto significa que requiere muy poca corriente de control comparado con un BJT.

---

## 7. Comparación BJT vs MOSFET

| Característica | BJT | MOSFET |
|---|---|---|
| Variable de control | Corriente de base | Voltaje Gate-Source |
| Terminal de control | Base | Gate |
| Conducción | Colector-emisor | Drain-source |
| Uso típico | Cargas pequeñas y medianas | Control eficiente de cargas DC |
| Cuidado principal | Corriente de base adecuada | Voltaje de compuerta y descarga del Gate |

---

## 8. Aplicaciones reales

- Activación de relés.
- Control de motores DC.
- Manejo de tiras LED.
- Salidas de microcontroladores.
- Tarjetas de control de portones, alarmas y automatismos.
- Etapas de potencia de bajo voltaje.

---

## 9. Ejemplo guiado

Se desea activar un LED con un BJT NPN usando una señal de 5 V. Se coloca el LED con resistencia en el colector y el emisor a tierra.

Para que el transistor actúe como interruptor, debe circular corriente suficiente por la base. Por eso se coloca una resistencia de base entre la señal de control y la base.

La idea principal es:

```text
Señal de control activa → corriente de base → transistor en saturación → carga encendida
```

```text
Señal de control inactiva → no hay corriente de base → transistor en corte → carga apagada
```

---

## 10. Errores comunes

- Conectar mal los terminales del transistor.
- No usar resistencia de base en el BJT.
- No colocar resistencia pull-down en el Gate del MOSFET cuando se requiere apagado seguro.
- Olvidar el diodo de protección en cargas inductivas como relés o motores.
- Superar la corriente máxima del transistor.
- No revisar la hoja de datos.

---

## 11. Preguntas orientadoras

1. ¿Por qué el BJT se considera controlado por corriente?
2. ¿Por qué el MOSFET se considera controlado por voltaje?
3. ¿Qué diferencia existe entre corte y saturación?
4. ¿Por qué una carga inductiva requiere diodo de protección?
5. ¿En qué casos conviene usar MOSFET en lugar de BJT?

---

## 12. Trabajo independiente

- Revisar las guías A02 y A03.
- Simular un BJT activando un LED.
- Simular un MOSFET controlando una carga DC.
- Comparar corrientes, voltajes y potencia en ambos casos.
- Preparar preguntas para el cierre del primer corte.