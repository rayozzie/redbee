#RedBee project
![RedBee Front](https://github.com/CascoLogix/RedBee/blob/master/Rendered_Pics/Bare_PCB/RedBee_Front_Bare_small.png "RedBee Front")
![RedBee ISO](https://github.com/CascoLogix/RedBee/blob/master/Rendered_Pics/Bare_PCB/RedBee_Front_ISO_Bare_small.png "RedBee ISO")

##About the RedBee project
RedBee was developed in support of [Safecast](http://blog.safecast.org/), a global volunter-centered citizen science project working to empower people with data about their environments. More specifically, it is made for integrating with Safecast's [bGeigie Nano](http://blog.safecast.org/bgeigie-nano/). 

##What does the RedBee do?
The RedBee allows for simple adaptation of the [RedBear BLE Nano](http://redbearlab.com/blenano/) to the bGeigie Nano XBee socket for integrating Bluetooth Low Energy functionality. The ReadBear BLE Nano uses Raytac's MDBT40 Bluetooth 4.0 radio module. Read more about Raytac's MDBT40 [here](https://www.nordicsemi.com/eng/Products/Bluetooth-Smart-Bluetooth-low-energy/nRF51822).

##What else can the RedBee be used for?
The RedBee also makes it easy to connect the [RedBear BLE Nano](http://redbearlab.com/blenano/) to any standard XBee socket where a standard UART communication interface is needed. The UART communication interface signals are (DTE perspective):
* TX: Transmit. The TX pin on the RedBee is an output (driver).
* RX: Receive. The RX pin on the RedBee is an input (high impedance).
* CTS: Clear-To-Send. The CTS pin on the RedBee is an output (driver).
* RTS: Request-To-Send. The RTS pin on the RedBee is an input (high impedance).

Custom firmware can be developed for the RedBear BLE Nano using the mbed's online IDE (Integraged Development Environment); however, the RedBear BLE Nano cannot be programmed directly from the RedBee PCB with the mbed IDE. Instead you must use RedBear Lab's USB adapter for programming. Alternatively, since the Raytac MDBT40 supports wireless DFU (device firmware update) over bluetooth, and therefore the ReadBear BLE Nano, this feature can be used for updating firmware wirelessly while in the RedBee configuration.

##How do I get a RedBee PCB?
There are a few options for getting the RedBee PCB:
* Use latest version of gerber files (PCB fabrication files) archived in this respository under RedBee/Hardware/Gerbers/Archive. 

   Note: these files can be sent to any PCB fabricator to build. You will have to specify the soldermask color, red. Some PCB fabricators only offer certain soldermask colors. Most commonly, unspecified soldermask color will be green. OSH Park, for example, uses only their signature color, purple.
* Buy from [Casco Logix](http://www.cascologix.com/store/p33/RedBee.html) on the Casco Logix store page.
* Buy from Casco Logix on [Tindie](https://www.tindie.com/stores/CascoLogix/).

##What headers should I use for the RedBee?
1. XBee Header [Harwin M22-2511005](http://www.digikey.com/product-detail/en/harwin-inc/M22-2511005/952-1316-ND/2264297)
2. RedBear BLE Nano Header [Sullins PPTC061LFBN-RC](http://www.digikey.com/product-detail/en/sullins-connector-solutions/PPTC061LFBN-RC/S7004-ND/810145)

   Note: this header is optional. The ReadBear BLE Nano can be mounted directly to the RedBee PCB for more permanent and lower-profile needs.

##Working with the RedBee native design files
RedBee was designed using [KiCAD](http://kicad-pcb.org/). KiCAD is an open source EDA (Electronic Design Automation) software package that supports multiple schematic pages, unlimited PCB outline, up to 32 PCB layers and gerber file output for free! 

All of the native KiCAD design files can be found in this repository under RedBee/Hardware/EDA. The schematic and PCB library files for both the XBee 2mm male pin headers and the RedBear BLE Nano 100mil female headers will not be found in the KiCAD default libraries included with the KiCAD install. Instead, the PCB footprints can be found in this repository under RedBee/Hardware/EDA/Footprint_Archive.pretty. The schematic should open and display the original schematic component decals without any manual intervention, as these decals are archived in the *-cache.lib file in the EDA directory. Once the schematic is opened, these decals can be saved to your own schematic library if desired.
