#  AI Voice Gender Classification on STM32

##  Project Overview

This project implements a **real-time voice gender classification system** (male/female) on an **STM32 Nucleo-L476RG** microcontroller using an **I²S digital microphone (INMP441)**. Audio is captured through the STM32 SAI peripheral and processed using a lightweight neural network deployed with **STM32Cube.AI**.

---

##  Hardware Used

* STM32 Nucleo-L476RG
* INMP441 I²S Digital Microphone
* USB (UART for serial monitoring)
* Jumper wires

---

##  Pin Connections (SAI2)

| Microphone Pin | STM32 Pin | Function   |
| -------------- | --------- | ---------- |
| SD             | PC12      | SAI2_SD_B  |
| SCK            | PC10      | SAI2_SCK_B |
| WS / FS        | PA15      | SAI2_FS_B  |
| VDD            | 3.3V      | Power      |
| GND            | GND       | Ground     |

---

##  Software & Tools

* STM32CubeMX
* STM32CubeIDE
* STM32Cube.AI
* TensorFlow / Keras (model training)
* C / Embedded C
* UART Serial Monitor

---

##  System Workflow

1. Capture audio data using **SAI2 with DMA**.
2. Preprocess audio samples for inference.
3. Run the trained **CNN model** on the STM32.
4. Output classification result (male/female) via **UART**.

---

##  Features

* Real-time audio acquisition using I²S
* On-device AI inference (no cloud required)
* Optimized neural network for low memory usage
* Serial output for easy debugging and monitoring

---

##  Output Example

```
Voice detected: Male
Confidence: 92%
```

---

## Repository Structure

```
/Model        -> Trained AI model files
/Core         -> STM32 application source code
/Drivers      -> STM32 HAL drivers
/Docs         -> Project documentation
```

---

##  License

This project is for **educational and research purposes**.

---

##  Acknowledgements

* STMicroelectronics
* STM32Cube.AI Documentation
* Open-source ML community

