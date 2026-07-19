# Marco teórico – Semana 03

# Transistor BJT como interruptor y controlador de cargas

## Propósito

Analizar el transistor BJT como dispositivo de conmutación y diseñar una etapa de control capaz de activar una carga de baja potencia a partir de una señal pequeña.

## Resultados de aprendizaje

- Identificar base, colector y emisor en un BJT a partir de su hoja de datos.
- Diferenciar transistores NPN y PNP.
- Reconocer las regiones de corte, activa y saturación.
- Calcular una resistencia de base para usar un BJT como interruptor.
- Seleccionar protección para una carga inductiva.
- Relacionar la etapa de control con el proyecto ABP.

## 1. El BJT como dispositivo de control

Un transistor bipolar de unión tiene tres terminales:

- **Base:** terminal de control.
- **Colector:** terminal asociado a la corriente de la carga.
- **Emisor:** terminal de referencia para la corriente principal.

En un BJT NPN, una corriente pequeña de base permite controlar una corriente mayor de colector. El pinout no es universal: debe consultarse la hoja de datos del componente exacto.

## 2. Regiones de operación

### Corte

La corriente de base es prácticamente cero y el transistor se comporta como un interruptor abierto. La carga permanece desactivada.

### Región activa

La corriente de colector depende aproximadamente de la corriente de base:

```text
IC ≈ β · IB
```

Esta región es útil en amplificación, pero β varía entre dispositivos y condiciones de operación.

### Saturación

El transistor está completamente activado para la carga disponible. El voltaje VCE(sat) suele ser pequeño y ya no se debe diseñar confiando solamente en β.

## 3. BJT NPN como interruptor de lado bajo

Una conexión típica ubica la carga entre VCC y el colector; el emisor se conecta a GND y la base recibe la señal de control por medio de una resistencia.

El diseño básico sigue estos pasos:

1. Determinar la corriente requerida por la carga.
2. Verificar que el transistor soporte corriente, tensión y potencia.
3. Escoger una beta forzada conservadora, por ejemplo 10.
4. Calcular la corriente de base.
5. Calcular la resistencia de base.

```text
IB = IC / βforzada
RB = (VIN - VBE) / IB
```

### Ejemplo

Una carga requiere 60 mA, la señal de control es 5 V y se usa βforzada = 10:

```text
IB = 60 mA / 10 = 6 mA
RB = (5 V - 0,7 V) / 6 mA ≈ 717 Ω
```

Puede seleccionarse 680 Ω o 750 Ω después de verificar la corriente disponible en la fuente de control.

## 4. Potencia y selección del dispositivo

En saturación:

```text
PBJT ≈ VCE(sat) · IC
```

También deben verificarse los límites IC máx., VCE máx. y potencia total. El hecho de que un transistor pueda conducir cierta corriente máxima no significa que pueda hacerlo sin considerar temperatura y disipación.

## 5. Cargas inductivas y diodo de protección

Cuando se interrumpe la corriente de una bobina, relé o motor aparece una tensión de polaridad opuesta que puede dañar el transistor. Un diodo conectado en antiparalelo con la carga proporciona una trayectoria segura para esa corriente transitoria.

En operación normal el diodo queda en inversa. Al apagar el BJT, conduce temporalmente y limita el pico de tensión.

## 6. Amplificación frente a conmutación

El BJT también puede operar en región activa como amplificador. Sin embargo, en el proyecto ABP el uso principal será la conmutación: estado desactivado en corte y estado activado en saturación.

Esta distinción evita confundir una etapa de control con un amplificador lineal.

## 7. Errores frecuentes

- Suponer el pinout sin consultar la hoja de datos.
- Conectar una carga sin compartir la referencia GND con la señal de control.
- Omitir la resistencia de base.
- Diseñar con β nominal sin margen para saturación.
- Omitir el diodo de protección en relés o motores.
- Exceder la corriente de salida del dispositivo que controla la base.
- Confundir VCE con VBE durante la medición.

## 8. Conexión con el Lab A02 y el ABP

El Lab A02 debe comprobar primero el BJT como interruptor para LED y luego una carga de baja potencia. La etapa de amplificación queda como profundización.

Dentro del proyecto, el BJT puede:

- Activar una alarma.
- Encender un indicador.
- Accionar un relé de baja tensión.
- Habilitar una carga cuando una condición lógica sea verdadera.

El grupo debe justificar corriente de carga, resistencia de base, protección y estado de operación.

## 9. Comprobación de aprendizaje

1. ¿Qué diferencia eléctrica existe entre corte y saturación?
2. ¿Por qué se usa una beta forzada para diseñar un interruptor?
3. ¿Qué ocurre si se elimina la resistencia de base?
4. ¿Qué función cumple el diodo conectado a un relé?
5. ¿Qué tres datos de la hoja de datos deben revisarse antes del montaje?

## Fuentes de consulta

- R. L. Boylestad y L. Nashelsky, *Teoría de circuitos y dispositivos electrónicos*.
- T. L. Floyd, *Dispositivos electrónicos*.
- Hoja de datos del BJT utilizado.
- All About Circuits, secciones de transistores BJT.

