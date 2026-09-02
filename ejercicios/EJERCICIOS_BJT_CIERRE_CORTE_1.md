# Ejercicios de cierre – Transistor BJT

**Asignatura:** Electrónica Analógica y Digital  
**Tema:** BJT como interruptor, corte, activa y saturación

Estos dos ejercicios están pensados para la clase de cierre del tema BJT.

- **Ejercicio 1:** resolución guiada con el docente.
- **Ejercicio 2:** resolución por estudiantes y sustentación en tablero.

---

# Ejercicio 1 – Guiado: activación de un relé de 5 V

Se desea accionar un relé de `5 V` utilizando un transistor NPN `2N2222` como interruptor de lado bajo.

Datos:

```text
VCC = 5 V
VIN = 5 V
Resistencia de la bobina = 250 Ω
VBE ≈ 0,7 V
VCE(sat) ≈ 0,2 V
β del transistor ≈ 100 en región activa
β forzado para diseño en saturación = 10
```

El relé es una carga inductiva y se conecta un diodo de protección en paralelo con su bobina.

## Preguntas

1. Con la entrada en `0 V`, indique:
   - región del transistor;
   - valor aproximado de `IB`;
   - valor aproximado de `IC`;
   - valor aproximado de `VCE`;
   - estado del relé.

2. Con la entrada activada, calcule la corriente máxima aproximada de colector suponiendo saturación.

3. Utilizando un `β forzado = 10`, determine la corriente de base necesaria para asegurar saturación.

4. Calcule la resistencia de base requerida.

5. Seleccione un valor comercial entre `1 kΩ`, `2,2 kΩ`, `4,7 kΩ` y `10 kΩ`.

6. Con el valor comercial seleccionado, calcule la corriente real aproximada de base.

7. Calcule el `β forzado` real:

```text
βforzado = IC / IB
```

8. Calcule la potencia aproximada disipada por el transistor en saturación:

```text
PT ≈ VCE(sat) · IC
```

9. Explique por qué en saturación no debe utilizarse simplemente `IC = β·IB` para afirmar que la corriente de colector seguirá aumentando.

10. Dibuje la orientación correcta del diodo de protección e indique:
    - dónde se conecta el cátodo;
    - dónde se conecta el ánodo;
    - qué ocurre cuando se abre el transistor.

11. Ahora sustituya temporalmente la resistencia de base por `100 kΩ`. Suponiendo `β = 100`, estime `IB` e `IC` y determine si el transistor podría alcanzar la corriente requerida por el relé.

---

# Ejercicio 2 – Para estudiantes: activación de una bobina de 9 V

Una bobina de un pequeño actuador trabaja con una fuente de `9 V` y tiene una resistencia de `180 Ω`. Se desea controlarla mediante un transistor NPN desde una señal de `5 V`.

Datos:

```text
VCC = 9 V
VIN = 5 V
Rbobina = 180 Ω
VBE ≈ 0,7 V
VCE(sat) ≈ 0,2 V
β del transistor ≈ 120 en región activa
β forzado recomendado = 10
```

## Actividad

El grupo debe resolver y una persona deberá sustentar el procedimiento en el tablero.

1. Dibuje el circuito completo con:
   - transistor NPN;
   - resistencia de base;
   - bobina;
   - diodo de protección;
   - tierras comunes.

2. Explique qué ocurre cuando `VIN = 0 V`.

3. Calcule la corriente aproximada de colector cuando el transistor está saturado.

4. Determine la corriente de base necesaria utilizando `β forzado = 10`.

5. Calcule `RB`.

6. Seleccione el valor comercial más conveniente entre:

```text
680 Ω
820 Ω
1 kΩ
2,2 kΩ
```

7. Con el valor seleccionado, vuelva a calcular `IB`.

8. Determine el `β forzado` real.

9. Calcule la potencia aproximada del transistor en saturación.

10. Indique los valores aproximados esperados de:

```text
VBE
VCE
```

11. Si se utilizara `RB = 100 kΩ`, estime la corriente de colector mediante `IC ≈ β·IB` y determine en qué región probablemente operaría el transistor.

12. Explique con sus palabras por qué el diodo de protección estudiado anteriormente vuelve a aparecer en este circuito.

---

## Fórmulas esenciales

```text
IB = (VIN - VBE) / RB
```

```text
IC ≈ β·IB            [región activa]
```

```text
IC(sat) ≈ (VCC - VCE(sat)) / Rcarga
```

```text
βforzado = IC / IB
```

```text
IE = IC + IB
```

```text
PT ≈ VCE · IC
```

---

## Pregunta de transición hacia MOSFET

Después de resolver ambos ejercicios, discutir:

> **Si para mantener encendido el BJT necesitamos suministrar corriente continuamente a la base, ¿existe un dispositivo capaz de controlar una carga principalmente mediante un voltaje de entrada y con una corriente de control mucho menor?**

Esta pregunta introduce el transistor MOSFET y permite comparar ambos dispositivos como interruptores electrónicos.
