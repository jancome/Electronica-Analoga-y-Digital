# Marco teórico – Semana 05

# Diodo Zener, LED y regulación básica

## 1. Tema de la semana

Aplicación de diodos especiales en circuitos electrónicos: LED como indicador luminoso y diodo Zener como regulador básico de voltaje.

![Unión PN y polarización del diodo](../../recursos/imagenes/analogica/diodo-union-pn-polarizacion.svg)

---

## 2. Objetivo de aprendizaje

Diseñar y analizar circuitos básicos con LED y diodo Zener, calculando resistencias limitadoras de corriente, condiciones de operación y potencia disipada en los componentes.

---

## 3. Contexto e importancia del tema

Los diodos no solo se utilizan para rectificar señales. También existen aplicaciones muy comunes como la indicación luminosa y la regulación básica de voltaje.

El LED es un diodo diseñado para emitir luz cuando conduce corriente. Se utiliza en indicadores, displays, iluminación, señalización, optoacopladores y sistemas de diagnóstico.

El diodo Zener se diseña para trabajar en polarización inversa dentro de una zona de ruptura controlada. Esta característica permite mantener un voltaje aproximadamente constante en sus terminales, por lo que se puede utilizar como regulador o referencia de voltaje.

---

## 4. LED

LED significa **Light Emitting Diode**, o diodo emisor de luz. Es un dispositivo semiconductor que emite luz cuando se polariza directamente.

Tiene dos terminales:

- Ánodo.
- Cátodo.

Cuando se conecta correctamente y circula corriente, el LED enciende. Si se conecta invertido, no conduce de forma normal y permanece apagado.

---

## 5. Caída de voltaje en un LED

La caída de voltaje de un LED depende del color y del material semiconductor. Valores típicos aproximados:

| Color del LED | Voltaje directo aproximado |
|---|---:|
| Rojo | 1.8 V a 2.2 V |
| Amarillo | 2.0 V a 2.4 V |
| Verde | 2.0 V a 3.0 V |
| Azul | 3.0 V a 3.5 V |
| Blanco | 3.0 V a 3.5 V |

Estos valores son aproximados. Siempre se debe consultar la hoja de datos del componente.

---

## 6. Resistencia limitadora para LED

Un LED no debe conectarse directamente a una fuente de voltaje, porque podría circular una corriente excesiva y dañarse.

Por eso se utiliza una resistencia en serie para limitar la corriente.

La resistencia se calcula con:

```text
R = (VS - VLED) / ILED
```

Donde:

- VS es el voltaje de la fuente.
- VLED es el voltaje directo del LED.
- ILED es la corriente deseada.

### Ejemplo

Se desea conectar un LED rojo a una fuente de 5 V. Se asume:

```text
VLED = 2 V
ILED = 10 mA
```

Entonces:

```text
R = (5 V - 2 V) / 0.01 A
R = 300 Ω
```

Se puede usar una resistencia comercial de 330 Ω.

---

## 7. Potencia en la resistencia

Además de calcular la resistencia, se debe verificar su potencia.

```text
P = I² × R
```

Para el ejemplo anterior:

```text
P = (0.01 A)² × 330 Ω
P = 0.033 W
```

Una resistencia de 1/4 W sería suficiente.

---

## 8. Diodo Zener

El diodo Zener es un diodo diseñado para operar en polarización inversa dentro de una región de ruptura controlada.

En esa región, mantiene un voltaje aproximadamente constante llamado **voltaje Zener**.

Por ejemplo, un Zener de 5.1 V intenta mantener en sus terminales un voltaje cercano a 5.1 V cuando está correctamente polarizado.

---

## 9. Regulador básico con Zener

Un regulador básico con Zener se construye con:

- Una fuente de entrada.
- Una resistencia serie.
- Un diodo Zener conectado en paralelo con la carga.
- Una resistencia de carga.

La resistencia serie es indispensable porque limita la corriente que llega al Zener y a la carga.

Si se elimina la resistencia serie, el Zener puede dañarse por exceso de corriente.

---

## 10. Condiciones de operación del Zener

Para que el Zener regule correctamente:

- Debe estar conectado en polarización inversa.
- El voltaje de entrada debe ser mayor que el voltaje Zener.
- Debe circular una corriente mínima por el Zener.
- No debe superarse la potencia máxima del dispositivo.

La potencia aproximada en el Zener se calcula como:

```text
PZ = VZ × IZ
```

---

## 11. Regulación de voltaje

Regular voltaje significa mantener una salida relativamente constante aunque cambie la entrada o la carga dentro de ciertos límites.

El regulador con Zener es simple, económico y útil para corrientes pequeñas. Sin embargo, no es el regulador más eficiente ni el más preciso para cargas grandes.

Para aplicaciones más exigentes se utilizan reguladores integrados, fuentes conmutadas o reguladores lineales dedicados.

---

## 12. Aplicaciones reales

### Aplicaciones del LED

- Indicadores de encendido.
- Señalización.
- Displays.
- Iluminación.
- Optoacopladores.
- Sistemas de alarma.
- Diagnóstico visual en tarjetas electrónicas.

### Aplicaciones del Zener

- Referencias de voltaje.
- Reguladores simples.
- Protección contra sobretensiones.
- Limitadores de voltaje.
- Etapas de polarización.
- Protección de entradas electrónicas.

---

## 13. Ejemplo guiado con Zener

Se tiene una fuente de 12 V, un Zener de 5.1 V y una resistencia serie de 470 Ω. Se desea estimar la corriente que circula por la resistencia si no se considera inicialmente la carga:

```text
IR = (VS - VZ) / R
IR = (12 V - 5.1 V) / 470 Ω
IR = 6.9 V / 470 Ω
IR ≈ 14.7 mA
```

Luego debe verificarse que la potencia del Zener no supere su valor máximo:

```text
PZ = VZ × IZ
```

---

## 14. Errores comunes

- Conectar un LED sin resistencia limitadora.
- Confundir ánodo y cátodo del LED.
- Suponer que todos los LED tienen el mismo voltaje directo.
- Conectar el Zener en directa cuando se desea regular.
- Eliminar la resistencia serie del Zener.
- No calcular la potencia disipada.
- Usar un Zener con potencia insuficiente.

---

## 15. Preguntas orientadoras para clase

1. ¿Por qué un LED necesita resistencia limitadora?
2. ¿Por qué el color del LED afecta su voltaje directo?
3. ¿Qué diferencia existe entre un diodo rectificador y un LED?
4. ¿Qué significa que el Zener trabaje en ruptura controlada?
5. ¿Por qué el Zener se conecta en polarización inversa para regular?
6. ¿Qué puede pasar si se elimina la resistencia serie del Zener?
7. ¿Qué limitaciones tiene un regulador Zener?

---

## 16. Trabajo independiente

Antes del cierre del primer corte, el estudiante debe:

1. Calcular resistencias para LED usando fuentes de 5 V, 9 V y 12 V.
2. Simular un regulador Zener de 5.1 V.
3. Medir o estimar corriente y potencia en el Zener.
4. Finalizar el informe del laboratorio A01.
5. Preparar dudas sobre diodos, LED, rectificación y regulación.

---

## 17. Relación con laboratorio

Este marco teórico sirve como base para la parte final de la **Guía A01 – Diodos, rectificación y regulación con Zener**, especialmente en los circuitos de LED con resistencia limitadora y regulador básico con diodo Zener.
