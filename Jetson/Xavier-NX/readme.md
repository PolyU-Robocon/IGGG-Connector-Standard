# NVIDIA Jetson Xavier NX GPIO Header Pinout
![image](https://user-images.githubusercontent.com/45313904/128246783-f8190494-cebc-41b1-9a55-3fa5eef4fbba.png)     
## J12 40-Pin Expansion Header
![image](https://user-images.githubusercontent.com/45313904/128247129-15d85bf7-f577-4f83-ac1d-f25347479ef7.png)     
Major Function
* I2S
* Audio Clock
* I2C (x2)
* SPI (x2)
* UART
* GPIOs   

According Nvidia,   
* `All the signals on the Expansion Header use 3.3V levels.`
* `All the interface signal pins (I2S, I2C, SPI, UART and Audio clock) can also be configured as GPIOs`
* `Any pull-up or pull-down resistors on the signals (except I2C) must be weak (limited to >50kΩ).`
## J17 4-Pin Optional CAN Header Pin
![image](https://user-images.githubusercontent.com/45313904/128248179-b5db5266-6994-408d-86f9-42214377a33e.png)   
4-Pin 2.54 Pitch
| Bus   | Pin | Pin Name | Module Pin | Description      | Note        |
|-------|-----|----------|------------|------------------|-------------|
| CAN   | 1   | CAN_TX   | 145        | CAN High         | 3.3V Output |
| CAN   | 2   | Orange   | 143        | CAN Low          | 3.3V Input  |
| Power | 3   | GND      | -          | Ground           | Ground      |
| Power | 4   | 3.3V     | -          | Main 3.3V supply | Power       |
