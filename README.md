# Medidor Ambiental de Luz y Sonido con Arduino

Este proyecto consiste en un sistema basado en **Arduino UNO** que permite **medir la intensidad de luz y el nivel de ruido en un ambiente**. A través de un botón pulsador, el usuario puede seleccionar qué desea medir. La información se muestra en una **pantalla LCD** y el modo activo se indica mediante **LEDs**. Este proyecto fue diseñado para aplicar conceptos de **control de entradas/salidas**, **detección de flancos**, **control lógico por tiempo**, y una **máquina de estados simple**.

---

## 🎯 Objetivo

El sistema permite alternar entre dos modos:

### 🔊 Modo Ruido
- Detecta la presencia de **ruidos fuertes** mediante una entrada **digital** de un sensor de sonido.
- Muestra en la pantalla LCD si hay **"Mucho ruido"** o **"No hay ruido"**.
- La medición es **lógica** (presencia/ausencia).

### 💡 Modo Luz
- Mide la **intensidad lumínica** usando una **fotoresistencia (LDR)** conectada a una entrada **analógica**.
- Informa en la pantalla si hay:
  - `Mucha luz`
  - `Luz media`
  - `Luz tenue`
- La medición es **analógica**, permitiendo una lectura más precisa.

El cambio de modo se realiza presionando un botón, y un LED se enciende para indicar el modo actual:
- LED rojo: Modo luz.
- LED verde: Modo sonido.

---

## 🧩 Componentes utilizados

- 1x Arduino UNO
- 1x Pantalla LCD 16x2 con módulo I2C
- 1x Fotoresistencia (LDR) 
- 1x Microfono Sensor de sonido (salida analógica y digital)
- 1x Pulsador (botón)
- 2x LEDs (rojo y verde)
- 5x Resistencias para LEDs, boton, sensores.
- Protoboard y cables

---

## ⚙️ Funcionalidades del Código

### ✅ Control de Entradas y Salidas
- Manejo de sensores (LDR y micrófono)
- Lectura de un botón
- Encendido de LEDs
- Salida por LCD y puerto serial

### ✅ Contador de Flancos
- Se detecta el **flanco de subida** del botón para alternar entre modos.

### ✅ Control Lógico por Tiempo
- Se usa `millis()` para evitar rebotes del botón.
- Se aplican `delay()` para temporizar mensajes en el LCD.

### ✅ Máquina de Estados
- Una variable `modo` define el estado actual del sistema:
  - `modo = 1`: medir luz
  - `modo = 0`: medir sonido

---

## 🚀 Cómo usar el proyecto

1. **Subí el código al Arduino UNO.**
2. **Conectá el circuito según el esquema del proyecto.**
3. **Abrí el Monitor Serial para ver los datos en bruto (opcional).**
4. **Presioná el botón para alternar entre los modos.**
5. **Observá el LED y la pantalla LCD para saber qué estás midiendo.**

---

## 📸 Esquema basico 

![image](https://github.com/user-attachments/assets/d83cccd1-526b-4bd5-8dd4-2c80e683669f)


---

## ✍️ Autores
Proyecto realizado por Leandro Rios, Misael Sirni, Sol Ottaviani. 

