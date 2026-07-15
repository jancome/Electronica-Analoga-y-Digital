# Quiz 1 – Unidad analógica

**Corte:** 1  
**Semana de aplicación:** Semana 04, al inicio de la clase  
**Peso:** 2% de la nota final  
**Modalidad:** individual  
**Tiempo sugerido:** 20 a 25 minutos  

## Indicaciones para el estudiante

- Responda con letra clara y ordenada.
- Justifique los cálculos cuando la pregunta lo solicite.
- Use unidades en todas las respuestas numéricas.
- No se permite el uso de celular durante el quiz, salvo autorización del docente.
- El quiz evalúa conceptos vistos antes de iniciar el tema de FET/MOSFET.

---

## Parte A – Conceptos básicos

### 1. Voltaje, corriente y resistencia

Explique brevemente la diferencia entre voltaje, corriente y resistencia.

**Valor:** 0.4 puntos

---

### 2. Ley de Ohm

Una resistencia de **1 kΩ** se conecta a una fuente de **5 V DC**.

Calcule la corriente que circula por la resistencia.

**Valor:** 0.5 puntos

---

### 3. Señal analógica y señal digital

Indique una diferencia entre una señal analógica y una señal digital. Dé un ejemplo de cada una.

**Valor:** 0.5 puntos

---

## Parte B – Diodos, LED y Zener

### 4. Diodo en polarización directa

Explique qué ocurre con un diodo de silicio cuando se conecta en polarización directa.

**Valor:** 0.5 puntos

---

### 5. LED con resistencia limitadora

Se desea encender un LED rojo con una fuente de **9 V**. El LED tiene una caída aproximada de **2 V** y se desea una corriente de **10 mA**.

Calcule el valor de la resistencia limitadora.

**Valor:** 0.8 puntos

---

### 6. Diodo Zener

Explique para qué se utiliza un diodo Zener en un circuito básico de regulación.

**Valor:** 0.5 puntos

---

## Parte C – Rectificación y BJT

### 7. Rectificación

¿Qué función cumple un rectificador en una fuente de alimentación?

**Valor:** 0.4 puntos

---

### 8. BJT como interruptor

En un transistor BJT NPN usado como interruptor, indique qué función cumple cada terminal:

- Base.
- Colector.
- Emisor.

**Valor:** 0.6 puntos

---

### 9. Resistencia de base

Explique por qué no se debe conectar la base de un BJT directamente a la fuente de control sin una resistencia.

**Valor:** 0.4 puntos

---

### 10. Aplicación

Mencione una aplicación real donde se pueda usar un BJT como interruptor en ingeniería eléctrica o electrónica.

**Valor:** 0.4 puntos

---

## Total

**5.0 puntos**

---

# Rúbrica de calificación

| Criterio | Peso |
|---|---:|
| Manejo conceptual | 40% |
| Cálculos y unidades | 30% |
| Claridad de explicación | 20% |
| Orden y presentación | 10% |

---

# Versión con respuestas orientadoras para el docente

> Esta sección es de apoyo docente. Puede retirarse antes de entregar el quiz a los estudiantes.

## Respuestas esperadas

1. El voltaje es diferencia de potencial, la corriente es flujo de carga y la resistencia se opone al paso de corriente.
2. `I = V/R = 5 V / 1000 Ω = 0.005 A = 5 mA`.
3. Una señal analógica varía de forma continua; una digital trabaja con niveles discretos. Ejemplos: temperatura medida por sensor, señal lógica 0/1.
4. El diodo conduce cuando el ánodo está a mayor potencial que el cátodo y supera su caída directa aproximada.
5. `R = (9 V - 2 V) / 0.01 A = 700 Ω`. Valor comercial cercano: 680 Ω o 750 Ω, verificando corriente.
6. El Zener se usa para mantener un voltaje aproximadamente constante cuando trabaja en ruptura inversa controlada.
7. Convierte una señal AC en una señal DC pulsante.
8. Base: controla el transistor; colector: terminal por donde entra la corriente de la carga; emisor: terminal de salida hacia referencia en configuración NPN de lado bajo.
9. Porque la unión base-emisor puede dañarse por exceso de corriente; se requiere resistencia limitadora.
10. Activación de relé, LED indicador, carga DC pequeña, etapa de control, alarma o interfaz con microcontrolador.
