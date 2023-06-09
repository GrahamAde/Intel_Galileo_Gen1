# Intel Galileo Gen 1

This repository outlines the capabilities of the Intel Galileo (First Generation) board and provides documenation, resources, and files which are no longer available.

![IntelGalileoGen1Front](/images/Intel_Galileo_Gen1_Front.jpg?raw=true "Intel Galileo Gen1 Front")

## Table of Contents

- [Board Specifications](#Board-Specs)
- [Connecting to Board via RS232 Serial Cable](#Connect-Via-Serial)
- [How to Update Board Firmware](#Update-Firmware)
- [Printing and Constructing Intel Galileo Case](#Galileo-Case)
- [Boot Log for SPI Image (Firmware Version 732)](#Boot-SPI-FV732)
- [Boot Log for SPI Image (Firmware Version 1.1.0)](#Boot-SPI-FV110)
- [Boot Log for SD Card Image (Firmware Version 1.1.0)](#Boot-SD-FV110)
- [Shutdown Log for SD Card Image (Firmware Version 1.1.0)](#Shutdown-SD-FV110)
- [Running Debian GNU/Linux on Intel Galileo](#Debian-Galileo)

***

<h2 id="Board-Specs">
Board Specifications
</h2>

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

***

<h2 id="Connect-Via-Serial">
Connecting to Board via RS232 Serial Cable
</h2>

The Intel Galileo Gen1 uses a custom serial port which utilizes a stereo headphone jack.  To connect via the serial headphone jack, you can create your own cable from a pair of headphones.

#### RS-232 Serial Jack Connection
![RS-232 Jack Connection Top](/images/RS232_Jack_Connection_Top.jpg?raw=true "RS-232 Jack Connection Top")
![RS-232 Jack Connection Front](/images/RS232_Jack_Connection_Front.jpg?raw=true "RS-232 Jack Connection Front")

#### RS-232 Serial Jack Pinout

![RS-232 DB-9 Pinout](/images/Intel_Galileo_Gen1_RS-232_DB-9_Pinout.jpg?raw=true "RS-232 DB-9 Pinout")
![Serial Jack Pinout](/images/Intel_Galileo_Gen1_Serial_Jack_Pinout.jpg?raw=true "Serial Jack Pinout")

***

<h2 id="Update-Firmware">
How to Update Board Firmware
</h2>

#### Updating Board Firmware on Windows 7
Intel Galileo Firmware Updater requires JRE (Java Runtime Environment 1.6.0).


#### Updating Board Firmware on Debian GNU/Linux 11 (Bullseye)


***

<h2 id="Galileo-Case">
Printing and Constructing Intel Galileo Case
</h2>

**Notes:** All CAD (FCStd) and .STL files are located in the 'Intel Galileo Case' directory.  Use FreeCAD 0.20 to open the FCStd file. https://www.freecad.org

The Intel Galileo Case is has five different components which need assembly.  They are as follows:

- Bottom Case
- WiFi Module
- RTC Battery
- Top Lid w/ Intel Logo
- Case Stand

The cumulative filament weight necessary for printing is 102.21g (@20% infill).

- Bottom Case - 61.09g
- Top Lid - 28.34g
- Case Stand - 12.78g

The case printed in this tutorial was printed with Polyterra PLA Blue.

#### Bottom Case Assembly

Parts Needed:

- (1) Printed Bottom Case Component
- (12) M3 Threaded Knurled Inserts

![BottomCaseUnfinished](/images/Intel_Galileo_Gen1_Case_Bottom_Unfinished.jpg?raw=true "Case Bottom Unfinished")

To set the M3 threaded inserts, use a soldering iron set to 500F and slowly push the inserts into the holes.

![BottomCaseFinished](/images/Intel_Galileo_Gen1_Case_Bottom_Finished.jpg?raw=true "Case Bottom Finished")

#### WiFi Module Assembly

Parts Needed:

- (1) Mini-PCIe WiFi Card (Intel AC7260 used)
- (1) Metal PCIe Half-Height Extender
- (2) SMA Pigtail Connectors
- (2) WiFi Antennas

![WiFiComponents](/images/Intel_Galileo_Gen1_WiFi_Components.jpg?raw=true "WiFi Components")

Attach SMA pigtail connectors to bottom case component.

![SMALeft](/images/Intel_Galileo_Gen1_WiFi_SMA_Left.jpg?raw=true "SMA Left")
![SMARight](/images/Intel_Galileo_Gen1_WiFi_SMA_Right.jpg?raw=true "SMA Right")

Attach WiFi Module to Galileo Board and Connect SMA wires.

![WiFiConstruction](/images/Intel_Galileo_Gen1_WiFi_Construction.jpg?raw=true "WiFi Construction")

#### RTC Battery Assembly

Parts Needed:

- (1) 3V Coin Battery (CR2032 Used)
- (2) 4" long 22 awg wires
- (2) Female Molex Pins
- Vinyl Electrical Tape (3M Scotch Super 88 recommended)

![BatteryComponents](/images/Intel_Galileo_Gen1_Battery_Components.jpg?raw=true "Battery Components")

Strip the ends of your wire approximately 1/4" on one end (battery terminal side) and 1/8" on the other end (molex pin side).  Crimp female molex pins to shorter leads.

![BatteryConstruction](/images/Intel_Galileo_Gen1_Battery_Construction.jpg?raw=true "Battery Construction")

Use electrical tape to secure the 1/4" leads to the battery terminals.  Finish by tightly wrapping the battery with electrical tape.

![BatteryFinished](/images/Intel_Galileo_Gen1_Battery_Finished.jpg?raw=true "Battery Finished")

Secure the battery assembly to the bottom of the case to the left of the WiFi Module.

![BatteryInstallation](/images/Intel_Galileo_Gen1_Battery_Installation.jpg?raw=true "Battery Installation")

#### Galileo Board Installation

Parts Needed:

- (1) Galileo Board w/ Attached WiFi Module
- (1) Bottom Case Component
- (4) Threaded Screws with Phillips Head

Mount Galileo board to bottom case component to after WiFi module and RTC battery installation.

![GalileoBoardInstallation](/images/Intel_Galileo_Gen1_Board_Installation.jpg?raw=true "Board Installation")

#### Top Lid w/ Intel Logo

Parts Needed:

- (1) Printed Top Lid Component
- (4) M3 x 6mm Bolts

![GalileoFinishedNoStand1](/images/Intel_Galileo_Gen1_Case_Finished_1_No_Stand.jpg?raw=true "Case Finished 1 - No Stand")
![GalileoFinishedNoStand2](/images/Intel_Galileo_Gen1_Case_Finished_2_No_Stand.jpg?raw=true "Case Finished 2 - No Stand")

#### Case Stand Installation

Parts Needed:

- (1) Printed Case Stand Component
- (2) M3 x 10mm Bolts

![GalileoStandComponents](/images/Intel_Galileo_Gen1_Case_Stand_Components.jpg?raw=true "Case Stand Components")

Attach case stand to back of the bottom case component with the M3 x 10mm bolts.

![GalileoStandInstallation](/images/Intel_Galileo_Gen1_Case_Stand_Installation.jpg?raw=true "Case Stand Installation")

#### Finished

You have now made your own Intel Galileo Gen1 case!

![GalileoCaseFinished1](/images/Intel_Galileo_Gen1_Case_Finished_1_With_Stand.jpg?raw=true "Case Finished 1 - With Stand")
![GalileoCaseFinished2](/images/Intel_Galileo_Gen1_Case_Finished_2_With_Stand.jpg?raw=true "Case Finished 2 - With Stand")

***

<h2 id="Boot-SPI-FV732">
Boot Process for SPI Image (Firmware Version 732)
</h2>

**Notes:** This early firmware version does not support booting off SD cards.  You must update to a later firmware version to enable SD card booting functionality.

#### Preboot Screen
![PrebootScreen](/images/Intel_Galileo_Gen1_Preboot_Screen.jpg?raw=true "Preboot Screen")

#### Boot Screen
![SPIBootScreenFV732](/images/Intel_Galileo_Gen1_SPI_Boot_Screen_FV732.jpg?raw=true "SPI Boot Screen Firmware Version 732")

#### Boot Log
[Image for 'SPI Boot Log Firmware Version 732'](/images/Intel_Galileo_Gen1_SPI_Boot_Log_FV732.jpg)

```
Found layout.conf @ 0xfff08200 len 0x00000d12
#Generated by Buildbot - Sysimage 732
#EXAMPLE LAYOUT.CONF FILE FOR FGPA/RELEASE

# WARNING: this file is indirectly included in a Makefile where it
# defines Make targets and pre-requisites. As a consequence you MUST
# run "make clean" BEFORE making changes to it. Failure to do so may
# result in the make process being unable to clean files it no longer
# has references to.

[main]
size=8388608
type=global

[MFH]
version=0x1
flags=0x0
address=0xfff08000
type=mfh

[LAYOUT.CONF_DUMP]
address=0xfff08200
type=mfh.build_information
meta=layout

[Flash Image Version]
type=mfh.version
meta=version
value=732

[ROM_OVERLAY]
address=0xfffe0000
#item_file=/p/clanton/swbuilds/BootRom/Ver_1_00_09/Clanton.rom
item_file=/p/clanton/swbuilds/EDK2/edk2_gcc_CP_00366/ClantonPeakCRBPlatform/RELEASE_GCC/FV/FlashModules/EDKII_BOOTROM_OVERRIDE.Fv
type=some_type
in_capsule=no

[signed-key-module]
address=0xfffd8000
item_file=config/SvpSignedKeyModule.bin
svn_index=0
type=some_type

[svn-area]
address=0xfffd0000
item_file=config/SVNArea.bin
type=some_type

[fixed_recovery_image]
address=0xfff90000
item_file=/p/clanton/swbuilds/EDK2/edk2_gcc_CP_00366/ClantonPeakCRBPlatform/RELEASE_GCC/FV/FlashModules/EDKII_RECOVERY_IMAGE1.Fv
sign=yes
type=mfh.host_fw_stage1_signed
svn_index=2
in_capsule=no

[NV_Storage]
address=0xfff30000
item_file=/p/clanton/swbuilds/EDK2/edk2_gcc_CP_00366/ClantonPeakCRBPlatform/RELEASE_GCC/FV/FlashModules/EDKII_NVRAM.bin
type=some_type

[RMU]
address=0xfff00000
item_file=/p/clanton/swbuilds/EDK2/edk2_gcc_CP_00366/ClantonPeakCRBPlatform/RELEASE_GCC/FV/FlashModules/RMU.bin
type=none_registered

[boot_stage1_image1]
address=0xffec0000
item_file=/p/clanton/swbuilds/EDK2/edk2_gcc_CP_00366/ClantonPeakCRBPlatform/RELEASE_GCC/FV/FlashModules/EDKII_BOOT_STAGE1_IMAGE1.Fv
sign=yes
boot_index=0
type=mfh.host_fw_stage1_signed
svn_index=1

[boot_stage1_image2]
address=0xffe80000
item_file=/p/clanton/swbuilds/EDK2/edk2_gcc_CP_00366/ClantonPeakCRBPlatform/RELEASE_GCC/FV/FlashModules/EDKII_BOOT_STAGE1_IMAGE2.Fv
sign=yes
boot_index=1
type=mfh.host_fw_stage1_signed
svn_index=1

[boot_stage_2_compact]
address=0xffd00000
item_file=/p/clanton/swbuilds/EDK2/edk2_gcc_CP_00355/ClantonPeakCRBPlatform/RELEASE_GCC/FV/FlashModules/EDKII_BOOT_STAGE2_COMPACT.Fv
sign=yes
type=mfh.host_fw_stage2_signed
svn_index=3

#address=0x002E1000
[Ramdisk]
address=0xffa60000
item_file=/p/clanton/swbuilds/meta-clanton_spi/meta-cln_spi_00103/image-spi-clanton.cpio.lzma
sign=yes
type=mfh.ramdisk_signed
svn_index=7

[Kernel]
address0xff851600
item_file=/p/clanton/swbuilds/meta-clanton_spi/meta-cln_spi_00103/bzImage
sign=yes
type=mfh.kernel_signed
svn_index=6

[grub.conf]
address=0xff850500
item_file=grub/grub-ce.conf
sign=yes
type=mfh.bootloader_conf_signed
svn_index=5

[grub]
address=0xff800000
item_file=/p/clanton/swbuilds/meta-clanton_spi/meta-cln_spi_00103/grub.efi
sign=yes
fvwrap=yes
guid=B43BD3E1-64D1-4744-9394-D0E1C4DE8C87
type=mfh.bootloader_signed
svn_index=4

# strings -n 16 '/p/clanton/swbuilds/EDK2/edk2_gcc_CP_00366/ClantonPeakCRBPlatform/RELEASE_GCC/FV/FlashModules/EDKII_BOOT_STAGE1_IMAGE.Fv' | grep -i 'clanton.*version' | head | unix2dos
# Clanton RomCode Version
# Clanton Microcode Version a0_1_00_23

[Linux-EFI SPI, setup=0x1070, size=0x1ef8f0]
[Initrd SPI, addr=0xdd77000, size=0x282954]
[   12.566946] console [ttyS1] enabled, bootconsole disabled
[   12.579863] Real Time Clock Driver v1.12b
[   12.597311] brd: module loaded
[   12.614795] cpuidle: using governor ladder
[   12.618962] cpuidle: using dovernor menu
[   12.631948] THRM: critical reset 86 c hot 70 c hardware failover 105 c
[   12.644112] TCP: cubic registered
[   12.647499] NET: Registered protocol family 17
[   12.653385] ... APIC ID:      00000000 (0)
[   12.657516] ... APIC VERSION: 00030010
[   12.661495] 0000000000000000000000000000000000000000000000000000000000000000
[   12.662035] 0000000000000000000000000000000000000000000000000000000000000000
[   12.662035] 0000000000000000000000000000000000000000000000000000000000000000
[   12.662035]
[   12.685243] testing the IO APIC.......................
[   12.692651] .................................... done.
[   12.697829] Using IPI Shortcut mode
[   12.714649]   Magic number: 1:0:0
[   12.732524] Freeing unused kernel memory: 268k freed
[   12.740454] Write protecting the kernel text: 2984k
[   12.746479] Write protecting the kernel read-only data: 1232k
[   12.752401] NX-protecting the kernel data: 3160k
[   12.759873] Failed to execute /init
INIT: version 2.88 booting
[   13.011196] tsc: Refined TSC clocksource calibration: 399.076 MHz
[   13.017532] Switching to clocksource tsc
[   13.155891] sdhci: Secure Digital Host Controller Interface driver
[   13.162249] sdhci: Copyright(c) Pierre Ossman
[   13.172895] sdhci-pci 0000:00:14.0: SDHCI controller found [8086:08a7] (rev 10)
[   13.252484] mmc0: SDHCI controller on PCI [0000:00:14.0] using ADMA
[   13.547530] g_serial: Vendor 0x8086 Product 0xbabe
[   13.555139] g_serial gadget: Gadget Serial v2.4
[   13.559788] g_serial gadget: g_serial ready
[   13.658636] stmmaceth 0000:00:14.6: enabling device (0000 -> 0002)
[   13.666292] stmmac MSI mode enabled
[   13.669655] Vendor 0x8086 Device 0x0937
[   13.674011] stmmac - user ID: 0x10, Synopsys ID: 0x37
[   13.679114]  DMA HW capability register supported
[   13.683802]  Enhanced/Alternate descriptors
[   13.688226]  RX Checksum Offload Engine supported (type 2)
[   13.693866]  TX Checksum insertion supported
[   13.698187]  Enable RX Mitigation via HW Watchdog Timer
[   13.755310] libphy: stmmac: probed
[   13.758779] eth0: PHY ID 20005c90 at 1 IRQ 0 (stmmac-1:01) active
[   13.831112] ACPI: bus type usb registered
[   13.838683] usbcore: registered new interface driver usbfs
[   13.846553] usbcore: registered new interface driver hub
[   13.854754] usbcore: registered new device driver usb
[   13.869854] ehci_hcd: USB 2.0 'Enhanced' Host Controller (EHCI) Driver
[   13.923347] ohci_hcd: USB 1.1 'Open' Host Controller (OHCI) Driver
[   13.930308] ohci_hcd 0000:00:14.4: OHCI Host Controller
[   13.937193] ohci_hcd 0000:00:14.4: new USB bus registered, assigned bus number 1
[   13.945057] ohci_hcd 0000:00:14.4: irq 16, io mem 0x9000c000
[   14.031203] hub 1-0:1.0: USB hub found
[   14.035617] hub 1-0:1.0: 2 ports detected
[   14.103964] Initializing USB Mass Storage driver...
[   14.111210] usbcore: registered new interface driver usb-storage
[   14.117270] USB Mass Storage support registered.
[   14.305287] cy8c9540a 0-0020: dev_id=0x40
[   14.457789] i2c /dev entries driver
[   14.625822] ce4100_spi 0000:00:15.0: enabling device (0000 -> 0002)
[   14.632899] pci spi probe(), enable_msi 1, mmio_base e0772000, dev c01c8800
[   14.641023] MSI enabled, irq number is 43
[   14.645078] ssp type is CE5X00 SSP
[   14.651271] cd4100_spi 0000:00:15.1: enabling device (0000 -> 0002)
[   14.657798] pci spi probe(), enable_msi 1, mmio_base e0774000, dev c01c9000
[   14.666127] MSI enabled, irq number is 44
[   14.670288] ssp type is CE5X00 SSP
[   14.728777] pxa2xx-spi pxa2xx-spi.0: master is unqueued, this is deprecated
[   14.745813] pxa2xx-spi pxa2xx-spi.1: master is unqueued, this is deprecated
Starting Bootlog daemon: bootlogd.
Configuring network interfaces... [   17.678018] eth0: device MAC address 98:4f:ee:01:32:70
udhcpc (v1.20.2) started
Sending discover...
Sending discover...
Sending discover...
No lease, failing
kernel.hotplug = /sbin/mdev
sh: %4Y%2m%2d%2H%2M: bad number
INIT: Entering runlevel: 5
Starting syslogd/klogd: done
Stopping Bootlog daemon: bootlogd.
/sketch/sketch.elf file does not exist or invalid permissions
clloader waiting to receive.
Poky 9.0 (Yocto Project 1.4 Reference Distro) 1.4.1 clanton /dev/ttyS1

clanton login:
```

***

<h2 id="Boot-SPI-FV110">
Boot Process for SPI Image (Firmware Version 1.1.0)
</h2>

**Notes:** This is the last firmware version released by Intel for the Galileo Gen 1.  The "Intel Galileo Firmware Updater and Drivers (Gen 1 & 2)" directory in this repository contains the software which will update the board to firmware version 1.1.0.

#### Preboot Screen
![PrebootScreen](/images/Intel_Galileo_Gen1_Preboot_Screen.jpg?raw=true "Preboot Screen")

#### Boot Screen
![SPIBootScreenFV110](/images/Intel_Galileo_Gen1_SPI_Boot_Screen_FV110.jpg?raw=true "SPI Boot Screen Firmware Version 1.1.0")

#### Boot Log
[Image for 'SPI Boot Log Firmware Version 1.1.0'](/images/Intel_Galileo_Gen1_SPI_Boot_Log_FV110.jpg)

```
Found layout.conf @ 0xffcff000 len 0x00000bf3

# WARNING: this file is indirectly included in a Makefile where it
# defines Make targets and pre-requisites. As a consequence you MUST
# run "make clean" BEFORE making changes to it. Failure to do so may
# result in the make process being unable to clean files it no longer
# has references to.

[main]
size=8388608
type=global


[MFH]
version=0x1
flags=0x0
address=0xfff08000
type=mfh


[Flash Image Version]
type=mfh.version
meta=version
value=0x01010000

[ROM_OVERLAY]
address=0xfffe0000
item_file=../../Quark_EDKII/Build/QuarkPlatform/RELEASE_GCC/FV/FlashModules/EDKII_BOOTROM_OVERRIDE.Fv
type=some_type

[signed-key-modules]
address=0xfffd8000
item_file=config/SvpSignedKeyModule.bin
svn_index=0
type=some_type
in_capsule=no

# On a deployed system, the SVN area holds the last known secure
# version of each signed asset.
# TODO: generate this area by collecting the SVN from the assets
# themselves.
[svn-area]
address=0xfffd0000
item_file=config/SVNArea.bin
type=some_type
# A capsule upgrade must implement some smart logic to make sure the
# highest Security Version Number always wins (rollback protection)
in_capsule=no

[fixed_recovery_image]
address=0xfff90000
item_file=../../Quark_EDKII/Build/QuarkPlatform/RELEASE_GCC/FV/FlashModules/EDKII_RECOVERY_IMAGE1.Fv
sign=yes
type=mfh.host_fw_stage1_signed
svn_index=2
# in_capsule=no

[NV_Storage]
address=0xfff30000
item_file=../../Quark_EDKII/Build/QuarkPlatform/RELEASE_GCC/FV/FlashModules/EDKII_NVRAM.bin
type=some_type

[RMU]
address=0xfff00000
item_file=../../Quark_EDKII/Build?QuarkPlatform/RELEASE_GCC/FV/FlashModules/RMU.bin
type=none_registered

[boot_stage1_image1]
address=0xffec0000
item_file=../../Quark_EDKII/Build/QuarkPlatform/RELEASE_GCC/FV/FlashModules/EDKII_BOOT_STAGE1_IMAGE1.Fv
sign=yes
boot_index=0
type=mfh.host_fw_stage1_signed
svn_index=1

[boot_stage1_image2]
address=0xffe80000
item_file=../../Quark_EDKII/Build/QuarkPlatform/RELEASE_GCC/FV/FlashModules/EDKII_BOOT_STAGE1_IMAGE2.Fv
sign=yes
boot_index=1
type=mfh.host_fv_stage1_signed
svn_index=1

[boot_stage_2_compact]
address=0xffd00000
item_file=../../Quark_EDKII/Build/QuarkPlatform/RELEASE_GCC/FV/FlashModules/EDKII_BOOT_STAGE2_COMPACT.Fv
sign=yes
type=mfh.host_fw_stage2_signed
svn_index=3

[Ramdisk]
address=0xffa60000
item_file=../../meta-clanton/yocto_build/tmp/deploy/images/image-spi-galileo-clanton.cpio.lzma
sign=yes
type=mfh.ramdisk_signed
svn_index=7

[LAYOUT.CONF_DUMP]
address=0xffcff000
type=mfh.build_information
meta=layout

[Kernel]
address=0xff852000
item_file=../../meta-clanton/yocto_build/tmp/deploy/images/bzImage
sign=yes
type=mfh.kernel_signed
svn_index=6

[grub.conf]
address=0xff851000
item_file=grub/grub-spi.conf
sign=yes
type=mfh.bootloader_conf_signed
svn_index=5

[grub]
address=0xff800000
item_file=../../meta-calnton/yocto_build/tmp/deploy/images/grub.efi
sign=yes
fvwrap=yes
guid=B43BD3E1-64D1-4744-9394-D0E1C4DE8C87
type=mfh.bootloader_signed
svn_index=4


[Linux-EFI SPI, setup=0x107f, size=0x1e0ac0]
[Initrd SPI, addr=0xdb5e000, size=0x299854]
[   0.000000] Initializing cgroup subsys cpuset
[   0.000000] Initializing cgroup subsys cpu
[   0.000000] Linux version 3.8.7-yocto-standard (calvin@U12) (gcc version 4.7.2 (GCC) ) #1 Mon Oct 31 14:39:35 PDT 2016
[   0.000000] Disabling PGE capability bit
[   0.000000] e820: BIOS-provided physical RAM map:
[   0.000000] BIOS-e820: [mem 0x0000000000000000-0x0000000000096fff] usable
[   0.000000] BIOS-e820: [mem 0x0000000000097000-0x0000000000097fff] reserved
[   0.000000] BIOS-e820: [mem 0x0000000000098000-0x000000000009ffff] usable
[   0.000000] BIOS-e820: [mem 0x0000000000100000-0x000000000efdefff] usable
[   0.000000] BIOS-e820: [mem 0x000000000efdf000-0x000000000f01efff] ACPI data
[   0.000000] BIOS-e820: [mem 0x000000000f01f000-0x000000000f0defff] reserved
[   0.000000] BIOS-e820: [mem 0x000000000f0df000-0x000000000fddefff] ACPI NVS
[   0.000000] BIOS-e820: [mem 0x000000000fddf000-0x000000000fdeefff] reserved
[   0.000000] BIOS-e820: [mem 0x000000000fdef000-0x000000000fdeffff] usable
[   0.000000] BIOS-e820: [mem 0x00000000e0000000-0x00000000e1ffffff] reserved
[   0.000000] BIOS-e820: [mem 0x00000000fed1c000-0x00000000fed1ffff] reserved
[   0.000000] Early serial console at MMIO32 0x9000b000 (options '115200n8')
[   0.000000] bootconsole [uart0] enabled
[   0.000000] NX (Execute Disable) protection: active
[   0.000000] efi: EFI v2.31 by EKI
[   0.000000] efi:  SMBIOS=0xfdee000  ACPI=0xf01e000  ACPI 2.0=0xf01e014
[   0.000000] efi: mem00: type=7, attr=0xf, range=[0x0000000000000000-0x0000000000095000) (0MB)
[   0.000000] efi: mem01: type=2, attr=0xf, range=[0x0000000000095000-0x0000000000097000) (0MB)
[   0.000000] efi: mem02: type=0, attr=0xf, range=[0x0000000000097000-0x0000000000098000) (0MB)
[   0.000000] efi: mem03: type=7, attr=0xf, range=[0x0000000000098000-0x00000000000a0000) (0MB)
[   0.000000] efi: mem04: type=2, attr=0xf, range=[0x0000000000100000-0x00000000002e1000) (1MB)
[   0.000000] efi: mem05: type=7, attr=0xf, range=[0x00000000002e1000-0x0000000001fde000) (28MB)
[   0.000000] efi: mem06: type=4, attr=0xf, range=[0x0000000001fde000-0x0000000002000000) (0MB)
[   0.000000] efi: mem07: type=7, attr=0xf, range=[0x0000000002000000-0x000000000bfe0000) (159MB)
[   0.000000] efi: mem08: type=4, attr=0xf, range=[0x000000000bfe0000-0x000000000c000000) (0MB)
[   0.000000] efi: mem09: type=7, attr=0xf, range=[0x000000000c000000-0x000000000db5e000) (27MB)
[   0.000000] efi: mem10: type=2, attr=0xf, range=[0x000000000db5e000-0x000000000e1f8000) (6MB)
[   0.000000] efi: mem11: type=4, attr=0xf, range=[0x000000000e1f8000-0x000000000e23d000) (0MB)
[   0.000000] efi: mem12: type=2, attr=0xf, range=[0x000000000e23d000-0x000000000e240000) (0MB)
[   0.000000] efi: mem13: type=1, attr=0xf, range=[0x000000000e240000-0x000000000e282000) (0MB)
[   0.000000] efi: mem14: type=4, attr=0xf, range=[0x000000000e282000-0x000000000e28b000) (0MB)
[   0.000000] efi: mem15: type=3, attr=0xf, range=[0x000000000e28b000-0x000000000e28f000) (0MB)
[   0.000000] efi: mem16: type=4, attr=0xf, range=[0x000000000e28f000-0x000000000e293000) (0MB)
[   0.000000] efi: mem17: type=3, attr=0xf, range=[0x000000000e293000-0x000000000e296000) (0MB)
[   0.000000] efi: mem18: type=4, attr=0xf, range=[0x000000000e296000-0x000000000e2f0000) (0MB)
[   0.000000] efi: mem19: type=3, attr=0xf, range=[0x000000000e2f0000-0x000000000e2fd000) (0MB)
[   0.000000] efi: mem20: type=4, attr=0xf, range=[0x000000000e2fd000-0x000000000e300000) (0MB)
[   0.000000] efi: mem21: type=3, attr=0xf, range=[0x000000000e300000-0x000000000e302000) (0MB)
[   0.000000] efi: mem22: type=4, attr=0xf, range=[0x000000000e302000-0x000000000e303000) (0MB)
[   0.000000] efi: mem23: type=3, attr=0xf, range=[0x000000000e303000-0x000000000e308000) (0MB)
[   0.000000] efi: mem24: type=4, attr=0xf, range=[0x000000000e308000-0x000000000e309000) (0MB)
[   0.000000] efi: mem25: type=3, attr=0xf, range=[0x000000000e309000-0x000000000e30f000) (0MB)
[   0.000000] efi: mem26: type=4, attr=0xf, range=[0x000000000e30f000-0x000000000e310000) (0MB)
[   0.000000] efi: mem27: type=3, attr=0xf, range=[0x000000000e310000-0x000000000e31e000) (0MB)
[   0.000000] efi: mem28: type=4, attr=0xf, range=[0x000000000e31e000-0x000000000e31f000) (0MB)
[   0.000000] efi: mem29: type=3, attr=0xf, range=[0x000000000e31f000-0x000000000e321000) (0MB)
[   0.000000] efi: mem30: type=4, attr=0xf, range=[0x000000000e321000-0x000000000e322000) (0MB)
[   0.000000] efi: mem31: type=3, attr=0xf, range=[0x000000000e322000-0x000000000e354000) (0MB)
[   0.000000] efi: mem32: type=4, attr=0xf, range=[0x000000000e354000-0x000000000e358000) (0MB)
[   0.000000] efi: mem33: type=3, attr=0xf, range=[0x000000000e358000-0x000000000e35b000) (0MB)
[   0.000000] efi: mem34: type=4, attr=0xf, range=[0x000000000e35b000-0x000000000e36e000) (0MB)
[   0.000000] efi: mem35: type=3, attr=0xf, range=[0x000000000e36e000-0x000000000e377000) (0MB)
[   0.000000] efi: mem36: type=4, attr=0xf, range=[0x000000000e377000-0x000000000e378000) (0MB)
[   0.000000] efi: mem37: type=3, attr=0xf, range=[0x000000000e378000-0x000000000e381000) (0MB)
[   0.000000] efi: mem38: type=4, attr=0xf, range=[0x000000000e381000-0x000000000e383000) (0MB)
[   0.000000] efi: mem39: type=3, attr=0xf, range=[0x000000000e383000-0x000000000e39c000) (0MB)
[   0.000000] efi: mem40: type=4, attr=0xf, range=[0x000000000e39c000-0x000000000e3b5000) (0MB)
[   0.000000] efi: mem41: type=3, attr=0xf, range=[0x000000000e3b5000-0x000000000e3c2000) (0MB)
[   0.000000] efi: mem42: type=4, attr=0xf, range=[0x000000000e3c2000-0x000000000e412000) (0MB)
[   0.000000] efi: mem43: type=3, attr=0xf, range=[0x000000000e412000-0x000000000e415000) (0MB)
[   0.000000] efi: mem44: type=4, attr=0xf, range=[0x000000000e415000-0x000000000e418000) (0MB)
[   0.000000] efi: mem45: type=3, attr=0xf, range=[0x000000000e418000-0x000000000e431000) (0MB)
[   0.000000] efi: mem46: type=4, attr=0xf, range=[0x000000000e431000-0x000000000e437000) (0MB)
[   0.000000] efi: mem47: type=3, attr=0xf, range=[0x000000000e437000-0x000000000e43f000) (0MB)
[   0.000000] efi: mem48: type=4, attr=0xf, range=[0x000000000e43f000-0x000000000e5a0000) (1MB)
[   0.000000] efi: mem49: type=3, attr=0xf, range=[0x000000000e5a0000-0x000000000e5b5000) (0MB)
[   0.000000] efi: mem50: type=4, attr=0xf, range=[0x000000000e5b5000-0x000000000e802000) (2MB)
[   0.000000] efi: mem51: type=3, attr=0xf, range=[0x000000000e802000-0x000000000e807000) (0MB)
[   0.000000] efi: mem52: type=4, attr=0xf, range=[0x000000000e807000-0x000000000e80a000) (0MB)
[   0.000000] efi: mem53: type=3, attr=0xf, range=[0x000000000e80a000-0x000000000e80e000) (0MB)
[   0.000000] efi: mem54: type=4, attr=0xf, range=[0x000000000e80e000-0x000000000e80f000) (0MB)
[   0.000000] efi: mem55: type=3, attr=0xf, range=[0x000000000e80f000-0x000000000e829000) (0MB)
[   0.000000] efi: mem56: type=4, attr=0xf, range=[0x000000000e829000-0x000000000e82a000) (0MB)
[   0.000000] efi: mem57: type=3, attr=0xf, range=[0x000000000e82a000-0x000000000e82c000) (0MB)
[   0.000000] efi: mem58: type=4, attr=0xf, range=[0x000000000e82c000-0x000000000e82e000) (0MB)
[   0.000000] efi: mem59: type=3, attr=0xf, range=[0x000000000e82e000-0x000000000e834000) (0MB)
[   0.000000] efi: mem60: type=4, attr=0xf, range=[0x000000000e834000-0x000000000e84e000) (0MB)
[   0.000000] efi: mem61: type=3, attr=0xf, range=[0x000000000e84e000-0x000000000e858000) (0MB)
[   0.000000] efi: mem62: type=4, attr=0xf, range=[0x000000000e858000-0x000000000e859000) (0MB)
[   0.000000] efi: mem63: type=3, attr=0xf, range=[0x000000000e859000-0x000000000e866000) (0MB)
[   0.000000] efi: mem64: type=4, attr=0xf, range=[0x000000000e866000-0x000000000e878000) (0MB)
[   0.000000] efi: mem65: type=3, attr=0xf, range=[0x000000000e878000-0x000000000e87a000) (0MB)
[   0.000000] efi: mem66: type=4, attr=0xf, range=[0x000000000e87a000-0x000000000e882000) (0MB)
[   0.000000] efi: mem67: type=3, attr=0xf, range=[0x000000000e882000-0x000000000e888000) (0MB)
[   0.000000] efi: mem68: type=4, attr=0xf, range=[0x000000000e888000-0x000000000e88f000) (0MB)
[   0.000000] efi: mem69: type=3, attr=0xf, range=[0x000000000e88f000-0x000000000e894000) (0MB)
[   0.000000] efi: mem70: type=4, attr=0xf, range=[0x000000000e894000-0x000000000efdf000) (7MB)
[   0.000000] efi: mem71: type=9, attr=0xf, range=[0x000000000efdf000-0x000000000f01f000) (0MB)
[   0.000000] efi: mem72: type=5, attr=0x800000000000000f, range=[0x000000000f01f000-0x000000000f07f000) (0MB)
[   0.000000] efi: mem73: type=6, attr=0x800000000000000f, range=[0x000000000f07f000-0x000000000f0df000) (0MB)
[   0.000000] efi: mem74: type=10, attr=0xf, range=[0x000000000f0df000-0x000000000fddf000) (13MB)
[   0.000000] efi: mem75: type=0, attr=0xf, range=[0x000000000fddf000-0x000000000fdef000) (0MB)
[   0.000000] efi: mem76: type=4, attr=0xf, range=[0x000000000fdef000-0x000000000fdf0000) (0MB)
[   0.000000] efi: mem77: type=11, attr=0x8000000000000000, range=[0x00000000e0000000-0x00000000e2000000) (32MB)
[   0.000000] efi: mem78: type=11, attr=0x8000000000000000, range=[0x00000000fed1c000-0x00000000fed20000) (0MB)
[   0.000000] SMBIOS 2.7 present.
[   0.000000] e820: last_pfn = 0xfdf0 max_arch_pfn = 0x1000000
[   0.000000] Scan for SMP in [mem 0x00000000-0x000003ff]
[   0.000000] Scan for SMP in [mem 0x0009fc00-0x0009ffff]
[   0.000000] Scan for SMP in [mem 0x000f0000-0x000fffff]
[   0.000000] Scan for SMP in [mem 0x000aaaa0-0x000aae9f]
[   0.000000] init_memory_mapping: [mem 0x00000000-0x0fdeffff]
[   0.000000] RAMDISK: [mem 0x0db5e000-0x0ddf7fff]
[   0.000000] ACPI: RSDP 0f01e014 00024 (v02 INTEL )
[   0.000000] ACPI: XSDT 0f01d0e8 0006C (v01 INTEL  TIANO    00000004      01000013)
[   0.000000] ACPI: FACP 0f01b000 000F4 (v03 INTEL  TIANO    00000004 INTL 0100000D)
[   0.000000] ACPI: DSDT 0f012000 02401 (v01 INTEL  QuarkNcS 00000003 INTL 20140424)
[   0.000000] ACPI: FACS 0f1c7000 00040
[   0.000000] ACPI: UEFI 0fbd5000 00042 (v01                 00000000      00000000)
[   0.000000] ACPI: APIC 0f01c000 0005A (v01 INTEL  TIANO    00000001 MSFT 00000000)
[   0.000000] ACPI: HPET 0f01a000 00038 (v01                 00000001      00000000)
[   0.000000] ACPI: MCFG 0f019000 0003C (v01                 00000001      00000000)
[   0.000000] ACPI: SSDT 0f018000 004D8 (v01 SsgPmm  Cpu0Cst 00000011 INTL 20140424)
[   0.000000] ACPI: SSDT 0f017000 0043F (v01 SsgPmm  Cpu0Ist 00000012 INTL 20140424)
[   0.000000] ACPI: SSDT 0f016000 0013B (v01 SsgPmm  Cpu0Tst 00000013 INTL 20140424)
[   0.000000] ACPI: SSDT 0f015000 00056 (v01 SsgPmm    CpuPm 00000010 INTL 20140424)
[   0.000000] mapped APIC to         ffffb000 (        fee00000)
[   0.000000] 0MB HIGHMEM available.
[   0.000000] 253MB LOWMEM available.
[   0.000000]   mapped low ram: 0 - 0fdf0000
[   0.000000]   low ram: 0 - 0fdf0000
[   0.000000] Zone ranges:
[   0.000000]   Normal   [mem 0x00010000-0x0fdeffff]
[   0.000000]   HighMem  empty
[   0.000000] Movable zone start for each node
[   0.000000] Early memory node ranges
[   0.000000]   node   0: [mem 0x00010000-0x00096fff]
[   0.000000]   node   0: [mem 0x00098000-0x0009ffff]
[   0.000000]   node   0: [mem 0x00100000-0x0efdefff]
[   0.000000]   node   0: [mem 0x0fdef000-0x0fdeffff]
[   0.000000] Using APIC driver default
[   0.000000] ACPI: PM-Timer IO Port: 0x1008
[   0.000000] mapped APIC to         ffffb000 (        fee00000)
[   0.000000] ACPI: LAPIC (acpi_id[0x01] lapic_id[0x00] enabled)
[   0.000000] ACPI: LAPIC_NMI (acpi_id[0x01] high edge lint[0x1])
[   0.000000] ACPI: IOAPIC (id[0x01] address[0xfec00000] gsi_base[0])
[   0.000000] IOAPIC[0]: Assigned apic_id 1
[   0.000000] IOAPIC[0]: apic_id 1, version 32, address 0xfec00000, GSI 0-23
[   0.000000] ACPI: INT_SRC_OVR (bus 0 bus_irq 0 global_irq 2 dfl dfl)
[   0.000000] Int: type 0, pol 0, trig 0, bus 00, IRQ 00, APIC ID 1, APIC INT 02
[   0.000000] APIC: INT_SRC_OVR (bus 0 bus_irq 9 global_irq 9 high level)
[   0.000000] Int: type 0, pol 1, trig 3, bus 00, IRQ 09, APIC ID 1, APIC INT 09
[   0.000000] Int: type 0, pol 0, trig 0, bus 00, IRQ 01, APIC ID 1, APIC INT 01
[   0.000000] Int: type 0, pol 0, trig 0, bus 00, IRQ 03, APIC ID 1, APIC INT 03
[   0.000000] Int: type 0, pol 0, trig 0, bus 00, IRQ 04, APIC ID 1, APIC INT 04
[   0.000000] Int: type 0, pol 0, trig 0, bus 00, IRQ 05, APIC ID 1, APIC INT 05
[   0.000000] Int: type 0, pol 0, trig 0, bus 00, IRQ 06, APIC ID 1, APIC INT 06
[   0.000000] Int: type 0, pol 0, trig 0, bus 00, IRQ 07, APIC ID 1, APIC INT 07
[   0.000000] Int: type 0, pol 0, trig 0, bus 00, IRQ 08, APIC ID 1, APIC INT 08
[   0.000000] Int: type 0, pol 0, trig 0, bus 00, IRQ 0a, APIC ID 1, APIC INT 0a
[   0.000000] Int: type 0, pol 0, trig 0, bus 00, IRQ 0b, APIC ID 1, APIC INT 0b
[   0.000000] Int: type 0, pol 0, trig 0, bus 00, IRQ 0c, APIC ID 1, APIC INT 0c
[   0.000000] Int: type 0, pol 0, trig 0, bus 00, IRQ 0d, APIC ID 1, APIC INT 0d
[   0.000000] Int: type 0, pol 0, trig 0, bus 00, IRQ 0e, APIC ID 1, APIC INT 0e
[   0.000000] Int: type 0, pol 0, trig 0, bus 00, IRQ 0f, APIC ID 1, APIC INT 0f
[   0.000000] Using ACPI (MADT) for SMP configuration information
[   0.000000] ACPI: HPET id; 0x8086a201 base: 0xfed00000
[   0.000000] mapped IOAPIC to ffffa000 (fec00000)
[   0.000000] e820: [mem 0x0fdf0000-0xdfffffff] available for PCI devices
[   0.000000] Built 1 zonelists in Zone order, mobility grouping on.  Total pages: 60787
[   0.000000] Kernel command line: root=/dev/ram0 console=ttyQRK1,115200n8 earlycon=uart8250,mmio32,0x9000b000,115200n8 reboot=efi,warm apic=debug rw efi_main=0x0000000141ebad1e jmp_code32=0x000000029951c0c0
[   0.000000] PID hash table entries: 1024 (order: 0, 4096 bytes)
[   0.000000] Dentry cache hash table entries: 32768 (order: 5, 131072 bytes)
[   0.000000] Inode-cache hash table entries: 16384 (order: 4, 65536 bytes)
[   0.000000] __ex_table already sorted, skipping sort
[   0.000000] Initializing CPU#0
[   0.000000] Initializing HighMem for node 0 (00000000:00000000)
[   0.000000] Memory: 220868k/260032k available (2849k kernel code, 24312k reserved, 1463k data, 308k init, 0k highmem)
[   0.000000] virtual kernel memory layout:
[   0.000000]     fixmap  : 0xfffa2000 - 0xfffff000   ( 372 kB)
[   0.000000]     pkmap   : 0xffc00000 - 0xffe00000   (2048 kB)
[   0.000000]     vmalloc : 0xd05f0000 - 0xffbfe000   ( 758 MB)
[   0.000000]     lowmem  : 0xc0000000 - 0xcfdf0000   ( 253 MB)
[   0.000000]       .init : 0xc1437000 - 0xc1484000   ( 308 kB)
[   0.000000]       .data : 0xc12c8592 - 0xc14363c0   (1463 kB)
[   0.000000]       .text : 0xc1000000 - 0xc12c8592   (2849 kb)
[   0.000000] Checking if this processor honours the WP bit even in supervisor mode...Ok.
[   0.000000] SLUB: Genslabs=15, HWalign=32, Order=0-3, MinObjects=0, CPUs=1, Nodes=1
[   0.000000] NR_IRQS:2304 nr_irqs:256 16
[   0.000000] Console: colour dummy device 80x25
[   0.000000] tsc: Fast TSC calibration using PIT
[   0.000000] tsc: Detected 399.076 MHz processor
[   0.010012] Calibrating delay loop (skipped), value calculated using timer frequency.. 798.15 BogoMIPS (lpj=3990760)
[   0.023034] pid_max: default: 32768 minimum: 301
[   0.065482] Security Framework initialized
[   0.070169] Mount-cache hash table entries: 512
[   0.076861] Initializing cgroup subsys cpuacct
[   0.080045] Initializing cgroup subsys freezer
[   0.085115] Disabling PGE capability bit
[   0.090039] Intel Pentium with F0 0F bug - workaround enabled.
[   0.096676] Last level iTLB entries: 4KB 0, 2MB 0, 4MB 0
[   0.096676] Last level dTLB entries: 4KB 0, 2MB 0, 4MB 0
[   0.096676] tlb_flushall_shift: 6
[   0.100040] CPU: Intel 05/09 (fam: 05, model: 09, stepping: 00)
[   0.110150] ACPI: Core revision 20121018
[   0.178736] Performance Events: no PMU driver, software events only.
[   0.185331] Enabling APIC mode:  Flat.  Using 1 I/O APICs
[   0.190048] Getting VERSION: 30010
[   0.193823] Getting VERSION: 30010
[   0.200037] Getting ID: 0
[   0.202947] Getting ID: f000000
[   0.206425] Getting LVT0: 700
[   0.210037] Getting LVT1: 400
[   0.213349] enabled ExtINT on CPU#0
[   0.217317] ENABLING ID-APIC IRQs
[   0.220036] Synchronizing Arb IDs.
[   0.225018] ..TIMER: vector=0x30 apic1=0 pin1=2 apic2=-1 pin2=-1
[   0.333662] Using local APIC timer interrupts.
[   0.333662] calibrating APIC timer ...
[   0.350000] ... lapic delta = 2494212
[   0.350000] ... PM-Timer delta = 357953
[   0.350000] ... PM-Timer result ok
[   0.350000] ..... delta 2494212
[   0.350000] ..... mult: 107125589
[   0.350000] ..... calibration result: 3990739
[   0.350000] ..... CPU clock speed is 399.0739 MHz.
[   0.350000] ..... host bus clock speed is 399.0739 MHz.
[   0.371438] devtmpgs: initialized
[   0.377216] PM: Registering ACPI NVS region [mem 0x0f0df000-0x0fddefff] (13631488 bytes)
[   0.390461] RTC time:  0:08:23, date: 01/01/01
[   0.395783] NET: Registered protocol family 16
[   0.410336] ACPI: bus type pci registered
[   0.417491] PCI: MMCONFIG for domain 0000 [bus 00-1f] at [mem 0xe0000000-0xe1ffffff] (base 0xe0000000)
[   0.420056] PCI: MMCONFIG at [mem 0xe0000000-0xe1ffffff] reserved in E820
[   0.430030] PCI: Using MMCONFIG for extended config space
[   0.440031] PCI: Using configuration type 1 for base access
[   0.514260] bio: create slab <bio-0> at 0
[   0.520806] ACPI: Added _OSI(Module Device)
[   0.525464] ACPI: Added _OSI(Processor Device)
[   0.530232] ACPI: Added _OSI(3.0 _SCP Extensions)
[   0.535470] ACPI: Added _OSI(Processor Aggregator Device)
[   0.594031] [Firmware Bug]: ACPI: BIOS _OSI(Linux) query ignored
[   0.606352] ACPI: Interpreter enabled
[   0.610063] ACPI: (supports S0 S3 S5)
[   0.614464] ACPI: Using IOAPIC for interrupt routing
[   0.722293] PCI: Using host bridge widnows from ACPI, if necessary, use "pci=nocrs" and report a bug
[   0.734067] ACPI: PCI Root Bridge [PCI0] (domain 0000 [bus 00-1f])
[   0.755202] PCI host bridge to bus 0000:00
[   0.759789] pci_bus 0000:00: root bus resource [bus 00-1f]
[   0.760246] pci_bus 0000:00: root bus resource [io  0x0000-0x0cf7]
[   0.770061] pci_bus 0000:00: root bus resource [io  0x0d00-0xffff]
[   0.776932] pci_bus 0000:00: root bus resource [mem 0x000a0000-0x000bffff]
[   0.780056] pci_bus 0000:00: root bus resource [mem 0x10000000-0xfebfffff]
[   0.802044] pci 0000:00:17.0: PCI bridge to [bus 01]
[   0.807832] pci 0000:00:17.1: PCI bridge to [bus 02]
[   0.815576]  pci0000:00: ACPI _OSC support notification failed, disabling PCIe ASPM
[   0.820046]  pci0000:00: unable to request _OSC control (_OSC support mask: 0x08)
[   0.866334] ACPI: PCI Interrupt Link [LNKA] (IRQs 3 4 5 7 9 10 11 12) *0, disabled.
[   0.876408] ACPI: PCI Interrupt Link [LNKB] (IRQs 3 4 5 7 9 10 11 12) *0, disabled.
[   0.886216] ACPI: PCI Interrupt Link [LNKC] (IRQs 3 4 5 7 9 10 11 12) *0, disabled.
[   0.900404] ACPI: PCI Interrupt Link [LNKD] (IRQs 3 4 5 7 9 10 11 12) *0, disabled.
[   0.911692] ACPI: PCI Interrupt Link [LNKE] (IRQs 3 4 5 7 9 10 11 12) *0, disabled.
[   0.922899] ACPI: PCI Interrupt Link [LNKF] (IRQs 3 4 5 7 9 10 11 12) *0, disabled.
[   0.933956] ACPI: PCI Interrupt Link [LNKG] (IRQs 3 4 5 7 9 10 11 12) *0, disabled.
[   0.945436] ACPI: PCI Interrupt Link [LNKH] (IRQs 3 4 5 7 9 10 11 12) *0, disabled.
[   0.959355] SCSI subsystem initialized
[   0.965376] Intel Quark Board Galileo Firmware Version 0x01010000
[   0.972798] Intel Quark side-band driver registered
[   0.981272] IMR alloc id 0 0x00010000 - 0x0001436c locked
[   0.991555] PCI: Using ACPI for IRQ routing
[   1.003313] HPET: 3 timers in total, 0 timers will be used for per-cpu timer
[   1.010232] hpet0: at MMIO 0xfed00000, IRQs 2, 8, 0
[   1.015678] hpet0: 3 comparators, 64-bit 14.318180 MHz counter
[   1.022421] Switching to clocksource hpet
[   1.030998] pnp: PnP ACPI init
[   1.034567] ACPI: bus type pnp registered
[   1.043620] system 00:00: [mem 0xe0000000-0xe1ffffff] has been reserved
[   1.051260] system 00:00: [mem 0xfed1c000-0xfed1ffff] has been reserved
[   1.058627] system 00:00: [mem 0x000c0000-0x000dffff] has been reserved
[   1.066067] system 00:00: [mem 0x000e0000-0x000fffff] could not be reserved
[   1.073889] system 00:00: [mem 0xff800000-0xffffffff] has been reserved
[   1.099383] system 00:03: [io  0x1000-0x100f] has been reserved
[   1.106070] system 00:03: [io  0x1010-0x101f] has been reserved
[   1.112737] system 00:03: [io  0x1100-0x113f] has been reserved
[   1.119330] system 00:03: [io  0x1040-0x107f] has been reserved
[   1.125992] system 00:03: [io  0x1140-0x117f] has been reserved
[   1.145229] pnp 00:07: unknown resource type 19 in _CRS
[   1.151129] pnp 00:07: can't evaluate _CRS: 1
[   1.161849] pnp 00:08: unknown resource type 19 in _CRS
[   1.167665] pnp 00:08: can't evaluate _CRS: 1
[   1.176417] pnp 00:09: unknown resource type 17 in _CRS
[   1.182321] pnp 00:09: can't evaluate _CRS: 1
[   1.188372] pnp: PnP ACPI: found IO devices
[   1.193267] ACPI: ACPI bus type pnp unregistered
[   1.322107] pci 0000:00:17.0: BAR 8: assigned [mem 0x10000000-0x101fffff]
[   1.329667] pci 0000:00:17.0: BAR 9: assigned [mem 0x10200000-0x103fffff 64bit pref]
[   1.338368] pci 0000:00:17.1: BAR 8: assigned [mem 0x10400000-0x105fffff]
[   1.346012] pci 0000:00:17.1: BAR 9: assigned [mem 0x10600000-0x107fffff 64bit pref]
[   1.354706] pci 0000:00:17.0: BAR 7: assigned [io  0x2000-0x2fff]
[   1.361580] pci 0000:00:17.1: BAR 7: assigned [io  0x3000-0x3fff]
[   1.368372] pci 0000:00:17.0: PCI bridge to [bus 01]
[   1.373976] pci 0000:00:17.0:   bridge window [io  0x2000-0x2fff]
[   1.380829] pci 0000:00:17.0:   bridge window [mem 0x10000000-0x101fffff]
[   1.388380] pci 0000:00:17.0:   bridge window [mem 0x10200000-0x103fffff 64bit pref]
[   1.397053] pci 0000:00:17.1: PCI bridge to [bus 02]
[   1.402653] pci 0000:00:17.1:   bridge window [io  0x3000-0x3fff]
[   1.402653] pci 0000:00:17.1:   bridge window [mem 0x10400000-0x105fffff]
[   1.417056] pci 0000:00:17.1:   bridge window [mem 0x10600000-0x107fffff 64bit pref]
[   1.426778] NET: Registered protocol family 2
[   1.433091] TCP established hash table entries: 2048 (order: 2, 16384 bytes)
[   1.441123] TCP bind hash table entries: 2048 (order: 1, 8192 bytes)
[   1.448229] TCP: Hash tables configured (established 2048 bind 2048)
[   1.455565] TCP: reno registered
[   1.459179] UDP hash table entries: 256 (order: 0, 4096 bytes)
[   1.465774] UDP-Lite hash table entries: 256 (order: 0, 4096 bytes)
[   1.473317] NET: Registered protocol family 1
[   1.479821] Trying to unpack rootfs image as initramfs...
[  11.547803] Freeing initrd memory: 2664k freed
[  11.572539] microcode: Intel CPU family 0x5 not supported
[  11.586194] HugeTLB registered 2 MB page size, pre-allocated 0 pages
[  11.654475] msgmni has been set to 464
[  11.663676] Block layer SCSI generic (bsg) driver version 0.4 loaded (major 253)
[  11.671962] io scheduler noop registered
[  11.676321] io scheduler deadline registered
[  11.682236] io scheduler cfq registered (default)
[  11.694229] input: Sleep Button as /devices/LNXSYSTM:00/LNXSYBUS:00/PNP0C0E:00/input/input0
[  11.703779] ACPI: Sleep Button [SLPB]
[  11.709025] input: Power Button as /devices/LNXSYSTM:00/LNXSYBUS:00/PNP0C0C:00/input/input1
[  11.718574] ACPI: Power Button [PWRB]
[  11.807413] Serial: 8250/16550 driver, 2 ports, IRQ sharing enabled
[  11.840843] 0000:00:14.1: ttyS0 at MMIO 0x9000f000 (irq = 17) is a 16550A
[  11.871469] 0000:00:14.5: ttyS1 at MMIO 0x9000b000 (irq = 17) is a 16550A
[  11.888049] brd: module loaded
[  11.897575] loop: module loaded
[  11.902216] lpc_sch_probe BIOS_CNTL 0x00000101
[  11.907158] lpc_sch_probe new BIOS_CNTL 0x00000101
[  11.912553] lpc_sch_probe RCBA @ 0xfed1c000
[  11.927434] rtc_cmos 00:01: RTC can wake from S4
[  11.934149] rtc_cmos 00:01: rtc core: registered rtc_cmos as rtc0
[  11.941261] rtc0: alarms up to one day, 242 bytes nvram, hpet irqs
[  11.948753] cpuidle: using governor ladder
[  11.953564] cpuidle: using governor menu
[  11.967756] eSRAM: CTRL 0x047f3f91 block 0x00000000
[  11.973256] eSRAM: pages 128
[  11.986948] intel_qrk_esram_test_probe/Oct 31 2016/14:39:21 complete OK !!
[  11.996662] THRM: critical reset 104 c hot 95 c hardware failover 105 c
[  12.006891] TCP: cubic registered
[  12.010843] NET: Registered protocol family 17
[  12.016312] ... APIC ID:      00000000 (0)
[  12.020612] ... APIC Version: 00030010
[  12.020612] 0000000000000000000000000000000000000000000000000000000000000000
[  12.020612] 0000000000000000000000000000000000000000000000000000000000000000
[  12.020612] 0000000000000000000000000000000000000000000000000000000000000000
[  12.020612]
[  12.050638] testing the IO APIC.......................
[  12.057736] .................................... done.
[  12.063497] Using IPI Shortcut mode
[  12.067422] turn off boot console uart0

Poky 9.0.4 (Yocto Project 1.4.4 Reference Distro) 1.4.4 clanton /dev/ttyS1

clanton login:
```

***

<h2 id="Boot-SD-FV110">
Boot Log for SD Card Image (Firmware Version 1.1.0)
</h2>

#### Preboot Screen
![PrebootScreen](/images/Intel_Galileo_Gen1_Preboot_Screen.jpg?raw=true "Preboot Screen")

#### Boot Screen
![SDBootScreenFV110](/images/Intel_Galileo_Gen1_SD_Boot_Screen_FV110.jpg?raw=true "SD Boot Screen Firmware Version 1.1.0")

#### Boot Log
[Image for 'SD Boot Log Firmware Version 1.1.0'](/images/Intel_Galileo_Gen1_SD_Boot_Log_FV110.jpg)

```
Found layout.conf @ 0xffcff000 len 0x00000bf3

# WARNING: this file is indirectly included in a Makefile where it
# defines Make targets and pre-requisites. As a consequence you MUST
# run "make clean" BEFORE making changes to it. Failure to do so may
# result in the make process being unable to clean files it no longer
# has references to.

[main]
size=8388608
type=global


[MFH]
version=0x1
flags=0x0
address=0xfff08000
type=mfh


[Flash Image Version]
type=mfh.version
meta=version
value=0x01010000

[ROM_OVERLAY]
address=0xfffe0000
item_file=../../Quark_EDKII/Build/QuarkPlatform/RELEASE_GCC/FV/FlashModules/EDKII_BOOTROM_OVERRIDE.Fv
type=some_type

[signed-key-module]
address=0xfffd8000
item_file=config/SvpSignedKeyModule.bin
svn_index=0
type=some_type
in_capsule=no

# On a deployed system, the SVN area holds the last known secure
# version of each signed asset.
# TODO: generate this area by collecting the SVN from the assets
# themselves.
[svn-area]
address=0xfffd0000
item_file=config/SVNArea.bin
type=some_type
# A capsule upgrade must implement some smart logic to make sure the
# highest Security Version Number always wins (rollback protection)
in_capsule=no

[fixed_recovery_image]
address=0xfff90000
item_file=../../Quark_EDKII/Build/QuarkPlatform/RELEASE_GCC/FV/FlashModules/EDKII_RECOVERY_IMAGE1.Fv
sign=yes
type=mfh.host_fw_stage1_signed
svn_index=2
# in_capsule=no

[NV_Storage]
address=0xfff30000
item_file=../../Quark_EDKII/Build/QuarkPlatform/RELEASE_GCC/FV/FlashModules/EDKII_NVRAM.bin
type=some_type

[RMU]
address=0xfff00000
item_file=../../Quark_EDKII/Build/QuarkPlatform/RELEASE_GCC/FV/FlashModules/RMU.bin
type=none_registered

[boot_stage1_image1]
address=0xffec0000
item_file=../../Quark_EDKII/Build/QuarkPlatform/RELEASE_GCC/FV/FlashModules/EDKII_BOOT_STAGE1_IMAGE1.Fv
sign=yes
boot_image=0
type=mfh.host_fw_stage1_signed
svn_index=1

[boot_stage1_image2]
address=0xffe80000
item_file=../../Quark_EDKII/Build/QuarkPlatform/RELEASE_GCC/FV/FlashModules/EDKII_BOOT_STAGE1_IMAGE2.Fv
sign=yes
boot_index=1
type=mfh.host_fw_stage1_signed
svn_index=1

[boot_stage_2_compact]
address=0xffd00000
item_file=../../Quark_EDKII/Build/QuarkPlatform/RELEASE_GCC/FV/FlashModules/EDKII_BOOT_STAGE2_COMPACT.Fv
sign=yes
type=mfh.host_fw_stage2_signed
svn_index=3

[Ramdisk]
address=0xffa600000
item_file=../../meta-clanton/yocto_build/tmp/deploy/images/image-spi-galileo-clanton.cpio.lzma
sign=yes
type=mfh.ramdisk_signed
svn_index=7

[LAYOUT.CONF_DUMP]
address=0xffcff000
type=mfh.build_information
meta=layout

[Kernel]
address=0xff852000
item_file=../../meta-clanton/yocto_build/tmp/deploy/images/bzImage
sign=yes
type=mfh.kernel_signed
svn_index=6

[grub.conf]
address=0xff851000
item_file=grub/grub-spi.conf
sign=yes
type=mfh.bootloader_conf_signed
svn_index=5

[grub]
address=0xff800000
item_file=../../meta-clanton/yocto_build/tmp/deploy/images/grub.efi
sign=yes
fvwrap=yes
guid=B43BD3E1-64D1-4744-9394-D0E1C4DE8C87
type=mfh.bootloader_signed
svn_index=4


[Linux-EFI, setup=0x109f, size=0x2373b0]
[    0.889305] console [ttyS1] enable, bootconsole disabled
[    0.900311] brd: module loaded
[    0.906579] loop: module loaded
[    0.910299] lpc_sch_probe BIOS_CNTL 0x00000101
[    0.914788] lpc_sch_probe new BIOS_CNTL 0x0000101
[    0.919612] lpc_sch_probe RCBA @ 0xfed1c000
[    0.926720] tun: Universal TUN/TAP device driver, 1.6
[    0.931893] tun: (C) 1999-2004 Max Krasnyansky <maxk@qualcomm.com>
[    0.938888] rtc_cmos 00:01: RTC can wake from S4
[    0.944521] rtc_cmos 00:01: rtc core: registered rtc_cmos as rtc0
[    0.950832] rtc0: alarms up to one day, 242 bytes nvram, hpet irqs
[    0.957252] cpuidle: using governor ladder
[    0.961468] cpuidle: using governor menu
[    0.965616] sdhci: Secure Digital Host Controller Interface driver
[    0.971924] sdhci: Copyright(c) Pierre Ossman
[    0.976440] sdhci-pci 0000:00:14.0: SDHCI controller found [8086:08a7] (rev 10)
[    1.030154] mmc0: SDHCI controller on PCI [0000:00:14.0] using ADMA
[    1.036999] sdhci-pltfm: SDHCI platform and OF driver helper
[    1.057220] eSRAM: CTRL 0x047f3f91 block 0x00000000
[    1.062222] eSRAM: pages 128
[    1.086319] intel_qrk_esram_test_probe/May 12 2016/08:16:55 complete OK !!
[    1.094454] THRM: critical reset 104 c hot 95 c hardware failover 105 c
[    1.101414] oprofile: using timer interrupt.
[    1.107309] TCP: cubic registered
[    1.110848] NET: Registered protocol family 17
[    1.116349] ... APIC ID:      00000000 (0)
[    1.120471] ... APIC VERSION: 00030010
[    1.120698] 0000000000000000000000000000000000000000000000000000000000000000
[    1.120698] 0000000000000000000000000000000000000000000000000000000000000000
[    1.120698] 0000000000000000000000000000000000000000000000000000000000000000
[    1.120698]
[    1.147872] testing the IO APIC.......................
[    1.154504] .....................................done.
[    1.159672] Using IPI Shortcut mode
[    1.168249]  Magic number: 1:0:0
[    1.172102] rtc_cmos 00:01: setting system clock to 2001-01-01 00:02:44 UTC (978307364)
[    1.182725] Waiting for root device /dev/mmcblk0p2...
[    1.195421] mmc0: new high speed SDHC card at address 0007
[    1.202109] mmcblk0: mmc0:0007 SD16G 14.9 GiB
[    1.209762]  mmcblk0: p1 p2
[    1.296177] kjournald starting.  Commit interval 5 seconds
[    1.304788] EXT3-fs (mmcblk0p2): using internal journal
[    1.310146] EXT3-fs (mmcblk0p2): mounted filesystem with writeback data mode
[    1.317302] VFS: Mounted root (ext3 filesystem) on device 179:2.
[    1.325407] devtmpfs: mounted
[    1.328794] Freeing unused kernel memory: 384k freed
[    1.336648] Write protecting the kernel text: 3416k
[    1.342058] Write protecting the kernel read-only data: 1524k
[    1.347844] NX-protecting the kernel data: 2728k
[    1.592955] systemd[1]: systemd 216 running in system mode. (-PAM -AUDIT -SELINUX +IMA -APPARMOR +SMACK +SYSVINIT -LIBCRYPTSETUP -GCRYPT +GNUTLS +ACL +XZ -LZ4 -SECCOMP +BLKID -ELFUTILS +KMOD -IDN )
[    1.613259] systemd[1]: Detected arhitecture 'x86'.

Welcome to iot-devkit (Intel IoT Development Kit) 3.5 (tarsier)!


[    1.719899] NET: Registered protocol family 10
[    1.727362] systemd[1]: Inserted module 'ipv6'
[    1.735887] systemd[1]: Set hostname to <galileo>
[    1.750177] tsc: Refined TSC clocksource calibrtation: 399.076 MHz
[    1.756331] Switching to clocksource tsc
[    2.316632] systemd[1]: [/lib/systemd/system/wyliodrin-server.service:3] Failed to add dependency on redis, ignoring: Invalid argument
[    2.340020] systemd[1]: [/lib/systemd/system/wyliodrin-hypervisor.service:3] Failed to add dependency on redis, ignoring: Invalid argument
[    2.355685] systemd[1]: [/lib/systemd/system/redis.service:7] Unknown lvalue 'ExecPre' in section 'Service'
[    2.440730] systemd[1]: Expecting device dev-ttyS1.device...
         Expecting device dev-ttyS1.device...
[    2.470593] systemd[1]: Starting Forward Password Requests to Wall Directory Watch.
[    2.479509] systemd[1]: Started Forward Password Requests to Wall Directory Watch.
[    2.487673] systemd[1]: Starting Dispatch Password Requests to Console Directory Watch.
[    2.496712] systemd[1]: Started Dispatch Password Requests to Console Directory Watch.
[    2.505066] systemd[1]: Starting Paths.
[  OK  ] Reached target Paths.
[    2.530545] systemd[1]: Reached target Paths.
[    2.535303] systemd[1]: Starting Swap.
[  OK  ] Reached target Swap.
[    2.560545] systemd[1]: Reached target Swap.
[    2.565184] systemd[1]: Expecting device dev-mmcblk0p1.device...
         Expecting device dev-mmcblk0p1.device...
[    2.590586] systemd[1]: Starting Root Slice.
[  OK  ] Created slice Root Slice.
[    2.640546] systemd[1]: Created slice Root Slice.
[    2.645615] systemd[1]: Starting /dev/initctl Compatibility Named Pipe.
[  OK  ] Listening on /dev/initctl Compatibility Named Pipe.
[    2.710553] systemd[1]: Listening on /dev/initctl Compatibility Named Pipe.
[    2.717876] systemd[1]: Starting Delayed Shutdown Socket.
[  OK  ] Listening on Delayed Shutdown Socket.
[    2.740549] systemd[1]: Listening on Delayed Shutdown Socket.
[    2.746656] systemd[1]: Starting Journal Socket (/dev/log).
[  OK  ] Listening on Journal Socket (/dev/log).
[    2.770550] systemd[1]: Listening on Journal Socket (/dev/log).
[    2.776909] systemd[1]: Starting udev Control Socket.
[  OK  ] Listening on udev Control Socket.
[    2.800549] systemd[1]: Listening on udev Control Socket.
[    2.806385] systemd[1]: Starting udev Kernel Socket.
[  OK  ] Listening on udev Kernel Socket.
[    2.830549] systemd[1]: Listening on udev Kernel Socket.
[    2.836266] systemd[1]: Starting Journal Socket.
[  OK  ] Listening on Journal Socket.
[    2.860549] systemd[1]: Listening on Journal Socket.
[    2.866060[ systemd[1]: Starting System Slice.
[  OK  ] Created slice System Slice.
[    2.890548] systemd[1]: Created slice System Slice.
[    2.895853] systemd[1]: Staring set initial time to last shutdown time...
[        Starting set initial time to last shutdown time...
[    2.926481] systemd[1]: Starting Load modules for the Intel galileo...
         Starting Load modules for the Intel galileo...
[    2.966609] systemd[1]: Started File System Check on Root Device.
[    2.990935] systemd[1]: Mounting Temporary Directory...
         Mounting Temporary Directory...
[    3.033997] systemd[1]: Starting system-serial\x2dgetty.slice.
[  OK  ] Created slice system-serial\x2dgetty.slice.
[    3.090568] systemd[1]: Created slice system-serial\x2dgetty.slice.
[    3.098200] systemd[1]: Starting system-getty.slice.
[  OK  ] Created slice system-getty.slice.
[    3.114884] systemd[1]: Created slice system-getty.slice.
[    3.122644] systemd[1]: Mounting POSIX Message Queue File System...
         Mounting POSIX Message Queue File System...
[    3.236198] systemd[1]: Starting udev Coldplug all Devices...
         Starting udev Coldplug all Devices...
[    3.318301] intel_qrk_gip 0000:00:15.2: enabling device (0000 -> 0002)
[    3.358038] systemd[1]: Starting Load Kernel Modules...
[    3.364538] platform qrk-gpio-restrict-sc.0: Driver qrk-gpio-restrict-sc requests probe deferral
         Starting Load Kernel Modules...
[    3.378607] intel_qrk_gpio_probe UIO addr 0x90006000 internal_addr 0xd2614000 size 4096 memtype 1
[    3.400442] intel_qrk_gip 0000:00:15.2: i2c speed set to 100kHz
[    3.419275] systemd[1]: Mounting Huge Pages File System...
[    3.431445] platform qrk-gpio-restrict-sc.0: Driver qrk-gpio-restrict-sc requests probe deferral
         Mounting Huge Pages File System...
[    3.507145] systemd[1]: Starting Create list of required static device nodes for the current kernel...
         Starting Create list of required st... nodes for the current kernel...
[    3.610141] i2c /dev entries driver
[    3.644872] systemd[1]: Mounting Debug File System...
         Mounting Debug File System...
[    3.701234] ACPI: bus type usb registered
[    3.705882] usbcore: registered new interface driver usbfs
[    3.717494] systemd[1]: Starting Journal Service...
[    3.762469] ce4100_spi 0000:00::15.0: enabling device (0000 -> 0002)
[    3.769804] platform qrk-gpio-restrict-sc.0: Driver qrk-gpio-restrict-sc requests probe deferral
[    3.779649] usbcore: registered new interface driver hub
         Starting Journal Service...
[    3.810516] usbcore: registered new device driver usb
[    3.825252] ce4100_spi 0000:00:15.1: enabling device (0000 -> 0002)
[  OK  ] Started Journal Service.
[    3.857165] platform qrk-gpio-restrict-sc.0: Driver qrk-gpio-restrict-sc requests probe deferral
[    3.870611] systemd[1]: Started Journal Service.
[  OK  ] Reached target Slices.
         Starting Remount Root and Kernel File Systems...
[    3.959493] spi_master spi0: will run message pump with realtime priority
[  OK  ] Mounted Debug File System.
[    3.991352] platform qrk-gpio-restrict-sc.0: Driver qrk-gpio-restrict-sc requests probe deferral
[    4.004351] Bluetooth: Core ver 2.16
[    4.008215] NET: Registered protocol family 31
[    4.012791] Bluetooth: HCI device and connection manager initialized
[    4.019339] spi_master spi1: will run message pump with realtime priority
[  OK  ] Mounted Huge Pages File System.
[  OK  ] Mounted POSIX Message Queue File System.
[    4.057219] platform qrk-gpio-restrict-sc.0: Driver qrk-gpio-restrict-sc requests probe deferral
[  OK  ] Mounted Temporary Directory.
[    4.142751] Bluetooth: HCI socket layer initialized
[    4.147711] Bluetooth: L2CAP socket layer initialized
[  OK  ] Started set initial time to last shutdown time.
[    4.178473] Bluetooth: SCO scoket layer initialized
[    4.237781] usbcore: registered new interface driver btusb
[  OK  ] Started Create list of required sta...ce nodes for the current kernel.
[    4.293541] platform qrk-gpio-restrict-sc.0: Driver qrk-gpio-restrict-sc requests probe deferral
[  OK  ] Started Remount Root and Kernel File Systems.
[    4.315356] EFI Variables Facility v0.08 2004-May-17
[  OK  ] Started Load modules for the Intel galileo.
[  OK  ] Started udev Coldplug all Devices.
         Starting Create Static Device Nodes in /dev...
[  OK  ] Started Create Static Device Nodes in /dev.
         Starting udev Kernel Device Manager...
[  OK  ] Reached target Local File Systems (Pre).
         Mounting /var/volatile...
[    6.221388] systemd-udevd[84]: starting version 216
[  OK  ] Started udev Kernel Device Manager.
[    6.324415] ehci_hcd: USB 2.0 'Enhanced' Host Controller (EHCI) Driver
[  OK  ] Mounted /var/volatile.
[    6.384701] ehci-pci: EHCI PCI platform driver
[    6.442001] ehci-pci 0000:00:14.3: EHCI Host Controller
[    6.477402] ehci-pci 0000:00:14.3: new USB bus registered, assigned bus number 1
[    6.512130] ehci-pci 0000:00:14.3: INSNREG01 is 0x007f007f
[    6.517672] ehci-pci 0000:00:14.3: INSNREG01 is 0x007f007f
[    6.570301] ehci-pci 0000:00:14.3: irq 19, io mem 0x9000d000
[    6.600220] ehci-pci 0000:00:14.3: USB 2.0 started, EHCI 1.00
         Starting Load/Save Random Seed...
[    6.639573] hub 1-0:1.0: USB hub found
[    6.680262] hub 1-0:1.0: 2 ports detected
[    6.684839] platform qrk-gpio-restrict-sc.0: Driver qrk-gpio-restrict-sc requests probe deferral
[  OK  ] Started Load/Save Random Seed.
[    6.814807] sch_gpio_probe UIO port addr 0x1080 size 64 porttype 1
[    6.862277] cy8c9540a 0-0020: dev_id=0x40
[    6.994695] at24 0-0050: byte_len looks suspicious (no power of 2)!
[    7.045914] at24 0-0050: 11264 byte at24 EEPROM, writable, 1 bytes/write
[    7.299890] cfg80211: Calling CRDA to update world regulatory domain
[    7.368407] Intel(R) Wireless WiFi driver for Linux, in-tree:
[    7.374315] Copyright(c) 2003-2013 Intel Corporation
[    7.439281] ohci_hcd: USB 1.1 'Open' Host Controller (OHCI) Driver
[    7.487576] ohci_hcd 0000:00:14.4: OHCI Host Controller
[    7.507565] ohci_hcd 0000:00:14.4: new USB bus registered, assigned bus number 1
[    7.548155] ohci_hcd 0000:00:14.4: irq 16, io mem 0x9000c000
[    7.631383] hub 2-0:1.0: USB hub found
[    7.635241] hub 2-0:1.0: 2 ports detected
[    7.814331] PPP generic driver version 2.4.2
[    7.902723] NET: Registered protocol family 24
[    8.038286] stmmaceth 0000:00:14.6: enabling device (0000 -> 0002)
[    8.120618] stmmac MSI mode enabled
[    8.123969] Vendor 0x8086 Device 0x0937
[    8.128166] stmmac - user ID: 0x10, Synopsys ID: 0x37
[    8.133365]  DMA HW capability register supported
[    8.137933]  Enhanced/Alternate descriptors
[    8.142408]  RX Checksum Offload Engine supported (type 2)
[    8.147928]  TX Checksum insertion supported
[    8.152288]  Enable RX Mitigation via HW Watchdog Timer
[  OK  ] Found device /dev/ttyS1.
[    8.260496] libphy: stmmac: probed
[    8.263951] eth0: PHY ID 20005c90 at 1 IRQ 0 (stmmac-1:01) active
[    8.485872] Initializing USB Mass Storage driver...
[    8.535326] usbcore: registered new interface driver usb-storage
[    8.541465] USB Mass Storage support registered.
[  OK  ] Found device /dev/mmcblk0p1.
[    8.652354] usbcore: registered new interface driver usbhid
[    8.657967] usbhid: USB HID core driver
         Mounting /media/card...
[    8.829324] g_acm_ms gadget: Mass Storage Function, version: 2009/09/11
[    8.836114] g_acm_ms gadget: Number of LUNs=1
[    8.842593]  lun0: LUN: removable file: /dev/mmcblk0p1
[    8.871351] g_acm_ms gadget: Composite Gadget (ACM + MS), version: 2011/10/10
[    8.915843] g_acm_ms gadget: g_acm_ms ready
[  OK  ] Mounted /media/card.
[  OK  ] Reached target Local File Systems.
         Starting Create Volatile Files and Directories...
         Starting Trigger Flushing of Journal to Persistent Storage...
[  OK  ] Started Load Kernel Modules.
[  OK  ] Started Create Volatile Files and Directories.
[   10.222845] systemd-udevd[87]: renamed network interface eth0 to enp0s20f6
[   10.244872] systemd-journald[64]: Received request to flush runtime journal from PID 1
[  OK  ] Started Trigger Flushing of Journal to Persistent Storage.
         Starting Network Time Synchronization...
         Starting Update UTMP about System Boot/Shutdown...
         Mounting FUSE Control File System...
         Starting Apply Kernel Variables...
[  OK  ] Mounted FUSE Control File System.
[  OK  ] Started Apply Kernel Variables.
[  OK  ] Started Network Time Synchronization.
[  OK  ] Started Update UTMP about System Boot/Shutdown.
[  OK  ] Reached target System Time Synchronized.
[  OK  ] Reached target System Initialization.
[  OK  ] Listening on Avahi mDNS/DNS-SD Stack Activation Socket.
[  OK  ] Listening on D-Bus System Message Bus Socket.
[  OK  ] Reached target Timers.
         Starting Restore Sound Card State...
[  OK  ] Listening on sshd.socket.
[  OK  ] Started Restore Sound Card State.
[  OK  ] Reached target Sockets.
[  OK  ] Reached target Basic System.
         Starting Connection service...
         Starting Target Communication Framework agent...
         Starting Zero-configuration networking...
         Starting Telephony service...
         Starting Wyliodrin hypervisor...
         Starting Lightning Fast Webserver With Light System Requirements...
         Starting Galileo Arduino Layer...
[  OK  ] Started Galileo Arduino Layer.
         Starting Wyliodrin server...
         Starting Login Service...
         Starting Avahi mDNS/DNS-SD Stack...
         Starting D-Bus System Message Bus...
[  OK  ] Started D-Bus System Message Bus.
[  OK  ] Started Avahi mDNS/DNS-SD Stack.
[  OK  ] Started Telephony service.
         Starting Provides static IP address...
[  OK  ] Started Target Communication Framework agent.
[  OK  ] Started Lightning Fast Webserver With Light System Requirements.
[   13.272402] enp0s20f6: device MAC address 98:f4:ee:01:32:70
[   13.458630] netlink: 12 bytes leftover after parsign attributes.
[  OK  ] Started Zero-configuration networking.
[   13.510255] netlink: 12 bytes leftover after parsing attributes.
[   13.516605] netlink: 12 bytes leftover after parsing attributes.
[  OK  ] Started Provides static IP address.
[  OK  ] Started Connection service.
[  OK  ] Started Login Service.
[  OK  ] Reached target Remote File Systems.
         Starting Permit User Sessions...
         Starting Bluetooth service...
         Starting Intel_XDK Daemon...
[  OK  ] Started Intel_XDK Daemon.
[  OK  ] Started Permit User Sessions.
         Starting Serial Getty on ttyS1...
[  OK  ] Started Serial Getty on ttyS1.
         Starting Getty on tty1...
[  OK  ] Started Getty on tty1.
[  OK  ] Reached target Login Prompts.
[  OK  ] Started Bluetooth service.
[   15.924386] Bluetooth: BNEP (Ethernet Emulation) ver 1.3
[   15.929748] Bluetooth: BNEP filters: protocol multicast
[   15.978129] Bluetooth: BNEP socket layer initialized
         Starting WPA supplicant...
         Starting Hostname Service...
[  OK  ] Started WPA supplicant.
[  OK  ] Started Hostname Service.
[  OK  ] Started Wyliodrin hypervisor.
[  OK  ] Started Wyliodrin server.
[  OK  ] Reached target Multi-User System.
         Starting Redis Server...
         Starting Update UTMP about System Runlevel Changes...
[  OK  ] Started Update UTMP about System Runlevel Changes.
[  OK  ] Started Redis Server.

galileo login:
```

***

<h2 id="Shutdown-SD-FV110">
Shutdown Log for SD Card Image (Firmware Version 1.1.0)
</h2>

#### Shutdown Log
[Image for 'SD Shutdown Log Firmware Version 1.1.0'](/images/Intel_Galileo_Gen1_SD_Shutdown_Log_FV110.jpg)

```
[  OK  ] Stopped target System Time Synchronized.
         Stopping WPA supplicant...
         Stopping Bluetooth service...
         Stopping Redis Server...
         Starting Store Sound Card State...
         Starting keep current date&time at shutdown by touching /etc/version...
[  OK  ] Stopped Bluetooth service.
[  OK  ] Stopped WPA supplicant.
[  OK  ] Stopped Redis Server.
[FAILED] Failed to start Store Sound Card State.
See 'systemctl status alsa-store.service' for details.
[  OK  ] Started keep current date&time at shutdown by touching /etc/version.
[  OK  ] Stopped target Multi-User System.
         Stopping Provides static IP address...
         Stopping Target Communication Framework agent...
         Stopping Telephony service...
         Stopping Lightning Fast Webserver With Light System Requirements...
         Stopping Galileo Arduino Layer...
         Stopping Intel_XDK_Daemon...
         Stopping Login Service...
[  OK  ] Stopped target Login Prompts
         Stopping Serial Getty on ttyS1...
         Stopping Getty on tty1...
         Stopping D-Bus System Message Bus...
[  OK  ] Stopped Telephony service.
[  OK  ] Stopped Target Communication Framework agent.
[  OK  ] Stopped Galileo Arduino Layer.
[  OK  ] Stopped Login Service.
[  OK  ] Stopped Avahi mDNS/DNS-SD Stack.
[  OK  ] Stopped D-Bus System Message Bus.
[  OK  ] Stopped Lightning Fast Webserver With Light System Requirements.
[  OK  ] Stopped Provides static IP address.
[  OK  ] Stopped Intel_XDK_Daemon.
[  OK  ] Stopped Serial Getty on ttyS1.
[  OK  ] Stopped Getty on tty1.
[  OK  ] Removed slice system-serial\x2dgetty.slice.
[  OK  ] Removed slice system-getty.slice.
         Stopping Permit User Sessions...
         Stopping Zero-configuration networking...
[  OK  ] Stopped Zero-configuration networking.
[  OK  ] Stopped Permit User Sessions.
[  OK  ] Stopped target Remote File Systems.
         Stopping Connection service...
[  OK  ] Stopped Connection service.
[  OK  ] Stopped target Basic System.
[  OK  ] Stopped target Slices.
[  OK  ] Removed slice User and Sessions Slice.
[  OK  ] Stopped target Paths.
[  OK  ] Stopped target Timers.
[  OK  ] Stopped target Sockets.
[  OK  ] Closed sshd.socket.
[  OK  ] Closed Avahi mDNS/DNS-SD Stack Activation Socket.
[  OK  ] Closed D-Bus System Message Bus Socket.
[  OK  ] Stopped target System Initialization.
         Stopping Network Time Synchronization...
         Stopping Update UTMP about System Boot/Shutdown...
         Stopping Load/Save Random Seed...
         Stopping Apply Kernel Variables...
[  OK  ] Stopped Apply Kernel Variables.
         Stopping Load Kernel Modules...
[  OK  ] Stopped Load Kernal Modules.
[  OK  ] Stopped target Swap.
[  OK  ] Stopped Network Time Synchronization.
[  OK  ] Stopped Update UTMP about System Boot/Shutdown.
[  OK  ] Stopped Load/Save Random Seed.
         Stopping Create Volatile Files and Directories...
[  OK  ] Stopped Create Volatile Files and Directories.
[  OK  ] Stopped target Local File Systems.
         Unmounting /media/card...
         Unmounting /var/volatile...
         Unmounting Temporary Directory...
[  OK  ] Unmounted /media/card.
[  OK  ] Unmounted /var/volatile.
[  OK  ] Unmounted Temporary Directory.
[  OK  ] Reached target Unmount All Filesystems.
[  OK  ] Stopped target Local File Systems (Pre).
         Stopping Create Static Device Nodes in /dev...
[  OK  ] Stopped Create Static Device Nodes in /dev.
         Stopping Remount Root and Kernel File Systems...
[  OK  ] Stopped Remount Root and Kernel File Systems.
[  OK  ] Reached target Shutdown.
[   78.279739] systemd-shutdown[1]: Sending SIGTERM to remaining processes...
[   78.329902] systemd-journald[64]: Received SIGTERM from PID 1 (systemd-shutdow).
[   78.348922] systemd-shutdown[1]: Sending SIGKILL to remaining processes...
[   78.393224] systemd-shutdown[1]: Unmounting file systems.
[   78.401045] systemd-shutdown[1]: Unmounting /sys/fs/fuse/connections.
[   78.407885] systemd-shutdown[1]: Unmounting /sys/kernel/debug.
[   78.414124] systemd-shutdown[1]: Unmounting /dev/hugepages.
[   78.420124] systemd-shutdown[1]: Unmounting /dev/mqueue.
[   79.398589] systemd-shutdown[1]: All filesystems unmounted.
[   79.404790] systemd-shutdown[1]: Deactivating swaps.
[   79.410093] systemd-shutdown[1]: All swaps deactivated.
[   79.415459] systemd-shutdown[1]: Detaching loop devices.
[   79.426452] systemd-shutdown[1]: All loop devices detached.
[   79.432248] systemd-shutdown[1]: Detaching DM devices.
[   79.438692] systemd-shutdown[1]: All DM devices detached.
[   79.450717] systemd-shutdown[1]: Rebooting.
[   79.459104] Restarting system.
[   79.462283] reboot: machine restart
```

***

<h2 id="Debian-Galileo">
Running Debian GNU/Linux on Intel Galileo
</h2>
