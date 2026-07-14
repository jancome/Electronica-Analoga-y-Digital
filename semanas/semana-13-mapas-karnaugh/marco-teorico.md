# Marco teórico – Semana 13

# Comparadores y paridad

## 1. Tema de la semana

Circuitos combinacionales para comparación de números binarios y detección básica de errores mediante paridad.

---

## 2. Objetivo de aprendizaje

Interpretar el funcionamiento de comparadores y circuitos de paridad, relacionándolos con aplicaciones de verificación, control y comunicación digital.

---

## 3. Comparadores

Un comparador digital permite determinar la relación entre dos números binarios A y B.

Sus salidas típicas son:

```text
A > B
A = B
A < B
```

---

## 4. Comparador de igualdad

Para dos bits, A y B son iguales cuando ambos valen 0 o ambos valen 1. Esta función puede implementarse con XNOR.

```text
A = B  →  A XNOR B
```

---

## 5. Comparador de magnitud

Un comparador de magnitud analiza cuál número es mayor. Para varios bits, se comparan primero los bits de mayor peso.

---

## 6. Paridad

La paridad agrega un bit adicional para verificar errores simples en una transmisión o almacenamiento digital.

- **Paridad par:** el número total de unos debe ser par.
- **Paridad impar:** el número total de unos debe ser impar.

---

## 7. Aplicaciones

- Comunicación serial.
- Memorias.
- Teclados.
- Sistemas de diagnóstico.
- Verificación básica de datos.
- Comparación de valores en control digital.

---

## 8. Errores comunes

- Confundir comparación de igualdad con comparación de magnitud.
- No considerar el peso de los bits.
- Confundir paridad par e impar.
- Creer que la paridad detecta todos los errores.

---

## 9. Preguntas orientadoras

1. ¿Qué diferencia hay entre A=B y A>B?
2. ¿Por qué se comparan primero los bits más significativos?
3. ¿Qué es un bit de paridad?
4. ¿Qué errores puede detectar la paridad?
5. ¿Qué limitaciones tiene un sistema basado solo en paridad?

---

## 10. Trabajo independiente

Completar el Lab 06 con tablas de comparación y tablas de paridad.
