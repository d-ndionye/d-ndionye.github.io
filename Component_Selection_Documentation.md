# Component Selection

This section provides a comparison of available components for the ESP32-based system, along with the rationale behind the selected parts.

---

## Table1. ESP32

| Solution | Pros | Cons |
|----------|------|------|
| **Option 1 - ESP32-S3-WROOM-1**  <br> Price: $2.95 <br> *Link* | - Easily Programmable with MPLAB XIDE <br> - Numerous GPIO pins for multiple uses <br> - High Data Rate 150Mbps | - Most Expensive <br> - Soldering Difficulty <br> - Fixed 2.4GHz Frequency |
| **Option 2 - ESP32-C3FH4** <br> Price: $1.30 <br> *Link* | - Cheaper Price <br> - Frequency Range: 2.402GHz–2.48GHz <br> - Supports Bluetooth V5.0 | - No ADC Pins <br> - Lowest Data Rate 54Mbps <br> - No Antenna Type Included |
| **Option 3 - ESP32-C3-MINI-1** <br> Price: $1.80 <br> *Link* | - Cheaper Price <br> - Programmable with MPLAB XIDE <br> - High Data Rate 150Mbps | - Difficult Surface Mount <br> - Not for new designs <br> - Difficult to program |

**Choice:** Option 1  
**Rationale:** Selected for familiarity, largest number of GPIO and UART pins necessary for handling internet communication.

---

## Table2. Voltage Regulator

| Solution | Pros | Cons |
|----------|------|------|
| **Option 1 - LM3671MF-3.3/NOPB** <br> Price: $1.56 <br> *Link* | - Fixed 3.3V output <br> - Good for step-down function <br> - Dependable for high voltage | - Max input 5.5V <br> - High temperature <br> - One output |
| **Option 2 - TLV61048DBVR** <br> Price: $0.63 <br> *Link* | - Lowest frequency <br> - Durable switching <br> - Lowest cost | - Adjustable output <br> - High current 3.7A <br> - Higher cost |
| **Option 3 - TPS62082DSGR** <br> Price: $1.55 <br> *Link* | - Fixed 3.3V <br> - 6V input <br> - 1.2A output | - Difficult soldering <br> - 8 pins make it hard to manage <br> - Higher cost |

**Choice:** Option 1  
**Rationale:** Easiest to solder, low current (600mA), and fixed 3.3V output avoids risk of overvoltage.

---

## Table3. Push Button

| Solution | Pros | Cons |
|----------|------|------|
| **Option 1 - PTS636SM43SMTR LFS** <br> Price: $0.18 <br> *Link* | - Fixed to OFF-MOM <br> - Inexpensive and bulk-buyable <br> - Easy to solder | - Long delivery time <br> - Non-illuminating <br> - Small package |
| **Option 2 - FSM2JMTR** <br> Price: $0.37 <br> *Link* | - Fixed to OFF-MOM <br> - Durable switching <br> - Inexpensive in bulk | - Long delivery time <br> - Undersoldering issues <br> - Smallest size |
| **Option 3** <br> Price: Not listed <br> *Link* | - OFF-MOM fixed <br> - Inexpensive <br> - Decent button size | - Long delivery time <br> - Non-illuminating <br> - Small package |

---

## Table4. ESP32 Model

| ESP Info | Answer | Help |
|----------|--------|------|
| Model | ESP32-S3-WROOM-1-N4 | Include full part number |
| Product Page URL | *Main Product Page* | Espressif.com |
| ESP32-S3-WROOM-1-N4 Datasheet | *Datasheet* | Use a link |
| ESP32 S3 Datasheet | *Datasheet* | Detailed functions |
| ESP32 S3 Technical Reference | *Manual* | I/O, USB, etc. |
| Vendor Link | *Vendor:Digikey* | Use vendor link |
| Code Examples | *LED & Button Code-GitHub* | GitHub/library resources |
| External Resources | *LED & Button ESP32* | YouTube/Google for specifics |
| Unit Cost | $2.95 | Vendor or parts site |
| Absolute Max Current (IC) | 50nA | Datasheet |
| Supply Voltage Range | 3.0–3.6V | Datasheet |
| Max GPIO Current (per pin) | 50nA | Datasheet |
| Supports External Interrupts | Yes | Datasheet |
| Programming Hardware | MPLAB XIDE, School Provided | Datasheet |

