# 🌍 Overview

This is a very first prototype for DesCap's future LoRaWAN product. The design entails:

1. LoRa transceiver embedded within the STM32WL55 microcontroller
2. BMV080 sensor and BME680 breakout board from Bosch
3. L80-R GPS module from Quectel to test radio coverage
4. SPV1050 solar energy harvesting module
5. BQ24074 battery charging module with USB capabilities

<details>
<summary><h1>📋STM32WL55CCU6 pinout configuration</h1>  </summary>

|**Pin number** | **Pin name**| **Description**
|---------------|--------------------|
|PA0|Blinky LED|To quick test if flashing works
|PA2|VCP_TX|STLinkV3 virtual com port
|PA3|VCP_RX|STLinkV3 virtual com port
|PA4|NSS1|SPI1 slave select
|PA5|SCK1|SPI1 clock signal
|PA6|MISO1|SPI1
|PA7|MOSI1|SPI1
|PA8|MCO|Hook up to oscilloscope to test TCXO 32MHz output
|PA9 |TX1|UART to communicate with GPS 
|PA10|RX1|UART to communicate with GPS 
|PA12|GPS_RESET|
|PA13|SWDIO|for flashing/debugging
|PA14|SWDCK|for flashing/debugging
|PB2|ALRT|From MAX17048 fuel gauge when battery is low
|PB3|SWO|for flashing/debugging
|PB6|SCL1|I2C to communicate with gas sensors and fuel gauge
|PB7|SDA1|I2C to communicate with gas sensors and fuel gauge
|PB8 |RF_SW_V2| RF switch control input 2 (to choose between receive and transmit)
|PB12|RF_SW_V!| RF switch control input 1
</details>

<details>
  
<summary><h1>🔌Testpoints setup</h1> </summary>

|**Testpoint name** | **Description**| **Expected result**
|---------------|--------------------|

|VBUS|USB voltage|5V when USB is connected
|OUT|output of BQ24074 battery charging module|4.2V when battery is full, ~3.5V when battery empty
|$\overline{ALRT}$|MAX17048 fuel gauge alert signal when battery is low|3.3V when battery is full, 0V when empty 

</details>

<details>
<summary><h1>🔍PCB inspection result</h1></summary>
  
## General remarks 

## Minor Issues


## Detailed testing
### Visual inspection
### Electrical tests

#### Power consumption of Fans

</details>

<details>
<summary><h1>✅<b>TODOs for next version</b></h1></summary>

- [ ] Replace SMA connector from Samtec with a cheaper one (see notes in schematic)
- [ ] Tune the antenna side matching network with NanoVNA
- [ ] Remove GPS module

</details>



