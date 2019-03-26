# Acrylic Emulation

## Table of Contents
- [Inspiration](#Inspiration)
- [Notes](#Notes)
- Files
    - [Number Set 1](numberSet1.pdf)
    - [Number Set 2](numberSet2.pdf)

## Inspiration

[Lixie](https://www.tindie.com/products/connornishijima/lixie-an-led-alternative-to-the-nixie-tube/) is an acrylic emulation of a nixie tube clock. It uses cut and engraved acrylic, along with LEDs, to create the same digit scrolling effect.

But I wanted to make my own.

## Notes

So the first thing I did was get good at cutting acrylic using the laser cutter I had access to. After doing so I came up with the size and font I planned on using (the final PDF files holding the letters are hosted in this folder). I first tried engraving in the number entirely. I soon realized that the full engrave would block more light as it travels from the bottom of the number to the top, creating less even lighting/coloring. So I redesigned them in Adobe Illustrator to be outlines, popped them over into InkScape, and then into FullSpectrum to cut and engrave. These resulted in much more even lighting across the vertical of the digit.

![INSERT IMAGE OF NUMBERS]()

**3/22/19 ~ish**
The next task was to design a PCB and housing to hold the digits, as well as illuminate them. I knew I wanted to use WS2812b LEDs (Neopixels), and had to consider that the size of the standard 5050 chip was greater than the spacing I wanted for the digits. The 3535 might have fit ok, but I didn't have any chips on hand to test. I've seen designs (like from Lixie) that stagger the LEDs along the horizontal so that more can be sandwiched in vertically. However I decided that I didn't want numbers lighted unevenly (across the horizontal). I have no decided the spacing yet, so I have to check the sizing of the 3535 chips on paper (or physically) to see if that is the kind of spacing I would want. Otherwise I will have to find another solution.
