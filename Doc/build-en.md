# ErgoDash Build Guide
**Feel free not to read completely, but pay attention when installing the Pro Micro!!!!!!**
Note: The below diagrams are for rev 1.1. For rev 1.2. and up, the part placement is slightly different.

Translated, with extra build notes (From: build.md https://github.com/omkbd/ErgoDash/commit/d12e8f7fd414fe89d38b77b3b0e6a0af4b639a47)

## Overview
<img width="700" alt="assembly" src="https://github.com/omkbd/picture/blob/master/assembly.png">

## 0 Preparation
Remove extra thumb key section if desired.
<img width="700" alt="PCBcut" src="https://github.com/omkbd/picture/blob/master/PCB_cut.jpg">
carefully break by hand


**Note:
Components in steps 3-6 and 10 must be inserted on the bottom of the board.
Components in steps 1 and 2 can be installed on the top or bottom.**

## 1 Install Diodes
When installing diodes the black stripe is towards the square pad
(diodes are all 1 square 1 round pad)
(resistors are all both round pad)
<img width="400" alt="diode" src="https://github.com/omkbd/picture/blob/master/Build_Diode.jpg">

Note the positions of diodes and resistors to avoid mistakes
<img width="700" alt="diode" src="https://github.com/omkbd/picture/blob/master/diode_complete.jpg">

**Rev 1.2 positions are changed as below.**
<img width="700" alt="diode" src="https://github.com/omkbd/picture/blob/master/ergodash-rev1.2-PCB.png">

## 2 Backlight LED [optional]
Install the MOSFET (Install note/suggestion: pre-soldering the single pad worked well)
Install 1kΩ resistor in silk rectangle as noted 。(Silk screen notation is improved on rev 1.2 [BL1k])
<img width="400" alt="1k" src="https://github.com/omkbd/picture/blob/master/1k_FET.jpg">

Install 470Ω resistors
<img width="700" alt="470" src="https://github.com/omkbd/picture/blob/master/Resistor.jpg">

-Note: Photo has a few surface mount resistors combined with through-hole
**(Rev 1.1) For the resistor found under the pro-micro: a surface mount resistor, or installing resistor on opposite side may be preferred to prevent interference (moved in rev 1.2)**

## 3 TRRS Jack
Install the TRRS Jack as indicated by the silkscreen.

## 4 Install reset switch
At the top of the board there are 2 locations for the pro-micro.
Pro Micro will be installed where the rectangular outline is printed
Reset switch is installed where the rectangular outline is not seen
Compare with photo on Step 6

## 5 Underglow LED [optional]
Choose which of the pair (left or right) will be master (where the USB cable will be attached), and solder the jumpers as below.
The board in the photo below has the jumpers soldered for left hand master. The left hand board is on the right, and the right hand board is on the left.
In the two diagrams, the upper image is for left hand master (labelled 左マスター), and the lower image is for right hand master (右マスター).
<img width="700" alt="jump" src="https://github.com/omkbd/picture/blob/master/Jump.jpg">

Install LED WS2812B
**IMPORTANT**
-On Master half, LED corner will Match the silkscreen
-On Slave half, LED corner needs to be 180 from silkscreen

-Installation notes:
  -use tape to hold in place, solder one side, remove tape, then solder other
  -Notes from first time soldering with these LED:
    -I attempted to pre-solder pads with bad results (As recommended for other surface mount I did before)
    -Leaving iron on too long appeared to melt the casing of the LED (Use fine tip if you have it? I didnt)
    -1sec on pad to pre-heat, then off and come back with iron and solder is what worked best for me

<img width="400" alt="RGB_Left" src="https://github.com/omkbd/picture/blob/master/RGB_Left.jpg">
<img width="700" alt="RGB_Left_Finish" src="https://github.com/omkbd/picture/blob/master/RGB_Left_Finish.jpg">

## 6 Pro Micro header  and reset switch installation
Attach Headers where you see the rectangular outline on silkscrean  (It is in the correct position on each side of the board)
**Do Not attach Pro Micro Yet**
When using spring headers, soldering the header to the board is unnecessary.

<img width="700" alt="pin" src="https://github.com/omkbd/picture/blob/master/pin.jpg">

## 7 Install Stabilizer （rev 1.2 or Later only）[optional]

(I used Rev 1.1 without Stabilizers, translation below)

If you will be using 2U keycap(s), then attach the stablizer(s). (If necessary; it's not always required).
**Note: Once the switch is installed, it's no longer possible to attach the stabilizer.**
Put together and attach as shown below.
<img width="400" alt="assembly" src="https://github.com/omkbd/picture/blob/master/Stabilizer.png">
If you're concerned about the noise of the stabilizer then apply grease (not included in kit).

## 8 Install Switches and Plate
Make sure all other components are installed before adding switches.
Place the plate with keyholes over top the PCB and snap in and solder switches.
Start with 4 corners in the plate to ensure alignment.
After the first 4 are soldered in, install remaining switches.

<img width="700" alt="switch" src="https://github.com/omkbd/picture/blob/master/switch.jpg">
<img width="700" alt="switch_complete" src="https://github.com/omkbd/picture/blob/master/switch_complete.jpg">

## 9 Backlight LED Install [optional]
Install the LEDs from the top on each switch
Round Pad  anode（＋）(Long LED Leg)
Square Pad  cathode（-) (Short Leg)
-Can be installed later (Except for the LED under pro-micro)

## 10 Pro Micro Install
**Before proceding connect the Pro Micro to a PC via USB and confirm it's working.**
-Confirm the TX0 lines up (USB port sandwiched between both PCBs)
-Check that all solder connections underneath the Pro Micro are done.
-Confirm no contact between Pro Micro and components (add insulating tape if desired)
-For spring headers, solder is required on the Pro Micro side.
-After installation, confirm the Pro Micro is properly seated. If not, cut the legs of the switch under the Pro Micro slightly.
-Trim headers after testing.

## 11 Case Assembly
Install the 5mm and 6mm spacers from the top。

<img width="700" alt="spacer" src="https://github.com/omkbd/picture/blob/master/spacer.jpg">

Install 5mm and 8mm screws according to the diagram。

<img width="700" alt="case" src="https://github.com/omkbd/picture/blob/master/case.jpg">

Install Rubber feet

<img width="700" alt="gom" src="https://github.com/omkbd/picture/blob/master/gom.jpg">

## 12 Firmware

Note: PCB Rev 1.1, 1.2 are QMK Rev2 firmware  (Rev1 (in QMK) PCB was not published)

QMK Build Guide
https://docs.qmk.fm/#/getting_started_build_tools

ErgoDash Firmware
https://github.com/qmk/qmk_firmware/tree/master/keyboards/ergodash

Attach the keycaps, and you're done!!!!!

<img width="700" alt="finish" src="https://github.com/omkbd/picture/blob/master/finish.jpg">
