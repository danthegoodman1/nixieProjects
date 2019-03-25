# Learning to use the IN-13 tube

IN-13 bargraph Nixie tubes work by powering the anode with 150v DC, grounding the AUX cathode (with a resistor!), and modulating the current running through the indicating cathode to determine how much of the bargraph is illuminated.

So following part of [this example from SMBaker](http://smbaker.com/experimenting-with-in-13-bargraph-nixie-tubes) (took me a bit to realize that R2 was a pre-set resistor/pot), I started running simulations on a virtual transistor to check current control using the MJE340 transistor:

![transistor simulation](../media/IN-13TransistorSimulation.png)

I am sure this will be quite different with actual hardware and using a IN-13 tube, but I wanted to see at what values I get the max current (4.6mA) for the tube at 150v, using 0-3.3v to control the transistor (V2 is labeled at 12v, but it was simulated from 0-3.3v).
