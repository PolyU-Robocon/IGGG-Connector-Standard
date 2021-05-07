# IGGG Standard for CAN BUS

## CAN BUS using Molex (IGGG-cAN-molex4p)
molex micro fit 3.0 is used.

![image](https://user-images.githubusercontent.com/45313904/114553290-11a63780-9c98-11eb-8e19-0a1c612a5f47.png)
| Pin Number | Cable Color | Twisted Pair   | Signal   | Description                                                             |
|------------|-------------|----------------|----------|-------------------------------------------------------------------------|
| 1          | Yellow      | Pair 1         | CAN High | CAN bus CAN high signal                                                 |
| 2          | Green       | Pair 1         | CAN Low  | CAN bus CAN low signal                                                  |
| 3          | Brown       | Doesn't Matter | CAN GND  | GND, normally does not connect to Devices  (unless start/ end of chain) |
| 4          | Shield      | Doesn't Matter | Shield   | Shield, Really up to you                                                |
## CAN Bus using RJ45 (IGGG-cAN-RJ45)
> Please follow the pinout! -- Leung, M.(2021)  


![image](https://user-images.githubusercontent.com/45313904/114553589-60ec6800-9c98-11eb-8ad2-a7183560f8a5.png)

## Note: About CAN Bus Signal
![image](https://user-images.githubusercontent.com/45313904/117434119-da593c80-af5e-11eb-868e-ab50f1c3080a.png)
> In a low speed CAN ***each device*** should have a ***120 Ohm resistor***.    
> In a ***high speed*** CAN-Bus (>100Kbit, used in automotive) ***only each end of the main loop*** should have a ***120 Ohm resistor***
