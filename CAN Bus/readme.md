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
### IGGG-cAN-RJ45 Types

#### Type A Devices(IGGG-cAN-RJ45-A)
(follows CiA-DS303-1)   
pin 8 as VCC(V+/5V). `However if user on99 like ... will gg`   

#### Type B Devices(IGGG-cAN-RJ45-B)
(follows IGGG Recommended Connection)   
pin 5 as VCC(5V)

#### Type C Devices(IGGG-cAN-RJ45-C)
User can manual switch between Tpye A and Tpye B through button or programe 

#### Type D Devices(IGGG-cAN-RJ45-D)
The system will automatic switch between Tpye A and Tpye B   
(Optional) allow user to switch to type C

## CAN Bus to VESC4 (IGGG-cAN-VESC4)(Added in altium lib)
![image](https://user-images.githubusercontent.com/45313904/125818491-0afa460d-7039-48d4-ae44-395cdfbe156e.png)   
***Normally***, JST PH with 2.0mm pitch 4 pin Connector is used     
![image](https://user-images.githubusercontent.com/45313904/117435003-f0b3c800-af5f-11eb-9364-77ea9db8444c.png)
![image](https://user-images.githubusercontent.com/45313904/117435311-4c7e5100-af60-11eb-908c-285dd6f57c5d.png)
| Pin Number | Cable Color  | Twisted Pair | Signal   | Description             |
|------------|--------------|--------------|----------|-------------------------|
| 4          | Yellow(Red)  | Pair 1       | +5V DC   | 5VDC, up to you         |
| 3          | White(Brown) | Pair 2       | CAN High | CAN bus CAN high signal |
| 2          | Red(Blue)    | Pair 2       | CAN Low  | CAN bus CAN low signal  |
| 1          | Black(Black) | Pair 1       | GND      | GND, up to you          |

## J17 4-Pin Optional CAN Header Pin (IGGG-cAN-NX-J17)
![image](https://user-images.githubusercontent.com/45313904/128248179-b5db5266-6994-408d-86f9-42214377a33e.png)   
4-Pin 2.54 Pitch
| Bus   | Pin | Pin Name | Module Pin | Description      | Note        |
|-------|-----|----------|------------|------------------|-------------|
| CAN   | 1   | CAN_TX   | 145        | CAN High         | 3.3V Output |
| CAN   | 2   | Orange   | 143        | CAN Low          | 3.3V Input  |
| Power | 3   | GND      | -          | Ground           | Ground      |
| Power | 4   | 3.3V     | -          | Main 3.3V supply | Power       |

[More About NX Pinout](https://github.com/PolyU-Robocon/IGGG-Connector-Standard/blob/main/Jetson/Xavier-NX/readme.md)

## Note: About CAN Bus Signal
![image](https://user-images.githubusercontent.com/45313904/117434119-da593c80-af5e-11eb-868e-ab50f1c3080a.png)
> In a low speed CAN ***each device*** should have a ***120 Ohm resistor***.    
> In a ***high speed*** CAN-Bus (>100Kbit, used in automotive) ***only each end of the main loop*** should have a ***120 Ohm resistor***    

## Note: Reference Circuit
![image](https://user-images.githubusercontent.com/45313904/131254961-2da84e7d-f47b-4d25-b13d-1445185df906.png)
> The common mode choke can be added to reduce common mode noise.   
> Approved for 500 kbit/s:    
> TDK ACT45C-101-2P-TL000, ACT1210-101-2P-TL00    
> Approved for up to 5 Mbit/s:    
> TDK ACT1210R-101-2P, ACT45B-101-2P-TL003, ACT45B-101-2P-TL002 Epcos B82789-C0104-N002, B82789-C0104-N001, B82789-C0104-H052, B82789-C0104-H002, B82789-C0104-H001   

## Note: CANopen
![image](https://user-images.githubusercontent.com/45313904/189868579-113a2414-ff0f-4b1b-9e17-adbfb045f985.png)
![image](https://user-images.githubusercontent.com/45313904/189869109-1805f1de-746f-4baf-85a7-e09780b4f417.png)
### Dataframe of CANopen
![image](https://user-images.githubusercontent.com/45313904/189872375-f94f6e41-804a-47bd-bf6f-805a6f9db065.png)

### CANopen Communication Model 
3 Type:
* Master-Slave
* Server-Client
* Productor-Consumer
#### Master-Slave
![image](https://user-images.githubusercontent.com/45313904/189870135-8b798703-80e9-4314-8bfa-806043f59b80.png)  
Number of Slave 0 to 127    
Note1: Node id 0 is reserved for master  
Note2: Max Node id is `127` (0x7F)  
#### Server-Client
![image](https://user-images.githubusercontent.com/45313904/189871148-77b96950-12e3-442a-9cb1-35682edc1ce6.png)   
CLient send a data request to server    
Server reply with data requested    
#### Productor-Consumer
![image](https://user-images.githubusercontent.com/45313904/189871475-ff9a7a25-85ea-4900-b0fe-215fd34ca28a.png)  
### Ferther Readering on the CANopen
[CANopen Explained - A Simple Intro (2020)](https://www.youtube.com/watch?v=DlbkWryzJqg)


