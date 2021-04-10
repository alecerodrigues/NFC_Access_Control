# NFC_Scan_Auth
This program builds on my previous authorizer to power two small 5V solenoids. My idea behind this is to create a small locking box with a battery to power the components when in use.
##### Parts List
- MFRC522: An integrated reader/writer IC for contactless communcication.
  - Operaterating frequency: 13.56 MHZ
  - Reading Capailities: NFC or RFID
![image](https://user-images.githubusercontent.com/57117759/113363113-04935b00-931e-11eb-8209-d7345604023a.png)

- Arduino Nano: Multi I/O microcontroller
  - Chipset: ATmega328
![image](https://user-images.githubusercontent.com/57117759/113363200-43c1ac00-931e-11eb-98c0-326f7fe39d33.png)

- Mini Push-Pull Solenoid:
  - Voltage: 5V
  - Current: 1.1A
  - DC Resistance: 4.5 ± 5% Ω
  - Throw (at DC 5V): 3mm / 80g
  - Lead Length: ~57mm / 2.2"
  - Weight: 12.6g
![image](https://user-images.githubusercontent.com/57117759/113364221-f266ec00-9320-11eb-8548-b1edb1c70be1.png)

- N-Channel MOSFET:
  - *IRLB8721*
    - Max Voltage: 30V
    - Max Current: 62A
    - Gate Threshold: 2.35V
  - 5V logic compatible
  - ![image](https://user-images.githubusercontent.com/57117759/113364799-6ce43b80-9322-11eb-811e-701f3ec89640.png)

- Rectifier Diode:
  - *1N4004*
    - Max Voltage: 400V
    - Forward Current: 1A
    - Max Current: 30A
  - ![image](https://user-images.githubusercontent.com/57117759/113364974-e419cf80-9322-11eb-94e2-5bcb42ddb802.png)


##### Putting it all together...
The MFRC522 and the two solenoids must be connected to the Nano is a specific way to function. Certain parameters can be changed within the program itself but for my purposes, I have listed the connecting pins below.
| MFRC522 | Arduino Nano |
| --- | --- |
| SDA | D10 |
| SCK | D13 |
| MOSI | D11 |
| MISO | D12 |
| IRQ | D9 |
| GND | GND |
| RST | (NONE) |
| 3.3V | 3V3 |

| Solenoids | Arduino Nano |
| --- | --- |
| (1) 5V | D3 |
| (2) 5V | D4 |

The solenoids also produce a current kickback when operating so it is critical to utilise a mosfet and a diode on each solenoid in order to ensure the operating safety of the solenoids. A example diagram of how to be setup one of the solenoids can be seen below, adding more solenoids is as simple as repeating this circuit and connecting it to the appropriate voltage, I/O, and GND pins: 
![image](https://user-images.githubusercontent.com/57117759/114279125-0be2f480-9a01-11eb-944b-5ce990d0414c.png)

##### Alpha Build
![](https://raw.githubusercontent.com/alecerodrigues/NFC_Access_Control/main/NFC_Scan_Auth_DualSol/assets/Alpha.gif)


