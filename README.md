# Phys-Index-EyetrackVR-HW
Custom solution for a clean, unobtrusive, EyetrackVR installation in the **Valve Index**.  

Everything fits entirely within the envelope of the Valve Index. No modifications to the Valve Index headset are required whatsoever; just some clever cable routing. 

![PXL_20231018_00404763e3](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/8c080cf6-a962-46f6-8bd3-6d09f6639588)

# Build It! 

## Camera and LED mounts
An evolution of bitbyt3r's index-eyetrackvr mounts for the Valve Index found here: https://github.com/bitbyt3r/index-eyetrackvr  

![ring1](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/75ffa358-d365-4c69-a2b8-b3b5f11d3ec9)

### Changes:
- Lowered all leds 0.5mm further from face.
- Thickened up thin points near LEDs so they are FDM-printable in a single fill-line.
- Chamfers and fillets for strength and comfort.
- Tweaked the fit on the LED posts to prevent binding on solderless kits.
- Moved the leds on brow and nose around slightly to fit my face better.
### Tips:
- Print in black PETG
- Mirror the provided file for the opposite eye
- If you need to extend the wires by about, stagger your cuts to prevent the joints from ever touching.
![image](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/733aed90-dc2c-43e0-855d-7d30ac13537b)


## Gum Stick USB Hub Dongle
Built around a specific ultra-slim 3-port USB hub. Fits two XIAO ESP32-S3s and a ETVR v4 PCB, as well as a spare USB port.

![PXL_20231018_0040476332](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/da7355d1-1a2c-4d7f-8379-2673ab07c646)

### You need this specific USB hub (various brands)
Found on the likes of Amazon and Aliexpress. Its easy to modify for our purpose.

![image](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/8e3a4ef0-a15b-4418-8a45-440920a90913)
#### common titles:
- "USB Hub 3.0 Extender 3-Port, sartyee Computer Networking Hubs for MacBook, Mac Pro, iMac, Ps4/5, Surface Pro,Flash Drive, Keyboard, Mouse, Windows"
- "3 Ports Multiple Expander with 1 USB3.0 and 2 USB2.0 Ports Type-C3.0/USB3.0 To 3USB HUB Ultra Slim Splitter 480Mbps-5.0Gbps"
- "3 Port USB 3.0 USB Hub 2.0 Multi Type-C Ultra Slim Splitter Hub Use Power Adapter Multiple Expander 2.0 USB 3.0 Hub for PC"
#### Links:
- Amazon: https://www.amazon.com/gp/product/B0BQ68QGYJ/  
- Aliexpress (choose the normal USB version): https://www.aliexpress.us/item/3256805344126437.html

### You want these other parts too
- 2x XIAO ESP32-S3 Sense Modules - https://www.seeedstudio.com/XIAO-ESP32S3-Sense-p-5639.html
- 1x Solder-less V4 kit - https://store.eyetrackvr.dev/products/v4-mini-fully-solderless-kit
- Misc 28-32AWG wire for lengthening LED power wires
- 7x M2x5mm Countersink Self-tapping screws
- 2x OV2640 160 degrees night version camera module 200MM (select 200MM night vision) - https://www.aliexpress.us/item/3256803720134565.html
![image](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/6d43e56d-f3b4-4b63-8018-cfa709f892cf)

Additional hardware options with more links available in the EyetrackVR docs: https://docs.eyetrackvr.dev/how_to_build/parts_list

## Assemble it!
Follow the EyetrackVR docs for primary assembly and programming: https://docs.eyetrackvr.dev/how_to_build/full_build

Steps specific to the dongle are as follows.

### Print 
- Print all 3 parts in PETG
- Refer or use the "PRINT ME" file for suggest orientations.
- ENABLE SUPPORT MATERIAL but dont support bridges!

### Mod the hub
- Take the aforementioned USB hub apart and de-solder all the connectors. Save at least one of the small USB 2.0 ones.
![image](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/3a32afaa-90f1-43b7-b7e9-bd138087fbd3)

### Place
- Insert your dismantled USB hub into the dongle along with the spare USB port.
- Verify that your XIAO ESPs and ETVR v4 PCB fit in their slots. It may be tight, but if not, use adheasives.

### Solder
- Solder your VUSB, GND, D+ and D- wires to your ESPs now.
- Solder 2 wires to the bottom side of the ETVR v4 PCB for power
- Route them like so. A small hole will let you route the ETVR v4 PCB wires into the main cavity.
![image](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/ebd1d97f-1db6-4820-9f7b-50051227cad2)
![image](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/52638c85-f386-4deb-83b4-8d3549d063b0)

### Cable Routing

### Finalizing


