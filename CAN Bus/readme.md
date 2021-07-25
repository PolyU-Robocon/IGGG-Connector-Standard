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
The pinout follow the CANopen standard CiA-DS303-1
| Bus   | Pin | Cable Color    | Description | Note                   |
|-------|-----|----------------|-------------|------------------------|
| CAN 1 | 1   | Orange & White | CAN High    |                        |
| CAN 1 | 2   | Orange         | CAN Low     |                        |
| GND   | 3   | Green & White  | PGND        |                        |
| DC+   | 4   | Blue           | N.C         | use as VCC_H if needed |
| DC+   | 5   | Blue & White   | N.C         | use as VCC if needed   |
| GND   | 6   | Green          | Shield      | Optional               |
| Power | 7   | Brown & White  | PGND        |                        |
| Power | 8   | Brown          | (CAN_V+)    | Do not used this as V+ |
### Recommended Symbol and Connection
![image](https://user-images.githubusercontent.com/45313904/126659219-d5840bf2-c0bf-42d5-8317-7306908a9d56.png)

## CAN Bus to AMTSeries (IGGG-cAN-AMT102-V)
![AMT102](https://user-images.githubusercontent.com/77326918/126895644-7e0f812e-15d7-4f9d-a44f-4a4bb5efa7a7.png)
Connectors used: Molex 50-57-9405 Housing, Molex 16-02-0086 Terminals

## CAN Bus to VESC4 (IGGG-cAN-VESC4)
![image](https://user-images.githubusercontent.com/45313904/125818491-0afa460d-7039-48d4-ae44-395cdfbe156e.png)   
***Normally***, JST PH with 2.0mm pitch 4 pin Connector is used     
![image](https://user-images.githubusercontent.com/45313904/117435003-f0b3c800-af5f-11eb-9364-77ea9db8444c.png)
![image](https://user-images.githubusercontent.com/45313904/117435311-4c7e5100-af60-11eb-908c-285dd6f57c5d.png)
| Pin Number | Cable Color  | Twisted Pair | Signal   | Description             |
|------------|--------------|--------------|----------|-------------------------|
| 1          | Yellow(Red)  | Pair 1       | +5V DC   | 5VDC, up to you         |
| 2          | White(Brown) | Pair 2       | CAN High | CAN bus CAN high signal |
| 3          | Red(Blue)    | Pair 2       | CAN Low  | CAN bus CAN low signal  |
| 4          | Black(Black) | Pair 1       | GND      | GND, up to you          |

## Note: About CAN Bus Signal
![image](https://user-images.githubusercontent.com/45313904/117434119-da593c80-af5e-11eb-868e-ab50f1c3080a.png)
> In a low speed CAN ***each device*** should have a ***120 Ohm resistor***.    
> In a ***high speed*** CAN-Bus (>100Kbit, used in automotive) ***only each end of the main loop*** should have a ***120 Ohm resistor***
