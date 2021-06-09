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
    * F103C8T6(Mbed not Support, use keil)
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
