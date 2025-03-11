# Renz-Index-EyetrackVR-HW
Custom solution for a clean, unobtrusive, EyeTrackVR installation in the **Valve Index**.

### Project Details:
- Based on the origional Gumstick by **Physics Dude** https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW.
- Remix includes slots for 3x XIAO ESP32-S3 Sense Modules - 2x for Eye Track VR and 1x for Project Babble.
- A smaller all-in-one USB Hub pcb board is used in place of the origional Gumstick version, benifits from no dissasembly required.
- Optional USB-C port at the end, allows for the use of the origional HTC Vive Mouth Tracker or other devices like wired headphones.
- Custom, highly iterated camera and LED mounts based on bitbyt3r's design that may be preferable to any builder, Supports most OV2640 cameras with an 8mm square & 2mm tall base.

Everything fits entirely within the envelope of the Valve Index. No modifications to the Valve Index headset are required whatsoever; just some clever cable routing. 

![newnewnewnwe](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/77e4141b-7da7-4cb3-ab16-d8d761c91930)

# Build It! 

## Camera and LED mounts
An evolution of bitbyt3r's index-eyetrackvr mounts for the Valve Index found here: https://github.com/bitbyt3r/index-eyetrackvr  

![cad-shot](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/2cbf5d3a-373e-462f-b100-7af70c85c683)

Light pattern:
![image](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/b65318e4-dffa-4f31-8510-e072caaddef4)

### Changes:
- Lowered all leds 0.5mm further from face.
- Thickened up thin points near LEDs so they are FDM-printable in a single fill-line.
- Chamfers and fillets for strength and comfort.
- Tweaked the fit on the LED posts to prevent binding on solderless kits.
- Moved the camera up to the side of the eye.
- Moved the all the LEDs to a more optimal position to prevent specular reflections, shadows, and silhouetting.
### Tips:
- Print in black PETG
- Mirror the provided file for the opposite eye
- If you need to extend the wires a bit, stagger your cuts to prevent the joints from ever touching.

## Gum Stick USB Hub Dongle
Built around a specific ultra-slim 3-port USB hub. Fits two XIAO ESP32-S3s and a ETVR v4 PCB, as well as a spare USB port.

![PXL_20231018_0040476332](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/da7355d1-1a2c-4d7f-8379-2673ab07c646)

### You need this specific USB hub (various brands)
Found on the likes of Amazon and Aliexpress. Its easy to modify for our purpose.

![image](https://github.com/user-attachments/assets/bdcc733b-51bd-4ede-82bb-b1b84189679e)

#### Common Titles:
- "USB Hub 3.0 Extender 3-Port, sartyee Computer Networking Hubs for MacBook, Mac Pro, iMac, Ps4/5, Surface Pro,Flash Drive, Keyboard, Mouse, Windows"
- "3 Ports Multiple Expander with 1 USB3.0 and 2 USB2.0 Ports Type-C3.0/USB3.0 To 3USB HUB Ultra Slim Splitter 480Mbps-5.0Gbps"
- "3 Port USB 3.0 USB Hub 2.0 Multi Type-C Ultra Slim Splitter Hub Use Power Adapter Multiple Expander 2.0 USB 3.0 Hub for PC"
#### Links:
- ~~Amazon: https://www.amazon.com/gp/product/B0BQ68QGYJ/~~ (Listing updated and now shows similar but different product.)
- Amazon: https://www.amazon.com/YaimhSound-Extender-Splitter-Extension-Keyborad/dp/B0BXJ21DXZ
- Aliexpress (choose the normal USB version): https://www.aliexpress.us/item/3256805344126437.html
#### Note/Avoid: 
- Avoid similar looking USB hubs with an LED indicator present between the two side-mounted ports. These likely won't fit since the PCB design on these seems to be flipped. If you do come across one such USB hub, consider using the (currently untested) no-spacer alternitive which gives you about 1mm of room to route soldered wires under the hub's PCB. [Gum Stick Dongle Custom USB Hub Case/No-Spacer alternate - XIAO-ESP32S3 ETVR v4 gum stick index mount v24.stl](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/blob/main/Gum%20Stick%20Dongle%20Custom%20USB%20Hub%20Case/No-Spacer%20alternate%20-%20XIAO-ESP32S3%20ETVR%20v4%20gum%20stick%20index%20mount%20v24.stl) 

### You want these other parts too
- 2x XIAO ESP32-S3 Sense Modules - https://www.seeedstudio.com/XIAO-ESP32S3-Sense-p-5639.html
- 1x Solder-less V4 kit - https://store.eyetrackvr.dev/products/v4-mini-fully-solderless-kit
- Misc 28-32AWG wire for lengthening LED power wires
- 7x M2x5mm Countersink Self-tapping screws
- 2x OV2640 160 degrees night version camera module 200MM (select 200MM night vision) - https://www.aliexpress.us/item/3256803720134565.html - https://www.aliexpress.us/item/3256804483974787.html
  
![image](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/6d43e56d-f3b4-4b63-8018-cfa709f892cf)

Additional hardware options with more links available in the EyeTrackVR docs: https://docs.eyetrackvr.dev/how_to_build/parts_list

## Assemble it!
Follow the EyetrackVR docs for primary assembly and programming: https://docs.eyetrackvr.dev/how_to_build/full_build

Steps specific to the dongle are as follows.

### Print 
- Print all 3 parts in PETG
- Refer or use the "PRINT ME" file for suggested orientations.
- ENABLE SUPPORT MATERIAL on build plate only.

### Mod the hub
- Take the aforementioned USB hub apart (it slides out when you plug something in the end with a little force) and de-solder all the connectors. Save at least one of the small USB 2.0 ones.
- If the case is stuck, you may have to get a Dremel or some snips and nip away at the corners, careful not to cut the PCB.
- I suggest using a hot air tool if possible. Adding your own flux and leaded solder will make desoldering easier too regardless.

![Untitled-1pin](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/575eaa7e-68a8-4790-8bea-ba3762f84eda)

### Place
- Insert your dismantled USB hub into the dongle along with the spare USB port. Make sure you removed all the support material in that cavity. 
- Verify that your XIAO ESPs and ETVR v4 PCB fit in their slots. It may be tight, but if not, use adhesives. Careful not to crush the ESP's buttons or riser connector!
  
![image](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/74e7402d-450c-492f-b3a7-142a5baf3cda)

### Solder
- Solder your VUSB, GND, D+ and D- wires to your ESPs now.
- Use the square ground pad on the bottom of the XIAO ESP for ground (not the GND pin on the edge of the board). 
- Observe the Connector orientation of the original USB hub and refrence it to a pin-out diagram of the USB A port. 
- Solder 2 wires to the bottom side of the ETVR v4 PCB for power. (and led wires for solder-kit)
- Route them like so and solder in place. A small hole will let you route the ETVR v4 PCB wires into the main cavity.
  
![image](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/ebd1d97f-1db6-4820-9f7b-50051227cad2)
![image](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/52638c85-f386-4deb-83b4-8d3549d063b0)

- quick wiring diagram to mitigate confusion
![image](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/c227dea9-11b9-47e1-90f2-7a918ab716e7)

### LEDs!
- You will follow the instructions in the ETVR docs and lengthen a couple of the wires with 36-32awg wire.
- The long main feed wires get extended to about 200-250mm, while two of the shorter wires get extended to about 80mm.
- Tip: Stagger your cuts when lengthening your wires so the soldered ends can never touch.

- Once you verify everyhting is working 100%, it might be a good idea to remove the unused connectors on the E/End LEDs. You can do this with a pair of snips and a soldering iron with fresh solder.  

![image](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/80250e8e-1768-4d3f-9a32-dec9507a6a59)

(early version of the modified mounts)
![image](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/bbc47e03-1810-4876-a0a2-2518bddf8ec5)

(latest version close up, installed )
![anotehr-new-bpic](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/07cc44d5-29f0-4d2c-a342-a5a05c0465dd)

### Cable Routing
- Your 200mm camera ribbons can be pushed up the "nose" of the headset and around the top of the PCB.

![PXL_20231018_004047633s](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/fd6dcf94-8be5-466a-bdce-bf8423faa027)

- They may seem to interfere with IPD adjustment, but try folding them so they take a twist as they travel behind the PCB and between the screens. Keep in mind you may loose a couple millimeters of IPD due to the LED placement when using solder-less kit.
- Then they can be massaged through the vent holes in the frunk along with the extended LED power wires.

![image](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/c754b300-ecd5-4464-b1a7-9f2dc4894f6c)

- It might help to gently fold your ribbon cable like so to get it to fit in the frunk vent holes. Note that some vent slots are blocked when assembled. 

![image](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/569eec91-3671-47af-9a7f-06ae1c785979)

- Pinch point! Watch here when the face pad is mounted. It's possible the ribbon cable can get trapped under this lip when adjusting screen-face distance. A small bend in the wire will teach it to stay away.
  
![pibce](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/e1828f6e-10d7-4bcf-89d2-83165ef862a6) 

- I also found that folding the camera ribbons like so can help teach them where to go.
  
![teach](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/0105fbfa-9eca-46bd-bde5-11b6f7d56244)

### Finalizing
- Plug everything in and secure the optional covers with M2x5mm Countersink Self-tapping screws.

![image](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/67f0c657-843d-442d-97dd-5f78bee0b4ff)
![image](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/c9c60c26-1061-466f-9613-d339a1038839)

- Use a Command Strip or piece of foam to ensure dongle does not come out during extreme VR stunts.
- Big nose? Consider removing the unused connector on the End LED if you expierence contact in that area. Felt may also be added for comfort.
![nose-bridge](https://github.com/user-attachments/assets/d6a93981-08d7-492f-8305-4b4bf575e079)



  
### Camera mount for Babble Face Tracking (uses same ESPs and Cameras)
- This part is in development, but working nicely from the start. You'll have to observe the pictures below to duplicate the build for your specific hardware.
- P.S. Did you notice the holes for a 25mm fan? Is optional, but there if you want to keep your ESPs chilly. 

![image](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/29765642-3fc5-432b-9d63-2af36fa26830)
![image](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/9c8fe1c3-a4ec-45bc-9c82-ff1429f1dfdb)
![extendd-mount](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/b6fd199d-d946-452a-a171-8b34abbd3bb7)
![image](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/assets/22563517/83e07ad4-2e42-403c-8994-e89f234fe881)


## In (experimental) summary:
- Use the same XIAO ESPs, with the same OpenIris firmware as the eye trackers.
- Use the same 200mm long OV2640 160 degrees night version IR camera module.
- Use two 3mm IR LEDs wired in series with a 100R resister on the 5v VBUS rail (use the 3V3 rail or a larger value resistor if you have more efficient LEDs). I sanded the lenses down on my leds for a wider, softer spread as well. 
- 3D print the print file in the Babble Face Tracker Cam-LED Mount folder with support material enabled. (EXTENDED version also available, print both to see what works for you)
- Stick camera mount base and cable clip to your Valve Index with double-sided VHB tape as shown.
- Use a 25mm countersink M3 screw with lock nut for the hinge.
- XIAO ESP can be placed at the end of the Gum Stick with more VBH tape.


