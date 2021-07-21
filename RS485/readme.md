# RJ45 Cable Harness
Please refer to this pinout   
**Do NOT use Crossover Cable**    
And we use RJ45 type B   
![image](https://user-images.githubusercontent.com/45313904/118519762-fbded300-b76b-11eb-9715-fc2743117bc4.png)
# [Proposed]RS 485(TIA-485) over RJ45 Verison 2 (IGGG-RS485-RJ45v2)
Default Buad Rate is assume to be 9600, otherwise please state it cleary and do documenation.    
![image](https://user-images.githubusercontent.com/45313904/126560117-48932c1a-aabe-4eb3-ab85-afe01431de24.png)
| Bus     | Pin | Cable Color    | Description            |
|---------|-----|----------------|------------------------|
| RS485_1 | 1   | Orange & White | RS-486 B               |
| RS485_1 | 2   | Orange         | RS-485 A               |
| GPIO    | 3   | Green & White  | GPIO Pin 0             |
| DC+     | 4   | Blue           | VCC_H(24~12VDC)        |
| DC+     | 5   | Blue & White   | VCC(reference to PGND) |
| GPIO    | 6   | Green          | GPIO Pin 1             |
| DC-     | 7   | Brown & White  | PGND                   |
| DC-     | 8   | Brown          | PGND                   |


# RS 485(EIA/TIA-485) over RJ45 Verison 1 (IGGG-RS485-RJ45v1)
![image](https://user-images.githubusercontent.com/45313904/126550070-70b3bf4f-532e-41e7-ba6e-ddbfa7954b3f.png)   
Default Buad Rate is assume to be 9600, otherwise please state it cleary and do documenation.    

# Extra: PoE(Power over Ethernet)
![image](https://user-images.githubusercontent.com/45313904/126553040-92a75e42-a123-4fd3-9dae-53db8f5f21a2.png)
`Devices that are powered with 24 volt PoE always use Mode B. That’s just the way it is.`
