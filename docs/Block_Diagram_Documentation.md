# Block Diagram

This block diagram represents the architecture and signal flow for the ESP32-based system with MQTT server integration and peripheral components.

---

## System Overview

The system utilizes an **ESP32 WiFi Module** to handle communication and control between peripherals and a remote MQTT server. It supports interaction with a **mobile device** using WiFi or BLE.

### Key Components:

- **ESP32 WiFi Module**
  - Transmit: RX1 (IO18)
  - Receive: TX1 (IO17)
  - UART:
    - RX0: IO43
    - TX0: IO44
  - GPIOs:
    - GPIO6: Connected to LED
    - GPIO38: Connected to Push Button

- **Power Supply**
  - 6V Power Jack (Outlet)
  - 3.3V Switch Regulator to power ESP32

- **Connectivity**
  - **WiFi (Wireless)** to MQTT ASU Server
  - **BLE/WiFi** connection to Phone/Mobile Device
  - Connector IN & OUT via 2x4 Header (Digital-Serial UART, 2 Pins)

---

## Communication Flow

```text
Phone/Mobile Device
        ⇅ (BLE/WiFi)
     MQTT ASU Server
        ⇅ (WiFi)
      ESP32 WiFi Module
        ↔ Peripherals (LED, Push Button)
        ↔ UART IN/OUT via 2x4 Header
```

---

## Diagram Summary

The ESP32 module acts as the central controller, interfacing with the MQTT server wirelessly and handling local inputs/outputs via GPIO and UART. The 3.3V regulated power ensures safe operation of the ESP32 and peripherals.

