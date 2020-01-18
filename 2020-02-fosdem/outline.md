% OpenElectronicsLab: Our Journey
% Ace Medlock, Kendrick Shaw, Eric Herman
% 2020-02-01

# OpenElectronicsLab
<!-- https://rmarkdown.rstudio.com/authoring_pandoc_markdown.html%23raw-tex#presentations -->
![Eric Herman, Kendrick Shaw, Ace Medlock](../photos/openElectronicsLab_groupPhoto.jpg)

# ADS1290 breakout
![2012 board](../photos/eeg-mouse_rev_0.0-DSC00681.jpg){ width=50% }

 - through-hole with 1 64pin QFP
 - 2011-11-26 begin desgin
 - 2012-01-23 boards arrive
     - populated 2012 rev0 board
 - 2012-03-04 reading data

[https://github.com/OpenElectronicsLab/ads1298-breakout](https://github.com/OpenElectronicsLab/ads1298-breakout)

# ExG Version 1
![OpenHardwareExG in the case](../photos/OpenHardwareExG-rev1-in-case.800.jpg){ width=50% }

- 3 boards stacked, but testing of base-board hard
- example usage: [http://openelectronicslab.github.io/eeg-mouse/](http://openelectronicslab.github.io/eeg-mouse/)

[https://github.com/OpenElectronicsLab/OpenHardwareExG](https://github.com/OpenElectronicsLab/OpenHardwareExG)

# ExG Shield
![OpenHardwareExG Shield](../photos/openhardware-exg-shield.jpg){ width=50% }

- designed testing, cheaper and easier for others
- made some errors and three different revs
- example usage: quantified self

[https://github.com/OpenElectronicsLab/OpenHardwareExG\_Shield](https://github.com/OpenElectronicsLab/OpenHardwareExG_Shield)

# Current Project: Holter Monitor

- asked for advice from Humatem and received some great guidance
- special purpose
- goal of FDA or EC certification
	- EC medical device regulation is currently changing (2020) and we don't really know the process yet
	- Need to design for safety from the start: Plan to do a ground-up redesign with eye on certification once we're happy with the prototype

# Many excellent FOSS tools to support hardware hackers
- for both hardware and firmware
- Arduino-type boards and tools lower the barrier to entry

[https://github.com/OpenElectronicsLab/OpenHardwareHolterMonitor](https://github.com/OpenElectronicsLab/OpenHardwareHolterMonitor)

# KiCAD eeschema
![kicad-eeschema-screenshot.png](../photos/kicad-eeschema-screenshot.png)

# KICAD PCB
![kicad-pcbnew-screenshot.png](../photos/kicad-pcbnew-screenshot.png)

# Populated PCB
![populated-holtermonitor.jpg](../photos/populated-holtermonitor.jpg)

# Arduino build environment
![arduino-build-screenshot.png](../photos/arduino-build-screenshot.png)

# OpenSCAD
![openscad-screenshot.png](../photos/openscad-screenshot.png)

<!-- pass floor to Ace -->

# Learning surface mount soldering
![rev0: through-hole except the chip](../photos/REV0CHIP.jpg)

# Learning surface mount soldering
- "Pin sweep" method of soldering ICs
- I learned it by watching YouTube!
<!-- At first we were intimidated by the tiny feet, but after watching some YouTube videos we were willing to give it a try - and it worked!
We felt like our first board had too much noise for what we wanted to do, so in our second design we focused on reducing noise - and that meant making the leap to all surface-mount components. -->
![YouTube](../photos/youTubeSolderICs.jpg)

# Learning surface mount soldering

![0603 surface mount resistor](../photos/surfaceMountTiny.jpg)

<!-- surface mount components are tiny -->

# Solder paste
<!-- so we thought it would be good to use solder paste a hot air gun. You apply the solder paste using a stencil, you end up with sticky paste just on the pads, and then you stick your component into the paste and heat it up with a hot air gun. Easy! -->
![solder paste](../photos/solderPasteOnBoard.jpg)

# Solder paste
<!-- After you apply the hot air gun, you get something like this, which looks fine... Except when we tested the board, it didn't work. We seemed to have a lot of bad solder joints. In trying to find the bad joints, I took the board under the microscope, and then I figured out why... -->
![surface mount components soldered with solder paste](../photos/solderPasteMeltedMacro.jpg)

# Solder paste
<!-- This is what solder paste looks like under the microscope. It's actually a bunch of little beads of solder, held together by paste. -->
![Solder paste under the microscope](../photos/solderPasteNotMelted.jpg)

# Solder paste
<!-- Some joints look like this - these are OK. -->
![solder paste joint: OK](../photos/solderPasteJointHot.jpg)

# Solder paste
<!-- But some look like this. Does this conduct electricity? Maybe. Probably not reliably. I found it really hard to tell which joints were OK. So, new plan: -->
![solder paste joint: cold solder](../photos/solderPasteJointCold.jpg)

# Soldering using a dissection scope
<!-- Use a microscope and hand-solder -->
![using a microscope for soldering](../photos/aceSolderingScope.jpg)

# Hand-soldering surface mount
<!-- The way I usually do it is to position the component, then get a little glob of solder on the tip of the iron. -->
![hand solder 01](../photos/handSolder01.jpg)

# Hand-soldering surface mount
<!-- Then use the glob to conduct the heat between the iron, pad, and component -->
![hand solder 02](../photos/handSolder02.jpg)

# Hand-soldering surface mount
<!-- Apply the solder -->
![hand solder 03](../photos/handSolder03.jpg)

# Hand-soldering surface mount
<!-- Here I'm cheating and using the solder itself to hold down the component while I pull the iron away, so it doesn't yank the component with it. -->
![hand solder 04](../photos/handSolder04.jpg)

# Hand-soldering surface mount
<!-- and there we are -->
![hand solder 05](../photos/handSolder05.jpg)

# Hand-soldering surface mount
<!-- Here's the other side. -->
![hand solder 06](../photos/handSolder06.jpg)

# Hand-soldering surface mount
![hand solder 07](../photos/handSolder07.jpg)

# Hand-soldering surface mount
![hand solder 08](../photos/handSolder08.jpg)

# Hand-soldering surface mount
<!-- This one's not quite as pretty. -->
![hand solder 09](../photos/handSolder09.jpg)

# Hand-soldering surface mount
- The job of a solder joint is to conduct electricity, not to look pretty
<!-- Using this method does not result in pretty solder joints. But the job of a solder joint is to conduct electricity, not to look pretty. -->

![ugly, but works](../photos/uglyHandSolder.jpg){ width=75% }

# Hand-soldering surface mount
<!-- You can even do an 0201 package - I refer to these as breathably small components. -->
![hand-soldered 0201 capacitor](../photos/activeElectrodeC1micro.jpg)

# Fixing misteaks
![rotated part](../photos/q10Wrong_unannotated.jpg)
<!-- One thing that is really good about learning to work with surface mount is that you learn that you don't have to be afraid of mistakes. And you will make mistakes - especially if you're working in the evenings and weekends like we do, sometimes with long breaks between. -->

# Fixing misteaks
![rotated part](../photos/q10Wrong_annotated.jpg)
<!-- The problem here was we got the wrong footprint: The pads are DGS, the feet are GSD -->

# Fixing mistakes
- You will make mistakes. You will be able to fix them.
<!-- So we just picked it up, rotated it, and stuck it back down. -->

![rotated Q10](../photos/rotatedPart.jpg){ width=75% }

# Fixing mistakes
<!-- But that wasn't the worst error on this board - Q1-Q2 had pin 1 and 2 reversed. This was my solution - turn the component 180 degrees and greenwire pin 3 to its pad. We also needed to add a couple resistors that we forgot. -->
![flipped Q1-Q2](../photos/Q1-Q2.jpg)

# Fixing mistakes
<!-- So what if you put a trace where you shouldn't have one? Well, you can just get a razor blade and cut it... provided you have a two-layer board. Or you can try lifting the foot of the IC up off the pad... -->

![cut traces](../photos/cutTrace.jpg)

# Fixing mistakes
<!-- And if you accidentally break off the foot while doing that... then you can just dremel into the chip itself, and hook the wire up straight to the chip. This is Kendrick's work, by the way. The problem was that PWRDWN and RESET should have been tied HIGH not LOW. D'oh! (https://github.com/OpenElectronicsLab/OpenHardwareExG_Shield/commit/507f61efbbbc3e7b2749c49335f21cd2c08a47c7)
-->
![green wire into the chip](../photos/kms15-shield-broken-pin-GreenwireZoomOut.jpg)

<!-- We've learned a lot along the way; one of the things we've learned about is safety, which Kendrick will talk to you about.
-->

<!-- end Ace -->

# Safety is important, and often fairly simple
<!--
https://en.wikipedia.org/wiki/Goggles#/media/File:Your_Quota_Two_eyes_that_see_Protect_them_2012_002_7217_xg94hq433_crop.tiff
(public domain from 1955 in USA, originally published without copyright notice)
-->
![goggles](../photos/Your_Quota_Two_eyes_that_see_Protect_them.png)


<!-- Ace hands floor to KMS -->

# General concepts
- What could go wrong?
- How serious is it
- How likely is it
- Risk = severity * probability
- Iterate design until risk is acceptable
  - freeclimbing
  <!-- moderate levels of risk more acceptable for yourself -->
  <!-- freeclimbing photo, not safe, but that can be an okay choice -->
  - Sometimes a high level of risk is acceptable
    - e.g. Defibrillator

# Risk of electrical shock
- Small currents can be dangerous when crossing the heart
- Current rather than voltage
    - Pacemaker voltages (~2 volts)
    - Minimum fibrilation currents
    - Resistances can be very low in a medical context
      - central lines, surgery, etc.
<!-- MAYBE Figure with patient and heart in circuit -->

# Isolation
- Batteries (Safety Extra Low Voltage, or SELV)
    - e.g.: unplugged laptop
- Creepage and clearance
  ![Creepage vs clearance](../photos/Creepage_vs_clearance.png)
- Power isolation
- Data isolation

# Leakage current standards

--------------------------------------------------------------------
Leakage Current    Body            Body Floating   Cardiac Floating
----------------- --------------- --------------- ------------------
Earth              500 $\mu$A      500 $\mu$A       500 $\mu$A

Enclosure          100 $\mu$A      100 $\mu$A       100 $\mu$A

Patient            100 $\mu$A      100 $\mu$A        10 $\mu$A
--------------------------------------------------------------------

- Can only be 2-5 times larger even if component fails
<!-- MAYBE Isolated, body float, cardiac float symbols -->

# Designing for failures
- Safe if any one component fails
- 2 means of patient protection
    - two layers of basic isolation
      vs. reinforced isolation
- Current limiting resistors on patient connections

# Take home message
- a little thought about safety goes a long way
- great tools and resources to support you
- don't be too intimidated
	- try
	- repeat
	- you'll improve as you go
- happy hardware hacking!

# References and Contacts

- Tools
	- https://www.arduino.cc/
	- https://kicad-pcb.org/
	- https://www.openscad.org/

- Books
	- The Art of Electronics, Horowitz and Hill
	- Medical Instrumentation Aplication and Design, Webster

- SMD Soldering technique videos
	- https://www.youtube.com/watch?v=eg2hxpy--gg
	- https://www.youtube.com/watch?v=JKqgU2Hw3mY

- Contact
	- https://github.com/OpenElectronicsLab
	- eric.herman@gmail.com
	- ace.medlock@gmail.com
	- kms15@case.edu
