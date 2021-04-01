# NFC_Scan_Auth
This program builds on my previous authorizer to pwer two small 5V solenoids. My idea behind this is to create a small locking box with a battery to power the components when in use.
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

##### Putting it all together...
The MFRC522 must be connected to the Nano is a specific way to function. Certain parameters can be changed within the program itself but for my purposes, I have listed the connecting pins below.
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
