# IN-14 Nixie Tube Clock Project

## Table of Contents
- [Versions](#Versions)
- Gerber Files:
    - [v1.0](pcbV1.0)
    - [v2.0](pcbV2.0)

## Purpose

Nixie Tubes are beautiful, no way around it. When I got my first IN-14 tube, I was surprised at how small it was, but I'll upgrade to IN-18 or [These amazing z568m tubes by Dalibor Farny](https://daliborfarny.com/product/rz568m-nixie-tube/) at some point. I really want to get my hands on some F9020AA tubes, but I can't seem to find any.

The clock was a good intro to Nixie tube usage and logic. Using an ESP32 to control the logic for the K155ID1 Nixie drivers ([great resource here](https://archive.fo/euOg7)), NCH6100HV for the power supply, some WS2812b LEDs for under-lighting of the tubes, and some other components to regulate current and change voltages was a goal.

I first designed a circuit and logic that would read the time from a i2c RTC module. Once that was working, I got indexing through a single IN-14 tube running from an UNO, then a WEMOS D1 Mini:

![indexing gif](media/in-14indexing.gif)

_In the background of this gif you can see the exploded capacitor on the yellow power supply. That ZVS capacitor charging supply exploded while I was working on it and may have damaged a 6e5 tube I was using. DO NOT USE THEM THEY ARE INCONSISTENT WITH THEIR OUTPUT SOMETIMES YOU PLUG IT IN AND IT GOES TO LIKE 600V!_

For some reason lighting the 7 started flickering 8. I don't believe it did this initially when I switched over from the UNO to the D1 mini, so I think it might be either the tube or the driver... We'll see when I start putting together the v1.0 PCB when it arrives.

![flickering](media/7flickering8.gif)

**3/25/19**
Unfortunately, for the v1.0 PCB I forgot to do copper pours for the top and bottom layer. No big deal, it should still work (but we'll see when it comes). I designed a second version of the PCB using the NCH8200HV which is much smaller and has a fixed 170v output, which is what I was using anyway. Designed it with through-hole components so I didn't have to order more parts, and for the tube resistors I will use 20k in order to extend tube life, even though I could use 15k or even 10k. This is really a first prototype after all.

## Versions

### v1.0:

- Initial design
- NCH6100HV power supply (set at 170v)
- ESP32 (38pin NodeMCU) for control
- 12v power supply
- 12v to 5v step down (in fixed mode) to power ESP32, Nixie ICs

### v2.0
