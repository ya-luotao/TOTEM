# TOTEM BUILD GUIDE

## PART LIST

### REQUIRED PARTS

| Part name       | Count | Remarks | 
| :-------------- | :---: | :------ |
| TOTEM PCB       | 01 | You can find the files for it [here](/PCB/) |
| Seeed XIAO      | 02 | You can choose between the BLE version (wireless) or the RP2040 version (wired) |
| Choc key switch | 38 | Kailh Choc low profile keyswitches |
| diodes 1N4148W  | 38 | These are surface mount diodes in SOD123 package |
| 1u Choc keycaps | 38 | You can use the black or white keycaps from Kailh, but I recommend MBK, LDSA or CFX keycaps |
| reset button    | 02 | Alps SKHLLCA010 |
| USB-C cable     | 01 | For connecting the keyboard with your PC |
| power switch    | 02 | MSK12C02 (only required for the bluetooth build) |
| Lipo battery    | 02 | There is space for a 15 x 22 x 7.5 mm battery (only required for the bluetooth build) |
| TRRS jack       | 02 | (only required for the wired build)|
| TRRS cable      | 01 | Alternatively, you can use a TRS cable for [half-duplex](https://github.com/qmk/qmk_firmware/blob/master/docs/serial_driver.md#usart-half-duplex) (only required for the wired build)|


### OPTIONAL PARTS

| Part name              | Count | Remarks | 
| :--------------------- | :---: | :------ |
| switch socket          | 38 | Switch sockets for Kailh choc switches |


### 3DP CASE PARTS

| Part name              | Count | Remarks | 
| :--------------------- | :---: | :------ |
| 3D printed case        | 02 | Find the case files [here](/case) |
| 7mm M2 standoffs       | 08 | 7mm standoffs for screwing top and bottom of the case together |
| 6mm M2 countersunk screws | 16 ||


## INTRODUCTION

Here is an overview of where and on which side each component needs to be soldered (click on the image to see a larger version).

![TOTEM solder guide](/docs/images/TOTEM_solderguide.png)


***

## BREAK OFF HALVES




***

## DIODES

The diodes needs to be soldered on the bottomm of the PCB. Pay attention to their orientation:  They have a small line on one side, which should be on the side the arrow on the PCB is facing to.

<p align="center">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="/docs/images/buildguide/diodes_dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="/docs/images/buildguide/diodes_bright.svg">
  <img alt="diode orientation" src="/docs/images/buildguide/diodes_dark.svg">
</picture>
</p>

Apply a small amount of solder on one pad.

![Solder on one pad](/docs/images/buildguide/diode_solder_pad.jpg)


Then use tweezers to place the diode on the pads and reheat the solder to secure the diode.

![Solder diode](/docs/images/buildguide/diode_in_place.jpg)


Now you can solder the second pad.

***
 
## SWITCH SOCKETS (optional)

Here you can apply the same technique as used for the diodes: Apply some solder on one of the pads first.

![switch sockets pad](/docs/images/buildguide/switch_pad.jpg)


Then place the switch socket in the silk screen markings and reheat the solder. Apply some pressure with a pair of tweezers to make sure the socket is fully seated.\
Now solder the second pad.

![switch socket soldered](/docs/images/buildguide/switchsocket.jpg)

***

## POWER SWITCHES (only required for bluetooth build)

Apply a tiny bit of solder on one of the bigger, outer pads on top of the PCB. The power switch has some tiny knobs on its bottom, which fits into the PCB holes. Hold it in place with tweezers and than reheat the solder on the pad. After this you can solder the other pad and the three pins.

![power switch](/docs/images/buildguide/power_switch.jpg)


***

## RESET SWITCHES

The reset switches are a bit fiddly to solder. It helps to apply a really thin film of solder to the pads first. Then hold the switch in place with tweezers and solder the big pads on the left and right of the switch (they do not fulfill any electrical purpose, but serve to hold the switches in place). If the switch is seated corretly reheat the solder pads under the switch to connect it. 

![reset switch](/docs/images/buildguide/reset_switch.jpg)

***

## TRRS JACKS (optional)

> **Warning**
> You don't need the TRRS jacks for running the TOTEM with ZMK. Actually you can damage your board when connecting it through TRRS, while also connected to a battery.

Install the TRRS jack on the bottom side of the PCB. The place where you should insert it is marked with a white line.
You may want to use some masking tape to hold it in place, since you need to solder it on the bottom.

![TRRS jack taped](/docs/images/buildguide/TRRS_tape.jpg)

![TRRS jack soldered](/docs/images/buildguide/TRRS.jpg)

***

## MICROCONTROLLER

> **Warning**
> First flash the microcontroller to make sure it works, before soldering it in.




> **Warning**
> When trimming with flush cutters wear eye protection or hold your hand close above the pins. Otherwise sharp metal pins flying around might hurt you.

***

## CLEANING

This is how your finished PCB probably will look like. You can use an old toothbrush and some isopropanol to clean it from residues. 

![Finished PCB](/docs/images/buildguide/PCB_finished_BLE.jpg)


***

## FIRMWARE

If you have not already flashed the firmware to the microcontroller you should do it now, to make sure everything works, before inserting it into the case.\
[Here](https://github.com/GEIGEIGEIST/zmk-config-totem) you can find the ZMK firmware for the TOTEM.\
You need to create an own fork of it. In this fork you can edit the keymap to trigger an Github action, which will create your firmware. 


***

## CASE


***

## FINAL BUILD

This is how the final keyboard will look like. 