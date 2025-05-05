# Block Diagram


![Block Diagram](./javascripts/block_diagram.png)

---


---

## Feedback

- Transitioned from using two UARTs for individual communication and MQTT server integration to a single UART to simplify the code and streamline communication.
- Incorporated additional switches to support more debugging features using LEDs. Originally, the setup included just one push button and one LED; the updated configuration allows for up to two LEDs and no more than three switches.
- Modified the daisy chain setup to meet updated requirements—specifically, using channel 2 for board-to-board communication, with pin 8 assigned to GND and pin 1 designated for Power (VIN).
- Adjusted the power input from 9V to 5V to accommodate a new power source.

---

## Decision Making Process

These improvements were driven by both the feedback I received and the opportunity to simplify the system using newer solutions. Removing the second UART eliminated unnecessary steps, making the programming process much more straightforward. With a single UART, I could manage communication with other boards and the MQTT server using one interface. I also enhanced the debugging process by adding more LEDs and push buttons, providing greater flexibility when testing message transmission and verifying whether messages were successfully sent, received, or failed.

