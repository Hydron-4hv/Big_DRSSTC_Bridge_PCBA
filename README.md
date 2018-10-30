# Big_DRSSTC_Bridge_PCBA
PCBA for 2x IGBT brick bridge for my 160mm DRSSTC

This is a PCBA I have designed to accomodate 2x half-bridge IGBTs, either CM300DY-24H or SKM200GB125D (or any which are dimensionally and pinout compatible). The footprints have enlarged pads to accomodate the difference between the CM300s and SKM200s - I only have a couple of CM300s so if I manage to blow them up I'd like flexibility for replacement!

As well as the IGBTs it allows for a variety of bus/decoupling capacitors and bleed resistors:
- 2x 75mm dia. electrolytic capacitors, in series, with bleed resistors. These will need a short external jumper between the innermost mounting holes (would have lost too much copper area if I'd done it on the PCBA).
- 2x RBPS (or similar sized) IGBT snubber capacitors, mounted directly to the IGBT terminals.
- 2x smaller film capacitors with 22.5mm lead spacing.
- 6x 57.5mm * 35mm film capacitors, with 4 pins each at 52.5mm spacing. These are designed to take the bulk of the ripple current, and should fit a variety of 40uF/900-1100V capacitors that are coming up in bulk lots on ebay in europe. In my case I will be using Kemet C4AEOBW5400A3NJs.
- 6x small HV MLCCs in 1812 and 1825 packages. Added as I have some of these available to use, but may not be very necessary/helpful on a coil using IGBT bricks rather than fast TO-247 devices.
- 2x MMC bleed resistors, in series between the two half-bridge outputs.

This board is designed to go with a matching gate drive connector PCBA, see my other repo for this.

As it's cheapest and easiest to get 2 layer 1oz copper PCBs, I have made sure everything is mirrored around the centre of the PCB, allowing for a stack of an odd number of boards, with every second one flipped, to be made and used as one "multi-layer" PCBA. This both reduces the copper resistance and also the inductance of the bridge. I'll be trying this out with a JLCPCB order of 5x0.8mm PCBs for a 4mm thick stack costing ~$25 USD. For people who don't care about the cost ideally it'd be done with 1 PCB of 2oz+ and 3.2mm thickness for rigidity.
