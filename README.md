# LDR Sensor Interface using ADC on STM32F411RE

## Overview
This project demonstrates interfacing an **LDR (Light Dependent Resistor)** sensor with the **STM32F411RE** microcontroller using its **Analog-to-Digital Converter (ADC)**. The setup captures ambient light intensity by converting the analog signal from the LDR into a digital value, which can be used for various applications such as light monitoring or automation.

---

## Features
- Real-time ambient light measurement using an LDR sensor.
- Precise ADC configuration for 12-bit resolution.
- Display of processed data via a serial terminal.
- Implementation of STM32 HAL drivers for efficient embedded development.

---

## Components Required
- **STM32F411RE Nucleo Board**
- **LDR Sensor**
- **10 kΩ Resistor** (pull-down resistor)
- Breadboard and connecting wires

---

## Circuit Description
- The LDR is part of a voltage divider circuit. Its resistance changes with ambient light intensity.
- Connect one terminal of the LDR to **VCC (3.3V)**.
- Connect the other terminal to **PA0 (ADC Pin)** and to a **10 kΩ pull-down resistor** tied to GND.
- The variable voltage from the divider is fed into the ADC pin.

---

## Configuration
### ADC Settings:
- **Resolution:** 12-bit
- **Sampling Time:** Adjusted for precision and speed
- **Channel:** ADC Channel 0 (PA0)
- **Mode:** Single or continuous conversion

---

## How It Works
1. The LDR’s resistance changes with light intensity, altering the voltage in the divider circuit.
2. The STM32F411RE’s ADC reads this voltage and converts it into a digital value.
3. The digital value is processed and displayed on a serial terminal.

---

## Instructions to Run
1. Clone this repository to your local machine.
2. Open the project in **STM32CubeIDE**.
3. Connect the STM32F411RE to your PC via USB.
4. Build and flash the code onto the microcontroller.
5. Open a serial terminal (e.g., PuTTY, Tera Term) to view the output.

---

## Applications
- Light-based automation systems
- Ambient light intensity measurement
- Low-power light monitoring solutions

---

## Future Enhancements
- Add an OLED or LCD for real-time feedback.
- Implement low-power modes for energy-efficient operation.
- Enhance calibration for improved measurement accuracy.

---

## License
This project is open-source and available under the MIT License. Feel free to use and modify it as needed.

---

## Contributing
Contributions are welcome! Feel free to create a pull request or open an issue if you have suggestions or improvements.
