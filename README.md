# MiniKbd

The MiniKbd is a USB device based on the Adafruit Trinket M0 development board. 

It's designed so that when plugging it on over USB your computer will recognize it as a "USB HID" (Human Interface Device), as if a keyboard or mouse had been plugged in. The keystrokes that are output by the MiniKbd can be configured by editing the CircuitPython code running on the device.

The project came out of the idea of wanting a keyboard that simply had a larger set of arrow keys that I could position to the left side of my keyboard. [OSH Park](http://www.oshpark.com), the prototyping service that I use  to manufacture PCBs will always make boards in sets of three, so instead of having three of the same device I designed the MiniKbd to be built in three separate ways.


### “Six Keyboard Keyswitches”

Six keyboard keys, with component footprints for the most popular Cherry MX, Cherry ML and Kalih Low Profile keyswitches. Choose keyswitches that are as clicky and springy as you wish.

Since the Trinket M0 only has five general purpose IO pins and this variation has six keyswitches, they are wired up as a matrix of three rows by two columns of keyswitches. I've written a simple library to read the keypresses of a small [button matrix](https://github.com/andyclymer/circuitpython_libs/tree/master/buttonMatrix) like this one.


### “Two Rotary Encoders”

Whereas a “potentiometer” is the kind of knob designed to turn from 0 to 100% (like a volumne knob), its cousin the Rotary Encoder can freely turn continuously in either direction, clicking like a jog-dial as it turns (usually 12 or 24 clicks per rotation). With each click, the MiniKbd receives a signal that it's able to interpret to know whether it was turned clockwise or counterclockwise. Then, with each click, a keyboard command can be sent to the computer.

For instance, if the "z" and "x" keys are set up to zoom in and out in your drawing application, you can make one of the encoders into a zoom knob by having it type the letter "z" with each click in one direction, and the letter "x" in the other. 


### “One rotary encoder and two keyboard keyswitches”

The best of both worlds, almost like a little mouse that only has a scroll wheel and two buttons for clicking.