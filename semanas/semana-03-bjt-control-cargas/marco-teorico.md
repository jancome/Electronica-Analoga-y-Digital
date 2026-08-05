# Marco teórico – Semana 03

# Transistor BJT como interruptor y control de cargas

## Metas de aprendizaje verificables

- Distinguir corte, región activa y saturación mediante corrientes y tensiones medidas.
- Dimensionar base, potencia y protección de una carga DC con margen y hoja de datos.
- Localizar fallas de control, pinout y carga sin sustituir componentes al azar.

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

## 17. Profundización: conmutación BJT con margen de diseño

El BJT contiene dos uniones PN y cumple `I_E=I_C+I_B`. En región activa suele emplearse `I_C≈βI_B`, pero `β` varía entre unidades, con corriente y temperatura. Al usarlo como interruptor se fuerza saturación con una relación conservadora `β_forzada=I_C/I_B`, frecuentemente entre 5 y 10 para cargas didácticas, dentro de la capacidad de la fuente de mando.

\[
I_B=\frac{V_{ctrl}-V_{BE}}{R_B},\qquad R_B=\frac{V_{ctrl}-V_{BE}}{I_B}
\]

\[
P_Q\approx V_{CE(sat)}I_C,\qquad P_R=I_B^2R_B
\]

La salida lógica o sensor debe poder entregar `I_B`; de lo contrario, un cálculo correcto en papel sobrecarga el bloque anterior.

## 18. Ejemplo guiado adaptado

Se controla una bobina de `5 V`, `60 mA` con una señal de `3,3 V` usando un NPN de lado bajo.

1. Con `β_forzada=10`, `I_B=6 mA`.
2. Con `V_BE≈0,8 V`, `R_B=(3,3-0,8)/6 mA=417 Ω`; se elige un valor comercial y se verifica la corriente.
3. Si `V_CE(sat)=0,2 V`, `P_Q≈12 mW`.
4. Se conecta un diodo de rueda libre: cátodo a `+5 V`, ánodo al colector.

Al abrir el BJT, el diodo proporciona trayectoria a la corriente almacenada en `E=½LI²` y limita la sobretensión. Las masas de control y potencia deben compartir referencia cuando no hay aislamiento.

## 19. Simulación, montaje y mediciones del Lab A02

1. Confirmar pinout y límites `VCEO`, `IC` y `PD` en la hoja de datos.
2. Simular corte y saturación, midiendo `VB`, `VE`, `VC`, `VBE`, `VCE` e `IC`.
3. Validar primero con LED/resistencia.
4. Montar con alimentación desconectada y comprobar continuidad de tierra.
5. Energizar con límite de corriente si está disponible.
6. Un `VCE` intermedio puede indicar base insuficiente y región activa.
7. Conectar al final la bobina y el diodo de protección.

## 20. Diagnóstico de fallas

| Medición | Interpretación probable |
|---|---|
| `VBE≈0 V` con orden de encendido | no llega control, base abierta o tierras separadas |
| `VBE≈0,7–0,9 V`, `VCE` alto | pinout incorrecto, carga abierta o base insuficiente |
| `VCE≈0,1–0,3 V`, carga apagada | problema en carga, alimentación o cableado de salida |
| transistor caliente | corriente excesiva, región activa o componente subdimensionado |
| ruido al apagar relé | diodo ausente, invertido o retorno deficiente |

## 21. Preguntas orientadoras y trabajo independiente

- ¿Por qué `β` típico no garantiza saturación?
- ¿Puede la salida de mando suministrar la corriente de base?
- ¿Cuál es el peor caso de potencia y temperatura?
- ¿Qué distingue una carga abierta de un transistor en corte?
- ¿Cómo cambia el diseño si la carga es inductiva?

El grupo entregará un diseño BJT propio con hoja de datos, cálculo de `R_B`, potencia, tabla de estados, simulación, seis mediciones esperadas y diagnóstico de una falla segura provocada.

## 22. Referencias de estudio

- Boylestad y Nashelsky, 10.ª ed., cap. 3, secs. 3.2–3.11, pp. 132–153: construcción, operación, límites, hoja de datos y prueba del BJT.
- Ibid., cap. 4, secs. 4.2 y 4.11, pp. 162 y 194: punto de operación y diseño.
- Ibid., cap. 4, secs. 4.15–4.18, pp. 206–228: conmutación, solución de fallas y aplicaciones.

## 23. Ruta de profundización recomendada

1. **Estructura y operación:** Boylestad, cap. 3, secs. 3.2–3.6, pp. 132–145.
2. **Selección real:** cap. 3, secs. 3.8–3.11, pp. 146–153, para límites, hoja de datos, prueba y terminales.
3. **Diseño de conmutación:** cap. 4, secs. 4.2, 4.11 y 4.15, pp. 162, 194 y 206 en adelante.
4. **Profundización aplicada:** cap. 4, secs. 4.16 y 4.18, pp. 210–228, para diagnóstico y aplicaciones.
