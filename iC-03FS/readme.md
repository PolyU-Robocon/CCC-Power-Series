# Already know problem
![image](https://user-images.githubusercontent.com/45313904/125517875-9afa547b-215a-413a-990e-f7d29ad9743c.png)
![image](https://user-images.githubusercontent.com/45313904/125517952-787a0210-2693-45ae-826c-b8cbf81313c5.png)

* SGND PGND what a messh(really no time to properly place them, wiat next ver. la)
* during bad emf, cannot turn off
* 12V power no protection
* 24V power naive protection
* polyu robocon gg
* CCC on999
* EIE become IAI


# iC-03FS Waff
![image](https://user-images.githubusercontent.com/45313904/120550068-f8fc0780-c426-11eb-9721-47f47f4ea195.png)
## Feature
 * Power 
    * [XT60 Source](#XT60-Source) x16
    * [XT60 Uninterrupted Source](#XT60-Uninterrupted-Source) x3
    * [IO-link Power(24V)](#io-link-power24v) X1
 * Auxiliary 
    * [12V Power vias KF127](#12V-Power-vias-KF127)
    * [Conetion to external E-Stop](#Conetion-to-external-E-Stop)
    * [On Board E-Stop](#On-Board-E-Stop)
 * BMS
    * [F103C8T6](#F103C8T6)(Mbed not Support, use keil)
    * Volatge sensor vias I2C
 * Mount Hole Dimension 
           
[M-CAD File Download](3Dfile)
## Power

### XT60 Source
![image](https://user-images.githubusercontent.com/45313904/120700605-7043a100-c4e4-11eb-836a-fc99aa1e005a.png)      
This board have  16 of this port.    
ATO Fuse should be inserted in order to use the port.       
If the have power to the XT60 port, The indication LED will light up.         
Motor and other devices that should be stop by the E-Stop button should be connect from here          
### XT60 Uninterrupted Source
![image](https://user-images.githubusercontent.com/45313904/120700920-d7615580-c4e4-11eb-8457-572481eb1b4c.png)      
This have 3 Port that will *not be interrupted* by the EStop      
         
         
### IO-link Power(24V)
For I/O link Master controller      
M12 connector is used      
         
         
## Auxiliary
### 12V Power vias KF127
![image](https://user-images.githubusercontent.com/45313904/120702845-21e3d180-c4e7-11eb-8051-02ba6c36d061.png)      
A 12V power source, you may power it for power anything less than 2A(such as remote relay)
      

### Conetion to external E-Stop
![image](https://user-images.githubusercontent.com/45313904/120703210-9585de80-c4e7-11eb-9093-53b2e239a737.png)      

| Port Name | Description                                                                |
|-----------|----------------------------------------------------------------------------|
| NO        | Connect to Relay/Switch NO port,     <br>Control XT60 port on/off,<br>pull-up circuit |
| COM       | Connect to Relay/Switch COM port,<br>PGND,<br>for pull down the NO port          |

### On Board E-Stop
![image](https://user-images.githubusercontent.com/45313904/120704306-0679c600-c4e9-11eb-8eca-8af658737fe6.png)      

## BMS
### F103C8T6
If you use mbed just ignore this part, mbed user go away   
Bluephill is used, remenber to check the jumper and oscillator crystal position   
![image](https://user-images.githubusercontent.com/45313904/125508969-ea37646e-36ce-4147-a828-d12760520afc.png)

#### Pin assignment
![image](https://user-images.githubusercontent.com/45313904/125509842-1ed60dcf-5a16-4506-9b02-57b9425f965f.png)      
| Pin  | Description                                                                                                   |
|------|---------------------------------------------------------------------------------------------------------------|
| PB4  | Control the FET to turn on/off (pull the pin to GND to turn off the FET)  (Recommended Pin mode: GPIO_Output) |
| PA15 | Detect whether manual E-stop switch is turn on (I forgot the Remote relay part, sorry!)                       |
| PB3  | N.C. for this version                                                                                         |

| Bus  | Pin | Description |
|------|-----|-------------|
| I2C1 | PB7 | SDA         |
| I2C1 | PB6 | SCL         |     

