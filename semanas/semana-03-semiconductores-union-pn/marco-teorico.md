# Marco teórico – Semana 03

# Transistor BJT como interruptor y control de cargas

## 1. Propósito de la semana

Comprender el transistor BJT como dispositivo de control y aplicarlo a la activación segura de indicadores, relés o cargas DC de baja potencia dentro de la Fase 1 del proyecto ABPr.

## 2. Resultado de aprendizaje

Al finalizar la semana, el estudiante estará en capacidad de:

- Identificar terminales y tipos básicos de BJT.
- Diferenciar corte, región activa y saturación.
- Explicar por qué el BJT se considera controlado por corriente.
- Calcular una resistencia de base para operación como interruptor.
- Verificar corriente y potencia en la carga y en el transistor.
- Incorporar protección para cargas inductivas.
- Relacionar la etapa de control con la arquitectura del proyecto.

## 3. Conexión con la Fase 1 ABPr

La etapa AC/DC desarrollada en la Semana 02 entrega energía al circuito. El BJT permite que una señal pequeña controle una carga mayor:

```text
Etapa AC/DC
     ↓
Señal de control
     ↓
BJT como interruptor
     ↓
LED, relé o carga DC
```

## 4. Estructura del BJT

Un BJT posee tres terminales:

- **Base (B):** terminal de control.
- **Colector (C):** conduce la corriente principal hacia la carga en una configuración típica NPN.
- **Emisor (E):** referencia de salida de la corriente principal.

Tipos principales:

- **NPN:** el más usado como interruptor de baja conexión.
- **PNP:** puede emplearse para conmutación en el lado positivo.

## 5. Relaciones de corriente

En región activa:

```text
IC ≈ β × IB
IE = IC + IB
```

Sin embargo, cuando se usa como interruptor no debe confiarse únicamente en el valor nominal de β. Se fuerza la saturación usando una corriente de base suficiente.

## 6. Regiones de operación

### Corte

```text
IB ≈ 0
IC ≈ 0
```

El transistor se aproxima a un interruptor abierto y la carga permanece apagada.

### Región activa

La corriente de colector depende de la corriente de base. Se usa principalmente en amplificación.

### Saturación

El transistor conduce como interruptor cerrado. En un BJT de silicio pequeño:

```text
VCE(sat) ≈ 0.1 a 0.3 V
```

## 7. Resistencia de base

Para una señal de control `Vcontrol`:

```text
RB = (Vcontrol - VBE) / IB
```

Con una aproximación inicial:

```text
VBE ≈ 0.7 V
IB ≈ IC / βforzado
```

Un valor de `βforzado` entre 5 y 10 puede utilizarse como criterio introductorio para asegurar saturación, siempre verificando la hoja de datos y la capacidad de la fuente de control.

## 8. Verificación de potencia

La potencia aproximada en saturación es:

```text
PBJT ≈ VCE(sat) × IC
```

También deben verificarse:

- Corriente máxima de colector.
- Potencia máxima del encapsulado.
- Temperatura de operación.
- Corriente que puede entregar la señal de control.

## 9. Carga inductiva y diodo de protección

Un relé, solenoide o motor almacena energía en su campo magnético. Al interrumpir la corriente puede generar una sobretensión.

Se coloca un diodo en paralelo con la bobina y en polarización inversa durante la operación normal. Este diodo proporciona una ruta segura a la corriente cuando el transistor se apaga.

## 10. Ejemplo guiado

Se desea controlar una carga de 60 mA con una señal de 5 V.

Usando `βforzado = 10`:

```text
IB = 60 mA / 10 = 6 mA
RB = (5 V - 0.7 V) / 6 mA
RB ≈ 717 Ω
```

Se seleccionaría un valor comercial cercano, comprobando que la fuente de control pueda entregar esa corriente y que el transistor soporte la carga.

## 11. Actividad de clase y Lab A02

Cada grupo deberá:

1. Identificar el pinout del transistor seleccionado.
2. Diseñar la resistencia de base.
3. Simular estados de corte y saturación.
4. Medir `VBE`, `VCE` e `IC`.
5. Activar una carga segura de baja potencia.
6. Agregar diodo de protección si la carga es inductiva.
7. Explicar qué bloque del proyecto utilizaría esta etapa.

## 12. Evidencia ABPr

- Cálculo de la resistencia de base.
- Esquema y simulación.
- Mediciones o capturas.
- Hoja de datos consultada.
- Explicación del control de la carga.
- Actualización del diagrama de bloques del proyecto.

## 13. Errores comunes

- Confundir colector y emisor.
- Usar el BJT sin resistencia de base.
- Suponer que `IC = βIB` garantiza saturación.
- Superar la corriente de una salida lógica.
- Omitir el diodo en cargas inductivas.
- No compartir referencia GND entre control y potencia cuando corresponde.

## 14. Preguntas orientadoras

1. ¿Por qué el BJT se considera controlado por corriente?
2. ¿Qué diferencia existe entre región activa y saturación?
3. ¿Por qué se utiliza un β forzado?
4. ¿Qué ocurre si la resistencia de base es demasiado grande?
5. ¿Qué riesgo produce una bobina al desconectarse?
6. ¿Cómo se verifica que el transistor está saturado?

## 15. Trabajo independiente

- Completar el informe del Lab A02.
- Comparar cálculo, simulación y medición.
- Revisar la hoja de datos del BJT utilizado.
- Identificar una carga del proyecto que pueda ser controlada mediante transistor.
- Preparar una comparación preliminar entre BJT y MOSFET.

## 16. Conexión con la Semana 04

La siguiente semana se estudiará el MOSFET como alternativa de control eficiente de cargas y se cerrará técnicamente la Fase 1 del proyecto.