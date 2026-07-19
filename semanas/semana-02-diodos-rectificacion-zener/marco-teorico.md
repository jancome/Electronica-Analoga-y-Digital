# Marco teórico – Semana 02

# Semiconductores, diodos, rectificación y regulación básica

## Propósito

Comprender cómo la unión PN da origen al comportamiento del diodo y aplicar ese comportamiento en una etapa de conversión AC/DC de baja tensión con rectificación, filtrado, indicador LED y regulación básica.

## Resultados de aprendizaje

Al finalizar la semana, el estudiante estará en capacidad de:

- Diferenciar conductor, aislante y semiconductor.
- Explicar el efecto de la polarización directa e inversa en una unión PN.
- Analizar circuitos sencillos con diodos usando Ley de Ohm y leyes de Kirchhoff.
- Reconocer las etapas de rectificación, filtrado y regulación de una fuente DC básica.
- Calcular una resistencia limitadora para LED y verificar la potencia disipada.
- Identificar las mediciones necesarias para validar la etapa analógica del proyecto ABP.

## 1. Del material semiconductor al diodo

Los materiales semiconductores, como el silicio, tienen una conductividad intermedia entre los conductores y los aislantes. Su comportamiento puede modificarse mediante dopaje:

- El material tipo **N** tiene electrones disponibles como portadores mayoritarios.
- El material tipo **P** tiene huecos como portadores mayoritarios.

Cuando ambos materiales se unen aparece una **región de agotamiento** y una barrera interna de potencial. Esta unión PN es la base del diodo.

![Unión PN y polarización del diodo](../../recursos/imagenes/analogica/diodo-union-pn-polarizacion.svg)

## 2. Polarización directa e inversa

En polarización directa, el ánodo se conecta hacia el potencial positivo y el cátodo hacia el potencial negativo. La barrera disminuye y el diodo conduce cuando se alcanza una tensión suficiente. Para un diodo de silicio se usa frecuentemente un modelo práctico con una caída aproximada de 0,7 V.

En polarización inversa, la barrera aumenta y la corriente es muy pequeña mientras no se alcance la tensión de ruptura. Por eso un diodo rectificador común no debe operar deliberadamente en ruptura.

El diodo es un elemento no lineal. No puede tratarse como una resistencia fija, pero una vez elegido un modelo se puede analizar el resto del circuito con Ley de Ohm y Kirchhoff.

### Ejemplo: corriente en un diodo

Para una fuente de 5 V, una resistencia de 1 kΩ y un diodo de silicio en conducción:

```text
I = (VS - VD) / R
I = (5 V - 0,7 V) / 1 kΩ
I = 4,3 mA
```

La potencia aproximada en la resistencia es:

```text
PR = I²R ≈ 18,5 mW
```

## 3. LED y resistencia limitadora

Un LED emite luz al conducir en polarización directa. Su caída de voltaje depende del color y de la tecnología. Nunca debe conectarse directamente a una fuente sin limitar la corriente.

```text
R = (VS - VLED) / ILED
```

Si VS = 5 V, VLED = 2 V e ILED = 10 mA:

```text
R = (5 V - 2 V) / 0,01 A = 300 Ω
```

Se selecciona un valor comercial igual o superior, por ejemplo 330 Ω.

## 4. Rectificación de corriente alterna

Una señal AC cambia de polaridad. Los equipos electrónicos requieren normalmente una tensión DC estable, por lo que una fuente básica puede organizarse así:

```text
AC de baja tensión → rectificación → filtrado → regulación → carga
```

![Rectificación y filtrado](../../recursos/imagenes/analogica/rectificacion-y-filtrado.svg)

### Rectificador de media onda

Utiliza un diodo y aprovecha un solo semiciclo de la señal. La salida es DC pulsante y presenta una separación amplia entre pulsos.

### Puente rectificador

Utiliza cuatro diodos y aprovecha ambos semiciclos. En cada trayectoria conducen dos diodos, por lo que el valor pico de salida se aproxima mediante:

```text
Vp(salida) ≈ Vp(entrada) - 2VD
```

Para una señal senoidal:

```text
Vp = VRMS · √2
```

## 5. Filtrado capacitivo

El capacitor se carga cerca del valor pico y entrega energía a la carga cuando el voltaje rectificado disminuye. La salida conserva una variación llamada rizado.

Una aproximación útil es:

```text
Vr(pp) ≈ IL / (fr · C)
```

donde IL es la corriente de carga, fr la frecuencia del rizado y C la capacitancia. Un capacitor mayor reduce el rizado, pero también puede aumentar la corriente de carga inicial.

## 6. Regulación con diodo Zener

El Zener se diseña para trabajar en ruptura inversa controlada. En un regulador sencillo se conecta en paralelo con la carga y se usa una resistencia serie para limitar corriente.

```text
RS = (VS - VZ) / (IZ + IL)
```

También debe verificarse la potencia:

```text
PZ = VZ · IZ
```

El Zener no crea energía ni reemplaza una fuente bien dimensionada. Su función es ayudar a mantener una tensión cercana a VZ dentro de un rango de corriente y potencia permitido.

## 7. Ejemplo integrado

Se dispone de 6 V RMS de baja tensión AC y un puente rectificador de silicio.

```text
Vp = 6 V · √2 ≈ 8,49 V
Vp(salida) ≈ 8,49 V - 1,4 V ≈ 7,09 V
```

Después del filtro, el valor DC sin carga estará cerca de ese máximo. Al conectar una carga aparecerá rizado y el valor medio disminuirá. Si se desea una salida regulada cercana a 5,1 V, se debe seleccionar el Zener y calcular la resistencia serie para la corriente esperada.

## 8. Errores frecuentes

- Confundir ánodo y cátodo.
- Usar el valor RMS como si fuera el valor pico.
- Olvidar las dos caídas de diodo en un puente.
- Conectar un capacitor electrolítico con polaridad invertida.
- Conectar un LED sin resistencia limitadora.
- Elegir un Zener sin revisar corriente y potencia.
- Medir corriente colocando el multímetro en paralelo.
- Conectar el protoboard directamente a la red eléctrica.

## 9. Conexión con el laboratorio y el ABP

El Lab A01 valida esta cadena mediante simulación, montaje y mediciones. Para el Preproyecto ABP 1, cada grupo debe registrar como mínimo:

- Tensión AC de entrada en baja tensión.
- Forma o valor de la señal rectificada.
- Tensión después del filtro.
- Tensión regulada.
- Corriente aproximada de carga.
- Protección e indicador seleccionados.
- Diferencia entre valores calculados, simulados y medidos.

## 10. Comprobación de aprendizaje

1. ¿Por qué el puente rectificador utiliza dos caídas de diodo por semiciclo?
2. ¿Qué ocurre con el rizado cuando aumenta la corriente de carga?
3. ¿Por qué un LED necesita resistencia limitadora?
4. ¿Qué potencia debe soportar un Zener de 5,1 V que conduce 20 mA?
5. ¿Qué medición demostraría que el filtro está funcionando?

## Fuentes de consulta

- R. L. Boylestad y L. Nashelsky, *Teoría de circuitos y dispositivos electrónicos*.
- T. L. Floyd, *Dispositivos electrónicos*.
- Hojas de datos del diodo, LED y Zener empleados.
- All About Circuits, secciones de diodos y rectificadores.

