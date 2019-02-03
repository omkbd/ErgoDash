# ErgoDash Build Guide
Note image below showing movement of some parts between Rev.1.1 and Rev.1.2

Translated using Microsoft Translate, and adding my own notes after completing assembly. ( Feb 2, 2019)

## Overview
<img width="700" alt="assembly" src="https://github.com/omkbd/picture/blob/master/assembly.png">  



## 0 Preparation
Remove Extra thumb key section if desired  
<img width="700" alt="PCBcut" src="https://github.com/omkbd/picture/blob/master/PCB_cut.jpg">  
carefully break by hand 


**Note: (Translation note, Pretty sure this is what the note was trying to say seems right)  
Components in Steps 3-6 and 10 must be inserted on the bottom of the board.   
Components in steps 1 and 2 can be installed on top or bottom.**

## 1 Install Diodes
When installing Diodes the black stripe is towards the square pad  
(Diodes are all 1 square 1 round pad)  
(Resistors are all both round pad)  
<img width="400" alt="diode" src="https://github.com/omkbd/picture/blob/master/Build_Diode.jpg">  

Note the positions of Diodes and resistors to avoid mistakes  
<img width="700" alt="diode" src="https://github.com/omkbd/picture/blob/master/diode_complete.jpg">  

**Rev1.2 Some positions have changed**  
<img width="700" alt="diode" src="https://github.com/omkbd/picture/blob/master/ergodash-rev1.2-PCB.png">  

## 2 [Option] Backlight LED
Install the MOSFET (Install note/suggestion: pre-soldering the single pad worked well)  
Install 1kΩ resistor in silk rectangle as noted 。(Silk screen notation is improved on Rev1.2 [BL1k])   
<img width="400" alt="1k" src="https://github.com/omkbd/picture/blob/master/1k_FET.jpg">  

Install 470Ω  resistors  
<img width="700" alt="470" src="https://github.com/omkbd/picture/blob/master/Resistor.jpg">  

-Note: Photo has a few surface mount resistors combined with through-hole   
**(Rev 1.1) For the resistor found under the pro-micro: a surface mount resistor, or installing resistor on opposite side may be preferred to prevent interference (moved in Rev1.2)**

## 3 TRRS Jack 
Install TRS Jack as indicated by the silkscreen

## 4 Install reset switch
At the top of the board there are 2 locations for the pro-micro.  
Pro Micro will be installed where the rectangular outline is printed  
Reset switch is installed where the rectangular outline is not seen  
Compare with photo on Step 6  

## 5 [Option] Undergrow LED 
-You must choose which side will be master now, before installing all the LED WS2812B  
(Translator doesn't have this working correctly, I installed all LEDs according to silkscreen which is WRONG, and the board would not work at all with both halfs connected with solder bridge in place)

(MS Translate) Left and right both to master (it points to the USB) decided, the jump in the solder.

Left Hand as master is shown soldered in the image below  
(Image Text Note:  First line matching the photo is Left Hand Master, Second line is for right hand master)  
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
(MS Translate) If you are using the spring pin head is no soldering on the Board side.

<img width="700" alt="pin" src="https://github.com/omkbd/picture/blob/master/pin.jpg">  

## 7 [Option] Install Stabilizer （Rev.1.2 or Later only）
 
(I used Rev 1.1 without Stabilizers, Pasting Microsoft translate version as is)

Install the stabilizers before installing the acrylic plate and switch to use U 2 caps. (Is not always necessary. )
Switch will no longer install stabilizers.
To assemble and install.  

<img width="400" alt="assembly" src="https://github.com/omkbd/picture/blob/master/Stabilizer.png">  
If you care about sound stabilizer grease. (Not included in the Kit. )  


## 8 Install Switches
Make sure all components are other components are installed before adding switches   
Start with 4 corners in the plate to ensure alignment.  
After the first 4 are soldered in, install remaining switches.  

<img width="700" alt="switch" src="https://github.com/omkbd/picture/blob/master/switch.jpg">  
<img width="700" alt="switch_complete" src="https://github.com/omkbd/picture/blob/master/switch_complete.jpg">  

## 9 [Optional] Backlight LED Install 
Install the LEDs from the top on each switch  
Round Pad  anode（＋）(Long LED Leg)  
Square Pad  cathode（-) (Short Leg)    
-Can be installed later (Except for the LED under pro-micro)

## 10 Pro Micro Install
**Before installing Pro Micro check the following:**
-confirm TX0 lines up (USB port sandwiched between both pcb)  
-Check all solder connections under pro-micro are done   
-Confirm no contact between Pro micro and components (add insulating tape if desired)  
-(From MS Translate not sure) If you are using spring head Pro Micro side solder. Cut the check and when I installed Pro Micro scum, scum under the Pro Micro switch legs a little bit.  
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


-Finished-

<img width="700" alt="finish" src="https://github.com/omkbd/picture/blob/master/finish.jpg">  
