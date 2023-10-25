# Solar Panel Tracker
Automatic solar panel tracker for rotation of solar panel based on illumination measurement

The system is installed on solar panels with a rotation mechanism based on a DC motor. Designed to turn the solar panel towards higher illuminance to maximize luminous flux.

Two light sensors are located on the panel - at an angle to the sides of rotation. If the illumination on the left or right sensor is higher by a certain amount, the panel will rotate in this direction. Only the difference in illumination that the system will respond to is manually adjusted (so that there are no constant twitches due to small fluctuations in illumination)

In the extreme positions of rotation, limit switches are installed that block the movement of the panel beyond the maximum rotation angles

## System parameters:
* Main controller		– Arduino Uno 
* Processor 			– 16 MGh, ATmega328P
* Controller memory		– 32 KB Flash + 2 kB SRAM + 1kB EEPROM
* IR receiver			– VS1838B
* Working frequency		– 38 KGh (940 µm)
* Motor controller		– Single h bridge (L298N)
* Motor power			– 450W (30A, 15V)
* Illumination sensor 		– BH1750
* Measurement range		– 0..65535 lx
* Measurement accuracy	– ±1 lx	
* Dimensions			
    - 60x90x30 mm (device body)
    - 2..5m (motors and sensors cable length)

## Components
* Controller Arduino UNO 
* Motor controller 30A 15V Single h bridge (L298N)
* DC motor for panel rotation with gearbox – 1pcs
* Illumination sensor BH1750 – 2pcs.
* Limit switches	– 2pcs
* Power supply 
    - 15V 30A (Motor)
    - 9V 0.5A (Logic)

## Wiring diagram

![Solar Panel Tracker wiring diagram](https://github.com/Brabn/SolarPanelTracker/blob/main/Wiring_diagram/SolarPanelTracker.Wiring_diagram.jpg)

## Further development of the system
- [ ] Adding manual control elements (buttons for manual tilting, control displays)
- [ ] More powerful motor controller for bigger motors
- [ ] Adding motors and switches groups (up to 3 panel sets per controller)
- [ ] Centralized control of multiple panels using a central control panel (connectrd to panels controllers via I2C or RS485 protocols
    - Control panel with sensor screen
    - Web interface
    - Mobile application
    - SMS informing
- [ ] Collection of statistics on the absolute illumination values of each panel to optimize the panel layout
- [ ] Control of additional parameters:
    - Current, voltage and power for each solar panel
    - Panel surface temperature

 
