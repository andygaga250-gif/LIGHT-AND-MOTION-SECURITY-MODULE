# LIGHT-AND-MOTION-SECURITY-MODULE
ESP32-WROOM-32-N4 SECURITY MODULE #1
Open
Open
ESP32-WROOM-32-N4 SECURITY MODULE
#1
@niyomugenga-123
Description
niyomugenga-123
opened 4 days ago · edited by niyomugenga-123
Owner

INTRODUCTION

A modular, manufacturable security system built around the ESP32-WROOM-32-N8 microcontroller. This project integrates motion sensing, ambient light detection, visual alerts, and serial debugging — all optimized for real-world PCB fabrication using EasyEDA

PROJECT OVERVIEW

This project is designed for hands-on electronics enthusiasts who want a compact, reliable, and customizable security module. It uses the ESP32-WROOM-32-N4 for its low power consumption, Wi-Fi/Bluetooth capabilities, and rich GPIO support. The system includes

    Motion detection via PIR sensor
    Light level monitoring via LDR
    Status indication via LEDs
    Serial debugging via UART header
    Clean power management via barrel jack and capacitors

FEATURES

🔹 Motion detection (GPIO33)
🔹 Light sensing (GPIO34 analog input)
🔹 Yellow and Red LED indicators (GPIO25, GPIO26)
🔹 Serial debug header (TXD0, RXD0, IO0, GND)
🔹 Power access header (5V, 3.3V, GND)
🔹 Optional LDR header for off-board mounting
🔹 Designed for EasyEDA and PCB fabrication

HARDWARE COMPONENTS

This project is built around the ESP32-WROOM-32-N4 microcontroller module, which serves as the brain of the system. Power is supplied through a standard DC barrel jack, delivering 5V to the board. To ensure stable operation, the circuit includes a 100µF capacitor for bulk filtering and two 0.1µF capacitors for decoupling — one near the power input and another close to the ESP32. Motion detection is handled by a PIR sensor connected via a 3-pin header, while ambient light sensing is achieved using an LDR configured in a voltage divider with a 10kΩ resistor. Visual feedback is provided by two LEDs — one yellow and one red — each paired with a 220Ω current-limiting resistor and connected to dedicated GPIO pins. For programming and debugging, a 4-pin serial header exposes TXD0, RXD0, IO0, and GND, compatible with USB-to-Serial adapters. Additional headers include a 4-pin power access header offering 5V, 3.3V, and dual GND lines, and an optional 2-pin header for off-board LDR placement. All components are chosen for ease of integration, manufacturability, and compatibility with EasyEDA’s PCB workflow

PIN MAPPING

The ESP32-WROOM-32-N4 module provides a rich set of GPIOs, and this project makes use of several key pins for sensor input, LED output, and serial communication. GPIO33 is connected to the PIR sensor’s output pin to detect motion events. GPIO34 is used as an analog input to read voltage from the LDR-based voltage divider, allowing ambient light sensing. GPIO25 and GPIO26 are configured as digital outputs to drive the yellow and red LEDs respectively, providing visual status indicators. For serial debugging and firmware flashing, TXD0 and RXD0 are connected to a 4-pin header alongside IO0 and GND — this setup allows easy interfacing with USB-to-Serial adapters. The IO0 pin is essential for entering boot mode during flashing. Power is supplied to the ESP32 via its 3.3V pin, and multiple GND pins are tied to the common ground rail. All connections are routed cleanly and labeled clearly in the schematic to ensure easy replication and reliable operation

PCB DESIGN NOTES

    Use ESP32-WROOM-32-N8 footprint with all 38 pins exposed
    Route power and ground rails cleanly across the board
    Place capacitors close to power entry and ESP32 pins
    Label all headers clearly for silkscreen printing
    Group related components (e.g., PIR + header, LEDs + resistors) for layout clarity
    Use wide traces for power lines (≥0.5mm)

THE SCHEMATIC
Image

SETUP INSTRUCTION

To begin using the ESP32-WROOM-32-N8 Security Module, first connect a regulated 5V DC power supply to the barrel jack input. Ensure that the onboard capacitors are correctly placed to stabilize the voltage rails. For firmware flashing and serial debugging, connect a USB-to-Serial adapter to the 4-pin debug header — matching TXD0 to RX, RXD0 to TX, and GND to GND. Hold the IO0 pin low during power-up to enter boot mode, which allows firmware upload via tools like or the Arduino IDE. Once flashed, the ESP32 will automatically boot into your program. The PIR sensor will trigger motion detection on GPIO33, while the LDR voltage divider feeds analog light readings into GPIO34. The yellow and red LEDs connected to GPIO25 and GPIO26 can be used to indicate system status or alerts. You can monitor serial output through your adapter to verify sensor readings and debug logic. All headers are labeled clearly in the schematic to simplify wiring and testing during setup

THE PCB LAYOUT OF ESP32-WROOM-32-N4 AND SENSORS BOARD
Image

FINAL BOARD OF LIGHT AND MOTION SECURITY MODULE
Image Image

CONCLUSION

The development of a light and motion-based security module using EasyEDA marks a significant step toward practical, manufacturable electronics design. This project successfully integrates sensor technology with real-time responsiveness, offering a compact and efficient solution for motion-triggered lighting and security alerts.
By leveraging EasyEDA’s schematic capture and PCB layout tools, the design process was streamlined—from component selection and circuit simulation to mounting hole placement and enclosure compatibility. The inclusion of motion sensors (e.g., PIR) and light control logic demonstrates a thoughtful balance between functionality and simplicity, ideal for both indoor and outdoor applications.
Beyond the technical execution, this project reflects a deeper understanding of modular design, mechanical integration, and documentation best practices. It’s not just a working prototype—it’s a deployable, scalable solution ready for real-world use and open-source sharing.
