# U2A3_MLP_TURTLE_JeanAcosta.pdf

## Descripción
Este proyecto implementa un **perceptrón multicapa (MLP)** para controlar un robot diferencial tipo **Zumo/Turtle** en **Proteus**, utilizando sensores de línea como entradas y dos salidas para controlar la velocidad de los motores.

El objetivo es que el robot pueda **seguir una línea de forma autónoma** mediante la inferencia de una red neuronal implementada directamente en **Arduino**.

---

## Objetivo
Desarrollar e implementar un modelo de red neuronal MLP que permita al robot:

- Detectar la posición de la línea.
- Procesar las lecturas de sensores.
- Generar velocidades para el motor izquierdo y derecho.
- Seguir la trayectoria en simulación.

---

## Tecnologías utilizadas
- **Arduino IDE**
- **Proteus 8 Professional**
- **Python (NumPy)** para entrenamiento del MLP
- **Librería ZumoShield**
- **GitHub** para control de versiones

---

## Estructura del modelo
El modelo implementado tiene la siguiente arquitectura:

- **Capa de entrada:** 3 neuronas  
  - Izquierda
  - Centro
  - Derecha

- **Capa oculta:** 6 neuronas

- **Capa de salida:** 2 neuronas  
  - Velocidad motor izquierdo
  - Velocidad motor derecho

Se utilizó la función de activación **tanh** en la capa oculta y en la capa de salida.

---

## Funcionamiento general
1. El robot lee los sensores de línea.
2. Las lecturas se agrupan en tres entradas principales:
   - Izquierda
   - Centro
   - Derecha
3. Estas entradas se introducen al modelo MLP.
4. El MLP calcula dos salidas:
   - `yL`
   - `yR`
5. Las salidas se escalan para controlar la velocidad de los motores mediante `motors.setSpeeds()`.

---

## Archivos principales
- `README.md`  
  Descripción general del proyecto.

---

## Resultados esperados
- El robot sigue la línea en la simulación.
- El modelo responde a cambios en la posición de la línea.
- Se valida el comportamiento del MLP mediante evidencia visual y terminal serial.

## enlace del video en google drive.
https://drive.google.com/drive/folders/1_VbwxrSnOR1rYuvLzb8nAcCe5vmAC6JM?usp=sharing
---

## Referencias
- Pololu Corporation. (s.f.). *Zumo Shield Arduino Library* [Repositorio de software]. GitHub. https://github.com/pololu/zumo-shield-arduino-library
- Arduino. (s.f.). *Arduino documentation*. https://www.arduino.cc/reference/en/
- Goodfellow, I., Bengio, Y., & Courville, A. (2016). *Deep Learning*. MIT Press.

---

## Autor
- Jean Paul Acosta Navarro
  
Alejandra Garcia

Proyecto académico realizado para la implementación de un seguidor de línea con red neuronal MLP en Arduino y Proteus.
