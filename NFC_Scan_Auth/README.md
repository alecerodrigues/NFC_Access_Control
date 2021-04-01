# NFC_Scan_Auth
This program is designed to be a simple authorizer that also outputs a scanned cards UID to the monitor. Line 44 can be changed to any UID(s) that match a scannable to allow authorization. This program can be expanded upon for other implemenations and I utilize it as a shell for future programs. 
##### Parts List
- MFRC522: An integrated reader/writer IC for contactless communcication.
  - Operaterating frequency: 13.56 MHZ
  - Reading Capailities: NFC or RFID
![image](https://user-images.githubusercontent.com/57117759/113363113-04935b00-931e-11eb-8209-d7345604023a.png)

- Arduino Nano: Multi I/O microcontroller
  - Chipset: ATmega328
![image](https://user-images.githubusercontent.com/57117759/113363200-43c1ac00-931e-11eb-98c0-326f7fe39d33.png)

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
