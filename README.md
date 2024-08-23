# *Simple**FOC*** ***Drive**Shield* *v1.2*

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?color=blue) 
<!-- ![GitHub release (latest by date)](https://img.shields.io/github/v/release/simplefoc/simplefoc-driveshield) ![GitHub Release Date](https://img.shields.io/github/release-date/simplefoc/simplefoc-driveshield?color=blue) -->

<img src="images/top.jpg"  height="220px"><img src="images/bottom.jpg"  height="220px"><img src="images/side.jpg"  height="220px">


This is an open-source low-cost BLDC driver boards in the form of a Arduino shield. It is a part of the *Simple**FOC*** project. The board is the big brother of the *Simple**FOC**Shield* and is designed to drive motors with higher current requirements, up to 30Amps. The board is created with the same philosophy as the *Simple**FOC**Shield* - to be simple to use, low-cost, and open-source and fully compatible with the *Simple**FOC***library. 

Additionally the aim of the board is to serve as a template project for the community to build their own motor drivers. 
- The board is relatively simple and can be easily modified to fit different requirements.
- The board is designed in EasyEDA and all the fabrication files are available for download

### Features
- **Plug & play**: In combination with Arduino *Simple**FOC**library* - [github](https://github.com/simplefoc/Arduino-FOC)
- **Low-cost**: Price of 25-40€ - [Check the pricing](https://www.simplefoc.com/shop) 
- **In-line current sensing**: Up to 5Amps bidirectional
   - ACS712 hall current sensor
- **Absolute max ratings** - Designed for Gimbal motors with the internal resistance >10 Ωs. 
   - Max current: 30A, 
   - Max input voltage: 35V
- **Stackable**: running 2 motors in the same time
- **Encoder/Hall sensors interface**: Integrated 3.3kΩ pullups (configurable)
- **I2C interface**: Integrated 4.7kΩ pullups (configurable)
- **Configurable pinout**: Hardware configuration - soldering connections
- **Arduino headers**: Arduino UNO, Arduino MEGA, STM32 Nucleo boards...
- **Open Source**: 
   - Fully designed in **EasyEDA**: [EasyEDA project](https://oshwlab.com/the.skuric/SimpleFOC-Drive)
   - Fully available fabrication files - [how to make it yourself](https://docs.simplefoc.com/arduino_simplefoc_shield_fabrication)


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
**Max voltage** | 24V | 35V | 35V | 35V 
**Protections** | Overtemperature | Overtemperature | Overtemperature, Overcurrent | Overcurrent
**Footprint** | 68mm x 53 mm | 68mm x 53 mm | 56mm x 53mm | 56mm x 53mm
**Design tool** | Altium Designer 2019 | Altium Designer 2019 | EasyEDA | EasyEDA 

## Board evolution timeline

To check the release timeline, click [here](https://github.com/simplefoc/SimpleFOC-driveShield/releases) 

Version  | release | Release date | Comment
----- | ----- | ---- | ----
*Simple**FOC** **Drive**Shield* v1.0 | v0.1 | 05/24 | - Test version <br> - **DRV8300** gate driver <br> - **SE3082G** dual mosfets <br> - ACS712 (range +-30Amps) <br> - 20V max voltage 
*Simple**FOC** **Drive**Shield* v1.0 | v1.0 | 06/24 | - Transition to **DRV8320H** gate driver <br>  - 30V max voltage
*Simple**FOC** **Drive**Shield* v1.1 | v1.1 | 07/24 | - Transition to 3x3mm **BSZ09x** mosfets instead of **SE3082G** <br> - 35V max voltage
*Simple**FOC** **Drive**Shield* v1.2 | v1.2 | 08/24 | Initial release <br>- Transition to **4 layer** PCB <br> - Enabling stacking (soldering pads) <br> - Configurable pullups (I2C and encoder) 


## Some more images

<img src="images/nucleo.png"  height="320px"><img src="images/comp.png"  height="320px">