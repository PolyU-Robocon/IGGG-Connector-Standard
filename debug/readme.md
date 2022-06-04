# SOIC-8 test clip
![image](https://user-images.githubusercontent.com/45313904/171992125-9104fd70-3131-49ef-a711-b0801f5d5dc5.png)
Based on [Simon Merrett](https://github.com/SimonMerrett/SOICbite)'s work
| Pin | UART | SPI       | SWIM | SWD   | ESP8266 | USB | I2C | PIC ICSP |
| --- | ---  | ---       | ---  | ---   | ---     | --- | --- | ---      |
| 1   | Vcc  | Vcc       | Vcc  | Vcc   | Vcc     | Vcc | Vcc | Vcc      |
| 2   | RX2  | CS        |      |       | GPIO0   | D-  |     | Vpp      |
| 3   | TX2  |           |      |       | GPIO2   | D+  |     |          |
| 4   | GND  | GND       | GND  | GND   | GND     | GND | GND | GND      |
| 5   | RX   | MOSI/MOMI | SWIM | SWDIO | RX      |     | SDA | DAT      |
| 6   | TX   | MISO      |      | SWO   | TX      |     |     | AUX      |
| 7   | CTS  | SCK/CLK   |      | SWCLK | CH_PD   |     | SCL | CLK      |
| 8   | RTS  | RST       | NRST | NRST  | RST     | ID  |     |          |
