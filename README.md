# *Simple**FOC*** ***Drive**Shield* *v1.2*

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?color=blue) 
![GitHub release (latest by date)](https://img.shields.io/github/v/release/simplefoc/SimpleFOC-DriveShield) ![GitHub Release Date](https://img.shields.io/github/release-date/simplefoc/SimpleFOC-DriveShield?color=blue)

<img src="images/top.jpg"  height="150px"><img src="images/bottom.jpg"  height="150px"><img src="images/side.jpg"  height="150px">


This is an open-source low-cost BLDC driver boards in the form of a Arduino shield. It is a part of the *Simple**FOC*** project. The board is the big brother of the *Simple**FOC**Shield* and is designed to drive motors with higher current requirements, up to 30Amps. The board is created with the same philosophy as the *Simple**FOC**Shield* - to be simple to use, low-cost, and open-source and fully compatible with the *Simple**FOC***library. 

Additionally the aim of the board is to serve as a template project for the community to build their own motor drivers. 
- The board is relatively simple and can be easily modified to fit different requirements.
- The board is designed in EasyEDA and all the fabrication files are available for download

### Components
- **DRV8320H** gate driver
    - Hardware configuration 
   - 3PWM
   -  Protections: undervoltage lockout, charge pump fault, MOSFET overcurrent, MOSFET short circuit, gate driver fault and overtemperature
- **BSZ0904NSI** mosfets
   - Standard 3mm x 3mm footprint (can be easily exchanged)
   - Max current 75A 
   - Max voltage 30V
- **ACS712**: 
   -  30Amps bidirectional
   - In-line current sensing

### Features
- **Boards absolute max ratings** 
   - Max current: 20A continuous (peak 30A - measured) 
   - Max input voltage: 30V
- **Stackable**: running 2 motors in the same time
- **Encoder/Hall sensors interface**: Integrated 3.3kΩ pullups (configurable)
- **I2C interface**: Integrated 4.7kΩ pullups (configurable)
- **Configurable pinout**: Hardware configuration - soldering connections
- **Arduino headers**: Arduino UNO, Arduino MEGA, STM32 Nucleo boards...
- **Open Source**: 
   - Fully designed in **EasyEDA**: [EasyEDA project](https://oshwlab.com/the.skuric/SimpleFOC-Drive)
   - Fully available fabrication files - [how to make it yourself](https://docs.simplefoc.com/arduino_simplefoc_shield_fabrication)
- **Low-cost**: Estimated price of 25-40€ - *Will be available in the SimpleFOC shop*


## Shield version comparison


Feature | <span class="simple">Simple<span class="foc">FOC</span>Shield</span> v1.x | <span class="simple">Simple<span class="foc">FOC</span>Shield</span> v2.x | <span class="simple">Simple<span class="foc">FOC</span>Shield</span> v3.x | <span class="simple">Simple<span class="foc">FOC</span> <b>Drive</b>Shield</span> v1.x
|-|-|-|-|-|
||<img src="https://simplefoc.com/assets/img/v1.jpg" height="120px" class="img300 img_half">|<img src="https://simplefoc.com/assets/img/v2.jpg" class="img300  img_half"  height="120px">|<img  height="120px" src="https://simplefoc.com/assets/img/v3.jpg" class="img300  img_half">|<img src="images/nucleo.png" class="img300  img_half"  height="120px">
**PWM Driver** | [L6234](https://www.st.com/resource/en/datasheet/l6234.pdf) | [L6234](https://www.st.com/resource/en/datasheet/l6234.pdf) | [DRV8313](https://www.ti.com/lit/ds/symlink/drv8313.pdf?ts=1719165774986&ref_url=https%253A%252F%252Fwww.google.com%252F)| gate driver: [DRV8320H](https://www.ti.com/lit/ds/symlink/drv8320.pdf) <br> mosfets: [BSZ0904NSI](https://www.infineon.com/dgdl/Infineon-BSZ0904NSI-DataSheet-v02_04-EN.pdf?fileId=db3a30432f29829e012f2a1ec7d90032)
**Current Sense** | ❌ | [INA240](https://www.ti.com/lit/ds/symlink/ina240.pdf?ts=1719180172738) | [ACS712 (5A)](https://www.allegromicro.com/en/products/sense/current-sensor-ics/zero-to-fifty-amp-integrated-conductor-sensor-ics/acs712) | [ACS712 (30A)](https://www.allegromicro.com/en/products/sense/current-sensor-ics/zero-to-fifty-amp-integrated-conductor-sensor-ics/acs712)
**Current measurement range** | ❌ | (configurable) ±3.3/5Amps | ±5Amps | ±30Amps
**Onboard LDO** | ❌ | LM7808 | LM7808 | ❌
**Stackable** | ✔️ | ✔️ | ✔️ | ✔️
**Max current** | 2Amps (5Amp peak) | 2Amps (5Amp peak) | 2Amps (3Amp peak) | 20Amps (30Amp peak)
**Max voltage** | 24V | 35V | 35V | 30V 
**Protections** | Overtemperature | Overtemperature | Overtemperature, Overcurrent | undervoltage lockout, charge pump fault, MOSFET overcurrent, MOSFET short circuit, gate driver fault, overtemperature
**Footprint** | 68mm x 53 mm | 68mm x 53 mm | 56mm x 53mm | 56mm x 53mm
**Design tool** | Altium Designer 2019 | Altium Designer 2019 | EasyEDA | EasyEDA 

## Board evolution timeline

To check the release timeline, click [here](https://github.com/simplefoc/SimpleFOC-driveShield/releases) 

Version  | release | Release date | Comment
----- | ----- | ---- | ----
*Simple**FOC** **Drive**Shield* v1.0 | v0.1 | 05/24 | - Test version <br> - **DRV8300** gate driver <br> - **SE3082G** dual mosfets <br> - ACS712 (range +-30Amps) <br> - 20V max voltage 
*Simple**FOC** **Drive**Shield* v1.0 | v1.0 | 06/24 | - Transition to **DRV8320H** gate driver <br>  - 30V max voltage
*Simple**FOC** **Drive**Shield* v1.1 | v1.1 | 07/24 | - Transition to 3x3mm **BSZ09x** mosfets instead of **SE3082G** <br> - 30V max voltage
*Simple**FOC** **Drive**Shield* v1.2 | [v1.2](https://github.com/simplefoc/SimpleFOC-DriveShield/releases/tag/v1.2) | 08/24 | Initial release <br>- Transition to **4 layer** PCB <br> - Enabling stacking (soldering pads) <br> - Configurable pullups (I2C and encoder) 


## Size comparison with SimpleFOCShield v3

<img src="images/comp.png"  height="320px">

## Temperature characteristics

This board can measure the phase currents up to 30Amps, so it is intended to be used in applications that require current draw up to around 20Amps continuous. For higher currents especially in the range of 15-30Amps the board can get quite hot. Depending on the copper thickness of the PCB chosen when ordering the board the temperature can vary, as well as the cooling conditions. The board can be fitted with a heatsink to improve the thermal performance.

So I've wanted to quantify the temperature characteristics of the board when a continuous current is applied to the motor. The measurements were done with a relatively constant ambient temperature of around 25°C. The board was powered with 24V. The motor was run at very low speed (0.1rad/s) in the open loop and the current (q component) was set to 10, 15 and 20 amps for prolonged periods of time. I've measured the temperature on the top of the board on the DRV8320H gate driver and the BSZ0904NSI mosfets. I've used the PICOLOG TC-08 thermocouple data logger to do the measuring.

Two copper thicknesses were tested
1. Standard 4-layer: 
    - **1oz** (35um) copper thickness on top and bottom layers, 
    - **0.5oz** (17.5um) copper thickness on inner layers

<img src="images/experiment/1oz (1).jpg" height="200px"><img src="images/experiment/1oz (2).jpg" height="200px">

2. Thick 4-layer: 
    - **2oz** (70um) copper thickness on top and bottom layers, 
    - **0.5oz** (35um) copper thickness on inner layers

<img src="images/experiment/2oz (1).jpg" height="200px"><img src="images/experiment/2oz (2).jpg" height="200px">


### Experiment results
Here is the table of the results

Current [A] | Standard 4-layer MOSFETS | Thick 4-layer  MOSFETS | Standard 4-layer DRV8320 |  Thick 4-layer DRV8320 
--- | --- | ---| --- | ---
10 | 57°C| 53°C | 50°C  | 52°C
15 | 78°C | 68°C| 62°C  | 62°C
20 | 125°C  | 100°C | 82°C | 82°C

So the results seem to suggest that, as the **BSZ0904NSI** mosfets are rated for temperatures up to 150°C and the **DRV8320H** gate driver up to 125°C, the board can be used up to 20Amps without additional cooling. 

**However, I would definitely recommend using a heatsink or a thicker copper PCB (2oz top and bottom layers) for currents above 15Amps continuous.**


<details>
<summary>Measured temperatures during the experiment</summary>

<img src="images/experiment/temp_record.jpg" >

</details>
