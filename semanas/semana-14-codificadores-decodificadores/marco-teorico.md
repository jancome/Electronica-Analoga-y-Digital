# Marco teórico – Semana 14

# Codificadores y decodificadores

## 1. Tema de la semana

Circuitos combinacionales de codificación y decodificación aplicados a representación de información digital.

## 2. Objetivo de aprendizaje

Comprender cómo los codificadores convierten información de entrada en códigos binarios y cómo los decodificadores convierten códigos binarios en salidas específicas o visualización.

## 3. Contexto

Los sistemas digitales necesitan representar datos de forma eficiente. Los codificadores y decodificadores permiten transformar señales entre diferentes formatos, por ejemplo de decimal a BCD o de BCD a display de 7 segmentos.

## 4. Codificador

Un codificador convierte varias entradas activas en un código binario de salida.

Ejemplo: un codificador decimal a BCD convierte una entrada decimal del 0 al 9 en su equivalente BCD de 4 bits.

## 5. Codificador con prioridad

Cuando más de una entrada está activa, el codificador con prioridad selecciona la entrada de mayor prioridad y entrega su código correspondiente.

## 6. Decodificador

Un decodificador realiza el proceso contrario: recibe un código binario y activa una salida específica.

Ejemplo: un decodificador 2 a 4 tiene 2 entradas y 4 salidas posibles.

## 7. BCD y display de 7 segmentos

BCD significa decimal codificado en binario. Cada dígito decimal se representa con 4 bits.

Un decodificador BCD a 7 segmentos convierte el código BCD en señales que encienden los segmentos necesarios para formar un número.

## 8. Ejemplo guiado

El número decimal 5 en BCD se representa como:

```text
5 = 0101
```

Un decodificador BCD a 7 segmentos usa ese código para encender los segmentos correspondientes al número 5.

## 9. Errores comunes

- Confundir codificador con decodificador.
- No identificar si las salidas son activas en alto o activas en bajo.
- Conectar un display sin resistencias limitadoras.
- Confundir BCD con binario puro.
- No revisar si el display es ánodo común o cátodo común.

## 10. Preguntas orientadoras

1. ¿Qué diferencia hay entre codificar y decodificar?
2. ¿Qué significa BCD?
3. ¿Por qué un display necesita resistencias?
4. ¿Qué implica que una salida sea activa en bajo?
5. ¿Qué ventaja tiene un codificador con prioridad?

## 11. Trabajo independiente

Diseñar o simular un decodificador BCD a 7 segmentos y completar la tabla de visualización de los dígitos 0 al 9.
