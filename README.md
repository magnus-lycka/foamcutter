# Foam Cutter

Hot wire foam cutter similar to Proxxon Micromot 230/E built from a broken Samsung BD-P1500 blue-ray player and an arduino nano clone.

## Concept

A home build foam cutter using the same kind of 0.2 mm NiCr 8020 wire used by the Proxxon.

## Operation

When used, the +13V will be used to feed current to the NiCr cutting wire. The arduino will use a PWN output to feed the PON signal to provide appropriate power to the wire.

The idea is to power the arduino with AL5V, and provide the following from it.

  - Pressing the power button will toggle the arduino program between idle and operational.
  - Pressing |< or >| will decrease or increase the settings for wire temperature, with the least being TBD and the most corresponding to a 1 A current. The setting should be displayed somehow...
  - Pressing a foot pedal will turn on the power to heat the wire, based in the |< / >| setting.
  
  
## Parts

The only things I use from the blue-ray player is the case, power led, buttons and the power supply.

### Case

The case is the blue-ray player case. The top surface is fairly smooth, but it should probably be reinforced with wood on the inside to make it possible to make a T-track for tools

### Bow

The upper end of the cutting wire will be held by a quarter of a bicycle wheel, approximately 300 mm inside radius, giving us the same maximum cutting distance and the same length of the wire regardless of cutting angle, 0.90 degrees.

### Power Supply

The power supply has an always present AL5V output and a PON input which enables the other voltage outputs when +5V is applied to it. I haven't been able to find a maximum rated current for the +13V I intend to use, but hope it will suffice.

The power control works like this: ![Schematics Power Control 13V](power-control-13v.png)

I hope that I will get a fairly stable and controlled output voltage by controlling PON with PWM output from the arduino.

### Pedal

Two pieces of plywood connected with a hinge, with a micro switch, a spring and a stop block between. A two-wire cable.
