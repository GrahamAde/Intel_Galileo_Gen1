# Intel Galileo Gen 1

This repository outlines the capabilities of the Intel Galileo (First Generation) board and provides documenation, resources, and files which are no longer available.

![IntelGalileoGen1Front](/images/Intel_Galileo_Gen1_Front.jpg?raw=true "Intel Galileo Gen1 Front")

## Board Specifications

#### Processor: Intel Quark SoC X1000 application processor
- Clock Speed: 400 MHz
- L1 Cache: 16 Kilobytes
- Embedded SRAM: 512 Kilobytes on-die
- Cores (Threads): 1 (1)
- Architecture: i586, 32-bit Intel Pentium instruction set
- Lithography: 32 nm
- TDP: 12.5 Watts
#### Memory:
- 256 MB DDR3 800MHz RAM (Max Memory Bandwith: 2.5 GB/s)
- 8 MB NOR flash memory (For Embedded SPI Boot Image)
- 8 KB EEPROM
#### Storage: MicroSD card slot (supports up to 32 GB)
#### Connectivity:
- 1x 10/100 Ethernet port
- PCIe x1 (Gen 2.0)
- Wi-Fi (via optional mini-PCIe card)
- Bluetooth (via optional mini-PCIe card)
#### USB:
- 1x USB 2.0 host port (for add-on devices)
- 1x USB 2.0 client port (for programming)
#### Expansion:
- 14x digital input/output pins
- 6x analog inputs (12-bit resolution)
- 2x PWM outputs
- 1x UART (serial) port
- 1x I2C interface
- 1x SPI interface
#### Operating Systems:
- Yocto Project Linux (default)
#### Dimensions: 4.2 x 2.8 inches (approx. 10.7 x 7.1 cm)
#### Input Power: 5V DC input (via barrel jack or header pin)
#### Operating Voltage: 3.3V

## Table of Contents

- Update the board firmware
- Compile new linux image
- Log in to board using RS232 serial connection

## Boot Process for SPI Image (Firmware Version 732)

**Notes:** This early firmware version does not support booting off SD cards.  You must update to a later firmware version to enable SD card booting functionality.

![PrebootScreen](/images/Intel_Galileo_Gen1_Preboot_Screen.jpg?raw=true "Preboot Screen")
![SPIBootScreenFV732](/images/Intel_Galileo_Gen1_SPI_Boot_Screen_FV732.jpg?raw=true "SPI Boot Screen Firmware Version 732")
[SPI Boot Log Firmware Version 732](/images/Intel_Galileo_Gen1_SPI_Boot_Log_FV732.jpg)

'''

'''

## Boot Process for SPI Image (Firmware Version 1.1.0)

**Notes:** This is the last firmware version released by Intel for the Galileo Gen 1.  The "Intel Galileo Firmware Updater and Drivers (Gen 1 & 2)" directory in this repository contains the software which will update the board to firmware version 1.1.0.

![PrebootScreen](/images/Intel_Galileo_Gen1_Preboot_Screen.jpg?raw=true "Preboot Screen")
![SPIBootScreenFV110](/images/Intel_Galileo_Gen1_SPI_Boot_Screen_FV110.jpg?raw=true "SPI Boot Screen Firmware Version 1.1.0")
![SPIBootLogFV110](/images/Intel_Galileo_Gen1_SPI_Boot_Log_FV110.jpg?raw=true "SPI Boot Log Firmware Version 1.1.0")

## Boot Process for SD Card Image (Firmware Version 1.1.0)


