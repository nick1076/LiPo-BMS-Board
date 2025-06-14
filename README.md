# 3.7V LiPo BMS
This repository contains all files for this project. The 3.7V LiPo BMS Board is a PCB that takes power from a USB-C port and charges a 3.7V LiPo battery.

Both battery terminals are soldered to the bottom side of the board via two SMD pads.

This project is intended not as a standalone board itself board but rather as a test of the BMS system I designed. The goal is to have a fully functional BMS system that once working I can then impliment into other project PCBs by copying the files over.

This BMS is capable of proper load sharing from the USB-C power source (when present), charging the battery via USB-C while also powering the circuit's load also via USB-C when present and not from the battery. This means when USB-C power is present, the load will draw current from USB-C, not the battery, and the battery will also charge via USB-C at the same time. Once unplugged, a P-type MOSFET gate is pulled LOW and allows the load to draw current from the LiPo as USB-C power is no longer present.

Additionally, the board hosts a status LED indicating whether the LiPo is properly charged or not.

Finally, the board is designed to be as compact and efficient as possible. The circuit steps down the 4.2V to 3.5V battery output to 3.3V at high efficiency using a buck converter. Additionally, components utilized are in small SMD packages and utilize both sides of the board, resulting in a very small overall circuit size. Lastly, the board features 2 M1 bolt mounting holes if mounting is needed.

DigiKey BOM link: https://www.digikey.com/en/mylists/list/CX3XVJEASW